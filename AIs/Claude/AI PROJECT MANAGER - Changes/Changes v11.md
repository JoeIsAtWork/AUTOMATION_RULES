# AIPM Changes v11
Origin: Claude, skill v11, 2026-11-20
Parent: 9f367856a4a1d3dfc49c32b69712656df87b93a3

Change 1: Push (section 5 step 9) and AIPM - SYNC (section 13 step 7) — a push of the sync record on its own (a sync that built nothing, only Already have or Declined lines) has no version bump, holds only that file, uses a fixed commit message, and is read back afterwards.
          Applies to: all AIs
          IDs: Claude UPD-027
          Synced from: Perplexity v1.11 Change 1
          Commands: AIPM - PUSH, AIPM - SYNC
          New text: (for reference, adapt to your platform)
                    9. Synced.txt alone (a sync that built nothing): no version bump. Show the exact write and ask Yes/No first. Then one commit on top of the fetched main that adds or replaces only AIs/<AI>/AI PROJECT MANAGER - Synced.txt, with the same checks and limits as above. Commit message: first line "AIPM - Synced (<N> Changes)", where <N> is the number of new lines; then a blank line and any attribution lines your platform requires. Afterwards, read the file back from the new commit ID and check that its bytes match.
          Platform parts: Folder AIs/Claude/ becomes your own folder; Claude adds its session attribution lines after the commit message.
