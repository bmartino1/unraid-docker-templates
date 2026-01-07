# Change Log

All major changes to this project will be documented here.

## 2026.07.01
- **ALL templates were sent through grammar and spellcheck**
- Deleted old Depriacted projects.
- **CKPool added**
- **Rocket.Chat**
  - Added a new required variable for Rocket.Chat SMTP email...

## 2026.05.01
- **Rocket.Chat**
  - Added AIO Docker to fix MongoDB issues for a Rocket.Chat deployment...

## 2025.18.12
- **Docker Requests**
  - Add Docker Request Templates data to template for new users, one-click setup and done. Only to add to CA.

## 2025.08.12
- **Sftp2**
  - Add more data to template for new users, one-click setup and done.

## 2025.11.30
- **Netprobe**
  - Add new template Netprobe

## 2025.09.11
- **Postgres**
  - Add template edit to fix repo and appdata to v18 per Postgres Docker PGDATA change...

## 2025.04.10
- **Valkey**
  - Add template edit to add autoupdate, stay on version of application or autoupdate...
- **Redis**
  - Change image template to Bitnami legacy repo to still have a working template Docker image install

## 2025.20.09
- **Sftp2**
  - Add template edit to add autoupdate, stay on version of application or autoupdate...
  - This is a new addition of the same functionality of the other Docker, just to re-enable the auto-update capabilities.

## 2025.28.06
- **BitcoinCore**
  - Add template edit to add autoupdate, stay on version of application or autoupdate...
- **BitcoinKnots**
  - Add template edit to add autoupdate, stay on version of application or autoupdate...

## 2025.24.06
- **BitcoinCore**
  - Add template edit to add stop time
- **BitcoinKnots**
  - Add template edit to add stop time
- **CKPool**
  - Updated template — not getting added to CA? Unicode or other error

## 2025.23.06
- **BitcoinCore**
  - Add new template and data
- **BitcoinKnots**
  - Add new template and data
- **CKPool**
  - Add new template and data

## 2025.04.06
- **Postgres**
  - Template fix port 5432 in template

## 2025.24.05
- **Redis**
  - Add new template and data

## 2025.23.05
- **Postgres**
  - Add new template and data

## 2025.19.05
- **RocketChat**
  - Add new template and data
- **MongoDB-RocketChat**
  - Minor fixes to additional requirements to complete the Unraid stack

## 2025.18.05
- **MongoDB-RocketChat**
  - Add new template and data

## 2025.12.04
- **SFTP**
  - Updated template, added variable for auto update

## 2025.10.04
- **SFTP**
  - Updated template, added support [Forum](https://forums.unraid.net/topic/189050-support-sftp-fail2ban)

## 2025.09.04
- **SFTP**
  - Add new template and data
  - Template was added — Hello World — to a new Unraid CA, updated from a previous maintainer...

## 2024.23.12
- **Avahi**
  - Add template option I'm running for IPv6 and fixed some template descriptions

## 2024.22.12
- **Avahi**
  - Fix issue with Docker repo and image pull

## 2024.14.12
- **Avahi**
  - Changed to use Debian over Alpine to fix warning for missing packages
  - Updated overview and options in template for mDNS

## 2024.14.12
- **Avahi**
  - Added new template for mDNS

## 2024.09.12
- **ClamAV-clamdscan**
  - Set PUID and PGID target for file access
  - Set privileged false due to template errors via CA

- **rejettohfs3**
  - Added feature request PUID and PGID to template [Forum](https://forums.unraid.net/topic/180463-support-rejetto-hfs-3/#findComment-1495700)

## 2024.06.11
- **ClamAV-clamdscan**
  - Add new template and data

- **rejettohfs3**
  - Set VFS home file in template
  - See discussion: https://github.com/rejetto/hfs/discussions/792
  - Updated Quick Guide for extra data and fixed presentation and spelling mistakes.

## 2024.03.11
- **rejettohfs3**
  - Set network to Unraid default br0
  - Removed duplicate line at top in overview
  - Fixed example cert path and command, set it to templates path shared
  - Updated icon from rejettohfs3.png to rejettohfs.png
  - Updated Quick Guide for presentation and spelling mistakes.

## 2024.02.11
- **rejettohfs3**
  - Add links and data for new application
