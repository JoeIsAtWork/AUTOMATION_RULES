# AIPM Changes v1.20
Origin: Perplexity, skill v1.20, 2026-11-21
Parent: 706620743ecb050fa2cab82cfcf809726d1ea4ce

Change 1: Rules link steps 1 and 8, Step 2 rule 4 — fixes a wording conflict from v1.19 Change 4: LOAD RULES said "no extra Yes/No" and "Do nothing else", but the new skill version check adds a question and a possible "behind GitHub" line. When NEW PROJECT or RESUME needs both the rules fetch question and the skill check question, they now share one card.
          Applies to: all AIs
          IDs: Perplexity UPD-056
          Commands: AIUPR - LOAD RULES, AIUPR - NEW PROJECT, AIUPR - RESUME
          New text: Rules link step 1 ends: "is the request for this one read; no extra Yes/No (the skill version check, step 2 rule 4, keeps its own question)."
                    Rules link step 8 ends: "Do nothing else, except the skill version check (step 2 rule 4): its Yes/No card, and the line `Saved skill v<X> is behind GitHub v<Y>.` with the `AIPM - PULL` offer when GitHub is higher."
                    Step 2 rule 4, new bullet: "**One card, not two.** When `AIUPR - NEW PROJECT` or `AIUPR - RESUME` needs both the rules fetch question (rule 3) and this question, ask them together in one card with one shared submit: \"Fetch the rules from GitHub to check they're current?\" and \"Also check the saved AIPM skill against GitHub?\", each Yes/No."
          Platform parts: card with one shared submit (Perplexity) or the AI's own way of asking two questions at once; section and step numbers in your own skill.
