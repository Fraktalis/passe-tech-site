---
title: "litellm : le braquage raté qui a quand même marché"
date: 2026-04-01
video_url: "#"
tags: ["liteLLM", "Supply Chain Attack", "Cybersécurité", "Python"]
---

# Sources — "litellm : le braquage raté qui a quand même marché"
### Passe-Tech | 01 avril 2026
 
---
 
## 🔎 Découverte & analyse initiale
 
**FutureSearch — Rapport de découverte (24 mars 2026)**
Première divulgation publique de l'attaque. Analyse technique du fichier `litellm_init.pth`, timeline de l'incident, description du payload en trois étapes.
🔗 https://futuresearch.ai/blog/litellm-pypi-supply-chain-attack
 
**FutureSearch — Analyse de l'ampleur : "Were You One of the 47,000?" (25 mars 2026)**
Requête BigQuery sur les téléchargements PyPI pendant la fenêtre d'attaque. Chiffres : 46 996 téléchargements, 2 337 paquets dépendants, 88% exposés. Distinction entre les deux vecteurs 1.82.7 et 1.82.8.
🔗 https://futuresearch.ai/blog/litellm-hack-were-you-one-of-the-47000
 
**FutureSearch — Checker interactif**
Outil permettant de vérifier si un paquet PyPI dépend de litellm et s'il était exposé pendant la fenêtre d'attaque.
🔗 https://futuresearch.ai/tools/litellm-checker
 
---
 
## 🏢 Réponse officielle des mainteneurs
 
**BerriAI / litellm — Security Update (25 mars 2026)**
Déclaration officielle des mainteneurs. Confirmation que la compromission provient de la dépendance Trivy dans le pipeline CI. Pause des nouvelles releases. Scripts de détection pour GitHub Actions et GitLab CI.
🔗 https://docs.litellm.ai/blog/security-update-march-2026
 
**GitHub Issue #24512 — BerriAI/litellm**
Thread communautaire original de signalement. Inclut la fermeture de l'issue par le compte compromis et la réponse de la communauté.
🔗 https://github.com/BerriAI/litellm/issues/24512
 
---
 
## 🔬 Analyses techniques approfondies
 
**Snyk — "How a Poisoned Security Scanner Became the Key to Backdooring LiteLLM"**
Analyse complète de la chaîne d'attaque Trivy → litellm. Timeline détaillée, description du mécanisme `.pth`, analyse du botnet de 88 comptes compromis en 102 secondes. Lien avec la campagne Trivy du 19 mars.
🔗 https://snyk.io/articles/poisoned-security-scanner-backdooring-litellm/
 
**Endor Labs — "TeamPCP Isn't Done"**
Analyse de la campagne globale TeamPCP sur 5 écosystèmes. Identification de la Phase 09. Évaluation des prochaines cibles probables (RubyGems, crates.io, Maven Central).
🔗 https://www.endorlabs.com/learn/teampcp-isnt-done
 
**Sonatype — "Compromised litellm PyPI Package Delivers Multi-Stage Credential Stealer"**
Analyse du payload multi-étapes. Détection automatique par Sonatype dans les secondes suivant la publication (sonatype-2026-001357). Mention des liens supposés avec LAPSUS$.
🔗 https://www.sonatype.com/blog/compromised-litellm-pypi-package-delivers-multi-stage-credential-stealer
 
**The Hacker News — "TeamPCP Backdoors LiteLLM Versions 1.82.7–1.82.8 via Trivy CI/CD Compromise"**
Synthèse de la campagne. Déclarations de TeamPCP sur Telegram. Collaboration supposée avec LAPSUS$. Chiffre Wiz : litellm présent dans 36% des environnements cloud.
🔗 https://thehackernews.com/2026/03/teampcp-backdoors-litellm-versions.html
 
**Truesec — Threat Notice**
Indicateurs de compromission (IOC). Domaines d'exfiltration : `models.litellm.cloud` et `checkmarx.zone/raw`.
🔗 https://www.truesec.com/hub/blog/malicious-pypi-package-litellm-supply-chain-compromise
 
