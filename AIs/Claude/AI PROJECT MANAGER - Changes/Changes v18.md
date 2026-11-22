# AIPM Changes v18
Origin: Claude, skill v18, 2026-11-22
Parent: b4b1c8dff857aeb79b01b7375e016c54f3bd6318

Change 1: Applying the rules — in an Arduino project, every download a check needs (arduino-cli, the board core, libraries) is asked as one Yes/No naming the exact sources, before any download; Yes covers those downloads for that check only, No reports the check as Blocked (AIUPR section 2 rule 12).
          Applies to: all AIs
          IDs: Claude UPD-040
          Commands: AIUPR - TEST, AIUPR - RESUME, AIUPR - BUILD (any compile or test check)
          New text: "**Arduino compile downloads.** In an Arduino project, when a check (compile, tests) needs anything downloaded (arduino-cli, the board core, libraries), ask it as one Yes/No card naming the exact sources, before any download. Yes covers those downloads for that check only; No reports the check as Blocked."
          Platform parts: how the Yes/No is shown (Claude: one clickable card; AIs without cards: one copy box per answer).
