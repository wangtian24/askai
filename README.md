# askai

Tiny CLI that asks Claude Haiku one question and either runs a bash command for you or answers a normal question.

## Install

```bash
git clone <this-repo> askai
cd askai
chmod +x askai
ln -s "$PWD/askai" /usr/local/bin/askai   # or anywhere on $PATH
```

Copy `.env.example` to `.env` (gitignored) and fill in your key:

```bash
cp .env.example .env
# edit .env and set ANTHROPIC_API_KEY=sk-ant-...
chmod 600 .env
```

`.env` lives next to the `askai` script in the repo and is loaded at startup.

## Use

```bash
askai 'find all files larger than 100MB under my home'
askai 'what is the capital of mongolia'
```

If the prompt looks like a bash request, askai prints 1–3 command options; pick one and it runs immediately. Otherwise it prints a one-paragraph answer.

Uses `claude-haiku-4-5-20251001`, one turn, stdlib only (no pip install).
