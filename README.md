<h1 align="center" id="heading">bmartino1 Unraid Docker Templates</h1>

Templates for Docker Containers to use with Unraid.

These templates help add containers to Unraid in a more GUI-friendly way, making updates easier in the future. The Docker containers referenced in this repository point to containers maintained by other individuals.

# Unraid Templates

- [RejettoHFS3](#rejettohfs3)
- [ClamAV-clamdscan](#clamav-clamdscan)
- [Avahi ZeroConf mDNS](#Avahi)
 
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

**Avahi ZeroConfig Mdns**

Docker image for the Avahi mDNS/DNS-SD daemon. Built on Alpine Linux to make the image as small as possible.

**Application Name:** Avahi  
**Application Site:** [https://avahi.org/](https://avahi.org/)

**Linux ManPages:** [https://linux.die.net/man/5/avahi-daemon.conf](https://linux.die.net/man/5/avahi-daemon.conf)  
**Images Repository:** [https://github.com/bmartino1/avahi](https://github.com/bmartino1/avahi)  
**Docker Repository:** [https://hub.docker.com/r/bmmbmm01/avahi](https://hub.docker.com/r/bmmbmm01/avahi)  
**Unraid Support Forum:** WIP

**[`^back to top^`](#unraid-templates)**

---

# WIP for Next Template Docker for CA
Work in progress! If another one comes up...
