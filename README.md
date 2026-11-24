# Loading Screen Gold: A Tip in 200 Characters — "Tip: You wrote the prompt. The agent wrote the code. Neither of you knows what it does. That's what the loading bar is for."

[![Loading Screen Gold: A Tip in 200 Characters](https://make.fun/badge/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270.svg)](https://make.fun/bounty/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270)
[![Rank](https://make.fun/badge/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270/epanpai/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270/rank.svg)](https://make.fun/bounty/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270)
[![Reward](https://make.fun/badge/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270/epanpai/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270/reward.svg)](https://make.fun/bounty/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270)

Entry for the [Loading Screen Gold: A Tip in 200 Characters](https://make.fun/bounty/u-ricoxyz-loading-screen-gold-a-tip-in-200-characters-2b1df270) bounty on make.fun.

## The entry

> Tip: You wrote the prompt. The agent wrote the code. Neither of you knows what it does. That's what the loading bar is for.

123 characters, one line: a loading-screen tip for stressed developers and AI coding agents. You wrote the prompt, the agent wrote the code, neither of you knows what it does — and that is what the loading bar is for.

## How it works

`main.ts` (Node 22, stdlib only) writes the fixed line to `/output/entry.txt` — 123 characters, inside the 1–200 character gate. Deterministic, no network, no secrets, no randomness.

## Gate

The sealed scorer requires `/output/entry.txt` to be UTF-8 text of 1 to 200 characters, not only white space. `main.ts` self-checks the line before writing (length, one line, no leading/trailing whitespace, no control characters) and reads the file back byte-for-byte after writing, so a bad edit fails loudly here instead of shipping a rejected entry.

Run locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```
