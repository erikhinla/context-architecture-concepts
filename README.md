# Context Architecture — Developer Handoff

> **OCD Experience × TB10X** | February 2026

---

## What This Repo Is

This repository contains all design concepts and implementation documentation for the **Context Architecture** landing page — a rebrand of the `/digital-organizing/` page on [ocdexperience.com](https://ocdexperience.com).

When handing off a project to development in GitHub, this README is the right place to start — not just a bare link to the repo. Everything a developer needs to understand, build, and deploy this page is documented here and in the linked files below.

---

## Quick Start

1. **Clone or open this repo** in your browser or editor.
2. **Open `index.html`** in a browser — it's the navigation hub linking to all design concepts.
3. **Open `v4-client-ready.html`** — this is the final approved design. Build from this file.
4. **Read `IMPLEMENTATION-NOTES.md`** — step-by-step WordPress build instructions.

---

## File Index

| File | Purpose |
|------|---------|
| `index.html` | Navigation hub — links to all concept versions |
| `v1-editorial.html` | Concept v1: editorial / long-form style |
| `v2-minimal.html` | Concept v2: minimal / clean style |
| `v3-conversion.html` | Concept v3: conversion-focused style |
| `v4-client-ready.html` | ✅ **FINAL APPROVED DESIGN** — build from this |
| `v4-wordpress-integration.html` | WordPress-annotated version of v4 |
| `user-flow.html` | User flow / journey map reference |
| `IMPLEMENTATION-NOTES.md` | WordPress build instructions, specs, and component breakdown |
| `positioning-statement.md` | Brand strategy, messaging, and voice/tone guidance |

---

## What Needs to Be Built

The developer's job is to implement `v4-client-ready.html` as a WordPress page on `ocdexperience.com`. See [`IMPLEMENTATION-NOTES.md`](./IMPLEMENTATION-NOTES.md) for the full breakdown. High-level tasks:

- [ ] Create a new WordPress page at `/context-architecture/`
- [ ] Set up a 301 redirect from `/digital-organizing/` → `/context-architecture/`
- [ ] Add "Context Architecture" as an active nav item (replacing "Digital O.C.D.")
- [ ] Build each section using Ohio theme Content Builder blocks (see table in IMPLEMENTATION-NOTES.md)
- [ ] Implement the Diagnostic Quiz as a Custom HTML block with the provided JavaScript
- [ ] Replace the `#book` placeholder in the booking CTA button with the live scheduling URL (Calendly, Acuity, etc.)
- [ ] Add a hero image (client to provide — suggested: split-screen before/after, 4:3 ratio)
- [ ] Add "Context Architecture" link under Services in the footer

---

## Key Contacts

| Role | Name | Contact |
|------|------|---------|
| Project Lead | Erik Howerbush / BizBuilders AI | erik@bizbuilders.ai |
| Client | Justin Klosky / OCD Experience | — |

---

## Design Specs at a Glance

- **Colors:** Dark background (`#141414`), teal accent (`#5EC4AC`)
- **Font:** Inter (Google Fonts — already available in Ohio theme)
- **Breakpoints:** Desktop >900px · Tablet 600–900px · Mobile <600px
- **Full specs:** See [IMPLEMENTATION-NOTES.md](./IMPLEMENTATION-NOTES.md)
