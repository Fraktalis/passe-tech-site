---
title: "WASM & WebGPU — Le Web natif"
date: 2026-03-25
video_url: "#"
tags: ["WASM", "WebGPU", "web", "performance"]
---

# Sources — WASM & WebGPU

---

## Démo
- [Lien vers le dépôt GitHub](https://github.com/Fraktalis/wgsl-nbody-simulation) de la simulation de particules

## 🕹️ Avant WASM — L'ère des plugins

### Java Applets
- Lancé en 1995, fin de support Oracle en 2017
- Source : [Wikipedia — Java Applet](https://en.wikipedia.org/wiki/Java_applet)

### Adobe Flash
- Steve Jobs, *Thoughts on Flash* — 29 avril 2010
  - Source : [Wikipedia](https://en.wikipedia.org/wiki/Thoughts_on_Flash)
- Flash EOL : 31 décembre 2020, contenu bloqué le 12 janvier 2021
  - Source : [Adobe Flash EOL page](https://www.adobe.com/products/flashplayer/end-of-life.html)
- Flash AVM2 : bytecode + JIT, **pas** du code natif
  - Source : Mozilla/Adobe Tamarin FAQ

### Google NaCl (Native Client)
- Annoncé décembre 2008, déprécié 2017
- Source : [Wikipedia — NaCl](https://en.wikipedia.org/wiki/Google_Native_Client)

### Doom dans le navigateur
- Alon Zakai, juin 2011 — portage JS via Emscripten
- Source : [Mozilla Hacks, 2 juin 2011](https://hacks.mozilla.org/2011/06/look-ma-no-plugin/) + [DoomWiki](https://doomwiki.org/)

---

## ⚙️ WebAssembly

### Standardisation
- Consensus MVP W3C : **28 février 2017**
  - Source : [W3C mailing list](https://lists.w3.org/Archives/Public/public-webassembly/)
- Support tous les navigateurs majeurs : **novembre 2017**
  - Source : [InfoQ](https://www.infoq.com/news/2017/11/webassembly-browser-support/)

### Unity & WASM
- Première démo WASM publique (2015) = jeu Unity
- Expérimental depuis Unity 5.6 (2017), défaut depuis Unity 2018.2
- Source : [Packt Hub](https://hub.packtpub.com/) + [Wikipedia — WebAssembly](https://en.wikipedia.org/wiki/WebAssembly)

### Performances réelles
- **Figma** : 3x plus rapide avec WASM
  - Source : [Figma Blog, juin 2017](https://www.figma.com/blog/webassembly-cut-figmas-load-time-by-3x/)
- **Photoshop Web** : SIMD 3-4x, jusqu'à 80-160x sur certaines opérations
  - Source : [web.dev — Photoshop on the Web](https://web.dev/articles/ps-on-the-web)

---

## 🎮 WebGPU

### Standardisation
- Basé sur Metal / Vulkan / D3D12
  - Source : [W3C WebGPU spec](https://www.w3.org/TR/webgpu/)
- Chrome 113 : **avril 2023**
  - Source : [Chrome Developers Blog](https://developer.chrome.com/blog/webgpu-release)
- Firefox 141 + Safari 26 : **2025**
  - Source : [Wikipedia — WebGPU](https://en.wikipedia.org/wiki/WebGPU)

### LLM dans le navigateur
- WebLLM — inférence LLM côté client via WebGPU
  - Source : [webllm.mlc.ai](https://webllm.mlc.ai)
  - ⚠ SOURCE À CONFIRMER : modèles disponibles et benchmarks à vérifier

---

*Sources v1 — Passe-Tech / "WASM & WebGPU"*
*Compilées le 25 mars 2026*
