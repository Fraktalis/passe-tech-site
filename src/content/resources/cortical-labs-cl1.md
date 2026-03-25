---
title: "Cortical Labs - CL1"
date: 2026-03-25
video_url: "#"
tags: ["IA", "neurosciences", "hardware"]
---

# Sources - Et si vos cellules jouaient à Doom sur Internet ?

---

## 🧬 Biologie & Technique

### iPSC - Cellules souches pluripotentes induites

- Yamanaka, S. et al. (2006). *Induction of Pluripotent Stem Cells from Mouse Embryonic and Adult Fibroblast Cultures by Defined Factors.* Cell.
- Prix Nobel de médecine 2012 - Shinya Yamanaka & John Gurdon
- Prix de la technologie du millénaire 2012 - Yamanaka & Linus Torvalds

### DishBrain - Le prototype

- Kagan, B.J. et al. (2022). *In vitro neurons learn and exhibit sentience when embodied in a simulated game-world.* Neuron. <https://pubmed.ncbi.nlm.nih.gov/36228614/>
- Apprentissage observé en moins de 5 minutes de gameplay
- 800 000 neurones, humains et murins, sur CMOS chip

### CL1 - Le produit commercial

- Cortical Labs - Page produit CL1 : <https://corticallabs.com/cl1>
- Lancé le 2 mars 2025 à Barcelone (MWC)
- 200 000 neurones sur HDMEA (High Density Multi-Electrode Array)
- Système biOS - Biological Intelligence Operating System
- Viabilité : jusqu'à 6 mois (certains cas documentés jusqu'à 1 an)
- Prix : 35 000 $ l'unité / 20 000 $ en rack de 30

### Doom sur CL1

