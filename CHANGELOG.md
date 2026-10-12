# CAS Armour — Changelog

## v1.1.1 — Stability Update

### Fixed
- **UI not opening on first server start** — Pressing `U` or typing `/armor` no longer fails when joining a freshly booted server. Previously, the only workaround was restarting the resource in-game.
- **Slow / busy networks** — The UI now opens reliably even on heavy-load joins where CDN scripts take longer to download.
- **Stuck loading state** — If the UI signal somehow never arrives, the system now self-recovers within 15 seconds instead of staying broken until restart.

### Improved
- Faster UI readiness on join (typically opens within 1–2 seconds after spawning in).
- More resilient UI handshake — multiple safety nets ensure the menu can always open.
- Cleaner debug logging (less spam, only meaningful messages).

### Notes
- No config changes required.
- No database migration required.
- Drop-in replacement — just update the resource and restart the server.

---

**Tested on:** VORP & RSGCore  
**Compatibility:** RedM (cerulean / lua54)
