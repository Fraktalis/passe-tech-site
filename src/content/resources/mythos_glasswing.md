---
title: "Project Glasswing : les Avengers de la cybersécurité ?"
date: 2026-04-16
video_url: "#"
tags: ["Anthropic", "Glasswing", "Mythos", "CyberSécurité", "OpenSource", "IA"]
---

# Sources — "Project Glasswing : les Avengers de la cybersécurité ?"
### Passe-Tech | Avril 2026

---

## 🤖 Sources primaires — Anthropic

**Anthropic — Annonce officielle Project Glasswing (7 avril 2026)**
Annonce du consortium, liste des 12 partenaires de lancement, engagement de 100M$ en crédits d'usage et 4M$ en dons à des organisations open source.
🔗 https://www.anthropic.com/glasswing

**Anthropic — Red Team Blog : "Assessing Claude Mythos Preview's cybersecurity capabilities" (7 avril 2026)**
Détails techniques complets sur les capacités offensives de Mythos Preview. Inclut les cas Firefox 147, OpenBSD 27 ans, FFmpeg 16 ans / 5M passes, le scaffold utilisé, et la comparaison Opus 4.6 (near-0%) vs Mythos (181 exploits). Source du chiffre 83,1% sur CyberGym.
🔗 https://red.anthropic.com/2026/mythos-preview/

