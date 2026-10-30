---
title: "Comment 2 ingénieurs gèrent leur mariage"
date: 2026-10-30
video_url: "https://youtu.be/V7x2QaQBako"
tags: ["Gaussian Splatting", "3D", "OR-Tools", "Obsidian", "Productivité"]
---

# Sources — "Comment 2 ingénieurs gèrent leur mariage"
### Passe-Tech | Octobre 2026

---

## 🗂️ LE SYSTÈME — Décisions, notes, synchronisation

**Vikunja** — gestionnaire de tâches open source, auto-hébergé (projet dédié, Kanban).
🔗 https://vikunja.io

**Obsidian** — prise de notes, pré-rédaction, comptes rendus : la « source de vérité unique ».
🔗 https://obsidian.md

**Syncthing** — synchronisation peer-to-peer entre appareils.
🔗 https://syncthing.net

**thewh1teagle — Vibe** (licence MIT)
Transcription vocale open source qui tourne en local, sans envoyer l'audio ailleurs ; les résumés peuvent passer par l'API Claude.
🔗 https://github.com/thewh1teagle/vibe

**Google Calendar** (échéances) · **Google Drive** (dernier mois, édition à deux) · **Google Forms** (formulaire des invités)
🔗 https://calendar.google.com · https://drive.google.com · https://forms.google.com

---

## 🧮 LE SOLVEUR — Placer 60 invités

**Google for Developers — CP-SAT Solver | OR-Tools**
CP-SAT est le solveur de programmation par contraintes d'OR-Tools, la bibliothèque open source de Google. On décrit les règles logiques, le solveur cherche une combinaison qui les respecte toutes.
🔗 https://developers.google.com/optimization/cp/cp_solver

---

## 🧊 LE JUMEAU VIRTUEL — De la vidéo au 3D

### Gaussian Splatting

**Kerbl, Kopanas, Leimkühler, Drettakis — *3D Gaussian Splatting for Real-Time Radiance Field Rendering*** (arXiv, 8 août 2023)
L'article fondateur de la technique, publié en 2023.
🔗 https://arxiv.org/abs/2308.04079

### Extraction des images

**FFmpeg** — outil en ligne de commande pour découper la vidéo en images.
🔗 https://ffmpeg.org

### Poses caméras

**COLMAP** — pipeline Structure-from-Motion et Multi-View Stereo (licence BSD). Retrouve, à partir de points communs entre les images, la position de chaque prise de vue (les « poses caméras »).
🔗 https://github.com/colmap/colmap
🔗 Documentation : https://colmap.github.io/

**Schönberger & Frahm — *Structure-from-Motion Revisited*** (CVPR 2016)
Article de référence cité par le dépôt COLMAP.
🔗 https://github.com/colmap/colmap (section « Citing »)

> L'analogie de la parallaxe (barrière, arbres, lune vus depuis une voiture) est une image pédagogique de la vidéo, pas une citation de ces travaux.

### Entraînement du splat

**MrNeRF — LichtFeld Studio** (licence GPLv3)
Logiciel libre qui entraîne des Gaussian Splats. Prérequis : GPU NVIDIA récent (RTX 20 ou plus) et pilote 570+. Le code source se compile gratuitement.
🔗 https://github.com/MrNeRF/LichtFeld-Studio
🔗 https://lichtfeld.io

**LichtFeld Studio — binaire Windows précompilé**
La FAQ du site indique que le binaire Windows est disponible via le portail pour une contribution minimale de 30 $, qui finance le développement. Le portail parle d'un accès pour la « current release window » v0.5.x. *Constaté le 30 octobre 2026 : conditions susceptibles d'évoluer.*
🔗 https://lichtfeld.io
🔗 https://portal.lichtfeld.io

### Modélisation

**Blender** — logiciel libre de modélisation 3D.
🔗 https://www.blender.org

**KIRI Engine — 3DGS Render for Blender** (GPL-2.0)
Extension pour importer, éditer et rendre des Gaussian Splats dans Blender (le splat sert de guide).
🔗 https://github.com/Kiri-Innovation/3dgs-render-blender-addon

### Application web

**three.js** — bibliothèque 3D pour le navigateur (lumières ponctuelles pour les bougies, etc.).
🔗 https://threejs.org/docs/
🔗 https://threejs.org/docs/PointLight.html

---

## 🌐 LE SITE DES INVITÉS

**Astro** — framework du site statique.
🔗 https://astro.build

**OWASP — Cross-Site Request Forgery (CSRF)**
Attaque qui pousse un utilisateur connecté à exécuter, sans le vouloir, des actions choisies par un attaquant : l'une des protections à prévoir dès qu'un site statique reçoit un formulaire.
🔗 https://community.owasp.org/attacks/csrf

---

*Faits personnels du récit (dates, 60 convives, dimensions de la salle, durées de calcul, nombre d'erreurs relevées dans les documents) : témoignage de l'auteur, sans source externe.*
*Crédits médias (images, vidéos, musiques) : voir la description de la vidéo.*
*Sources compilées le 30 octobre 2026.*