---
 
## 📊 Analyse d'impact
 
**Comet — Post-mortem public**
Seule organisation à avoir communiqué publiquement sur l'incident. Confirmation de deux pipelines CI compromis. Audit de 50+ dépôts GitHub.
🔗 https://www.comet.com/site/blog/litellm-supply-chain-attack/
 
**Arctic Wolf — Campaign Analysis**
Analyse de la campagne globale TeamPCP (Trivy + Checkmarx KICS + litellm). Estimation : au moins 1 000 environnements SaaS d'entreprise potentiellement affectés.
🔗 https://arcticwolf.com/resources/blog/teampcp-supply-chain-attack-campaign-targets-trivy-checkmarx-kics-and-litellm-potential-downstream-impact-to-additional-projects/
 
---
 
## 🕵️ Contexte de la campagne TeamPCP
 
**Kaspersky — "Trojanization of Trivy, Checkmarx, and LiteLLM"**
Vue d'ensemble de la campagne. CVE-2026-33634 (score CVSS4B : 9.4). Timeline complète des trois attaques. Description de la technique de réécriture des tags Git.
🔗 https://www.kaspersky.com/blog/critical-supply-chain-attack-trivy-litellm-checkmarx-teampcp/55510/
 
**Microsoft Security Blog — "Detecting, Investigating, and Defending Against the Trivy Supply Chain Compromise"**
Analyse technique de la compromission Trivy. Explication du mécanisme de tags Git mutables. Détections Microsoft Defender.
🔗 https://www.microsoft.com/en-us/security/blog/2026/03/24/detecting-investigating-defending-against-trivy-supply-chain-compromise/
 
**ReversingLabs — "TeamPCP Software Supply Chain Attack Spreads to LiteLLM"**
Analyse de la compromission du compte GitHub du co-fondateur de litellm, Krish Dholakia. Défacement automatisé des dépôts le 24 mars à 14h00 UTC.
🔗 https://www.reversinglabs.com/blog/teampcp-supply-chain-attack-spreads
 
**Aikido Security — Documentation du hackerbot-claw**
Documentation de l'utilisation d'un agent IA autonome (`hackerbot-claw`) dans la compromission initiale de Trivy. Premier cas documenté d'agent IA utilisé opérationnellement dans une supply chain attack.
*(Référencé via Snyk et Endor Labs)*
 
---
 
## 🏛️ Alertes institutionnelles
 
**PyPI — Advisory officiel**
Avis de quarantaine des versions 1.82.7 et 1.82.8. Recommandations de rotation des credentials.
🔗 https://pypi.org *(advisory interne, référencé dans les analyses Snyk et CSO Online)*
 
**FBI Cyber Division — Alerte formelle (27 mars 2026)**
Déclaration publique de Brett Leatherman, Assistant Director. Anticipation d'une vague d'annonces de compromissions et de tentatives d'extorsion.
*(Référencé via Infosecurity Magazine)*
🔗 https://www.infosecurity-magazine.com/news/teampcp-litellm-pypi-supply-chain/
 
---
 
## 📖 Documentation technique de référence
 
**Python — Documentation officielle des fichiers `.pth`**
Spécification du mécanisme `site-packages` et du comportement d'exécution des fichiers `.pth` au démarrage de l'interpréteur.
🔗 https://docs.python.org/3/library/site.html
 
**PyPI Blog — Analyse de l'attaque Ultralytics (décembre 2024)**
Contexte historique : précédent notable d'attaque supply chain via GitHub Actions sur un paquet Python IA (Ultralytics YOLO). Mécanisme de cache poisoning documenté.
🔗 https://blog.pypi.org/posts/2024-12-11-ultralytics-attack-analysis/
 
---
 
*Sources compilées le 29 mars 2026. La campagne TeamPCP étant en cours, certaines informations peuvent avoir évolué depuis la publication de cette vidéo.*
 
