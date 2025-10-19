# Full GitHub Action Workflow for Custom Snake Animations

## 📁 Step 1: Create the Workflow File

Create this file in your repo: `.github/workflows/snake.yml`

---

## 🐍 Option 1: Ocean Theme

```yaml
name: Generate Ocean Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/ocean-snake.svg?palette=ocean_plus
            dist/ocean-snake-dark.svg?palette=ocean_dark

      - name: Push github-contribution-grid-snake.svg to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**README Code:**
```markdown
![](https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/ocean-snake-dark.svg)
```

---

## 🌈 Option 2: Rainbow/Colorful Theme

```yaml
name: Generate Rainbow Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push github-contribution-grid-snake.svg to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**README Code:**
```markdown
![](https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/github-contribution-grid-snake-dark.svg)
```

---

## 🔥 Option 3: Custom Neon Colors

```yaml
name: Generate Neon Snake

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Generate github-contribution-grid-snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/neon-snake.svg?color_snake=purple&color_dots=#dc143c,#ff4500,#ff8c00,#ffd700,#9acd32
            dist/neon-snake-dark.svg?palette=github-dark&color_snake=cyan&color_dots=#ff1493,#00ff00,#1e90ff,#ffd700,#ff00ff

      - name: Push github-contribution-grid-snake.svg to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**README Code:**
```markdown
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake.svg">
  <img alt="snake animation" src="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake.svg">
</picture>
```

---

## 🎨 Option 4: All Themes Combined

```yaml
name: Generate All Snake Themes

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: Generate all snake themes
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/ocean.svg?palette=ocean_plus
            dist/ocean-dark.svg?palette=ocean_dark
            dist/fire.svg?color_snake=orange&color_dots=#ff0000,#ff4500,#ff8c00,#ffa500,#ffd700
            dist/neon.svg?color_snake=magenta&color_dots=#00ff00,#0000ff,#ff00ff,#ffff00,#00ffff

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

**README Code (pick any):**
```markdown
<!-- Ocean -->
![](https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/ocean-dark.svg)

<!-- Fire -->
![](https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/fire.svg)

<!-- Neon -->
![](https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon.svg)
```

---

## ⚙️ Setup Instructions:

1. Create `.github/workflows/snake.yml` in your `mehara-rothila` repo
2. Copy ONE of the code blocks above
3. Commit and push
4. Go to Actions tab and manually run the workflow
5. Once complete, use the README code to display it
6. Done! �
