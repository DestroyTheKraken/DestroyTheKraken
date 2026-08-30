# GitHub polish report — 2026-08-29

Executed against `github-maint-20260828.md`, with profile language updated for Google AI Essentials (Markdown prompting / docs-as-code) and Linux Foundation LFS101 / LFS207 (CLI, Bash, Ubuntu / Canonical focus). Tone: relaxed professional, honest about AI use.

## A. Files changed per repo

| Repo | Changes |
|------|---------|
| **DestroyTheKraken** (profile) | `README.md` job landing rewrite; `RESUME.md` cert/AI/Linux alignment; `REPORT.md` |
| **aide-os** | Removed personality PDFs, family media scan (contained Tailscale IP), Obsidian plugin tree, chat/session dumps, screenshots; stubs + slim README + tighter `.gitignore`; kept `brain/bootcamp` LFCS curriculum |
| **homelab** | Role-name device inventory in `docs/04-tailscale.md` and `docs/05-inventory-observed-*.md`; README lead-in; `.gitignore` |
| **nc-lin-cs** | Portfolio framing; removed price/product pitch block |
| **ssh-ufw-ts-install** | Full README (no tskey; interactive `tailscale up`); `.gitignore` |
| **HickMedia** | Short honest README (not job portfolio) |
| **dtk** | `.gitignore` tighten; description updated (not archived without your OK) |
| **SovereignAid** | Already archived; description left (API read-only) |

Repo descriptions/topics updated via API for portfolio repos.

## B. Files removed or privatized (and why)

| Path | Why |
|------|-----|
| `aide-os/ara_tutor/user-profile/*.pdf` + `profile-summary.md` | Personality assessments — not public portfolio |
| `aide-os/docs/ops/USER-PROFILE.md` (replaced with 10-line learner stub) | Personal calibration dump |
| `aide-os/console-pack/SCAN-fam-media-2026-07-12.md` | Family host scan + **Tailscale IP** |
| `aide-os/brain/.obsidian/**`, `.spark/conversations/**`, `sessions/**`, canvases | Personal vault / chats |
| `aide-os/.grok/docs/user-attachments/screenshots/**` | Account UI screenshots |
| `aide-os/.obsidian/**` | Root Obsidian runtime |

Stubs state that personal assessments and vault data stay private.

## C. Remaining risks not fully cleared

1. **Git history** still contains deleted files (PDFs, scan with Tailscale IP). Needs `gitleaks` / history rewrite or accept residual exposure until force-push policy allows.
2. **GitHub profile bio/company** still studio-flavored — API needs `user` scope (`gh auth refresh -h github.com -s user`). Manual edit in GitHub Settings → Profile works too.
3. **PDF résumé** may lag Markdown (noted on README).
4. **dtk / HickMedia / bashcrawl / cmdchallenge / clmystery** still public; not on profile table.
5. **dtk-site-archive** left private (untouched).
6. Local `aide-os` WIP was stashed as `wip-before-portfolio-privacy` (includes untracked `NODE1-PUBKEY.txt` — do not commit).

## D. Suggested next manual steps

1. Refresh GitHub auth with `user` scope and update bio, or edit bio in the UI:
   - Bio: `Linux systems administration · Networking · IT operations. Army veteran. AI-assisted learning; I still type, test, and document.`
   - Company: `Open to junior Linux / networking / IT ops roles`
2. Run gitleaks (or similar) on `aide-os` history; rotate any exposed Tailscale credentials if that IP/status dump ever mattered.
3. Regenerate `JoshuaHickman-Resume.pdf` from current `RESUME.md` / Word source.
4. Archive `dtk` and/or `HickMedia` if you agree they add no reviewer value.
5. `git stash pop` in `aide-os` when you want lab WIP back — keep pubkey scripts untracked.
