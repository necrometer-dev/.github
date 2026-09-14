# ☩ THE NECROMETER ☩

<p align="center">
  <em>An instrument for measuring how dead your GitHub repositories are.</em>
</p>

<p align="center">
  <a href="https://necrometer.dev/?u=necrometer-dev">
    <img src="necrometer.svg" alt="Necrometer — necrometer-dev" width="495">
  </a>
</p>

<p align="center">
  <a href="https://necrometer.dev"><img src="https://img.shields.io/badge/web-necrometer.dev-7dffa8?style=flat-square&logo=googlechrome&logoColor=0a0812" alt="Website"></a>
  <a href="https://github.com/necrometer-dev/necrometer/releases/latest"><img src="https://img.shields.io/github/v/release/necrometer-dev/necrometer?style=flat-square&color=b78cff&label=release" alt="Release"></a>
  <a href="https://github.com/necrometer-dev/necrometer-action"><img src="https://img.shields.io/badge/action-necrometer--action@v1-e8b34b?style=flat-square&logo=githubactions&logoColor=0a0812" alt="Action"></a>
  <a href="https://github.com/necrometer-dev/necrometer/blob/master/LICENSE"><img src="https://img.shields.io/badge/license-MIT-8a80a8?style=flat-square" alt="License"></a>
</p>

---

### The Necrosis Spectrum

Every GitHub account accumulates corpses: abandoned side-projects, forgotten forks, and code left to freeze in the dark. The Necrometer examines your commit history, push recency, archived status, and stranded stars to weigh your soul on a scale from vital to fully necrotic:

| Index | Status | Diagnosis |
|:---:|:---|:---|
| **0% – 14%** | 🟢 **Hale & Active** | *The Maintainer* — recent commits, fresh life, corpses cleanly buried. |
| **15% – 49%** | 🟡 **Cooling** | *Cemetery Groundskeeper* — signs of life remain, but winter approaches. |
| **50% – 79%** | 🟠 **Cold & Morbid** | *Crypt Keeper* — the graveyard outnumbers the living; stars stranded. |
| **80% – 100%** | 🔴 **Necrotic** | *Mausoleum* — no heartbeat detected; total digital decay. |

---

### Organization Repositories

| Repository | Purpose |
|:---|:---|
| [**`necrometer`**](https://github.com/necrometer-dev/necrometer) | **The Core Engine.** High-performance Rust CLI, SVG gauge card renderer with embedded Creepster typography, and WebAssembly compilation target. |
| [**`necrometer.dev`**](https://github.com/necrometer-dev/necrometer-dev.github.io) | **The Web Instrument.** Static haunted CRT web application hosted on GitHub Pages. Zero servers, client-side WASM necromancy, 1-click 𝕏 sharing, and high-res card exporter. |
| [**`necrometer-action`**](https://github.com/necrometer-dev/necrometer-action) | **The GitHub Action.** Automated composite action that summons the pinned release binary, verifies SHA-256 checksums, and carves an updated SVG into your repo daily. |

---

### The Ritual — Bind the Necrometer to Your Profile or Repo

#### 1. Inscribe the Daily Action
Create `.github/workflows/necrometer.yml` in your profile repository (e.g. `<username>/<username>`) or project repo:

```yaml
name: necrometer
on:
  schedule: [{cron: "17 6 * * *"}]   # daily
  workflow_dispatch:                  # manual "run now"
permissions: { contents: write }
jobs:
  necrometer:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: necrometer-dev/necrometer-action@v1
        with:
          token: ${{ secrets.NECRO_TOKEN || secrets.GITHUB_TOKEN }}
```

#### 2. Speak Its Name in your `README.md`
Add the badge just beneath your profile or repository title:

```markdown
[![Necrometer](necrometer.svg)](https://necrometer.dev/?u=YOUR_USERNAME)
```

Run the workflow once from your **Actions** tab. The Necrometer will carve `necrometer.svg` and keep it refreshed daily.

---

<p align="center">
  <sub>Conjured with 🖤 by <a href="https://necrometer.dev">necrometer.dev</a> — no servers were harmed. They were already dead.</sub>
</p>
