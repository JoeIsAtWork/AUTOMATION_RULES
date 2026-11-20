# AIPM Changes v10
Origin: Claude, skill v10, 2026-11-20
Parent: a07f414aa393b1e84a7322d138876753d830fe47

Change 1: Push (section 5), changes file (section 12) and AIPM - SYNC (section 13) — aligned with UAPR-1.19 section 2 rule 16d. The shared template sets the changes-file format; change IDs are written with the AI's name; Origin always names the writing AI and each synced change carries its own "Synced from" line; the sync record moves to AI PROJECT MANAGER - Synced.txt, one line per change (Applied, Already have or Declined); versions are compared number by number; a push writes up to five files, and Synced.txt pushed on its own needs a Yes/No. Correction: in Changes v9.md the IDs UPD-022 and UPD-023 mean Claude UPD-022 and Claude UPD-023 (the v9 file stays as published).
          Applies to: all AIs
          IDs: Claude UPD-025
          Commands: AIPM - PUSH, AIPM - SYNC
          New text: (for reference, adapt to your platform)
                    Changes file: format exactly as in AIs/AIPM Changes TEMPLATE.md (UAPR section 2 rule 16d); if your skill and the template differ, the template wins. Origin always names you; IDs always carry your AI's name; a synced change adds "Synced from: <AI> v<VER> Change <N>".
                    Sync record: AIs/<AI>/AI PROJECT MANAGER - Synced.txt, one line per change read from another AI: "<AI> v<VER> Change <N> - <Result>", optionally followed by " (<your AI> <ID>)"; Result is Applied, Already have or Declined; lines sorted by AI, then version compared number by number (v9 before v10, 1.9 before 1.10), then change number.
                    AIPM - SYNC: skip without a line every change that already has a line, every change for another AI only, and every change that started with you; offer the rest per change (approve, Already have, Decline); undecided changes get no line and come back next sync. With a build, Synced.txt goes in the same push as the skill (rule 16); with nothing built, push Synced.txt alone after one Yes/No.
                    Push: up to five files in one commit: skill, archive copy, CMDS.txt, Changes v<VER>.md, and Synced.txt when it changed.
          Platform parts: Claude's "Card saved" button and saved-skill SHA-256 check before pushing; the AIs/Claude/ paths (use your own folder).
