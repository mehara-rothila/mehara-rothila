# Mehara Rothila Ranawaka

<div align="center">

## 🎨 Custom Snake Animations

### 🌊 Ocean Theme
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/ocean-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/ocean-snake.svg">
  <img alt="ocean snake" src="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/ocean-snake.svg">
</picture>

**GitHub Action Code:**
```yaml
- uses: Platane/snk@v3
  with:
    github_user_name: mehara-rothila
    outputs: |
      dist/ocean-snake.svg?palette=ocean_plus
      dist/ocean-snake-dark.svg?palette=ocean_dark
```

---

### 🌈 Rainbow Theme
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/rainbow-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/rainbow-snake.svg">
  <img alt="rainbow snake" src="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/rainbow-snake.svg">
</picture>

**GitHub Action Code:**
```yaml
- uses: Platane/snk@v3
  with:
    github_user_name: mehara-rothila
    outputs: |
      dist/rainbow-snake.svg?palette=github
      dist/rainbow-snake-dark.svg?palette=github-dark
```

---

### 💜 Neon/Cyberpunk Theme
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake.svg">
  <img alt="neon snake" src="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/neon-snake.svg">
</picture>

**GitHub Action Code:**
```yaml
- uses: Platane/snk@v3
  with:
    github_user_name: mehara-rothila
    outputs: |
      dist/neon-snake.svg?color_snake=#ff00de&color_dots=#00ff00,#0000ff,#ff0000,#ffff00
      dist/neon-snake-dark.svg?color_snake=#ff00de&color_dots=#00ff00,#0000ff,#ff0000,#ffff00,#00ffff
```

---

### 🔥 Fire Theme
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/fire-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/fire-snake.svg">
  <img alt="fire snake" src="https://raw.githubusercontent.com/mehara-rothila/mehara-rothila/output/fire-snake.svg">
</picture>

**GitHub Action Code:**
```yaml
- uses: Platane/snk@v3
  with:
    github_user_name: mehara-rothila
    outputs: |
      dist/fire-snake.svg?color_snake=#ff4500&color_dots=#ff0000,#ff4500,#ff8c00,#ffa500,#ffd700
      dist/fire-snake-dark.svg?color_snake=#ff4500&color_dots=#8b0000,#ff0000,#ff4500,#ff8c00
```

---

## 📝 How to Use:

1. Go to your `mehara-rothila/mehara-rothila` repository
2. Create/edit `.github/workflows/snake.yml`
3. Replace with one of the code blocks above
4. Update your README.md with the corresponding image path
5. Push and wait for the action to run!

</div>
