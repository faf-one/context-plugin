The FAF plugin for any Agent Plugins client.

One plugin. It carries the `faf-mcp` 4.2.0 server and no skills. The server runs locally over stdio. It keeps a project's facts (stack, goal, commands, who, what, why) in `project.faf` (IANA media type `application/vnd.faf+yaml`), scores how complete that file is, and writes AGENTS.md, .cursorrules, CLAUDE.md, and GEMINI.md from it. Name the project path when you set a project up.

It needs Node.js 22 or later. `faf-mcp@4.2.0` sets `engines.node` to `>=22.0.0`, and `npx` uses that Node to start the server.

The plugin root is `plugins/faf/` (`plugin.json` is in that directory, not at the repository root). To install it locally in Cursor:

1. Copy `plugins/faf/` to `~/.cursor/plugins/local/faf`, so `plugin.json` is at `~/.cursor/plugins/local/faf/plugin.json`.
2. Run Developer: Reload Window, or restart Cursor.
3. Open Customize and confirm the `faf` MCP server.

Cursor's docs say a symlink under `~/.cursor/plugins/local` loads only when its target is a directory inside that folder, so copy the plugin directory rather than linking the repository.

## Use it

Point, run, get.

In Cursor's chat, name the project: `Set up FAF for /path/to/your/project`. project.faf goes next to that project's README.md.

Or run `npx faf-cli init` in your project's terminal.

Licence: MIT. See LICENSE.
