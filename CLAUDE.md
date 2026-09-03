# CLAUDE.md — GitHub Profile README Project

This file is the standing brief for Claude Code (or any future Claude session)
working on `ujjwalmishraa24/ujjwalmishraa24`, the special GitHub repo that
renders as the profile page.

## Owner

- **Name:** Ujjwal Mishra
- **GitHub:** [@ujjwalmishraa24](https://github.com/ujjwalmishraa24)
- **LinkedIn:** https://www.linkedin.com/in/ujjwal-mishra-7b65aa323/
- **Daily driver:** Arch Linux + Hyprland
- **Editor:** Neovim + tmux
- **Background:** pre-final year CS student, likes deep-diving into low-level
  systems, mainly codes in C/C++ and Python, tinkers in other stacks,
  into hardware/electronics, into open source.

## Aesthetic — non-negotiable

- Dark, terminal/CLI-flavored. Think `neofetch` output, not a SaaS landing page.
- Palette: **Tokyo Night** — bg `#1a1b26`, fg `#a9b1d6`, accent `#7aa2f7`,
  muted accent `#565f89`. No neon glow, no rainbow badges, no gradients.
- Monospace font for headers (Fira Code via readme-typing-svg).
- Every external widget (stats card, streak card, activity graph, snake) is
  pinned to the `tokyonight` / `tokyo-night` theme option and transparent
  background so it sits flush on GitHub's dark mode.
- No emoji spam. A few used sparingly as section markers is fine, not as
  decoration on every line.

## Structure of README.md

1. Typing-SVG header — name + rotating one-liners (tagline: "Curious about
   everything").
2. `whoami` block — neofetch-style fenced code block with OS/WM/editor/shell.
3. Tech stack — grouped by family, NOT one flat wall of badges:
   - Languages
   - Web / Backend
   - Data / ML
   - Databases
   - Cloud / DevOps / Tools
4. GitHub stats row — stats card + top languages, side by side.
5. Streak stats.
6. Contribution activity graph (dynamic, theme-matched).
7. Snake contribution animation (needs the workflow below — GitHub can't
   generate this from a static README alone).
8. Contact — LinkedIn badge only, per owner's request.
9. Footer — visitor counter, base offset **1111**, via komarev's `ghpvc`
   endpoint (`&base=1111`). This is a third-party best-effort counter, not a
   real analytics source — note that if asked.

## Companion file: `.github/workflows/snake.yml`

The "dynamic contribution graph" that looks like a snake eating the
contribution squares is NOT possible from README markdown alone — it needs
a scheduled GitHub Action (`platane/snk`) that generates an SVG on an
`output` branch, which the README then embeds. Ship this workflow alongside
the README or the snake image will 404.

## Do

- Keep badge label/background colors consistent across all shields.io badges
  (`color=1a1b26&logoColor=7aa2f7&style=for-the-badge`) so the stack section
  reads as one coherent block, not a badge farm.
- Keep line lengths and section order stable if regenerating — diffs should
  stay readable.
- When adding a new tech to the stack, put it in the correct family row, not
  at the end of a random row.

## Don't

- Don't add glowing/animated GIF banners, wave dividers, or "typing code"
  screenshots — that's the "flashy slop" aesthetic explicitly rejected.
- Don't use `github-profile-views-counter` style badges that show raw
  numbers without the `base` offset — the ask was specifically "start from
  1111."
- Don't invent projects, stats, or achievements not confirmed by the owner.

## Open items / things Claude should ask about before changing

- Pinned repos section (not requested yet — ask before adding).
- Whether to enable the snake workflow requires repo Actions permissions;
  Claude can draft the YAML but the owner has to push it and let the first
  scheduled run fire (or trigger manually via `workflow_dispatch`).
