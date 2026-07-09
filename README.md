# claude-commands

Personal [Claude Code](https://claude.com/claude-code) slash commands, distributed as a plugin marketplace.

Marketplace name: **`kuno-commands`**

## Install (recommended: plugin marketplace)

Inside Claude Code:

```
/plugin marketplace add Papillon6814/claude-commands
/plugin install japanese-english@kuno-commands
```

Updates later:

```
/plugin marketplace update kuno-commands
```

## Commands

### `/japanese-english`

Converts Japanese (or a rough English draft) into **simple, correct English that a Japanese non-native speaker could naturally have written themselves**. Built for Slack / chat messages with overseas teammates.

- Vocabulary limited to CEFR A2–B1 (junior/senior high school level)
- Grammar stays correct. The goal is *plain* English, not *broken* English
- One idea per sentence; avoids idioms, slang, and business jargon
- Slack-casual tone by default; pass `--formal` for polite email style

Usage:

```
/japanese-english 来週のリリースに間に合いそうか教えてほしい
/japanese-english "here is my draft ..." --formal
```

## Install without the marketplace

Copy the command file into your commands directory.

Globally (all projects):

```bash
curl -o ~/.claude/commands/japanese-english.md \
  https://raw.githubusercontent.com/Papillon6814/claude-commands/main/plugins/japanese-english/commands/japanese-english.md
```

Per project: put the file in `.claude/commands/` instead.

## Repository layout

```
.claude-plugin/marketplace.json          # marketplace catalog
plugins/japanese-english/
  .claude-plugin/plugin.json             # plugin manifest
  commands/japanese-english.md           # the slash command
```

To add more commands: create another folder under `plugins/`, add its `plugin.json` and `commands/`, then list it in `marketplace.json`.

## License

MIT
