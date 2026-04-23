# Installation — solscan-skill

## Claude Code

```bash
git clone https://github.com/Vo1ganin/solscan-skill.git
mkdir -p ~/.claude/skills
cp -R solscan-skill ~/.claude/skills/solscan
```

Restart Claude Code — the skill auto-triggers on relevant prompts.

## Codex / Cursor / other AI agents

This repo follows the [agents.md](https://agents.md) spec. Most agents auto-read `SKILL.md` or `AGENTS.md` on project load. Alternatively, paste `SKILL.md` into your agent's rules / system prompt.

## API keys

```bash
cp .env.example .env
# fill in your keys, then:
set -a; source .env; set +a
```

## Run the Python examples directly

```bash
pip install aiohttp httpx
python references/examples/<example>.py --help
```

## Part of [`crypto-claude-skills`](https://github.com/Vo1ganin/crypto-claude-skills)

This skill is also included in the umbrella [`crypto-claude-skills`](https://github.com/Vo1ganin/crypto-claude-skills) collection alongside `dune-skill`, `solscan-skill`, `nansen-skill`, and `solana-rpc-skill`.
