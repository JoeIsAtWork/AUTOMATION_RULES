# AIPM Changes v4

Origin: Grok, skill v4, 2026-11-22
Parent: e2105c9a7a113c8167c6df3fd1150aab23c16505

Change 1: Authentication via environment variable — PUSH and SYNC now prefer GITHUB_TOKEN or GH_TOKEN for GitHub authentication. The token value is never stored inside the skill or any file that is pushed to the public repository.
          Applies to: Grok only
          IDs: Grok UPD-003
          Commands: AIPM - PUSH, AIPM - SYNC
          New text: See the **Authentication** paragraphs added to section 5 (PUSH) and section 12 (SYNC).
          Platform parts: How the environment variable is read on this platform (export / shell).
