<h1 align="center" id="heading">bmartino1 Unraid Docker Templates</h1>

Templates for Docker Containers to use with Unraid.

These templates help add containers to Unraid in a more GUI-friendly way, making updates easier in the future. The Docker containers referenced in this repository point to containers maintained by other individuals.

# Unraid Templates

- [RejettoHFS3](#rejettohfs3)
- [ClamAV-clamdscan](#clamav-clamdscan)
- [Avahi ZeroConf mDNS](#Avahi)
- [SFTP-Fail2ban](#SFTP)
- [MongoDB](#MongoDB-RocketChat)
- [RocketChat](#RocketChat)
- [Postgress](#Postgress_Immich)
- [Redis](#Redis_Immich)
- [Bitcoin Core](#BitcoinCoreGUI)
- [Bitcoin Knots](#BitcoinKnotsGUI)
- [CKPool](#CKPool)


---

# RejettoHFS3

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rejettohfs.png" width="64" height="64">

**HFS ~ HTTP File Server by Rejetto**

Access your files directly from your disk via the web. You become the server! Share files directly from your disk, with unlimited space and bandwidth.

- **Fast!** Try zipping 100GB; downloads start immediately!
- **Virtual File System:** Share even a single file, with a different name if needed, without altering the real file.
- **Customizable:** Present things the way you want!
- **Real-time Monitoring:** Watch all activities in real-time.
- **Bandwidth Control:** Decide how much bandwidth to allocate.
- **Direct Sharing:** Share large files with friends without uploading them to a server.
- **Intelligent Problem Detection:** HFS tries to detect problems and suggest solutions.
- **Expandable:** Find the right plugin, or create your own.

**Application Name:** HFS  
**Application Site:** [https://www.rejetto.com/hfs/](https://www.rejetto.com/hfs/)

**Application Repository:** [https://github.com/rejetto/hfs](https://github.com/rejetto/hfs)  
**Images Repository:** [https://github.com/damienzonly/hfs-docker](https://github.com/damienzonly/hfs-docker) and [https://github.com/bmartino1/hfs-docker](https://github.com/bmartino1/hfs-docker)  
**Docker Repository:** [https://hub.docker.com/r/rejetto/hfs](https://hub.docker.com/r/rejetto/hfs)  
**Additional Support:** [https://github.com/rejetto/hfs/discussions](https://github.com/rejetto/hfs/discussions)  
**Unraid Support Forum:** [https://forums.unraid.net/topic/180463-support-rejetto-hfs-3/](https://forums.unraid.net/topic/180463-support-rejetto-hfs-3/)

**[`^back to top^`](#unraid-templates)**

---

# ClamAV-clamdscan

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/clamav.png" width="64" height="64">

**ClamAV using Clamd**

Scan and access your files directly from your disk. Use Clamdscan over Clamscan to enable multi-core support.  
**This reduced a 48-hour scan of 6 TB or more to a 6-hour scan.**

**Application Name:** ClamAV  
**Application Site:** [https://www.clamav.net/](https://www.clamav.net/)

**Application Repository:** [https://github.com/Cisco-Talos/clamav](https://github.com/Cisco-Talos/clamav)  
**Images Repository:** [https://github.com/bmartino1/clamav-alpine](https://github.com/bmartino1/clamav-alpine)  
**Docker Repository:** [https://hub.docker.com/r/bmmbmm01/clamav-alpine](https://hub.docker.com/r/bmmbmm01/clamav-alpine)  
**Additional Support Documentation:** [https://docs.clamav.net/](https://docs.clamav.net/)  
**Unraid Support Forum:** [https://forums.unraid.net/topic/80868-support-clamav/](https://forums.unraid.net/topic/80868-support-clamav/)

**[`^back to top^`](#unraid-templates)**

---

# Avahi

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/avahi.png" width="64" height="64">

**Avahi a ZeroConfig Mdns Server**
Docker image for the Avahi mDNS/DNS-SD daemon. Built on Debian Linux to make the image as feautre rich.
- **Simple Default** View the config via the log and make the config via docker settings.
- **one log location** easily see error and mdns status in the docker log.
- **Diag tools builtin** open console run mdns-scan to check configuration and see whats available via mdns.

**Application Name:** Avahi  
**Application Site:** [https://avahi.org/](https://avahi.org/)

**Linux ManPages:** [https://linux.die.net/man/5/avahi-daemon.conf](https://linux.die.net/man/5/avahi-daemon.conf)  
**Images Repository:** [https://github.com/bmartino1/avahi](https://github.com/bmartino1/avahi)  
**Docker Repository:** [https://hub.docker.com/r/bmmbmm01/avahi](https://hub.docker.com/r/bmmbmm01/avahi)  
**Unraid Support Forum:** [https://forums.unraid.net/topic/183175-support-bmartino1-avahi/](https://forums.unraid.net/topic/183175-support-bmartino1-avahi/)

**[`^back to top^`](#unraid-templates)**

---

# SFTP

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/SFTP.png" width="64" height="64">

**SFTP and Fail2ban Server**

Docker image for SFTP running openssh-server and harend against attacks with fail2bann. Built on a Ubuntu Linux Docker image to make the image feautre rich.  
- **Simple by Default** Once Click install and sftp is running... View the config folder for advance configuration changes...  
- **Easy Log Location** easily see error and check status in the docker log.  
- **Orginal Fork: https://github.com/MarkusMcNugen/docker-sftp a Fork of https://hub.docker.com/r/atmoz/sftp  

**Application Name:** SFTP (Openssh)  
**Application Site:** [https://www.openssh.com/](https://www.openssh.com/)  
**Linux ManPages:** [https://manpages.ubuntu.com/manpages/noble/man5/sshd_config.5.html](https://manpages.ubuntu.com/manpages/noble/man5/sshd_config.5.html)  

**Application Name:** Fail2Ban (fail2ban and jails)  
**Application Site:** [https://github.com/fail2ban/fail2ban](https://github.com/fail2ban/fail2ban)  
**Linux ManPages:** [https://manpages.ubuntu.com/manpages/noble/man1/fail2ban.1.html](https://manpages.ubuntu.com/manpages/noble/man1/fail2ban.1.html)  

**Images Repository:** [https://github.com/bmartino1/docker-sftp](https://github.com/bmartino1/docker-sftp)  
**Docker Repository:** [https://hub.docker.com/r/bmmbmm01/sftp](https://hub.docker.com/r/bmmbmm01/sftp)  
**Unraid Support Forum:** [https://forums.unraid.net/topic/189050-support-sftp-fail2ban](https://forums.unraid.net/topic/189050-support-sftp-fail2ban)  

**[`^back to top^`](#unraid-templates)**

---

# MongoDB-RocketChat

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rocketchatmongo.png" width="64" height="64">

**MongoDB by bitnami for RocketChat**

Docker image for MongoDB for easier use to run RocketChat per RocketChat Maintainer: https://docs.rocket.chat/docs/deploy-with-docker-docker-compose 

**Application Name:** Mongo  
**Application Site:** [https://www.mongodb.com/](https://www.mongodb.com/)  

**Images Repository:** [https://github.com/bitnami/charts/tree/main/bitnami/mongodb](https://github.com/bitnami/charts/tree/main/bitnami/mongodb)  
**Docker Repository:** [https://hub.docker.com/r/bitnami/mongodb](https://hub.docker.com/r/bitnami/mongodb)  
**Unraid Support Forum:** https://forums.unraid.net/topic/61337-support-rocketchat  

**[`^back to top^`](#unraid-templates)**

---

# RocketChat

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/rocketchat.png" width="64" height="64">

**RocketChat**

Docker image for RocketChat for easier use to run RocketChat per RocketChat Maintainer: https://docs.rocket.chat/docs/deploy-with-docker-docker-compose 

**Application Name:** Rocketchat   
**Application Site:** https://www.rocket.chat/pricing 

**Images Repository:** https://github.com/RocketChat/Docker.Official.Image  
**Docker Repository:** https://hub.docker.com/r/rocketchat/rocket.chat/   
**Unraid Support Forum:** https://forums.unraid.net/topic/61337-support-rocketchat  

**[`^back to top^`](#unraid-templates)**

---

# Postgress_Immich

<img src="https://raw.githubusercontent.com/bmartino1/unraid-docker-templates/refs/heads/main/images/postgresql-immich-logo.png" width="64" height="64">

**Postgress_Immich**

Docker image for immich running postgress v14 using the new Vector Chord Plugin. 
Immich is taking over the orginal tensorchord/pgvecto-rs:pg16-v0.3.0 migrating off the deprecated pgvecto.rs

**Application Name:** Postgress
**Application Site:** https://www.postgresql.org/support/  

**Images Repository:** https://github.com/immich-app/base-images/pkgs/container/postgres  
**Docker Repository:** https://github.com/immich-app/immich/releases/tag/v1.133.0  
**Unraid Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# Redis_Immich

<img src="https://raw.githubusercontent.com/A75G/docker-templates/master/templates/icons/redis.png" width="64" height="64">

**Redis_Immich**

Docker image for immich running bitnami redis. Some adational Docker Varables for a easier 1 CLick Install

**Application Name:** Redis  
**Application Site:** https://redis.io/   

**Images Repository:** https://github.com/bitnami/charts/tree/main/bitnami/redis  
**Docker Repository:** https://hub.docker.com/r/bitnami/redis  
**Unraid Support Forum:** https://forums.unraid.net/topic/146106-immich-docker-self-hosted-google-photos-setup  

**[`^back to top^`](#unraid-templates)**

---

# BitcoinCoreGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**BitcoinCore**

Docker image for Bitcoin-qt run and monitor via webpage access over vnc. latter will add another docker for electrum and lightning nodes. Help-full for self hosting a bitcoin wallet, running a node for single mineing against on Unriad.

**Application Name:** Bitcoin core   
**Application Site:** https://bitcoin.org/en/ 

**Images Repository:** https://github.com/bmartino1/Docker-BitcoinCoreGUI       
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/bitcoin-core-gui     
**Unraid Support Forum:** https://forums.unraid.net/topic/191428-suppot-bitcoin-gui/      

**[`^back to top^`](#unraid-templates)**

---

# BitcoinKnotsGUI

<img src="https://bitcoin.org/img/icons/opengraph.png" width="64" height="64">

**BitcoinKnots**

Docker image for Bitcoin-qt run and monitor via webpage access over vnc. latter will add another docker for electrum and lightning nodes. Help-full for self hosting a bitcoin wallet, running a node for single mineing against on Unriad.

**Application Name:** Bitcoin knots   
**Application Site:** https://bitcoinknots.org/   

**Images Repository:** https://github.com/bmartino1/Docker-BitcoinKnotsGUI   
**Docker Repository:** https://hub.docker.com/r/bmmbmm01/bitcoin-knots-gui     
**Unraid Support Forum:** https://forums.unraid.net/topic/191428-suppot-bitcoin-gui/       

**[`^back to top^`](#unraid-templates)**

---

# CKPool

<img src="https://raw.githubusercontent.com/animai/unraid-templates/master/public-pool/img/public-pool.png" width="64" height="64">

**CKPool**

Docker image for running a Solo Pool asociated aginst a Bitcoin node via RPC for SOLO/single mineing on Unriad.

**Application Name:** CKPool

**Images Repository:** https://github.com/golden-guy/docker-ckpool   
**Docker Repository:** https://hub.docker.com/r/pinkyswear/ckpool-solo   
**Unraid Support Forum:** WIP ??? - https://forums.unraid.net/topic/191428-suppot-bitcoin-gui/       

**[`^back to top^`](#unraid-templates)**

---
