# Unraid Docker Compose Templates

These Compose files are alternate deployment references corresponding to the original [Community Applications XML templates](../templates). **Nothing in the templates/ directory is modified by this collection.**

The original XMLs remain the authoritative CA WebUI representations. Compose is meant for manual Compose managers on Unraid and is not automatically imported by the Unraid CA template manager.

All examples are self-contained and include environment variables within compose.yaml. Before deployment, review mount locations, networking, credentials, permissions, image compatibility and application-specific upstream instructions.

- [NetProbe](netprobe/compose.yaml) — [original XML](../templates/netprobe.xml)
- [SFTP-Fail2ban](sftp2/compose.yaml) — [original XML](../templates/sftp2.xml)
- [ClamAV-clamdscan](clamdscan/compose.yaml) — [original XML](../templates/clamdscan.xml)
- [PlexDBRepair](plexrepair/compose.yaml) — [original XML](../templates/plexrepair.xml)
- [RetroAssembly](retroassembly/compose.yaml) — [original XML](../templates/retroassembly.xml)
- [SMB User Web Portal](sambaweb/compose.yaml) — [original XML](../templates/sambaweb.xml)
- [Immich PostgreSQL 18](immich-postgress/compose.yaml) — [original XML](../templates/immich-postgress.xml)
- [Immich Valkey](immich-valkey/compose.yaml) — [original XML](../templates/immich-valkey.xml)

**Special cases:** PostgreSQL 18 migrations need independent backups and vendor instructions; Valkey requires a new password and matching Immich settings; SFTP needs administrator credentials; PlexDBRepair requires a verified backup and grants high privilege via Docker socket; SMB portal uses host networking and Unraid's /boot/config.
