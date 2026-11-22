# Herd for Claude

[Herd](https://useherd.app) finds public posts on Threads, Reddit, Instagram, X and YouTube that
name your business, and labels each post positive, neutral or negative. This plugin connects
Claude to your Herd account, so you can ask Claude about your mentions, your weekly report and
your keywords.

You need a Herd account. The Free Plan works. Finish the setup at https://useherd.app/app first.

## Install

Claude Code:

```bash
claude plugin marketplace add limwaihong/herd-claude-plugin
claude plugin install herd@useherd
```

claude.ai and Cowork: add Herd from the Claude directory, or add `https://useherd.app/mcp`
as a custom connector.

The first time Claude uses Herd, you sign in to Herd and select **Allow**. To remove the access,
go to Herd → Settings → Connected apps.

## Skills

| Skill | Does |
| --- | --- |
| `/herd:brief` | A short summary of this week's posts, with the main topics of negative posts |
| `/herd:replies` | Reply drafts for the latest negative posts. Herd posts nothing. |

## Tools

`list_keywords`, `add_keyword`, `remove_keyword`, `list_mentions`, `get_report` and
`translate_post`.

## What the plugin sends, and where

The plugin has no code. It sends tool calls to one place only: the Herd MCP server at
`https://useherd.app/mcp`, with your Herd OAuth token. Herd reads and changes only your own
Herd data. The plugin keeps no data. Read the [Herd privacy policy](https://useherd.app/privacy).

## Support

https://useherd.app/support or hello@useherd.app.
