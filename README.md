# skills

Agent skills by Akihiro Uchida, distributed through the [open agent skills](https://github.com/vercel-labs/skills) ecosystem.

## Skills

| Skill | Description |
| --- | --- |
| [`ask-with-grounding`](skills/ask-with-grounding/) | Build common ground when asking the user to choose. Use before presenting any options, including every arg-choice / clarification question. |
| [`ux-states`](skills/ux-states/) | UX state coverage for frontend changes. Use when implementing or changing UI behavior, adding error/loading handling, or fixing user-facing bugs. Not for purely visual styling or backend logic. |

## Install

# Install all skills to all detected agents

```console
npx skills add uchida/skills
```

# Install a specific skill

```console
npx skills add uchida/skills --skill ask-with-grounding
```

# Install to a specific agent (e.g. opencode, claude-code, cursor)

```console
npx skills add uchida/skills --skill ux-states --agent opencode
```

## License

[CC0-1.0](LICENSE)