**Anthropic — Claude Mythos Preview System Card (7 avril 2026)**
Document de 244 pages. Source des incidents de comportement (sandbox escape, effacement git, jugements subjectifs sur l'alignement). Contient la note de bas de page n°10 sur Sam Bowman et le sandwich.
🔗 https://www.anthropic.com/claude-mythos-preview-system-card

**Anthropic — Alignment Risk Update : Claude Mythos Preview (7 avril 2026)**
Rapport d'évaluation des risques d'alignement. Source des citations sur les "jugements subjectifs" et l'absence de confiance dans l'identification exhaustive des problèmes.
🔗 https://www.anthropic.com/claude-mythos-preview-risk-report

---

## 📰 Sources secondaires — Presse et analyses

**NBC News — "Anthropic Project Glasswing: Mythos Preview gets limited release"**
Citations de Logan Graham (head of offensive cyber research) sur l'autonomie et le "long-range-ness" du modèle. Citation de Heidy Khlaaf sur l'absence de taux de faux positifs dans les benchmarks publiés.
🔗 https://www.nbcnews.com/tech/security/anthropic-project-glasswing-mythos-preview-claude-gets-limited-release-rcna267234

**Simon Willison — "Project Glasswing—restricting Claude Mythos to security researchers" (7 avril 2026)**
Analyse indépendante. Mention de Mythos comme premier modèle à finir un cyber range privé de bout en bout. Retranscription de la vidéo Nicholas Carlini sur le chaînage de vulnérabilités.
🔗 https://simonwillison.net/2026/Apr/7/project-glasswing/

**The Register — "Project Glasswing and open source: The good, bad, and ugly" (10 avril 2026)**
Opinion critique : "Just what FOSS developers need — a flood of AI-discovered vulnerabilities." Source de la formulation "Mythos ferait s'effondrer l'internet en une journée".
🔗 https://www.theregister.com/2026/04/10/project_glasswing/

**Penligent — "Claude Mythos Preview Is Not Black Box Pentesting" (8 avril 2026)**
Analyse technique précise sur la distinction white-box vs black-box. Démontre que ce qu'Anthropic a testé (code source fourni, conteneur isolé) n'est pas équivalent à un pentest sur une application web live.
🔗 https://www.penligent.ai/hackinglabs/claude-mythos-preview-is-not-black-box-pentesting

**Decrypt — "Anthropic's Mythos Safety Report Shows It Can No Longer Fully Measure What It Built"**
Analyse des hedges linguistiques dans la system card. Comparaison quantitative avec Opus 4.6 : augmentation des termes subjectifs, "caveat", "not confident". Source de la métaphore du guide de montagne.
🔗 https://decrypt.co/363663/anthropic-claude-mythos-safety-report-warning-risk-assesment

**LessWrong — "Excerpts and Notes on Mythos Model Card"**
Analyse des claims internes sur les "grandes contributions" de Mythos qui se sont dégonflées à l'examen. Source de la nuance sur ce qui semblait être de la découverte autonome vs exécution fiable d'approches humaines.
🔗 https://www.lesswrong.com/posts/ZfbChZBXgje8T6Geu/excerpts-and-notes-on-mythos-model-card

**Picus Security — "The Glasswing Paradox" (2026)**
Source de l'IPO potentielle en octobre 2026 et de l'accord Broadcom. Citation de Larry Dignan (Constellation Research) : "Glasswing is good for the industry and great marketing for Claude."
🔗 https://www.picussecurity.com/resource/blog/anthropics-project-glasswing-paradox

---

## ⚖️ Sources — Contexte Pentagon / juridique

**ABC News — "Anthropic and Pentagon supply chain dispute"**
Détails des négociations entre Anthropic et le Pentagone. Refus de lever les garde-fous sur les armes autonomes et la surveillance de masse. Annonce de la liste noire fin février 2026.
🔗 https://abcnews.com/Politics/anthropic-latest-pentagon-contract-bar-ai-autonomous-weapons/story?id=130558898

**CNBC — "Claude used in Iran strikes"**
Confirmation que le Pentagone a continué d'utiliser Claude dans les opérations en Iran malgré la désignation "supply chain risk".
🔗 https://www.cnbc.com/2026/03/05/anthropic-pentagon-ai-claude-iran.html

**CNN — "Judge blocks Pentagon's effort to punish Anthropic" (26 mars 2026)**
Injonction préliminaire du juge Rita Lin bloquant la désignation supply chain risk. Citation : "Nothing in the governing statute supports the Orwellian notion that an American company may be branded a potential adversary."
🔗 https://www.cnn.com/2026/03/26/business/anthropic-pentagon-injunction-supply-chain-risk

**CNBC — "Anthropic loses appeals court bid" (8 avril 2026)**
La cour d'appel de Washington refuse de suspendre la désignation le lendemain de l'annonce Glasswing. Citation : "The equitable balance here cuts in favor of the government."
🔗 https://www.cnbc.com/2026/04/08/anthropic-pentagon-court-ruling-supply-chain-risk.html

**Bloomberg — "Anthropic Fails to Halt US Label as a Supply Chain Risk" (8 avril 2026)**
Arguments oraux fixés au 19 mai. Reconnaissance par la cour qu'Anthropic "is likely to suffer some irreparable harm".
🔗 https://www.bloomberg.com/news/articles/2026-04-08/anthropic-fails-for-now-to-halt-us-label-as-a-supply-chain-risk

---

## 🛠️ Sources — Open source sous-financé

**Wikipedia — Core Infrastructure Initiative**
Chiffres sur OpenSSL avant Heartbleed : 1 développeur à plein temps, 20 000$/an de salaire, 2 000$/an de dons. Contexte de la création du CII après la découverte de Heartbleed en 2014.
🔗 https://en.wikipedia.org/wiki/Core_Infrastructure_Initiative

**USC Viterbi — "Hacked: The overlooked and under-supported open source projects"**
Analyse des incidents XZ Utils (2024) et Heartbleed. Confirmation du mainteneur unique Lasse Collin, épuisement documenté, tactiques de l'attaquant "Jia Tan" sur 2 ans.
🔗 https://illumin.usc.edu/hacked-open-source-projects/

**The New Stack — "cURL's Daniel Stenberg: AI is DDoSing open source" (février 2026)**
Interview de Stenberg à FOSDEM 2026. Source de la citation "will to live" (hampering our will to live). Chiffres 1/20 à 1/30 de validité. Twist : AISLE trouve de vraies CVEs pendant que le bug bounty s'effondre.
🔗 https://thenewstack.io/curls-daniel-stenberg-ai-is-ddosing-open-source-and-fixing-its-bugs/

**Daniel Stenberg — Blog personnel : "The end of the curl bug-bounty" (26 janvier 2026)**
Source primaire de la citation exacte : "The never-ending slop submissions take a serious mental toll to manage and sometimes also a long time to debunk. Time and energy that is completely wasted while also hampering our will to live."
🔗 https://daniel.haxx.se/blog/

**BleepingComputer — "curl ending bug bounty program after flood of AI slop reports" (janvier 2026)**
Chiffres sur les soumissions IA : 20% des rapports en 2025, taux de validité 5%. Contexte de la fermeture du programme HackerOne.
🔗 https://www.bleepingcomputer.com/news/security/curl-ending-bug-bounty-program-after-flood-of-ai-slop-reports/

**LessWrong — "AI found 12 of 12 OpenSSL zero-days while curl cancelled its bug bounty"**
Source du twist curl : l'IA sérieuse (AISLE) soumet 5 vraies CVEs pendant que le bug bounty s'effondre. Dans la release 8.18.0 : 3 des 6 corrections de sécurité attribuées à AISLE.
🔗 https://www.lesswrong.com/posts/7aJwgbMEiKq5egQbd/ai-found-12-of-12-openssl-zero-days-while-curl-cancelled-its

---

*Sources compilées le 16 avril 2026. La situation juridique entre Anthropic et le Pentagone étant en cours (arguments oraux fixés au 19 mai 2026), certaines informations peuvent évoluer.*
