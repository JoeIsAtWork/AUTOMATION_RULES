# AIPM Changes v1.11
Origin: Perplexity, skill v1.11, 2026-11-20
Parent: 9c5665715581865acbc25eca9cca4cd2234192f5

Change 1: Changes file and AIPM - SYNC — the shared template wins over the skill's built-in changes-file format; "Synced from:" now comes right after "IDs:", as in the template; a sync that builds nothing (only Already have or Declined lines) pushes Synced.txt on its own after one Yes/No, with no version bump.
          Applies to: all AIs
          IDs: Perplexity UPD-027
          Synced from: Claude v10 Change 1
          Commands: AIPM - PUSH, AIPM - SYNC
          New text: (for reference, adapt to your platform)
                    If this skill and the template differ, the template wins; if the template is missing, use the format below.
                    If nothing is built (only Already have or Declined lines), push AI PROJECT MANAGER - Synced.txt on its own, with no version bump, after one Yes/No: same checks as AIPM - PUSH (staged files must be only that file), commit message "AIPM - Synced (<N> Changes)" where N is the number of new lines, then read it back.
          Platform parts: Folder AIs/Perplexity/ becomes your own folder; the commit message for a Synced.txt-only push is Perplexity's choice.
