# AIPM Changes v1.17
Origin: Perplexity, skill v1.17, 2026-11-20
Parent: 45957f7172b9f8b8d57e2affea59025c5e8c1f7e

Change 1: AIUPR short name and command prefix — AIUPR-1.25 renames the rules' short name from UAPR to AIUPR, so the skill uses AIUPR and the "AIUPR - " command prefix everywhere, while still working with older UAPR rules.
          Applies to: all AIs
          IDs: Perplexity UPD-046, Perplexity UPD-047
          Commands: every rules command (for example AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME, AIUPR - SAVE AIUPR, AIUPR - HELP), AI - LOAD AIUPR, AIPM - HELP, AIPM - RULES
          New text: Step 2 rule 2: "AIUPR commands start with `AIUPR - ` (one space on each side of the dash, AIUPR-1.25 or later), for example `AIUPR - SAVE AIUPR`. A command without the prefix, with the old `UAPR - ` prefix, or written as `AIPM - <AIUPR command>` (for example `AIPM - NEW PROJECT`), is not a command; ask whether the user meant the `AIUPR - ` form. If the rules in use are UAPR-1.24, their commands start with `UAPR - ` (for example `UAPR - SAVE UAPR`); if they are older than UAPR-1.24, use their command names as written there."
                    Step 1 item 3: "Compare by number: AIUPR-x.y continues the UAPR-x.y series (AIUPR-1.25 is higher than UAPR-1.24)."
                    Every other UAPR mention becomes AIUPR (`UAPR - <COMMAND>` becomes `AIUPR - <COMMAND>`, `SAVE UAPR` becomes `SAVE AIUPR`, `AI - LOAD UAPR` becomes `AI - LOAD AIUPR`), except GitHub file names, the rules link, the `UPDATE UAPR` note and references to older UAPR versions (for example UAPR-1.16, UAPR-1.21).
          Platform parts: none.

Change 2: New title AI UNIVERSAL PROJECT RULES — the rules title changes from UNIVERSAL AI PROJECT RULES, so the skill finds rules files with either title and either file name style, and names the new title in its help and description.
          Applies to: all AIs
          IDs: Perplexity UPD-048
          Commands: AIPM - HELP, AIPM - RULES, AIUPR - LOAD RULES
          New text: A rules file is one whose first heading is "# AI UNIVERSAL PROJECT RULES" or the older "# UNIVERSAL AI PROJECT RULES"; file names match "(universal[ _-]*ai|ai[ _-]*universal)[ _-]*project[ _-]*rules" in any capitalization.
                    Help item 2: "AI UNIVERSAL PROJECT RULES (AIUPR, formerly UNIVERSAL AI PROJECT RULES) is the rulebook"
                    Rules link: "The folder, file name and link keep `UNIVERSAL_AI_PROJECT_RULES` and `UAPR` on purpose (AIUPR section 2 rule 14a)."
          Platform parts: how each AI finds attached files (Perplexity uses a bash finder script over its uploads and workspace).
