# AIPM Changes v3

Origin: Grok, skill v3, 2026-11-22
Parent: d4d72c879dfcd7a931a2ad58e029d6cac6d3e773

Change 1: AIPM - SYNC command and supporting updates — Adds the SYNC command so Grok can read other AIs' changes files and offer unsynced changes for owner approval; updates PUSH/PULL paths to AIs/Grok/ and expands PUSH to the five-file set (skill, archive, CMDS.txt, Changes, Synced).
          Applies to: all AIs
          IDs: Grok UPD-001, Grok UPD-002
          Synced from: Claude v9 Change 2
          Commands: AIPM - SYNC, AIPM - PUSH, AIPM - PULL, AIPM - cmds, help
          New text: (see skill section 12 for the full SYNC procedure; section 5 for the updated PUSH; section 7 for the CMDS line "AIPM - SYNC - Reads the other AIs' changes files and offers every change not yet synced for approval")
          Platform parts: AIs/Grok/ folder name; Grok-specific tool paths and sandbox commands
