# Livraison Continue

En plus de tout ce que l'[intégration continue](integration-continue.md) propose, la **livraison continue** ajoute une dernière étape au process permettant aux parties prenantes autorisées de **déployer** la dernière version **en production par simple clic** mais également de **rollback** à la version précédente en cas de problème.

En plus de cette fonctionnalité, la livraison continue **implique surtout une façon de concevoir et de développer** les produits respectant les règles suivantes :

* Le code de l'environnement d'intégration doit fonctionner en production.
* L'intégralité du déploiement doit se faire automatiquement _\(y compris les migrations de base de données par exemple\)_.
* Le déploiement ne doit pas causer d'interruption de service.

![Continuous Delivery](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LHD4wSD1i9v5yCa767m%2F-LHJ4GPYKCKTQ1Xvm1al%2F-LHJDAedZr6u4V5h5w3U%2Fcontinuous-delivery.png?alt=media&token=70ff30f6-1a89-498c-a723-569d98ed7934)

