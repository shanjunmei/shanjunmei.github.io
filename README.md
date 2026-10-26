# Personal Landing Pages

> A set of self-contained, single-file HTML personal pages for shanjunmei — Go backend architect, open-source maintainer (dig / digen), and AI Agent practitioner.

**[中文版](README.zh.md)**

---

## 1. Overview

Three independent HTML pages targeting different audiences, plus a standalone résumé. Every page is a single self-contained file (inline CSS + JS + i18n) that opens directly via `file://` or any static host. No build step, no shared dependencies, no external runtime — each file can be published on its own.

## 2. Sections per version

- **General** — About · Projects · Principles · Stack · Contact
- **Job-seeking** — About · Projects · Principles · **Skills** · Stack · Contact
- **Client-acquisition** — Services · Cases · Process · Why · Contact

Each page ships with a built-in English / 中文 language toggle and a light / dark theme toggle. Content switching is handled entirely client-side via `data-i18n` attributes.

## 3. Features

- **Mobile navigation** — A hamburger menu (`.nav-toggle`) replaces the desktop link bar on screens ≤ 640px; tap-to-close, click-outside-to-close, `Esc` to close, with `aria-expanded` / `aria-controls`.
- **Contact closure** — The client version's placeholder email is now a real `mailto:shanjunmei@qq.com` link; all three pages expose the email in the contact block.
- **Social / SEO metadata** — Open Graph, Twitter Card, and `JSON-LD Person` structured data added to every `<head>` for rich link previews.
- **Safari compatibility** — `-webkit-backdrop-filter` added alongside `backdrop-filter` for the frosted nav bar.
- **Accessibility** — A "Skip to main content" `skip-link` is the first focusable element; `aria-label`, `aria-hidden` on icons, and `prefers-reduced-motion` are already covered.
- **Consistent layout** — Section spacing is governed by a single `--gap-section` token so vertical rhythm can be tuned in one place.

## 4. Preview & Publish

1. Open any `.html` file directly in a browser (double-click or `file://` path). No server required.
2. To publish: upload the single file to any static host (GitHub Pages, Netlify, object storage, etc.). Each file is fully self-contained.

## 5. Notes & Conventions

- **Location** — All pages normalize the location to `深圳 · China` / `Shenzhen · China`.
- **Fonts** — Typography loads from the `miaoda.feishu.cn` font CDN with a system-font fallback and `display=swap`. Self-hosting was intentionally skipped to preserve single-file independence.
- **Email** — `shanjunmei@qq.com` is the shared contact address across all pages.
- **No git commits** — Edits are left uncommitted by default; commit only when explicitly requested.

## 6. Customization

To change copy, edit the `i18n` dictionaries (zh + en) inside each file; UI text is bound to `data-i18n` keys. To change colors/spacing, edit the CSS custom properties at the top of the `<style>` block. To add a section, duplicate a `.section` block and register its nav link + i18n keys.
