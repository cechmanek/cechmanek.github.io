# Personal Website — Execution Plan

## Goal
Rebuild cechmanek.github.io as a distinctive AI/software portfolio on Hugo, deployed via existing GitHub Actions workflow. Deliverable #1 is `TODO.txt` at repo root; then execute P0 first.

## Theme decision
- **Switch**: Ananke (current) → **TOHA v4** (Hugo module), customized so it doesn't look stock.
- Requires **Hugo 0.163.0+** (extended). Local is 0.156.0 → bump via `brew upgrade hugo`, and bump `HUGO_VERSION` in `.github/workflows/hugo.yaml`.
- TOHA setup: `hugo mod init`, add module import `github.com/hugo-toha/toha/v4`, `hugo mod tidy`, `hugo mod npm pack`, `npm install`. Remove Ananke submodule from `.gitmodules`/`themes/`.
- Customization via documented hooks: color scheme + fonts (custom CSS override), custom hero, custom homepage sections (data-file driven).

## TODO.txt content (write to repo root)
```markdown
# Personal Site — Build TODO
Priorities: P0 = foundation/identity, P1 = content, P2 = quality/CI, P3 = polish.

## P0 — Foundation & identity (uniqueness)
- [x] Bump Hugo to 0.163.0+ (brew + CI workflow)
- [x] Switch theme Ananke → TOHA v4 (Hugo module; update .gitmodules/theme setup)
- [ ] Customize TOHA: color scheme + fonts via documented CSS override hooks
- [ ] Custom hero / homepage — personalized intro, AI focus, distinctive layout
- [ ] Custom sections beyond stock (e.g. "What I'm building", featured talks)

## P1 — Content (portfolio substance)
- [ ] About page — bio from README + legacy site (RedisVL, AI engineer, past roles)
- [ ] Skills inventory (Python, Go, Rust, computer vision, LLM/agent tooling, …)
- [ ] Experience timeline — Venmo, Bright Machines, Piaggio, Dephy, Redis (legacy data)
- [ ] Education — Waterloo (MASc), Calgary (BSc Eng, BA Psych)
- [ ] Projects — RedisVL, Monocle, Spectacles, semantic caching (links + logos)
- [ ] Publications page — arXiv:2504.02268, Redis blog author profile
- [ ] Professional links — GitHub, LinkedIn, Hugging Face, RSS (header/footer)

## P2 — Blog
- [ ] Set up posts workflow (archetype, categories/tags)
- [ ] Migrate 2 legacy posts (Spectacles, Monocle intros)
- [ ] Write first new posts (AI/semantic caching/agent memory topics)

## P3 — Quality / CI & test coverage
- [ ] CI: build-check on all PRs (not just push to main)
- [ ] Link checker in CI (internal + external links)
- [ ] Fail-on-warning build flag so broken content doesn't ship
- [ ] Makefile/scripts: `make build`, `make check`, `make serve`
- [ ] SEO: sitemap, meta description, Open Graph
- [ ] Favicon + social share image
- [ ] 404 page; RSS feed
- [ ] README: document todo lifecycle + how to add posts
```

## Execution order
1. Write `TODO.txt` (above) to repo root.
2. P0: `brew upgrade hugo` → verify `hugo version` ≥ 0.163.0.
3. P0: update CI `HUGO_VERSION` to match.
4. P0: switch theme — `hugo mod init`, add TOHA module, `hugo mod tidy` + `npm pack/install`; deinit/remove Ananke submodule.
5. P0: customize palette, fonts, hero, sections; build + verify locally.
6. Stop, report, await go-ahead for P1 content migration (experience, education, projects, publications, blog).
7. Deploy to `hugo/main` only when user confirms (deploy branch per workflow).
