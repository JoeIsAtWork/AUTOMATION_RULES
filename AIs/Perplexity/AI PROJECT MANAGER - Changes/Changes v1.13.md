# AIPM Changes v1.13
Origin: Perplexity, skill v1.13, 2026-11-20
Parent: 75d6d68a495013fd0c171b985fd90176dd2d61a4

Change 1: Changes file and AIPM - SYNC — three rules for writing changes files so every AI can follow them without questions (UAPR-1.20 section 2 rule 16e, drafted). The rules were proposed by Claude in conversation, not in a Claude changes file, so this change has no Synced from line.
          Applies to: all AIs
          IDs: Perplexity UPD-029
          Commands: AIPM - PUSH, AIPM - SYNC
          New text: (for reference, adapt to your platform)
                    - Writing changes clearly (UAPR section 2 rule 16e, if the rules in use have it; follow it either way):
                      1. One change, one origin. A change with a "Synced from:" line holds only what came from that source. Anything added while syncing goes in a separate change of this skill's own, with no "Synced from:" line, so the other AIs can sync it.
                      2. Shared behavior is never a platform part. Anything every AI should do the same way (file names, commit messages, version-bump rules, record formats) is written as shared text in the change. "Platform parts:" lists only what really differs, such as folder names, tools and buttons.
                      3. Exact text, not descriptions. "New text:" gives the literal words to use (for example the exact commit message), never "the AI's choice".
                    AIPM - SYNC step 7: On BUILD, apply the approved items into a new skill version (anything added beyond the synced change is its own item and its own change, rule 1 above).
          Platform parts: none.
