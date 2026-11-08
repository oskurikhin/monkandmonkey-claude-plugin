# MonkAndMonkey for Claude

![MonkAndMonkey](logo.png)

[MonkAndMonkey](https://monkandmonkey.org) is a planner for tasks, shared project boards, habits, goals, journals and time tracking. This plugin connects Claude to your MonkAndMonkey account and teaches Claude how to use it well: compact daily briefs, safe edits by stable record IDs, and clear separation between board placement, deadlines, personal plans and completion.

## What it contains

- **MCP server reference** (`.mcp.json`): the hosted MonkAndMonkey connector at `https://monkandmonkey.org/mcp`. It is the same server as the MonkAndMonkey connector in the Claude directory, so you see one set of tools if you have both.
- **Skill** (`skills/monkandmonkey/SKILL.md`): guidance for daily briefs, analytics, shared projects and boards, and writes.

The plugin runs no local code, installs no packages, sets no hooks and reads no credentials from your machine.

## What you can do

- Get an actionable morning brief and see the tasks that need attention today.
- Create, edit, complete, reschedule or backlog tasks, add checklist steps and track time.
- Read shared project boards and members, create and edit cards, assign members and deadlines, move cards, and create or rename columns.
- Analyze habits, goals, streaks, journals and tracked time by day, project, life area, client, tag or goal.

The connector cannot delete or archive records, change shared-project membership or roles, manage payments, or reach other people's private data.

## Install

In Claude Code:

```bash
/plugin marketplace add oskurikhin/monkandmonkey-claude-plugin
/plugin install monkandmonkey@monkandmonkey
```

Then run `/mcp`, select **monkandmonkey** and sign in to MonkAndMonkey in your browser. In claude.ai, the desktop app and Cowork, install the plugin from the directory, or connect the MonkAndMonkey connector under Customize, then Connectors.

## Data and sign-in

Sign-in uses OAuth on monkandmonkey.org; no token is stored in this plugin. When Claude calls a MonkAndMonkey tool, the request goes to `https://monkandmonkey.org/mcp`, which checks it against your account's existing permissions. Data the tools return is sent to Claude so it can answer you. MonkAndMonkey receives only the tool requests, not your conversation. See the [privacy policy](https://monkandmonkey.org/privacy) and [setup guide](https://monkandmonkey.org/claude).

## Support

Email [support@monkandmonkey.org](mailto:support@monkandmonkey.org). Never send your password or tokens.

## License

MIT
