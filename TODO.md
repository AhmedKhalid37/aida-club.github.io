# AIDA Site — Manual TODO

These steps require action in the GitHub UI or by hand — they cannot be automated.

## Required Before Site Goes Live

- [ ] **GitHub Pages source**: In the repo Settings → Pages → Build and deployment → Source, select **"GitHub Actions"**. Without this, the deployment workflow will not trigger.
- [ ] **Actions enabled**: In Settings → Actions → General, confirm Actions are enabled for the repo.
- [ ] **Verify baseURL**: If the actual GitHub repo name differs from `aida-club/aida-club.github.io`, update `baseURL` in `hugo.toml` to match the correct Pages URL before the first push.

## Required for Content

- [ ] **Replace contact email**: In `content/join.md`, replace `aida@ajman.ac.ae` with the real club contact email once confirmed.
- [ ] **Add cover image**: Add a `cover.png` to `content/posts/2026-04-18-welcome/` for the welcome post's cover image. Any 1200×630px image works for the Open Graph card.

## Required for Workflow

- [ ] **Paste discovery prompt**: Open `prompts/discovery.md` and replace the placeholder with the actual prompt from `nexus_v0_manual_playbook.md` §3.
- [ ] **Paste daily drafts prompt**: Open `prompts/daily_drafts.md` and replace the placeholder with the actual prompt from `nexus_v0_manual_playbook.md` §4.
- [ ] **Paste weekly recap prompt**: Open `prompts/weekly_recap.md` and replace the placeholder with the actual prompt from `nexus_v0_manual_playbook.md` §5.
- [ ] **Paste Arabic translation prompt**: Open `prompts/arabic_translate.md` and replace the placeholder with the actual translation prompt.
- [ ] **Paste full playbook**: Open `docs/v0_playbook.md` and paste the complete manual playbook from `nexus_v0_manual_playbook.md`.

## Optional (Week 2+)

- [ ] **Custom domain**: Once acquired, add it in Settings → Pages → Custom domain, then add a `static/CNAME` file with the domain name.
- [ ] **Analytics**: Add a GoatCounter or Plausible snippet to `layouts/partials/extend_head.html`. Both have free tiers suitable for a club site.
