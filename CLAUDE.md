# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this project is

A single-page personal "визитка" (bio/portfolio card) for Александр — who he is, what he does, how to reach him. Audience is acquaintances, colleagues, and potential clients. It is explicitly **not** a blog or a corporate site, and it must stay a compact single page, not grow into a multi-page structure.

There is no build system, package manager, or test suite — the entire site is [index.html](index.html), a self-contained file with inline `<style>` and `<script>`. Open it directly in a browser to preview changes; there's nothing to build or lint.

## File layout

- [index.html](index.html) — the whole site. Structure: inline CSS (`:root` variables, then component styles) → `<body>` with a fixed background photo (`.bg-fixed`, embedded as a base64 data URI — this is why the file is large despite few lines) → content sections (`.about`, `.work-section`, `.facts-section`) → a small inline script that copies the hero photo into a blurred background layer.
- [profile.md](profile.md) — the owner's profile (who Александр is, strengths, interests). Read this first to understand who the site is for and to write in his voice.
- [про-меня.md](про-меня.md), [проекты.md](проекты.md), [факты.md](факты.md) — source drafts for the "Обо мне" / "Чем занимаюсь" / "Интересные факты" sections. These are the content of record; `index.html` is their rendered form. When content changes, keep the `.md` source and the HTML section in sync.
- [images/](images/) — source image(s) (e.g. `Основа.jpg`) used to produce the embedded photo in `index.html`.

## Content & tone rules

- Simple and honest — no pathos, no corporate clichés. Write in Александр's own words, using [profile.md](profile.md) as the reference for voice.
- Don't embellish or "sell" — substance over polish.
- Design: avoid bright/loud colors, avoid clutter and animation-for-its-own-sake, avoid generic corporate-landing-page templates. Current palette is a dark, warm, muted theme (`--accent: #D89A45` gold on near-black `--ink: #14110E`) with a serif (Georgia) typeface — stay consistent with this rather than introducing a new visual language.
- Keep the page compact. Before adding any new section or feature, check it against the project's purpose (a bio card, not a platform) — if it doesn't serve "show who I am and what I do," don't add it.
