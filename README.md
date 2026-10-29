# AxForge agents

Five ready agents for [Claude Code](https://code.claude.com) and [OpenCode](https://opencode.ai), each running on
the model your tool is set to on the [AxForge](https://axforge.ai) API: Qwen, MiMo or GLM.

| Agent | What it does |
|---|---|
| `fullstack` | Builds a feature end to end in the project's own stack: data, API, user interface and tests. |
| `frontend` | Builds and fixes user interfaces: components, styles, state, forms, accessibility. |
| `backend` | Builds and fixes services: APIs, data models, queries, migrations, background jobs. |
| `devops` | Sets up and fixes building, testing, shipping and running: Dockerfiles, CI, infrastructure, logs. It asks before it runs a command. |
| `security` | Reviews code and configuration for security problems and reports each with its fix. It changes nothing. |

The same five are here twice, once in each tool's format: `.claude/agents/` for Claude Code and `.opencode/agents/`
for OpenCode.

## Before you start

1. **An AxForge API key**, and your tool set up for AxForge. The console's
   [Connect page](https://console.axforge.ai/connect) gives your tool's settings with a key made for it, filled in.
2. **Our web search** for the agents (optional): the same page adds `axforge-search`, an MCP server with
   `web_search` and `read_page`. The agents use it to look up current documentation and unknown errors.

## Use them

**Claude Code.** Copy the folder `.claude/agents/` into your project, or into `~/.claude/agents/` (on Windows
`%USERPROFILE%\.claude\agents\`) to have them in every project. Then ask for one by name ("Use the backend agent to
add a health route") or type `@` and pick it. Each runs on your main model (`model: inherit`): Qwen, MiMo or
GLM, the one your tool's guide set.

**OpenCode.** Copy the folder `.opencode/agents/` into your project, or into `~/.config/opencode/agents/` to have
them in every project. Press Tab to switch to one, or mention it (`@backend add a health route`). Each runs on
the model your `opencode.json` starts with: Qwen, MiMo or GLM from the AxForge provider.

## Make them yours

Each agent is one Markdown file: a few lines on top that say its name, what it is for and its model, then its
instructions in plain words. Change the words to fit your project, or copy one to make a sixth.

## License

MIT, see [LICENSE](LICENSE).
