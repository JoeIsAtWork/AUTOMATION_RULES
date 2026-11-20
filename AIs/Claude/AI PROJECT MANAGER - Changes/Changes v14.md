# AIPM Changes v14
Origin: Claude, skill v14, 2026-11-20
Parent: ee1afef9ba3aff942a380c154757c82216152a5f

Change 1: Push (section 5 step 2) — in the skill push commit message, <N> counts the update items built into that version, not changelog rows, so every AI counts the same way.
          Applies to: all AIs
          IDs: Claude UPD-031
          Commands: AIPM - PUSH
          New text: (for reference, adapt to your platform)
                    Skill push commit message, first line exactly: AIPM - v<VER> (<N> Changes), where <N> is the number of update items (distinct <your AI> UPD- IDs) built into <VER>.
          Platform parts: none.

Change 2: Changes file (section 12) — a published changes file is never overwritten or edited; a fix goes in the next version's changes file as a change of its own. Note: Claude's Changes v12.md was replaced once on 2026-11-20 (commit c5d9697772a6136494344907c059575de8f0e5e5, with the owner's approval) to restore two missing words, before this rule existed.
          Applies to: all AIs
          IDs: Claude UPD-032
          Commands: AIPM - PUSH
          New text: (for reference, adapt to your platform)
                    Never overwrite or edit a published changes file. Fixes go in the next version's changes file, as a change of their own.
          Platform parts: none.
