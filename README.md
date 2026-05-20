<h1 align="center" id="heading">bmartino1 Unraid Docker Templates</h1>

Templates for Docker containers to use with Unraid.

These templates allow Docker containers to be added to Unraid through the Community Applications (CA) interface in a more GUI-friendly way, making deployment, management, and updates easier.

The templates in this repository reference Docker images and applications maintained by various upstream developers. While some containers and templates are original work, many reference open-source projects (often MIT-licensed or similarly licensed) created and maintained by others.

These templates primarily provide the configuration needed to integrate those containers into the Unraid Community Applications ecosystem. This repository, therefore, represents a combination of original templates and integrations for existing open-source Docker projects, intended to simplify the deployment of these applications within Unraid.

# Unraid Templates

## ✅ Active Maintained
- [Netprobe](#Netprobe)
- [SFTP-Fail2ban](#SFTP)
- [Unraid Samba Passwords](#SMB)

---

## ⚠️ Keep in CA (Limited Support)
- [Postgress](#Postgress_Immich)
- [Valkey Redis Immich](#Redis_Valkey)
- [PlexDBRepair](#PlexDBRepair)
- [RetroAssembly](#retroassembly)


## 🧊 Removing From CA

- [Logmein Hamachi VPN](#Hamachi-VPN)
- [Crowdstrike Security Bouncer for unifi](#cs-unifi-bouncer)
- [RejettoHFS3](#rejettohfs3)
- [Unifi-OS-Server](#Unifi_OS)
- [Bitcoin Core](#BitcoinCoreGUI)
- [Bitcoin Knots](#BitcoinKnotsGUI)
- [CKPool Solo Mine](#CKPool)
- [ClamAV-clamdscan](#clamav-clamdscan)
- [Avahi ZeroConf mDNS](#Avahi)


## ❌ End of Life (EOL)
- [RocketChatAIO](#RocketChatAIO)
- [Old Bitnami Redis](#Redis_Immich)
- [Previlaged Unifi-OS-Server](#Unifi_OS)
- [icloudpd web](#icloudpd)

---
---

## ✅ Active Maintained

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

# SFTP

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/samba.png" width="64" height="64">
**Images Repository:** https://github.com/bmartino1/sftp2  
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/sftp2  
**Unraid Support Forum:** WIP


---
---

## ⚠️ Keep in CA (Limitied Support)

---

# Postgress_Immich
 
<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/postgresql-immich-logo.png" width="64" height="64">

* see Immich guides https://bmartino1.weebly.com/guides.html

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

# Redis_Valkey

<img src="https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png" width="64" height="64">

**Valkey_Immich**

* see immich guides https://bmartino1.weebly.com/guides.html

Docker image for Immich running Valkey, a Redis-compatible alternative. Includes additional Docker variables for an easier one-click install.

**Application Name:** Valkey  
**Application Site:** https://valkey.io/

**Docker Repository:** https://hub.docker.com/r/valkey/valkey  
**Unraid Valkey Support Forum:** https://forums.unraid.net/topic/186953-support-valkey/  
**Unraid Immich Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# PlexDBRepair

<img src="https://raw.githubusercontent.com/linuxserver/docker-templates/master/linuxserver.io/img/plex-logo.png" width="64" height="64">

**PlexDBRepair**

Docker image providing [ChuckPa](https://github.com/ChuckPa) Plex DBRepair script to Unraid. https://github.com/ChuckPa/DBRepair

**Application Name:**  DB-Plex-Repair   
**Images Repository:** https://github.com/bmartino1/plex-dbrepair-docker     
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/plex-dbrepair     
**Unraid Support Forum:** https://forums.unraid.net/topic/196453-support-plex-db-repair-docker   

**[`^back to top^`](#unraid-templates)**

---

# Docker_Requests
https://forums.unraid.net/topic/32276-docker-requests  
To add to CA only... data per forum post...

**[`^back to top^`](#unraid-templates)**

---

# retroassembly  

<img src="https://github.com/arianrhodsandlot/retroassembly/raw/main/public/assets/logo/logo-512x512.png" width="64" height="64">  

**Application Site:** https://retroassembly.com/    
**Images Repository:** https://github.com/arianrhodsandlot/retroassembly#option-2-self-host-with-docker  

**[`^back to top^`](#unraid-templates)**


---
---

## 🧊 Removing From CA

---

# Hamachi-VPN:

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/hamachi-logmein-inc.jpg" width="64" height="64">

**Application Name:** Logmein Hamachi

**Application Site:** https://vpn.net



**[`^back to top^`](#unraid-templates)**

---

# cs-unifi-bouncer

<img src="https://github.com/teifun2/cs-unifi-bouncer/raw/main/docs/assets/crowdsec_unifi_logo.png" width="64" height="64">

**Application Project Site:** https://github.com/Teifun2/cs-unifi-bouncer



**[`^back to top^`](#unraid-templates)**

---

# RejettoHFS3

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rejettohfs.png" width="64" height="64">

**Application Name:** HFS

**Application Site:** https://www.rejetto.com/hfs/



**[`^back to top^`](#unraid-templates)**

---

# Unifi_OS

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/unifi.png" width="64" height="64">

**Unifi Os Server**

** Per Unifi Use a VM **
Ubquity/Unifi Server OS system to run Unifi Protect, and network self-hosted...

**Application Name:** Unifi OS   
**Application Site:** https://blog.ui.com/article/introducing-unifi-os-server   

**Application Repository:** https://ui.com/download       
**Images Repository:** https://github.com/lemker/unifi-os-server        
**Docker Repository:** https://github.com/lemker/unifi-os-server/pkgs/container/unifi-os-server/versions      

**[`^back to top^`](#unraid-templates)**


---

# BitcoinCoreGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**Application Name:** Bitcoin Core

**Application Site:** https://bitcoin.org/en/



**[`^back to top^`](#unraid-templates)**

---

# BitcoinKnotsGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**Application Name:** Bitcoin Knots

**Application Site:** https://bitcoinknots.org/



**[`^back to top^`](#unraid-templates)**

---

# CKPool

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/ckpool.png" width="64" height="64">

**Application Name:** CKPool

**Application Site:** https://github.com/Casraw/bitcoin-ckpool 



**[`^back to top^`](#unraid-templates)**

---

# ClamAV-clamdscan

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/clamav.png" width="64" height="64">

**Application Name:** ClamAV

**Application Site:** https://www.clamav.net/



**[`^back to top^`](#unraid-templates)**

---

# Avahi

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/avahi.png" width="64" height="64">

**Application Name:** Avahi

**Application Site:** https://avahi.org/



**[`^back to top^`](#unraid-templates)**

---

## ❌ End of Life (EOL)

---

# RocketChatAIO

* Removed due to rocket.chat support attempted a AIO... see https://github.com/bmartino1/unraid-rocket.chat for proper implementation...
  
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

# Redis_Immich

<img src="https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png" width="64" height="64">

**Application Name:** Redis

**Application Site:** https://redis.io/



**[`^back to top^`](#unraid-templates)**

---

# Previlaged Unifi-OS-Server

** Per Unifi Use a VM **
<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/unifi.png" width="64" height="64">

**Application Name:** Unifi OS  
**Application Site:** https://blog.ui.com/article/introducing-unifi-os-server

**[`^back to top^`](#unraid-templates)**

---

# icloudpd

<img src="https://raw.githubusercontent.com/Womabre/-unraid-docker-templates/master/images/photos_icon_large.png" width="64" height="64">

**Application Name:** icloudpd-web  
**Application Site:** https://github.com/AirswitchAsa/icloudpd-web

**[`^back to top^`](#unraid-templates)**

