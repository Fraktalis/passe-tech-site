---
title: "Le protocole le plus sous-côté"
date: 2026-07-31
video_url: "https://youtu.be/7Ola74jiKEg"
tags: ["HTTP", "SSE", "WebSocket", "Streamable HTTP", "MCP", "Réseau"]
---

# Sources — "Le protocole le plus sous-côté"
### Passe-Tech | Juillet 2026

---

## 🔀 BASCULE — Le mythe (HTTP continue d'évoluer)

**IETF / RFC Editor — RFC 10008 : The HTTP QUERY Method** (juin 2026)
Nouveau verbe HTTP QUERY : safe, idempotent et cacheable comme GET, mais portant un corps comme POST. Publié comme Proposed Standard par le groupe de travail HTTPBIS.
🔗 https://www.rfc-editor.org/info/rfc10008

**IETF Datatracker — Historique du draft QUERY / SEARCH**
Draft individuel de 2015, relancé en 2019, adopté par HTTPBIS en 2021 sous le nom SEARCH, renommé QUERY en 2021-2022.
🔗 https://datatracker.ietf.org/doc/draft-snell-search-method/history/

**IETF Datatracker — RFC 5323 (WebDAV SEARCH)**
Précédent historique d'une méthode HTTP safe-with-body, antérieur à QUERY.
🔗 https://datatracker.ietf.org/doc/html/rfc5323

---

## 🔌 ACTE 2 — WebSocket

**MDN Web Docs — 101 Switching Protocols**
Mécanisme d'upgrade HTTP : header `Upgrade`, réponse 101, transition immédiate vers le nouveau protocole.
🔗 https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/101

**sitechecker.pro — What is HTTP Status Code 101 "Switching Protocols"?**
Usage historique du 101 pour l'upgrade HTTP/1.1 → HTTP/2 en clair, aujourd'hui largement obsolète (remplacé par ALPN pendant le handshake TLS).
🔗 https://sitechecker.pro/what-is-101-status-code/

**OpenFront sur Steam**
Jeu de stratégie multijoueur en WebSocket, environ un million de joueurs par mois, mêmes serveurs pour le web et Steam.
🔗 https://store.steampowered.com/app/3560670/OpenFront/

**Nolen Royalty (eieio.games) — Scaling One Million Checkboxes to 650,000,000 checks** (25 juillet 2024)
Récit de l'auteur : lancement le 26 juin 2024, 8 VM workers, snapshot complet renvoyé toutes les 30 secondes, pub/sub Redis pour diffuser l'état entre instances.
🔗 https://eieio.games/blog/scaling-one-million-checkboxes/

**Nolen Royalty (eieio.games) — The Secret Inside One Million Checkboxes** (30 août 2024)
Messages secrets cachés en ASCII binaire dans des séquences de cases cochées, détectés en dumpant la base Redis.
🔗 https://eieio.games/blog/the-secret-inside-one-million-checkboxes/

**Taskade Blog — History of WebSockets: How the Web Got Real-Time**
Netscape Navigator 2.0 (1996) et `multipart/x-mixed-replace` pour un server push précoce ; déploiements Comet chez Meebo, Gmail Chat et Facebook Chat à la fin des années 2000.
🔗 https://www.taskade.com/blog/websockets-history

**Ably — The history of WebSockets: an evolution of HTTP-based techniques**
Comet popularisé par Google (Gmail Chat) et Meebo (chat multi-réseaux dans le navigateur).
🔗 https://ably.com/topic/websockets-history

**Grokipedia — Comet (programming)**
Alex Russell nomme la famille de techniques "Comet" en 2006.
🔗 https://grokipedia.com/page/Comet_(programming)

---

## 📡 ACTE 3 — Streamable HTTP / MCP

**Model Context Protocol — Transports (spec 2025-11-25)**
`Mcp-Session-Id` assigné à l'initialisation, GET autonome pour ouvrir un flux SSE passif, reprise via `id:` + `Last-Event-ID`.
🔗 https://modelcontextprotocol.io/specification/2025-11-25/basic/transports

**The New Stack — How MCP Uses Streamable HTTP for Real-Time AI Tool Interaction**
Mécanisme de session comme statefulness applicative posée sur un transport HTTP par ailleurs stateless.
🔗 https://thenewstack.io/how-mcp-uses-streamable-http-for-real-time-ai-tool-interaction/

**Model Context Protocol — spec draft, Streamable HTTP**
Révision en préparation : suppression du endpoint GET autonome, des sessions au niveau protocole et de la reprise via `Last-Event-ID`, remplacées par un endpoint `subscriptions/listen` et des headers miroir pour le routing par les load balancers/gateways.
🔗 https://modelcontextprotocol.io/specification/draft/basic/transports/streamable-http

---

## 📖 Concepts généraux

**Wikipedia — Modèle OSI**
Couche 7 (application) et couche 4 (transport, TCP), base de la distinction entre les mécanismes évoqués dans la vidéo.
🔗 https://en.wikipedia.org/wiki/OSI_model

Problème C10K nommé par Dan Kegel ; Ian Hickson, éditeur HTML5 chez Google, à l'origine de SSE et WebSocket comme réponses distinctes au bricolage Comet.

---

*Sources compilées le 24 juillet 2026, à l'occasion de la publication de la vidéo.*
