---
title: "Reverse Proxy, Load Balancer, API Gateway : c'est quoi la différence ?"
date: 2026-05-01
video_url: "https://youtu.be/_1-UA1PUAB4"
tags: ["Reverse Proxy", "Load Balancer", "API Gateway", "Nginx", "Traefik", "Kong", "Réseau", "Architecture"]
---

# Sources - "Reverse Proxy, Load Balancer, API Gateway : c'est quoi la différence ?"
### Passe-Tech | Mai 2026

---

## 🎟️ L'incident Ticketmaster - Eras Tour

**Ticketmaster - Communiqué officiel : "Taylor Swift The Eras Tour On-Sale Explained"**
Source primaire de l'incident. Chiffres officiels : 3,5 millions de pré-inscrits au programme Verified Fan, 3,5 milliards de requêtes système en une journée ("4x notre précédent pic").
🔗 https://business.ticketmaster.com/press-release/taylor-swift-the-eras-tour-onsale-explained/

**Wikipedia - Taylor Swift–Ticketmaster controversy**
Chronologie de l'incident, effondrement du site en moins d'une heure, réactions des fans et des législateurs.
🔗 https://en.wikipedia.org/wiki/Taylor_Swift%E2%80%93Ticketmaster_controversy

**CBS News - "Taylor Swift fans battle ticket bots and Ticketmaster"**
Le chiffre de "14 millions de tentatives" qui circule dans les médias. ⚠️ Le chiffre officiel Ticketmaster est "3,5 milliards de requêtes système" - à préférer.
🔗 https://www.cbsnews.com/news/taylor-swift-fans-battle-ticket-bots-and-ticketmaster/

---

## 🔧 Documentation officielle des outils

**Nginx - Documentation officielle**
Reverse Proxy et Load Balancer. Référence principale pour la configuration des upstreams, les algorithmes de répartition de charge, et la terminaison SSL.
🔗 https://nginx.org/en/docs/

**Caddy - Documentation officielle**
Reverse Proxy avec HTTPS automatique via Let's Encrypt. Configuration déclarative via Caddyfile.
🔗 https://caddyserver.com/docs/

**Traefik - Documentation officielle**
Reverse Proxy et API Gateway cloud-native. Détection automatique des services (Docker, Kubernetes).
🔗 https://doc.traefik.io/traefik/

**HAProxy - Documentation officielle**
Load Balancer haute performance, référence du secteur pour les déploiements critiques.
🔗 https://www.haproxy.org/#docs

**AWS Elastic Load Balancer - Documentation officielle**
Load Balancer managé AWS. Couvre les types ALB (L7), NLB (L4), et CLB.
🔗 https://docs.aws.amazon.com/elasticloadbalancing/

**Kong - Documentation officielle**
API Gateway open source. Gestion des plugins (auth, rate limiting, cache, logging).
🔗 https://docs.konghq.com/

**AWS API Gateway - Documentation officielle**
API Gateway managé AWS. Intégration native avec Lambda, IAM, et CloudWatch.
🔗 https://docs.aws.amazon.com/apigateway/

**Apigee - Documentation officielle**
API Gateway Google Cloud. Gestion du cycle de vie des APIs, analytics, monétisation.
🔗 https://cloud.google.com/apigee/docs

---

## 🔬 Points techniques

**Nginx - Health Checks : actifs vs passifs**
Health checks passifs natifs en version open source ; health checks actifs (polling proactif) disponibles uniquement sur Nginx Plus.
🔗 https://docs.nginx.com/nginx/admin-guide/load-balancer/http-health-check/

**Kong - Proxy Cache Plugin**
Cache de réponses HTTP via Redis ou mémoire. Réduction de la charge sur les services upstream.
🔗 https://docs.konghq.com/hub/kong-inc/proxy-cache/

**Nginx - SSL/TLS : Termination vs Passthrough (L4)**
SSL offloading (déchiffrement au niveau du Load Balancer) vs SSL passthrough (trafic chiffré transféré tel quel jusqu'au serveur backend).
🔗 https://docs.nginx.com/nginx/admin-guide/security-controls/terminating-ssl-tcp/

**Wikipedia - Modèle OSI**
Les 7 couches du modèle OSI. L4 = Transport (TCP/UDP), L7 = Application (HTTP/HTTPS). Base pour comprendre la distinction entre Load Balancing L4 et L7.
🔗 https://en.wikipedia.org/wiki/OSI_model

---

## ⚖️ Algorithmes de Load Balancing

**Nginx - Load Balancing : documentation des algorithmes**
Description et configuration des trois algorithmes principaux :
- **Round-robin** - distribution séquentielle cyclique (défaut)
- **Least connections** - envoi vers le serveur avec le moins de connexions actives
- **IP hash** - même client → même serveur (affinité de session) ⚠️ limité derrière NAT
🔗 https://nginx.org/en/docs/http/load_balancing.html

---
