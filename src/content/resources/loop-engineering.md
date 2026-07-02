---
title: "L'agent, c'est un LLM avec une boucle"
date: 2026-07-02
video_url: "#"
tags: ["IA", "Agents", "ClaudeCode", "LoopEngineering", "Automatisation"]
---

# Sources — L'agent, c'est un LLM avec une boucle

Sources primaires utilisées dans le script. Classées par bloc narratif.

---

## Le précédent — AutoGPT / BabyAGI

**Significant Gravitas (2023)**
*AutoGPT — An Autonomous GPT-4 experiment*
GitHub — <https://github.com/Significant-Gravitas/AutoGPT>
Dépôt d'origine d'AutoGPT. Premier projet à populariser le pattern agent-loop autonome avec un LLM.

**Nakajima, Y. (2023)**
*BabyAGI*
GitHub — <https://github.com/yoheinakajima/babyagi>
Dépôt d'origine de BabyAGI, cité en parallèle d'AutoGPT pour illustrer la lignée des premiers loops LLM.

---

## La pile — prompt, skill, MCP, loop

**Anthropic (2026)**
*When AI Builds Itself*
Rapport officiel Anthropic — <https://www.anthropic.com/research/when-ai-builds-itself>
Documente que plus de 80 % du code mergé en production chez Anthropic en mai 2026 était écrit par Claude.

**Anthropic**
*Skills — skill-creator/SKILL.md*
GitHub — <https://github.com/anthropics/skills/blob/main/skills/skill-creator/SKILL.md>
Format de référence officiel du standard Skills : structure, chargement progressif, injection dans le contexte.

**Huntley, G. (2025)**
*Perpetual Generative Agents with Claude Code — The Ralph Wiggum Pattern*
<https://ghuntley.com/ralph/>
Post original de la technique Ralph Wiggum : boucle statique sur un fichier PROMPT.md, progrès persisté via le disque et git.

**Huntley, G.**
*how-to-ralph-wiggum*
GitHub — <https://github.com/ghuntley/how-to-ralph-wiggum>
Complément au post ghuntley.com sur le mécanisme exact de la boucle Ralph Wiggum.

**Anthropic — documentation officielle Claude Code**
*Commande `/goal`*
<https://code.claude.com/docs/en/goal.md>
Condition de complétion évaluée après chaque tour par un modèle rapide séparé, qui rend une décision oui/non sans rien exécuter lui-même.

---

## Le trou du conditionnel — verifier agent

**Maloyan, N., Ashinov, B., Namiot, D. (2025)**
*Investigating the Vulnerability of LLM-as-a-Judge Architectures to Prompt-Injection Attacks*
International Journal of Open Information Technologies, 13(9):1–6 — ArXiv:2505.13348 — <https://arxiv.org/abs/2505.13348>
Formalise deux attaques (Comparative Undermining Attack, Justification Manipulation Attack) contre les architectures LLM-as-a-Judge par injection de prompt.

**Braintrust**
<https://www.braintrustdata.com>
Outil d'évaluation cité comme exemple de la catégorie "outils dédiés à l'évaluation de verifiers".

---

## Les limites structurelles

**Cat Wu (Anthropic)**
*Reflecting on a year of Claude Code*
YouTube, chaîne ClaudeDevs — <https://www.youtube.com/watch?v=Hth_tLaC2j8>
Conversation avec Boris Cherny sur le risque de micromanagement d'un harness trop chargé en contexte.

**Karpathy, A. (2026)**
*autoresearch*
GitHub — <https://github.com/karpathy/autoresearch>
Boucle qui édite un unique fichier `train.py`, lance une expérience bornée dans le temps, garde ou rejette le résultat selon une métrique, recommence.

---

## Les filtres et le conflit d'intérêt

**Cherny, B. (Anthropic, créateur de Claude Code)**
*Talk WorkOS Acquired Unplugged* (2026)
Corroboré par le blog officiel WorkOS — <https://workos.com/blog>
Citation : "I don't prompt Claude anymore. My job is to write loops."

**Steinberger, P. (@steipete, créateur d'OpenClaw)**
*Tweet* (7 juin 2026)
x.com/@steipete
Tweet de consécration du loop engineering, publié après avoir rejoint OpenAI mi-février 2026.

**Osmani, A. (Google, 2026)**
*Loop Engineering*
Essai qui structure le concept en six briques (automations, worktrees, skills, connectors, sub-agents, external state) et lui donne son nom.

---

## Sources secondaires de contexte

**thenewstack.io**
*Loop Engineering* (juin 2026)
<https://thenewstack.io/loop-engineering/>
Couverture de référence pour dater la propagation du terme dans la presse tech grand public.

**explainx.ai**
*Loop Engineering — mainstream AI skill, June 2026*
<https://explainx.ai/blog/loop-engineering-mainstream-ai-skill-june-2026>
Synthèse de contexte, à ne pas citer comme fait établi (mono-sourcée sur plusieurs éléments).
