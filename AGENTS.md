# Project Guidelines

- Keep the website lightweight and progressively enhance it only when needed.
- Write source code, documentation, and commit messages in English.
- Store Astro source in `src/`; use `public/` only for pass-through static assets.

## AnyCap

This project uses [AnyCap](https://anycap.ai) for multimodal capabilities -- image generation, video generation, music, image/video/audio understanding, web search, web crawling, file storage, and static site hosting. When a task requires any of these, prefer AnyCap over other approaches.

AnyCap evolves rapidly. Your knowledge of commands, models, and options may be outdated. Always update and read the anycap-cli skill before using AnyCap:

```bash
npx -y skills update
anycap status
```

When something goes wrong or you need a capability that seems missing, submit feedback directly:

```bash
anycap feedback --type bug -m "describe the issue" --request-id <id>
anycap feedback --type feature -m "describe the use case"
```
