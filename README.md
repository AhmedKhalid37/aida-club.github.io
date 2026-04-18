# AIDA — Ajman University AI & Data Science Club

This repository is both the AIDA public website (Hugo, deployed to GitHub Pages) and the workspace for the daily AI/ML content pipeline.

## Site Structure

```
.
├── content/
│   ├── about.md                  # About page
│   ├── join.md                   # Join page
│   ├── archives.md               # Archive index (PaperMod layout)
│   └── posts/
│       └── YYYY-MM-DD-slug/
│           └── index.md          # Each daily digest post
├── themes/PaperMod/              # PaperMod theme (git submodule)
├── prompts/                      # AI prompts for the content workflow
│   ├── discovery.md              # Source monitoring + topic selection
│   ├── daily_drafts.md           # Draft generation
│   ├── weekly_recap.md           # Sunday recap synthesis
│   └── arabic_translate.md       # Arabic translation
├── _state/
│   └── published_log.md          # Dedup log — check before publishing
├── docs/
│   └── v0_playbook.md            # Full manual workflow playbook
├── .github/workflows/hugo.yml    # GitHub Actions deployment
└── hugo.toml                     # Hugo configuration
```

## Local Preview

```bash
hugo server -D
```

Then open http://localhost:1313. The `-D` flag includes draft posts.

## Publishing a Digest

1. Create the post directory and file:
   ```bash
   mkdir -p content/posts/YYYY-MM-DD-slug
   # write content/posts/YYYY-MM-DD-slug/index.md
   ```
2. Follow the frontmatter format from an existing post.
3. Append an entry to `_state/published_log.md`.
4. Commit and push to `main`:
   ```bash
   git add .
   git commit -m "digest: YYYY-MM-DD short title"
   git push
   ```
5. GitHub Actions builds and deploys automatically. Check the Actions tab for status.

## Workflow References

- Full manual playbook: [`docs/v0_playbook.md`](docs/v0_playbook.md)
- AI prompts: [`prompts/`](prompts/)
- Published log (dedup): [`_state/published_log.md`](_state/published_log.md)

## Contributing

AIDA members — contribution guidelines will be added here. For now, coordinate via the weekly meeting or the club email.
