# BCS703 — Cryptography & Network Security (VTU Scheme 2022)

Promotional site for the free module-wise video lecture series.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site — one self-contained file (inline CSS + JS) |
| `dr_lokesh_professor_new.png` | Portrait used in the hero and the teacher section |
| `render.yaml` | Render Blueprint (static site + cache/security headers) |
| `robots.txt` | Search-engine crawl rules |

Keep `index.html` and `dr_lokesh_professor_new.png` side by side — the HTML
references the photo as `./dr_lokesh_professor_new.png`.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

Open it through a server, not by double-clicking the file: YouTube refuses to
embed video on `file://` pages. (The player detects this and opens YouTube in a
new tab instead, but the in-page player only works over http/https.)

## Deploy to Render

See `DEPLOY-RENDER.md` in the parent folder, or in short:

1. Push this folder to a GitHub repository.
2. Render Dashboard -> New -> Blueprint -> pick the repo -> Apply.
3. Your site appears at https://bcs703-lectures.onrender.com

## Editing content

- Lecture links: `const MODULES = [...]` near the top of the `<script>` block.
  An empty `url: ""` renders a greyed-out "Coming soon" card automatically.
- Study planner maths: `const PLANNER = { multiplier: 3, ... }` just below it.
- Placeholders: search the HTML for `[Add` (institution, VTU rules, etc.).
- "Last updated" date: search for `datetime="2026-11-10"`.
- Canonical + Open Graph URLs: search for `bcs703-lectures.onrender.com`.
