# Instructor Notes

CPSI 17503 / Programming I (PyBook). Student-facing content lives in module folders; this file is for setup and term prep.

Related docs:

- [Syllabus.md](Syllabus.md) — reusable syllabus template (institution/instructor placeholders)
- [Course Map Guide.md](Course%20Map%20Guide.md) — CLOs, MLOs, materials links, practice rubric
- Each module `README.md` — reading order for that folder

---

## Customizing this book

Those links below are the **original** book. You can still **clone a clone**: fork or copy someone else’s fork (or the original), edit freely, and teach from your copy. TxtBook renders whatever GitHub repo you point it at.

**Original (dev / reference)**

| Kind | URL |
|------|-----|
| Rendered (TxtBook) | <https://txtbook.dev/NicholasSeward/pybook> |
| GitHub source | <https://github.com/nicholasseward/pybook> |

**URL trick**

- GitHub → rendered: replace `github.com` with `txtbook.dev` in the repo URL.
- Rendered → GitHub: replace `txtbook.dev` with `github.com` in the book URL.

Example (original): `https://github.com/nicholasseward/pybook` ↔ `https://txtbook.dev/NicholasSeward/pybook`

Point your LMS / students at **your** rendered TxtBook URL after you clone (even if that clone came from another instructor’s clone) and customize accept links, wording, and any optional community space.

---

## TxtBook vs Think Python

TxtBook and Think Python are different reading experiences. Do not treat the in-repo chapter copies as a full substitute for Think Python.

| Source | How students should use it |
|--------|----------------------------|
| **TxtBook** (this repo) | Custom sections, quizzes, tutorials, and module structure. Code playgrounds run in the browser per block. |
| **Think Python** | Prefer the official online book / Colab workflow. In Colab, **all code cells share one environment** (variables and imports persist across cells). |

This repo keeps a **reference copy** of the Think Python chapters for convenience and linking. For the best learning experience, send students **directly to Think Python** (Colab) when a module lists a Think Python chapter.

When you write LMS overviews or announcements, link Think Python chapters to the live Think Python / Colab pages when you can, and use TxtBook URLs for the custom TxtBook sections.

---

## Course videos

Module videos often include **specifics from a past class** (dates, deadlines, tools, or jokes tied to that term). For the most part they still work for the concepts. You are free to **keep them**, **skip the dated bits**, or **replace them** with your own recordings.

Student pages (Practices, Projects, and some overviews) also have **aspirational placeholders** such as "Insert walkthrough video." Those are optional. You can:

- Cover that material in class instead
- Record your own short video and paste the link
- Delete the placeholder block if you are not using a video

---

## Getting started (LMS)

A Discord or Slack space is **recommended** so students have a place for quick help. If you use one, put the invite in the LMS **Getting Started** section and refresh it if it expires.

> NOTE: Prefer the LMS Getting Started page over the public textbook repo for term-specific invites.

---

## Assignment delivery: classroom50 (Fall 2026)

Classic **GitHub Classroom is deprecated**. The replacement is **classroom50**.

> NOTE: classroom50 is **not live yet**. Plan on it for **Fall 2026**. Details below are a **best guess** from how Classroom worked and what classroom50 is aiming to replace. Re-check the classroom50 docs when it ships and adjust this page.

### Best-guess classroom50 flow

1. Connect your course / roster in classroom50.
2. Create one assignment per Practice (short title / prefix helps).
3. Attach the right **starter template** (see table below). Almost everything uses the main template; only **project04** and **Practice 13** differ.
4. Publish the assignment and copy the **student accept / invite link**.
5. Paste that link into the matching Practice / project materials under **Accept link:** (and into the LMS if students start there).
6. Optionally add one **Example repository URL** after a test accept so students see the naming pattern. Student repos live wherever classroom50 creates them (not in the template’s home).
7. Students accept → get their own repo from the template → work in Codespaces or locally → commit and push.
8. LMS: collect the **repository URL** as a clickable backup for one-off grading. Do **not** accept Codespaces / `github.dev` links (private to the student).

### Templates

**Default:** use the main Codespaces Python template (`programming-1`) for **all** assignments except the two exceptions below.

| Use | Template | Notes |
|-----|----------|-------|
| All Practices / projects (default) | [programming-1](https://github.com/Seward-Classes/programming-1) | Main template; Codespace / `.devcontainer` for Python |
| **Practice 13** (C++) | [programming-2](https://github.com/Seward-Classes/programming-2) | Exception: C++ starter |
| **project04** | <https://github.com/env3d/cs1-llm-local-chatbot> | Exception: local LLM chatbot starter |

> NOTE: Do not attach `programming-1` to project04 or Practice 13.


### What to fill in the Practice files (collectively)

For every Practice that has a classroom50 block (01–13), plus each Project (01–04) when you publish it:

- Paste the **Accept link** when the assignment exists.

Projects live in the module folder where they are due:

- Module 03: [Project 01 - Quiz Game](Module%2003%20-%20Conditionals%20and%20Functions/Project%2001%20-%20Quiz%20Game.md)
- Module 06: [Project 02 - Course Registration Simulator](Module%2006%20-%20Data%20Structures/Project%2002%20-%20Course%20Registration%20Simulator.md)
- Module 09: [Project 03 - Course Registration Simulator OOP](Module%2009%20-%20Classes/Project%2003%20-%20Course%20Registration%20Simulator%20OOP.md)
- Module 12: [Project 04 - Persistent Local Chatbot](Module%2012%20-%20Fancy%20Data%20Structures/Project%2004%20-%20Persistent%20Local%20Chatbot.md)


---

## Grading

Use the [Practice Rubric](Course%20Map%20Guide.md#practice-rubric) in the Course Map Guide.

For a **just-good-enough but working** automated helper, contact **njseward@ualr.edu** about a rough autograder app. It uses the `gh` command line and the OpenAI API. Cost has been under about **$10 / semester** at ~100 students for the author, but you must set up billing yourself. OpenAI is **prepaid**, so you are not exposed to an unbounded surprise bill if you cap the balance.

---

## Term checklist

- [ ] Optional: Discord or Slack invite in the LMS **Getting Started** section (recommended)
- [ ] classroom50 available for the term (Fall 2026+); do not rely on classic GitHub Classroom
- [ ] Templates: `programming-1` for everything except **project04** (`cs1-llm-local-chatbot`) and **Practice 13** (`programming-2`)
- [ ] One classroom50 assignment per Practice (including Module 12) and per Project (01–04)
- [ ] Accept links (and optional example repo URLs) filled in Practice / Project `.md` files and LMS
- [ ] LMS asks for repository URL, not Codespaces URL
- [ ] Rubric / late / resubmit policy matches the syllabus

---

## Other course pieces

| Piece | Where | Notes |
|-------|--------|------|
| Quizzes / tutorials | Each module folder | Autograded in TxtBook / LMS |
| In-class activities | `Activity 1/2 - ….md` per module | Handouts; linked from Course Map |
| Reading order | Module `README.md` | Mix of TxtBook sections + Think Python chapters (see [TxtBook vs Think Python](#txtbook-vs-think-python)) |
| Videos / participation | Course shell (LMS) | Often past-term specifics; usually still usable, or replace (see [Course videos](#course-videos)) |
