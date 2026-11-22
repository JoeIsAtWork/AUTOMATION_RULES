# AIPM Changes v17
Origin: Claude, skill v17, 2026-11-21
Parent: 6f17a308fb49e3c0d016a70db3a6dafd28a3449f

Change 1: Check the save and the skill version check — read a saved skill back before reporting it saved, and compare the saved skill with GitHub at the start of the GitHub and rules commands.
          Applies to: all AIs
          IDs: Claude UPD-038
          Synced from: Perplexity v1.19 Change 4
          Commands: AIPM - PUSH, AIPM - PULL, AIPM - SYNC, AIPM - COMPARE, AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME
          New text: "**Check the save.** After the owner saves an update card for this skill, read the saved skill back (on Claude, the synced copy of its `SKILL.md`; the copy can lag a minute behind the save) and compute its SHA-256. Its `Skill version:` line and SHA-256 must equal the built file. Only then report `Saved v<VER>`. If they differ, report `Save failed: library has v<X>, built v<Y>` and push nothing until it is fixed."
                    "**Skill version check (start of `AIPM - PUSH`, `AIPM - PULL`, `AIPM - SYNC`, `AIPM - COMPARE`, `AIUPR - LOAD RULES`, `AIUPR - NEW PROJECT` and `AIUPR - RESUME`, including an automatic resume).** Before anything else the command does, compare this saved skill's `Skill version:` with that of `AIs/Claude/AI_PROJECT_MANAGER.md` on `main` of `JoeIsAtWork/AUTOMATION_RULES`, number by number. If GitHub is higher, say so first in one line, `Saved skill v<X> is behind GitHub v<Y>.`, and offer `AIPM - PULL` before anything else; run nothing more until the owner answers. Same or lower: say nothing and continue."
          Platform parts: Claude reads the synced copy of its SKILL.md and checks its `Skill version:` line (Perplexity reloads its library and uses metadata.version); Claude keeps offering an update card on `AIPM - PULL` instead of replacing the saved skill itself; folder AIs/Claude/.

Change 2: Wording fix for the skill version check — LOAD RULES keeps "no extra Yes/No" and "do nothing else" except the skill check's own question and "behind GitHub" line; two questions due at once share one card.
          Applies to: all AIs
          IDs: Claude UPD-039
          Synced from: Perplexity v1.20 Change 1
          Commands: AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME
          New text: Section 10 step 1: "no extra Yes/No (the skill version check, section 3, keeps its own question)."
                    Section 10 step 6: "Do nothing else, except the skill version check (section 3): its Yes/No, and the line `Saved skill v<X> is behind GitHub v<Y>.` with the `AIPM - PULL` offer when GitHub is higher."
                    "**One card, not two.** When `AIUPR - NEW PROJECT` or `AIUPR - RESUME` needs both the rules fetch question (section 11 step 1) and the skill version check question, ask them together in one card with one shared submit: \"Fetch the rules from GitHub to check they're current?\" and \"Also check the saved AIPM skill against GitHub?\", each Yes/No."
          Platform parts: section and step numbers in Claude's skill; Claude's question card.
