# Terminal handoff

How to publish and update this site from a terminal.

## 0. Prerequisites

```bash
git --version          # any recent git
gh --version           # GitHub CLI, optional but easiest
gh auth status         # should show you logged in
```

If `gh auth status` fails: `gh auth login` and follow the prompts.

## 1. Enter the folder

```bash
cd back-to-the-1850s
open index.html        # macOS; the app should open in dark mode
```

## 2. Create the repo and push

Option A, GitHub CLI:

```bash
git init -b main
git add .
git commit -m "Back to the 1850s: infection-control atlas"
gh repo create malevolentmicrobes-stack/back-to-the-1850s --public --source=. --push
```

Option B, without gh: create an empty public repo named `back-to-the-1850s` on github.com (no README), then:

```bash
git init -b main
git add .
git commit -m "Back to the 1850s: infection-control atlas"
git remote add origin https://github.com/malevolentmicrobes-stack/back-to-the-1850s.git
git push -u origin main
```

Before the first commit, check `git config user.name` and `git config user.email`. Those values are published with every commit.

## 3. Turn on GitHub Pages

```bash
gh api -X POST repos/malevolentmicrobes-stack/back-to-the-1850s/pages \
  -f "source[branch]=main" -f "source[path]=/"
```

Or on github.com: repo → Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.

The site appears in 1–2 minutes at:
`https://malevolentmicrobes-stack.github.io/back-to-the-1850s/`

## 4. Updating later

```bash
# replace index.html with the new version, then:
git add index.html
git commit -m "Update: <what changed>"
git push
```

Pages redeploys on every push to `main`.
