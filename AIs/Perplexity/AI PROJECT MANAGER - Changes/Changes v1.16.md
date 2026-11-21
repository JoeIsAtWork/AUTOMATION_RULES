# AIPM Changes v1.16
Origin: Perplexity, skill v1.16, 2026-11-20
Parent: 833182d800cfb18486b9dca89ae6d2c6a1795f63

Change 1: UAPR command prefix — UAPR-1.24 makes every UAPR command start with "UAPR - " (one space on each side of the dash), so the skill now uses the prefixed forms everywhere and treats unprefixed forms as near-misses.
          Applies to: all AIs
          IDs: Perplexity UPD-039
          Commands: every UAPR command (for example UAPR - LOAD RULES, UAPR - NEW PROJECT, UAPR - RESUME, UAPR - SAVE UAPR, UAPR - HELP), AIPM - HELP
          New text: Step 2 rule 2: "UAPR commands start with `UAPR - ` (one space on each side of the dash, UAPR-1.24 or later), for example `UAPR - SAVE UAPR`. A UAPR command without the prefix, or written as `AIPM - <UAPR command>` (for example `AIPM - NEW PROJECT`), is not a command; ask whether the user meant the `UAPR - ` form. If the rules in use are older than UAPR-1.24, use their command names as written there."
                    AIPM - HELP also accepted: "`APM - help`, `AI PROJECT MANAGER help`, `AI PROJECT MANAGER - help`" (plain `help` removed).
                    Help item 5: "If the table has no help row, add `UAPR - HELP`."
                    Every other UAPR command mention: `<COMMAND>` becomes `UAPR - <COMMAND>`.
          Platform parts: none.
