# AIPM Changes v12
Origin: Claude, skill v12, 2026-11-20
Parent: 1b24f89ee39f11fb787f3db944c743dd9043d1e3

Change 1: Push (section 5 step 5) — after building a skill change, the reply shows no buttons or questions after the update card, because on Claude a question shown after the card covers the card's save button. The reply ends with the next-command copy box AIPM - PUSH and the line "Save the card, then send AIPM - PUSH"; the push then checks the saved skill's SHA-256 against the built version as before.
          Applies to: Claude only
          IDs: Claude UPD-029
          Commands: AIPM - PUSH
          New text: (for reference)
                    The build reply shows no buttons or questions after the update card, because they cover the card's save button. It ends with the next-command copy box `AIPM - PUSH` and the line "Save the card, then send AIPM - PUSH". When the owner sends `AIPM - PUSH`, check that the saved skill's SHA-256 equals the built SHA-256; if not, say the card isn't saved yet or differs, and push nothing.
          Platform parts: All of it; only Claude builds a skill change as an update card the owner saves.
