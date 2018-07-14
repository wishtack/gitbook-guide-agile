# Déploiement Continu

L'une des limitations de la [Livraison Continue](livraison-continue.md) est que la validation manuelle du déploiement **favorise la procrastination** et peut alors **encourager le déploiement par lot**. On retrouve alors les problèmes de l'Integration Hell en production ou alors des divergences de fonctionnement entre l'environnement de développement et la production.

Pour remédier à cela, le **Déploiement Continu** reprend exactement le même fonctionnement que la [Livraison Continue](livraison-continue.md) sauf que cette fois-ci le **déploiement est automatisé**. Chaque changement est donc automatiquement déployé jusqu'en production.

Le Déploiement Continu ne peut être efficace que si le produit dispose d'un jeu de tests automatisés largement suffisant pour garantir le bon fonctionnement de l'application.

La validation manuelle est toujours possible mais en utilisant une approche à base de [Review Apps](review-apps.md).

