# AGENTS.md

> Instructions for AI coding agents. Follows the [agents.md](https://agents.md) spec.

This repository provides a Claude Code skill for **solscan** (see `SKILL.md`), packaged standalone. Content works with any AI agent — Claude Code auto-triggers it; Codex / Cursor / Windsurf / OpenCode read `SKILL.md` or this file as rules.

## Operating rules

1. **Credits are real money.** Respect budget thresholds documented in `references/credits.md` (where present). Announce estimated cost before expensive calls; stop at hard caps without explicit user approval.
2. **Scripts for batches, direct calls for exploration.** Over ~10 API calls of similar shape → write an async Python script with `asyncio.Semaphore`, resume-safe JSONL output, and rate-limit header monitoring. Templates in `references/examples/`.
3. **Prefer batch / parsed / enhanced endpoints** where the provider offers them (documented in each reference file).
4. **Never hardcode API keys** — read from env vars listed in `.env.example`.

## Setup

See `README.md` and `INSTALL.md`. For Python examples: `pip install aiohttp httpx` and set the keys from `.env.example`.

## Part of a collection

This skill is one of four — see umbrella at https://github.com/Vo1ganin/crypto-claude-skills.

## License

MIT.
