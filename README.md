# AgriConnectCM
**AgriConnectCM** est une plateforme web visant à optimiser la chaîne logistique agricole au Cameroun. Elle met en relation les producteurs, transporteurs et acheteurs pour réduire les pertes post-récolte et améliorer l’accès au marché pour les petits producteurs. La plateforme offre un suivi en temps réel des colis, des alertes pour les anomalies (retards, température), et une messagerie intégrée.

## Contexte
Les petits producteurs agricoles au Cameroun font face à des pertes post-récolte importantes et à des difficultés d’accès au marché. Cette application, développée dans un cadre académique, propose une solution basée sur une architecture microservices avec Spring Boot (backend), Angular (frontend), Docker, et une pipeline CI/CD avec GitHub Actions.

## Fonctionnalités
- **Gestion des profils** : Inscription et gestion des comptes pour producteurs, transporteurs et acheteurs.
- **Publication d’offres** : Annonces de produits agricoles (type, quantité, localisation).
- **Suivi en temps réel** : Localisation GPS et surveillance IoT.
- **Optimisation des itinéraires** : Calcul des trajets pour les transporteurs.
- **Alertes** : Notifications pour retards ou anomalies via RabbitMQ.
- **Messagerie** : Communication en temps réel via WebSocket.

## Architecture
L’application utilise une architecture microservices :

```
agrichain-cameroon/
├── backend/
│   ├── users-service/        # Gestion des utilisateurs
│   ├── offers-service/       # Gestion des offres
│   ├── tracking-service/     # Suivi GPS/IoT
│   ├── alerts-service/       # Gestion des alertes
│   ├── routing-service/      # Optimisation des itinéraires
│   ├── messaging-service/    # Messagerie WebSocket
│   ├── gateway/              # Spring Cloud Gateway
│   └── common/               # Code partagé
├── frontend/                 # Application Angular
├── devops/
│   ├── docker-compose.yml    # Orchestration des services
│   ├── scripts/              # Scripts de déploiement
├── .github/
│   ├── workflows/
│   │   ├── pipeline.yml         # Pipeline CI/CD
├── README.md
└── .gitignore
```

