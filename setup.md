# 🛠️ Setup Instructions — Your Cyberpunk GitHub Profile

This repo is set up exactly like Ainan's cyberpunk-themed profile, but personalized with your info (name, email, tech stack, GitHub username `sidyusufdev`).

## 1. Repo name must match your username

GitHub only turns a repo's README into your profile page if the repo is named **exactly** the same as your username. So:

1. Create (or rename) a repo on GitHub called **`sidyusufdev`**.
2. Make sure it's **public**.

## 2. Push these files

```bash
git init
git add .
git commit -m "Cyberpunk profile setup"
git branch -M main
git remote add origin https://github.com/sidyusufdev/sidyusufdev.git
git push -u origin main
```

## 3. Enable GitHub Actions

This repo has 4 workflows in `.github/workflows/`:

1. **`snake.yml`** – animated contribution snake (pushes to an `output` branch).
2. **`3d.yml`** – 3D isometric contribution render (writes into `profile-3d-contrib/`).
3. **`metrics.yml`** – generates `github-metrics.svg` (your achievements card).
4. **`waka.yml`** – your existing WakaTime stats updater (kept as-is).

To turn them on:
1. Go to your repo → **Actions** tab.
2. Click **"I understand my workflows, go ahead and enable them."**
3. Open each workflow on the left and click **Run workflow** once, so images generate immediately instead of waiting for the schedule.

> **Note on `metrics.yml`**: it needs a Personal Access Token (classic, `public_repo` scope) saved as a repo secret named `METRICS_TOKEN`. Go to Settings → Secrets and variables → Actions → New repository secret.

## 4. Fill in the blanks

A couple of spots still say `#` as placeholders — update them with your real links:
- Portfolio badge link (currently `#`) — add your portfolio URL once you have one.

## 5. Verify

After the actions run once:
- The snake animation should appear under "Contribution Grid Matrix".
- `profile-3d-contrib/profile-night-rainbow.svg` should update with your real contribution graph.
- `github-metrics.svg` should appear in the repo root and show under "Achievements Showcase".

That's it — same setup as Ainan's, just running on your data. 🚀
