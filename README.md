# psce Claude Code Plugin

Starter Claude Code plugin based on the Claude Code plugin docs.

## Structure

```text
.
├── .claude-plugin/
│   └── plugin.json
├── skills/
│   ├── hello/
│   │   └── SKILL.md
│   └── project-brief/
│       └── SKILL.md
└── README.md
```

## Local Test

From this directory:

```bash
claude --plugin-dir .
```

Then run one of the namespaced skills inside Claude Code:

```text
/psce:hello Alex
/psce:project-brief Build a small task tracker
```

After editing plugin files in an open Claude Code session, reload them:

```text
/reload-plugins
```

## Notes

- `.claude-plugin/plugin.json` contains plugin metadata.
- `skills/<skill-name>/SKILL.md` defines each skill.
- Skills are namespaced by the plugin name, so `skills/hello` becomes `/psce:hello`.
