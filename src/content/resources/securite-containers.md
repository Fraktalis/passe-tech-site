---
title: "Ton container Docker n'est pas sécurisé. Voilà pourquoi."
date: 2026-05-23
video_url: "#"
tags: ["Docker", "Containers", "Cybersécurité", "DevOps", "Kubernetes"]
---

# Sources — "Ton container Docker n'est pas sécurisé. Voilà pourquoi."
### Passe-Tech | À venir
 
---
 
## 🏗️ Fondamentaux — Isolation & surface d'attaque
 
**Docker Documentation — Security overview**
Vue d'ensemble officielle du modèle de sécurité Docker. Namespaces Linux, cgroups, capabilities, seccomp. Point de départ incontournable pour comprendre ce que le runtime garantit (et ne garantit pas).
🔗 https://docs.docker.com/engine/security/

**Linux Kernel — Namespaces & cgroups**
Documentation des primitives noyau qui fondent l'isolation des containers. Explique pourquoi un container n'est pas une VM.
🔗 https://man7.org/linux/man-pages/man7/namespaces.7.html

---

## 🔓 Vecteurs d'attaque courants

**OWASP Docker Security Cheat Sheet**
Liste structurée des mauvaises configurations les plus exploitées : daemon exposé, conteneur privilégié, montage du socket Docker, volumes sensibles.
🔗 https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html

**NCC Group — "Understanding and Hardening Linux Containers" (2016)**
Référence technique sur la profondeur des mécanismes d'isolation. Toujours pertinent pour comprendre les limites fondamentales.
🔗 https://research.nccgroup.com/wp-content/uploads/2020/07/ncc_group_understanding_hardening_linux_containers-1-1.pdf

**Trail of Bits — "Docker for Pentesters"**
Techniques d'évasion de container documentées : abus du socket Docker, escape via `/proc`, exploitation des capabilities non restreintes.
🔗 https://blog.trailofbits.com/2019/07/19/docker-for-pentesters/

---

## 🖼️ Sécurité des images

**Snyk — State of Open Source Security Report (dernière édition)**
Statistiques sur la présence de CVE dans les images Docker Hub officielles. Chiffres d'impact réels.
🔗 https://snyk.io/reports/open-source-security/

**Chainguard — "Minimal Container Images"**
Approche distroless/minimal pour réduire la surface d'attaque. Comparaison avec les images classiques Alpine et Debian.
🔗 https://www.chainguard.dev/unchained/minimal-container-images-towards-a-more-secure-future

**Google — Distroless Images**
Dépôt de référence des images sans shell ni gestionnaire de paquets, utilisées en production chez Google.
🔗 https://github.com/GoogleContainerTools/distroless

---

## 🔬 Runtime Security

**Falco (CNCF) — Documentation**
Outil de détection comportementale en temps réel pour containers. Règles basées sur les syscalls.
🔗 https://falco.org/docs/

**gVisor — Sandbox kernel (Google)**
Noyau applicatif en espace utilisateur pour isoler les containers de l'hôte. Architecture et cas d'usage.
🔗 https://gvisor.dev/docs/

**Kata Containers**
Containers dans des micro-VMs légères. Isolation renforcée par hyperviseur.
🔗 https://katacontainers.io/learn/

---

## 🛠️ Durcissement & outils

**CIS Docker Benchmark**
Référentiel de durcissement Docker publié par le Center for Internet Security. Base des audits de conformité.
🔗 https://www.cisecurity.org/benchmark/docker

**Docker Bench for Security**
Script d'audit automatisé qui vérifie la conformité au CIS Benchmark sur un hôte Docker.
🔗 https://github.com/docker/docker-bench-security

**Trivy (Aqua Security) — Scanner de vulnérabilités**
Scanner de CVE pour images, filesystems, dépôts Git et configurations IaC. Standard de facto dans les pipelines CI.
🔗 https://trivy.dev/

**Dockle — Linter d'images Docker**
Analyse les bonnes pratiques de sécurité dans un Dockerfile (USER non-root, HEALTHCHECK, etc.).
🔗 https://github.com/goodwithtech/dockle

---

## ☸️ Kubernetes & orchestration

**Kubernetes — Pod Security Standards**
Trois niveaux de politique de sécurité (Privileged, Baseline, Restricted). Remplacement des PodSecurityPolicies.
🔗 https://kubernetes.io/docs/concepts/security/pod-security-standards/

**NSA/CISA — Kubernetes Hardening Guide (2022)**
Guide officiel de durcissement Kubernetes publié par les agences de sécurité américaines. Sections sur la sécurité des containers dans un cluster.
🔗 https://www.nsa.gov/Press-Room/News-Highlights/Article/Article/2716980/nsa-cisa-release-kubernetes-hardening-guidance/

---

## 📖 Contexte & incidents notables

**Sysdig — "TeamTNT : Inside a Container Attack"**
Analyse d'une campagne réelle ciblant les démons Docker exposés sur Internet. Cryptomining, lateral movement, exfiltration de credentials AWS.
🔗 https://sysdig.com/blog/teamtnt-malicious-docker-hub-container/

**Aqua Security — "The Container Threat Landscape Report"**
Rapport annuel sur les attaques observées en production contre des containers et clusters Kubernetes.
🔗 https://www.aquasec.com/cloud-native-threats/

---

*Sources compilées le 23 mai 2026.*