- Vidéo officielle Cortical Labs : [https://www.youtube.com/watch?v=\[lien à compléter\]](https://www.youtube.com/watch?v=yRV8fSw6HaE)
- Développeur externe : Sean Cole, via l'API publique Cortical Labs
- Développement : moins d'une semaine
- Référence Tom's Hardware : <https://www.tomshardware.com/tech-industry/artificial-intelligence/200-000-living-human-neurons-on-a-microchip-demonstrated-playing-doom>

---

## ⚡ Énergie & Industrie

### Consommation IA

- GPT-4 entraînement : estimations indépendantes ~20-25 MW sur ~3 mois (équivalent 20 000 foyers américains)
  - Source : Epoch AI - <https://epoch.ai/gradient-updates/how-much-energy-does-chatgpt-use>
- GPT-5 inférence : ~18,35 Wh par réponse en moyenne (vs 2,12 Wh pour GPT-4) - soit ×8,6
  - Source : University of Rhode Island AI Lab, relayé par Tom's Hardware et The Guardian (août 2025)
  - <https://www.tomshardware.com/tech-industry/artificial-intelligence/chatgpt-5-power-consumption>
- OpenAI ne publie pas ses chiffres officiels de consommation

### CL1 vs GPU

- CL1 unité : ~30 watts
- Rack de 30 CL1 (maintien en vie inclus) : 850–1 000 watts
- Rack GPU équivalent pour tâches IA : dizaines de kilowatts
- Source : Cortical Labs / IEEE Spectrum <https://spectrum.ieee.org/biological-computer-for-sale>

### Data centers biologiques

- Melbourne : 120 unités CL1, opérationnel
- Singapour : partenariat DayOne Data Centers, jusqu'à 1 000 unités
- Annonce : mars 2026
- Source : Gizmodo <https://gizmodo.com/the-company-that-made-a-dish-of-neurons-play-doom-is-getting-into-brain-cell-powered-data-centers-2000731875>
- Source : Tom's Hardware <https://www.tomshardware.com/tech-industry/artificial-intelligence/human-brain-cells-set-to-power-two-new-data-centers>

---

## 🧠 Neurosciences & Apprentissage

### Principe d'Énergie Libre - Karl Friston

- Friston, K. (2010). *The free-energy principle: a unified brain theory?* Nature Reviews Neuroscience.
- Application à DishBrain : Kagan et al. 2022 (voir ci-dessus)
- Friston sur CL1 : "the ultimate in neuromorphic computing using real neurons" - IEEE Spectrum 2025

### Paradoxe de Moravec

- Moravec, H. (1988). *Mind Children.* Harvard University Press.
- Observation : tâches cognitives complexes faciles pour les machines, tâches motrices/perceptives faciles pour les humains - et inversement
- Lien avec CL1 : la biologie court-circuite le problème au lieu de le résoudre en silicium

### Mémoire et limites actuelles

- Apprentissage intra-session : démontré
- Apprentissage inter-sessions : non robuste à ce jour
- Source : Kagan et al. 2022 + David Kingsley Substack (2025) <https://davidkingsley.substack.com/p/lab-grown-neurons-learn-to-play-doom>

---

## ⚖️ Éthique & Consentement

### Consentement des donneurs

- Lewis, J. & Holm, S. (2022). *Organoid biobanking, autonomy and the limits of consent* - Bioethics.
  - Argument : le consentement large des biobanques ne couvre pas structurellement les usages imprévus comme les organoïdes
- Enquête donneurs (2022) : enthousiastes mais souhaitent information continue et droit de retrait
- Source secondaire : blockbuster.thoughtleader.school <https://blockbuster.thoughtleader.school/p/cortical-labs-trains-200000-living>

### Statut moral des cultures neuronales

- Cortical Labs - premier papier publié : papier d'éthique (avant tout papier technique)
- Brett Kagan : "these neuron networks are not conscious" - position officielle
- Parallèle historique : Descartes & animaux-machines → législation progressive sur le bien-être animal
- Henrietta Lacks / HeLa cells : précédent historique sur le consentement en biologie commerciale

### Réglementation

- Pas de cadre légal existant pour les cultures neuronales computationnelles
- Expérimentation animale : réglementée dans la plupart des pays industrialisés
- Seuil moral discuté : à quelle échelle de neurones la question devient-elle pertinente ?

---

## 🎬 Culture & Références

### Matrix

- Wachowski, L. & L. (1999). *The Matrix.* Warner Bros.
- Script original : humains utilisés comme réseau de calcul distribué, pas comme batteries
  - Source : Matrix Wiki Fandom <https://matrix.fandom.com/wiki/Power_plant>
  - Source forum : sci-fi.narkive.fr + multiple Reddit/GameFAQs threads
  - Statut : bien documenté dans les documents de production, non confirmé officiellement par les Wachowski en interview

### Expériences de pensée philosophiques

- **Zombie philosophique** - David Chalmers (1995). *The Conscious Mind.* Oxford University Press.
  - Un être physiquement identique à un humain, sans expérience subjective
- **Chambre chinoise** - John Searle (1980). *Minds, Brains, and Programs.* Behavioral and Brain Sciences.
  - Un système traite des symboles parfaitement sans les comprendre
- **Chambre de Mary** - Frank Jackson (1982). *Epiphenomenal Qualia.* Philosophical Quarterly.
  - On peut tout savoir sur la physique d'une expérience sans la vivre

---

## 📰 Articles de référence principaux

| Source | URL | Date |
|--------|-----|------|
| IEEE Spectrum | <https://spectrum.ieee.org/biological-computer-for-sale> | Juin 2025 |
| New Atlas | <https://newatlas.com/brain/cortical-bioengineered-intelligence> | Mars 2025 |
| Live Science | <https://www.livescience.com/technology/computing/worlds-1st-computer-that-combines-human-brain-with-silicon-now-available> | Mai 2025 |
| Discover Magazine | <https://www.discovermagazine.com/brain-cells-on-a-computer-chip> | Oct 2025 |
| Interesting Engineering | <https://interestingengineering.com/innovation/cortical-labs-neurons-computing> | Nov 2025 |
| David Kingsley Substack | <https://davidkingsley.substack.com/p/lab-grown-neurons-learn-to-play-doom> | Mars 2026 |
| Blockbuster Newsletter | <https://blockbuster.thoughtleader.school/p/cortical-labs-trains-200000-living> | Mars 2026 |

---

*Sources v1 - Passe-Tech / "Et si vos cellules jouaient à Doom sur Internet ?"*
*Compilées le 19 mars 2026*
