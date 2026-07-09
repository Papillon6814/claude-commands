# claude-commands

Personal [Claude Code](https://claude.com/claude-code) slash commands.

## Commands

### `/japanese-english`

Converts Japanese (or a rough English draft) into **simple, correct English that a Japanese non-native speaker could naturally have written themselves**. Built for Slack / chat messages with overseas teammates.

- Vocabulary limited to CEFR A2–B1 (junior/senior high school level)
- Grammar stays correct — the goal is *plain* English, not *broken* English
- One idea per sentence; avoids idioms, slang, and business jargon
- Slack-casual tone by default; pass `--formal` for polite email style

**Usage**

```
/japanese-english 来週のリリースに間に合いそうか教えてほしい
/japanese-english "here is my draft ..." --formal
```

## Install

Copy the command(s) into your Claude Code commands directory.

**Globally (all projects):**

```bash
git clone https://github.com/Papillon6814/claude-commands.git
cp claude-commands/commands/*.md ~/.claude/commands/
```

**Per project:**

```bash
cp claude-commands/commands/*.md .claude/commands/
```

Then run the command inside Claude Code, e.g. `/japanese-english`.

## License

MIT
