<h1 align="center" id="heading">bmartino1 Unraid Docker Templates</h1>

Templates for Docker containers to use with Unraid.

These templates help add containers to Unraid in a more GUI-friendly way, making updates easier in the future. The Docker containers referenced in this repository point to containers maintained by other individuals.

# Unraid Templates

- [RejettoHFS3](#rejettohfs3)
- [ClamAV-clamdscan](#clamav-clamdscan)
- [Avahi ZeroConf mDNS](#Avahi)
- [SFTP-Fail2ban](#SFTP)
- [RocketChatAIO](#RocketChatAIO)
- [Postgress](#Postgress_Immich)
- [Old Redis](#Redis_Immich)
- [Valkey Redis Immich](#Redis_Valkey)
- [Bitcoin Core](#BitcoinCoreGUI)
- [Bitcoin Knots](#BitcoinKnotsGUI)
- [Netprobe](#Netprobe)   
- [Docker_Requests](#Docker_Requests)
- [Deprecated](#Deprecated)

---

# RejettoHFS3

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rejettohfs.png" width="64" height="64">

**HFS ~ HTTP File Server by Rejetto**

Access your files directly from your disk via the web. You become the server! Share files directly from your disk, with unlimited space and bandwidth.

- **Fast!** Try zipping 100GB; downloads start immediately!
- **Virtual File System:** Share even a single file, with a different name if needed, without altering the real file.
- **Customizable:** Present things the way you want!
- **Real-time Monitoring:** Watch all activities in real time.
- **Bandwidth Control:** Decide how much bandwidth to allocate.
- **Direct Sharing:** Share large files with friends without uploading them to a server.
- **Intelligent Problem Detection:** HFS tries to detect problems and suggest solutions.
- **Expandable:** Find the right plugin, or create your own.

**Application Name:** HFS  
**Application Site:** https://www.rejetto.com/hfs/

**Application Repository:** https://github.com/rejetto/hfs  
**Images Repository:** https://github.com/damienzonly/hfs-docker and https://github.com/bmartino1/hfs-docker  
**Docker Repository:** https://hub.docker.com/r/rejetto/hfs  
**Additional Support:** https://github.com/rejetto/hfs/discussions  
**Unraid Support Forum:** https://forums.unraid.net/topic/180463-support-rejetto-hfs-3/

**[`^back to top^`](#unraid-templates)**

---

# ClamAV-clamdscan

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/clamav.png" width="64" height="64">

**ClamAV using Clamd**

Scan and access your files directly from your disk. Use Clamdscan over Clamscan to enable multi-core support.  
**This reduced a 48-hour scan of 6 TB or more to a 6-hour scan.**

**Application Name:** ClamAV  
**Application Site:** https://www.clamav.net/

**Application Repository:** https://github.com/Cisco-Talos/clamav  
**Images Repository:** https://github.com/bmartino1/clamav-alpine  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/clamav-alpine  
**Additional Support Documentation:** https://docs.clamav.net/  
**Unraid Support Forum:** https://forums.unraid.net/topic/80868-support-clamav/

**[`^back to top^`](#unraid-templates)**

---

# Avahi

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/avahi.png" width="64" height="64">

**Avahi — a ZeroConfig mDNS Server**

Docker image for the Avahi mDNS/DNS-SD daemon. Built on Debian Linux to make the image as feature-rich as possible.

- **Simple Defaults:** View the configuration via logs and modify settings through Docker variables.
- **Single Log Location:** Easily view errors and mDNS status in the Docker log.
- **Diagnostic Tools Built In:** Open the console and run `mdns-scan` to check configuration and discover available services.

**Application Name:** Avahi  
**Application Site:** https://avahi.org/

**Linux Man Pages:** https://linux.die.net/man/5/avahi-daemon.conf  
**Images Repository:** https://github.com/bmartino1/avahi  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/avahi  
**Unraid Support Forum:** https://forums.unraid.net/topic/183175-support-bmartino1-avahi/

**[`^back to top^`](#unraid-templates)**

---

# SFTP

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/SFTP.png" width="64" height="64">

**SFTP and Fail2ban Server**

Note — Known as **sftp2**, an update to the Docker fork to move away from the base image and apply required fixes.  
Setting the Docker variable `debug_testing=true` will create debug folders in the `/config` volume for crossover testing.

This template adds additional Docker variables and capabilities. It is a full overhaul of SFTP, rebuilt on **Debian-slim** due to Ubuntu and OpenSSH issues in the original SFTP Fail2ban Docker image. Alpine was considered, but is not compatible with other required applications.

Docker image for SFTP running OpenSSH server and hardened against attacks with Fail2ban.

- **Simple by Default:** One-click install and SFTP is running. View the config folder for advanced configuration.
- **Easy Log Location:** Easily see errors and check status in the Docker log or the appdata log folder.

**Application Name:** SFTP (OpenSSH)  
**Application Site:** https://www.openssh.com/  
**Linux Man Pages:** https://manpages.ubuntu.com/manpages/noble/man5/sshd_config.5.html  

**Application Name:** Fail2Ban  
**Application Site:** https://github.com/fail2ban/fail2ban  
**Linux Man Pages:** https://manpages.ubuntu.com/manpages/noble/man1/fail2ban.1.html  

**Images Repository:** https://github.com/bmartino1/sftp2  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/sftp2  
**Unraid Support Forum:** https://forums.unraid.net/topic/189050-support-sftp-fail2ban  

**[`^back to top^`](#unraid-templates)**

---

# RocketChatAIO

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rocketchataio.png" width="64" height="64">

**RocketChatAIO**

Docker image for Rocket.Chat AIO, including MongoDB and the Rocket.Chat application, for simplified deployment.  
Based on the Rocket.Chat maintainer documentation:  
https://docs.rocket.chat/docs/deploy-with-docker-docker-compose

**Application Name:** Rocket.Chat  
**Application Site:** https://www.rocket.chat/pricing  

**Images Repository:** https://github.com/bmartino1/rocket.chat/tree/main/unraidAIO  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/rocketchat-aio  
**Unraid Support Forum:** https://forums.unraid.net/topic/61337-support-rocketchat  

**[`^back to top^`](#unraid-templates)**

---

# Postgress_Immich

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/postgresql-immich-logo.png" width="64" height="64">

**Postgress_Immich**

Docker image for Immich running Postgres v14 using the new Vector Chord plugin.  
Immich is migrating from the deprecated `tensorchord/pgvecto-rs` to a maintained alternative.

**Application Name:** Postgres  
**Application Site:** https://www.postgresql.org/support/

**Images Repository:** https://github.com/immich-app/base-images/pkgs/container/postgres  
**Docker Repository:** https://github.com/immich-app/immich/releases/tag/v1.133.0  
**Unraid Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# Redis_Immich

<img src="https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png" width="64" height="64">

**Redis_Immich**

Docker image for Immich running Bitnami Redis. Includes additional Docker variables for an easier one-click install.

Broadcom changed Bitnami licensing — use `bitnamilegacy` for transition. Valkey is recommended going forward.

**Application Name:** Redis  
**Application Site:** https://redis.io/

**Images Repository:** https://github.com/bitnami/charts/tree/main/bitnami/redis  
**Docker Repository:** https://hub.docker.com/r/bitnami/redis  
**Unraid Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# Redis_Valkey

<img src="https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png" width="64" height="64">

**Valkey_Immich**

Docker image for Immich running Valkey, a Redis-compatible alternative. Includes additional Docker variables for an easier one-click install.

**Application Name:** Valkey  
**Application Site:** https://valkey.io/

**Docker Repository:** https://hub.docker.com/r/valkey/valkey  
**Unraid Valkey Support Forum:** https://forums.unraid.net/topic/186953-support-valkey/  
**Unraid Immich Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# BitcoinCoreGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**BitcoinCore**

Docker image for Bitcoin-Qt, allowing monitoring via web-based VNC access.  
Future additions may include Electrum and Lightning node containers.

Helpful for self-hosting a Bitcoin wallet and running a node for solo mining on Unraid.

**Application Name:** Bitcoin Core  
**Application Site:** https://bitcoin.org/en/

**Images Repository:** https://github.com/bmartino1/Docker-BitcoinCoreGUI  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/bitcoin-core-gui  
**Unraid Support Forum:** https://forums.unraid.net/topic/191428-support-bitcoin-gui/  

**[`^back to top^`](#unraid-templates)**

---

# BitcoinKnotsGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**BitcoinKnots**

Docker image for Bitcoin-Qt, allowing monitoring via web-based VNC access.  
Future additions may include Electrum and Lightning node containers.

Helpful for self-hosting a Bitcoin wallet and running a node for solo mining on Unraid.

**Application Name:** Bitcoin Knots  
**Application Site:** https://bitcoinknots.org/

**Images Repository:** https://github.com/bmartino1/Docker-BitcoinKnotsGUI  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/bitcoin-knots-gui  
**Unraid Support Forum:** https://forums.unraid.net/topic/191428-support-bitcoin-gui/  

**[`^back to top^`](#unraid-templates)**


# Netprobe

<img src="https://github.com/bmartino1/unraid-docker-templates/blob/main/images/netprobe.png?raw=true" width="64" height="64">

**Netprobe**

Docker image providing Netprobe functionality in a single Python-based container.

**Application Name:** Netprobe  
**Application Site:** https://github.com/plaintextpackets/netprobe_lite

**Images Repository:** https://github.com/bmartino1/NetProbe_Python  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/netprobe  
**Unraid Support Forum:** https://forums.unraid.net/topic/195469-support-netprobe  

**[`^back to top^`](#unraid-templates)**

---

# Docker_Requests
https://forums.unraid.net/topic/32276-docker-requests  
To add to CA only... data per forum post...

# retroassembly  

<img src="https://github.com/arianrhodsandlot/retroassembly/raw/main/public/assets/logo/logo-512x512.png" width="64" height="64">  

**Application Site:** https://retroassembly.com/    
**Images Repository:** https://github.com/arianrhodsandlot/retroassembly#option-2-self-host-with-docker  

# cs-unifi-bouncer   

<img src="https://github.com/teifun2/cs-unifi-bouncer/raw/main/docs/assets/crowdsec_unifi_logo.png" width="64" height="64">  

**Application Project Site:** https://github.com/Teifun2/cs-unifi-bouncer    
** Github Docker Repository:** https://github.com/teifun2/cs-unifi-bouncer/pkgs/container/cs-unifi-bouncer#configuration  

---

# Deprecated

icloudpd-web: https://github.com/AirswitchAsa/icloudpd-web - Beta teamplates test can't get to work right for stability use Docker Compose.   

Hamachi-VPN: Couldn't get CA to accept xml   


# CKPool
* ckpool: Couldn't get CA to accept xml
  
<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/ckpool.png" width="64" height="64">

**CKPool Solo Mining Pool**

Docker image for running a **Bitcoin solo mining pool** using CKPool.  
This allows miners to connect directly to your own pool instance while submitting work to your Bitcoin node.

This template is based on the `pinkyswear/ckpool-solo` Docker image and supports configuration for Bitcoin Core RPC connectivity and custom pool settings.

Please review the following projects for configuration examples and background information:
- https://github.com/golden-guy/ckpool-solo
- https://hub.docker.com/r/pinkyswear/ckpool-solo

**Application Name:** CKPool  
**Application Site:** https://bitcointalk.org/index.php?topic=164896.0  

**Images Repository:** https://github.com/golden-guy/ckpool-solo  
**Docker Repository:** https://hub.docker.com/r/pinkyswear/ckpool-solo  

**Notes:**
- Requires access to a Bitcoin Core node via RPC.
- A valid Bitcoin address is required for block rewards.
- Intended for **solo mining**, not pooled payouts.

**[`^back to top^`](#unraid-templates)**

---
