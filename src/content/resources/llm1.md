---
title: "Comment marche un LLM ? Pas comme vous croyez"
date: 2026-06-13
video_url: "https://youtu.be/kJsZNBfJ8ZA"
tags: ["IA", "LLM" , "ChatGPT" , "MachineLearning" , "Transformer" , "Vulgarisation"]
---

# Sources — Comment marche un LLM

Sources primaires utilisées dans le script. Classées par chapitre d'utilisation.

---

## Chapitre 3 — Découper le langage

**Sennrich, R., Haddow, B., & Birch, A. (2016)**
*Neural Machine Translation of Rare Words with Subword Units* (BPE)
ArXiv:1508.07909 — <https://arxiv.org/abs/1508.07909>
Papier original du Byte Pair Encoding. Fondement du chapitre 3 sur la tokenisation.

**Batsuren, K., et al. (2024)**
*Counting letters in LLMs: a systematic study*
ArXiv:2412.18626 — <https://arxiv.org/abs/2412.18626>
Étude expérimentale systématique sur les erreurs de comptage de lettres dans les LLMs. Confirme que les erreurs sont liées à la tokenisation et aux limites de l'attention. Utilisé pour le device "strawberry" et sa contextualisation sur les modèles sans raisonnement activé.

---

## Chapitre 4 — La carte des mots

**Mikolov, T., Chen, K., Corrado, G., & Dean, J. (2013)**
*Efficient Estimation of Word Representations in Vector Space* (Word2Vec)
ArXiv:1301.3781 — <https://arxiv.org/abs/1301.3781>
Papier fondateur des word embeddings statiques. Introduit les propriétés d'analogie vectorielle (roi−homme+femme≈reine) sur lesquelles le chapitre 4 s'appuie pour illustrer la sémantique géométrique — en distinguant explicitement ces embeddings statiques des embeddings contextualisés des LLMs actuels.

---

## Chapitre 5 — Lire tout en même temps

**Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, Ł., & Polosukhin, I. (2017)**
*Attention Is All You Need*
ArXiv:1706.03762 — <https://arxiv.org/abs/1706.03762>
Papier fondateur du Transformer. Introduit le mécanisme d'attention multi-têtes et l'architecture encodeur-décodeur sans récurrence. Utilisé pour le mécanisme Q/K/V et la justification de la parallélisation sur GPU.

---

## Chapitre 6 — Ce qu'il a avalé

**Brown, T., Mann, B., Ryder, N., et al. (2020)**
*Language Models are Few-Shot Learners* (GPT-3)
ArXiv:2005.14165 — <https://arxiv.org/abs/2005.14165>
Papier de référence sur le pre-training à grande échelle. Documente les capacités few-shot émergentes à 175B paramètres, corpus d'entraînement (~570 Go de CommonCrawl filtré + corpus complémentaires). Utilisé pour les ordres de grandeur du pre-training et l'émergence des capacités.

**Ouyang, L., Wu, J., Jiang, X., et al. (2022)**
*Training language models to follow instructions with human feedback* (InstructGPT)
ArXiv:2203.02155 — <https://arxiv.org/abs/2203.02155>
Papier de référence sur le RLHF. Décrit le pipeline SFT + reward model + PPO. Utilisé pour expliquer la transformation du compléteur en assistant.

**Wei, J., Tay, Y., Bommasani, R., et al. (2022)**
*Emergent Abilities of Large Language Models*
Transactions on Machine Learning Research (TMLR)
ArXiv:2206.07682 — <https://arxiv.org/abs/2206.07682>
Formalise le concept de capacités émergentes. Définition : capacité absente dans les petits modèles, présente dans les grands, non prédictible par extrapolation. Utilisé pour le bloc sur l'émergence.

**Schaeffer, R., Miranda, B., & Koyejo, S. (2023)**
*Are Emergent Abilities of Large Language Models a Mirage?*
NeurIPS 2023 Outstanding Paper Award
ArXiv:2304.15004 — <https://arxiv.org/abs/2304.15004>
Contre-argument à Wei et al. Argumente que les ruptures apparentes sont des artefacts des métriques non-linéaires. Utilisé pour présenter le débat scientifique sur l'émergence.

---

## Chapitre 8 — Ce qu'il ne voit pas

**Liu, N. F., Lin, K., Hewitt, J., Paranjape, A., Bevilacqua, M., Petroni, F., & Liang, P. (2023)**
*Lost in the Middle: How Language Models Use Long Contexts*
Transactions of the Association for Computational Linguistics
ArXiv:2307.03172 — <https://arxiv.org/abs/2307.03172>
Documente la tendance des LLMs à mieux traiter les informations en début et fin de contexte qu'au milieu. Utilisé pour nuancer l'affirmation "une grande fenêtre de contexte résout tout".

---

## Sources secondaires et guides

**promptingguide.ai**
<https://www.promptingguide.ai>
Guide de référence sur les LLMs et les techniques de prompting. Base de matière pour l'ensemble de la série de vidéos.

**Holtzman, A., Buys, J., Du, L., Forbes, M., & Choi, Y. (2020)**
*The Curious Case of Neural Text Degeneration* (nucleus sampling / Top-P)
ArXiv:1904.09751 — <https://arxiv.org/abs/1904.09751>
Papier original du nucleus sampling. Non cité explicitement dans le script mais fondement du chapitre 7 sur la température et le Top-P.
