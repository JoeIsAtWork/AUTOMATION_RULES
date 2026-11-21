# AIPM Changes v15
Origin: Claude, skill v15, 2026-11-20
Parent: 13689dbccb4729396212aef78f0c4b6489388371

Change 1: LOAD RULES and the rules check — UPDATE UAPR was merged into LOAD RULES (UAPR-1.21), so the skill no longer runs UPDATE UAPR steps; LOAD RULES compares versions when rules are already in use.
          Applies to: all AIs
          IDs: Claude UPD-033
          Synced from: Perplexity v1.15 Change 1
          Commands: AIUPR - LOAD RULES, UPDATE UAPR (removed), AIUPR - NEW PROJECT, AIUPR - RESUME
          New text: Section 10 step 4: "If no rules are in use yet, choose between this copy and any uploaded copy as section 2 step 3 says; if `PROJECT.md` or a handoff records a different rules version or hash, quote both version lines and ask before any other work (AIUPR section 2 rule 13d). If rules are already in use, compare this copy with them (AIUPR section 2 rule 13f): a higher version becomes the rules in use (for `AIUPR - NEW PROJECT` and `AIUPR - RESUME`, for that command itself) and the old and new version and SHA-256 are reported; same version and same SHA-256 means already current; same version with different content gets both version lines quoted and a question; a lower version is kept out and both versions are reported."
                    Section 11 step 3: "do what `AIUPR - LOAD RULES` does with rules in use (section 10 step 4, AIUPR section 2 rule 13f) with the fetched copy"
                    Note: "`UPDATE UAPR` is no longer a command (merged into `LOAD RULES` in UAPR-1.21); if the rules in use still list it, follow them."
          Platform parts: none.

Change 2: Rules command prefix — UAPR-1.24 makes rules commands start with a prefix, so unprefixed and AIPM - forms of rules commands are no longer commands; plain help is removed.
          Applies to: all AIs
          IDs: Claude UPD-034
          Synced from: Perplexity v1.16 Change 1
          Commands: every rules command, AIPM - help, AIPM - LOAD RULES (removed), AIPM - <rules command> (removed)
          New text: "A rules command without the prefix, with the old `UAPR - ` prefix, or written as `AIPM - <rules command>` (for example `AIPM - NEW PROJECT`), is not a command; ask whether the owner meant the `AIUPR - ` form. If the rules in use are UAPR-1.24, their commands start with `UAPR - ` (for example `UAPR - SAVE UAPR`); if they are older than UAPR-1.24, use their command names as written there."
                    Help forms: "`AIPM - help`, `APM - help`, `AI PROJECT MANAGER help`, `AI PROJECT MANAGER - help`" (plain `help` removed).
          Platform parts: Claude removed its own `AIPM - LOAD RULES` and `AIPM - <rules command>` lines from its command list, trigger table and help page.

Change 3: Short name AIUPR and the AIUPR - prefix — AIUPR-1.25 renames the rules' short name from UAPR to AIUPR.
          Applies to: all AIs
          IDs: Claude UPD-035
          Synced from: Perplexity v1.17 Change 1
          Commands: every rules command (for example AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME, AIUPR - SAVE AIUPR, AIUPR - HELP), AIPM - help, AIPM - rules
          New text: "Rules commands start with `AIUPR - ` (one space on each side of the dash, AIUPR-1.25 or later), for example `AIUPR - SAVE AIUPR`."
                    Section 2 step 3: "Compare by number: AIUPR-x.y continues the UAPR-x.y series (AIUPR-1.25 is higher than UAPR-1.24)."
                    Every other UAPR mention becomes AIUPR, except GitHub file names, the rules link, the `UPDATE UAPR` note and references to older UAPR versions.
          Platform parts: Claude keeps the name `AI - LOAD UAPR` for its separate AI skill, which still uses that trigger.

Change 4: New title AI UNIVERSAL PROJECT RULES — the skill finds rules files under either title and either file-name style.
          Applies to: all AIs
          IDs: Claude UPD-036
          Synced from: Perplexity v1.17 Change 2
          Commands: AIPM - help, AIPM - rules, AIUPR - LOAD RULES
          New text: "A rules file is one whose first heading is `# AI UNIVERSAL PROJECT RULES` or the older `# UNIVERSAL AI PROJECT RULES`; file names match `(universal[ _-]*ai|ai[ _-]*universal)[ _-]*project[ _-]*rules` in any capitalization."
                    Help: "AI UNIVERSAL PROJECT RULES (AIUPR, formerly UNIVERSAL AI PROJECT RULES) is the rulebook."
                    Section 10: "The folder, file name and link keep `UNIVERSAL_AI_PROJECT_RULES` and `UAPR` on purpose."
          Platform parts: how each AI finds attached files (Claude uses `ls -t /mnt/user-data/uploads/ | grep -iE '(universal[ _-]*ai|ai[ _-]*universal)[ _-]*project[ _-]*rules'`).
