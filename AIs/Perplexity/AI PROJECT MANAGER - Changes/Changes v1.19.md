# AIPM Changes v1.19
Origin: Perplexity, skill v1.19, 2026-11-21
Parent: fc1ce5711a8753a6d58e10873b642ab74f540ff8

Change 1: AIPM - COMPARE (steps 1 and 6) — ask before reading, and label platform-only differences. Reading the repository is a fetch, so the compare names the source and the AIs picked and asks Yes/No first (AIUPR section 2 rule 12). In the results, a difference that comes only from the platform is marked "platform (expected)".
          Applies to: all AIs
          IDs: Perplexity UPD-052
          Synced from: Claude v13 Change 2
          Commands: AIPM - COMPARE
          New text: "1. Name the source (`JoeIsAtWork/AUTOMATION_RULES`, `main`) and the AIs picked, and ask one Yes/No card before reading (AIUPR section 2 rule 12). No stops with nothing read."
                    "Mark differences that come only from the platform (folders, connectors, tools) as **platform (expected)**."
          Platform parts: Yes/No card (Perplexity) or the AI's own way of asking.

Change 2: AIPM - PUSH (step 4) — in the skill push commit message, N counts the distinct update IDs built into that version, so every AI counts the same way.
          Applies to: all AIs
          IDs: Perplexity UPD-053
          Synced from: Claude v14 Change 1
          Commands: AIPM - PUSH
          New text: "Commit message: first line `AIPM - v<VER> (<N> Changes)`, where N is the number of update items (distinct `Perplexity UPD-` IDs) built into that version; then any attribution lines the platform requires."
          Platform parts: the AI name in the ID prefix (`Perplexity UPD-` becomes your own).

Change 3: Changes file and AIPM - PUSH (step 3) — a published changes file is never overwritten or edited; a fix goes in the next version's changes file as a change of its own.
          Applies to: all AIs
          IDs: Perplexity UPD-054
          Synced from: Claude v14 Change 2
          Commands: AIPM - PUSH
          New text: "Never overwrite or edit a published changes file. Fixes go in the next version's changes file, as a change of their own."
          Platform parts: none.

Change 4: After every save, AIPM - PULL and Step 2 rule 4 — check that a saved skill really landed, and check the saved skill against GitHub before GitHub commands. Why: Perplexity v1.15 to v1.18 were pushed to GitHub but the skill library kept v1.14, because "saved" was reported without reading the library back.
          Applies to: all AIs
          IDs: Perplexity UPD-055
          Commands: AIPM - PUSH, AIPM - PULL, AIPM - SYNC, AIPM - COMPARE, AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME
          New text: "1. **Check the save.** Load the skill again from the library (same name and scope) and compute the SHA-256 of its `SKILL.md`. Its `metadata.version` and SHA-256 must equal the built file. Only then report `Saved v<VER>`. If they differ, report `Save failed: library has v<X>, built v<Y>` and push nothing until it is fixed."
                    "AIPM - PULL, Higher: replace the saved skill in place (same name, same scope) automatically, check the save (\"After every save or update of this skill\" step 1) and report `Replaced v<old> → v<new>`."
                    "4. **Skill version check (start of `AIPM - PUSH`, `AIPM - PULL`, `AIPM - SYNC`, `AIPM - COMPARE`, `AIUPR - LOAD RULES`, `AIUPR - NEW PROJECT` and `AIUPR - RESUME`).** Before anything else the command does, compare this saved skill's `metadata.version` with that of `AIs/<AI>/AI_PROJECT_MANAGER.md` on `main`, number by number. If GitHub is higher, say so first in one line, `Saved skill v<X> is behind GitHub v<Y>.`, and offer `AIPM - PULL` before anything else; run nothing more until the user answers. Same or lower: say nothing and continue."
                    "This read needs the user's approval (AIUPR section 2 rule 12). `AIPM - PUSH` is covered by its own fetch of `main` (and by rule 16 after `AIUPR - BUILD`); `AIPM - SYNC` and `AIPM - COMPARE` include it in their one Yes/No card; for `AIPM - PULL` the pull itself is the check. For `AIUPR - LOAD RULES`, `AIUPR - NEW PROJECT` and `AIUPR - RESUME`, the rules-link standing approval covers only the rules file, so ask one Yes/No first, \"Also check the saved AIPM skill against GitHub?\", unless the rules in use give standing approval for this read. No skips the check. If the read fails, say so in one line and continue."
          Platform parts: how the saved skill is read back (Perplexity reloads it from the skill library; Claude checks the saved update card); the folder AIs/Perplexity/ becomes your own; Yes/No card or the AI's own way of asking.
