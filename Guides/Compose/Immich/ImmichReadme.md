# Immich on Unraid — Docker Compose Setup

How to install [Immich](https://immich.app/) on Unraid via the Docker Compose plugin.

- **Web version of this guide**: [bmartino1.weebly.com/immich-on-unraid-docker-compose-guide](https://bmartino1.weebly.com/immich-on-unraid-docker-compose-guide.html)
- **Unraid Forum Support**: [Immich Docker — Self-Hosted Google Photos Setup](https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup)
- **YouTube walkthrough**: [Immich Docker Compose Setup on Unraid](https://www.youtube.com/watch?v=VP-uzo9tB14)

---

## 1) Prerequisites

- **Compose.Manager** plugin installed via Community Apps.
- **Official docs**:
  - [Immich Unraid Install](https://docs.immich.app/install/unraid)
  - [Immich Docker Compose](https://immich.app/docs/install/docker-compose/)
  - [docker-compose.yml (latest release)](https://github.com/immich-app/immich/releases/latest/download/docker-compose.yml)
  - [example.env (official)](https://github.com/immich-app/immich/blob/main/docker/example.env)

---

## 2) Prepare Unraid folders

Create these ahead of time for stack + data paths:

```bash
# Pre-create Unraid folders for the Immich stack
mkdir -p /mnt/user/appdata/immich/{config,database/postgres,database/redis,photos}
```

Resulting structure:
- `/mnt/user/appdata/immich/config/`
- `/mnt/user/appdata/immich/database/postgres/`
- `/mnt/user/appdata/immich/database/redis/`
- `/mnt/user/appdata/immich/photos/`

---

## 3) Add stack in Unraid UI

1. Unraid (Web UI) → **Docker** → **Compose.Manager** → **Add New Stack**
2. **New Stack**, name: `immich`
3. **Click Advanced** → Set your stack path: `/mnt/user/appdata/immich`

![Compose Manager — new stack creation](https://bmartino1.weebly.com/files/theme/UnraidComposeStack.png)

---

## 4) Edit Compose file

1. ⚙️ → *Edit Stack* → **Compose File**

![Edit Stack](https://bmartino1.weebly.com/files/theme/EditStack.webp)
![Edit Stack button](https://bmartino1.weebly.com/files/theme/EditStackButton.webp)
![Compose file editor](https://bmartino1.weebly.com/files/theme/composefile.webp)

2. Paste the `docker-compose.yml` below and adjust paths for your environment.

**Source file**: [docker-compose.yml on GitHub](https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/Guides/Compose/Immich/docker-compose.yml)

```yaml
# Always use the compose file from the current release:
# https://github.com/immich-app/immich/releases/latest/download/docker-compose.yml
# Main branch may not match the latest release.

name: immich

services:
  immich-server:
    container_name: immich_server
    image: ghcr.io/immich-app/immich-server:${IMMICH_VERSION:-release}
    # extends:
    #   file: hwaccel.transcoding.yml
    #   service: cpu
    volumes:
      - immich-photos:/usr/src/app/upload
      - /etc/localtime:/etc/localtime:ro
    env_file:
      - .env
    ports:
      - '2283:2283'
    depends_on:
      - redis
      - database
    restart: always
    healthcheck:
      disable: false
    networks:
      immich-net:
        ipv4_address: 172.19.0.10
    labels:
      net.unraid.docker.icon: 'https://raw.githubusercontent.com/imagegenius/templates/main/unraid/img/immich.png'
      net.unraid.docker.webui: http://[IP]:[PORT:2283]
      folder.view: immich
      net.unraid.docker.managed: 'composeman'

  immich-machine-learning:
    container_name: immich_machine_learning
    image: ghcr.io/immich-app/immich-machine-learning:${IMMICH_VERSION:-release}
    volumes:
      - model-cache:/cache
    env_file:
      - .env
    restart: always
    healthcheck:
      disable: false
    networks:
      immich-net:
        ipv4_address: 172.19.0.11
    labels:
      net.unraid.docker.icon: 'https://raw.githubusercontent.com/imagegenius/templates/main/unraid/img/immich.png'
      folder.view: immich
      net.unraid.docker.managed: 'composeman'

  redis:
    container_name: immich_redis
    image: docker.io/valkey/valkey:8-bookworm@sha256:ff21bc0f8194dc9c105b769aeabf9585fea6a8ed649c0781caeac5cb3c247884
    volumes:
      - redis-data:/data
    healthcheck:
      test: redis-cli ping || exit 1
    restart: always
    networks:
      immich-net:
        ipv4_address: 172.19.0.12
    labels:
      net.unraid.docker.icon: 'https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png'
      folder.view: immich
      net.unraid.docker.managed: 'composeman'

  database:
    container_name: immich_postgres
    image: ghcr.io/immich-app/postgres:16-vectorchord0.3.0-pgvectors0.3.0
    environment:
      POSTGRES_PASSWORD: ${DB_PASSWORD}
      POSTGRES_USER: ${DB_USERNAME}
      POSTGRES_DB: ${DB_DATABASE_NAME}
      POSTGRES_INITDB_ARGS: '--data-checksums'
    volumes:
      - postgres-data:/var/lib/postgresql/data
    restart: always
    networks:
      immich-net:
        ipv4_address: 172.19.0.13
    labels:
      net.unraid.docker.icon: 'https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/postgres.png'
      folder.view: immich
      net.unraid.docker.managed: 'composeman'

networks:
  immich-net:
    driver: bridge
    ipam:
      config:
        - subnet: 172.19.0.0/16
          gateway: 172.19.0.1

volumes:
  model-cache:
    driver: local
    driver_opts:
      type: none
      device: /mnt/user/appdata/immich/config
      o: bind

  immich-photos:
    driver: local
    driver_opts:
      type: none
      device: /mnt/user/appdata/immich/photos
      o: bind

  postgres-data:
    driver: local
    driver_opts:
      type: none
      device: /mnt/user/appdata/immich/database/postgres
      o: bind

  redis-data:
    driver: local
    driver_opts:
      type: none
      device: /mnt/user/appdata/immich/database/redis
      o: bind
```

3. **Save Changes**

![Save changes](https://bmartino1.weebly.com/files/theme/immichsavechanges.webp)

4. **UI Labels pop-up**: Click OK to save.

> Data from compose auto-populates only on first import; later edits won't update UI labels.

![UI labels dialog](https://bmartino1.weebly.com/files/theme/uilablescomposefile.webp)

---

## 5) Edit the .env file

1. ⚙️ → *Edit Stack* → **Env File**

![Env file editor](https://bmartino1.weebly.com/files/theme/envcomposefile.webp)

2. Paste from [example.env](https://github.com/immich-app/immich/blob/main/docker/example.env), then update values.

**Source file**: [.env on GitHub](https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/Guides/Compose/Immich/.env)

```env
# Documentation for all supported env variables:
# https://immich.app/docs/install/environment-variables

# The location where uploaded files are stored (see compose bind mount)
# UPLOAD_LOCATION=./library  # (handled by compose: /usr/src/app/upload)

# Database files location (handled by compose; network shares not supported for DB)
# DB_DATA_LOCATION=./postgres

# To set a timezone, uncomment and choose a TZ from:
# https://en.wikipedia.org/wiki/List_of_tz_database_time_zones#List
# TZ=America/Chicago

# Immich version (pin to a specific version like "v1.71.0" if desired)
IMMICH_VERSION=release

# Postgres connection
DB_PASSWORD=postgres
DB_USERNAME=postgres
DB_DATABASE_NAME=immich
```

3. **Save Changes**

![Save env changes](https://bmartino1.weebly.com/files/theme/immichsavechangesenv.webp)

---

## 6) Start the Immich stack

1. Click **Compose Up**.

![Compose Up](https://bmartino1.weebly.com/files/theme/compuseupdone.webp)

> On first run (image pulls), stay on this page until containers are created and running, then click **Done**.

2. Open Immich from the Docker tab via the WebUI option.

![Immich stack in Docker view](https://bmartino1.weebly.com/files/theme/immichstackwebui.webp)

3. Finish: [Post-install steps](https://immich.app/docs/install/post-install/)

---

## Optional: Hardware Acceleration

Download the extra compose files into the same folder as your stack, then uncomment the `extends` block(s) in your main compose.

```bash
cd /mnt/user/appdata/immich && ls   # verify docker-compose.yml is present
wget https://raw.githubusercontent.com/immich-app/immich/refs/heads/main/docker/hwaccel.ml.yml
wget https://raw.githubusercontent.com/immich-app/immich/refs/heads/main/docker/hwaccel.transcoding.yml
```

- [ML hardware acceleration docs](https://docs.immich.app/features/ml-hardware-acceleration)
- [Server hardware transcoding docs](https://immich.app/docs/features/hardware-transcoding/)
- [Remote ML quick start](https://docs.immich.app/guides/remote-machine-learning/)

This may require adding additional device mappings and environment variables to pass the hardware into the needed containers.
