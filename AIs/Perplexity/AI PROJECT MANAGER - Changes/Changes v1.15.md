# AIPM Changes v1.15
Origin: Perplexity, skill v1.15, 2026-11-20
Parent: 312fc903c95a3d52aa8d34655e1c8471345ecf4e

Change 1: Rules check and LOAD RULES — UPDATE UAPR was merged into LOAD RULES and removed (UAPR-1.21), so the skill no longer refers to UPDATE UAPR. LOAD RULES now also handles the case where rules are already in use, by comparing versions.
          Applies to: all AIs
          IDs: Perplexity UPD-033
          Commands: LOAD RULES, UPDATE UAPR (removed), NEW PROJECT, RESUME
          New text: Rules check before NEW PROJECT and RESUME: "Do what `LOAD RULES` does, whether or not rules are in use (with rules in use, a higher version on GitHub becomes the rules in use, Rules link step 6)."
                    LOAD RULES step 6: "Read the whole file. If no rules are in use yet, choose between this copy and any uploaded copy as step 1 item 3 says; if `PROJECT.md` or a handoff records a different rules version or hash, quote both version lines and ask before any other work. If rules are already in use, compare this copy with them (UAPR section 2 rule 13f): a higher version becomes the rules in use (for `NEW PROJECT` and `RESUME`, for that command itself) and the old and new version and SHA-256 are reported; same version and same SHA-256 means already current; same version with different content gets both version lines quoted and a question; a lower version is kept out and both versions are reported."
                    LOAD RULES step 8: "For `LOAD RULES`, reply with the full check line `Rules: <version>, read from GitHub <C>, SHA-256 <hash> | Mode: <mode>` and one line confirming the version and mode (when rules were already in use, the old and new version and SHA-256, or "already current"). Do nothing else."
                    Note: "`UPDATE UAPR` is no longer a command (merged into `LOAD RULES` in UAPR-1.21); if the rules in use still list it, follow them."
          Platform parts: none.
