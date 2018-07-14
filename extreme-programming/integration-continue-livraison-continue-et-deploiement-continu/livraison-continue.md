# Livraison Continue

En plus de tout ce que l'[intégration continue](integration-continue.md) propose, la **livraison continue** ajoute une dernière étape au process permettant aux parties prenantes autorisées de **déployer** la dernière version **en production par simple clic** mais également de **rollback** à la version précédente en cas de problème.

En plus de cette fonctionnalité, la livraison continue **implique surtout une façon de concevoir et de développer** les produits respectant les règles suivantes :

* Le code de l'environnement d'intégration doit fonctionner en production.
* L'intégralité du déploiement doit se faire automatiquement _\(y compris les migrations de base de données par exemple\)_.
* Le déploiement ne doit pas causer d'interruption de service.
* Le rollback doit être automatisable et se faire en un clic _\(Pensez à la backward et forward compatibility ! e.g. : Le schéma de base de données est compatible avec la version précédente et la nouvelle version\)_.

![Continuous Delivery](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LHD4wSD1i9v5yCa767m%2F-LHJ4GPYKCKTQ1Xvm1al%2F-LHJDAedZr6u4V5h5w3U%2Fcontinuous-delivery.png?alt=media&token=70ff30f6-1a89-498c-a723-569d98ed7934)

## Blue-Green Deployment

Le Blue-Green Deployment consiste à mettre en place **deux environnements identiques** : **Green** et **Blue** avec un Router en amont permettant de conduire le traffic vers Green ou Blue.

En supposant que **la version actuelle du produit tourne sur l'environnement Blue**, le Router conduit le traffic vers l'environnement Blue.

Au déploiement d'une nouvelle version du produit :

1. La nouvelle version est déployée sur l'environnement Green.
2. L'équipe de développement peut tester la nouvelle application en allant sur un nom de domaine particulier ou en modifiant leur configuration DNS ou en mettant un flag dans un header par exemple...
3. Une fois que le déploiement est validé, **l'intégralité du traffic de production est conduit vers l'environnement Green** plutôt que l'environnement Blue.

Le traffic est donc toujours conduit vers un seul environnement.

En cas de rollback, il suffit de reconduire le traffic vers l'environnement précédent.

![Blue / Green Deployment by Cloud Foundry](../../.gitbook/assets/image%20%286%29.png)

## Feature Flags

Une fonctionnalité finalisée doit être **livrée en production** le plus rapidement possible même si **celle-ci ne doit pas encore être accessible aux utilisateurs**.

L'activation de la fonctionnalité pourra se faire par configuration via des **Feature Flags**.

{% hint style="success" %}
Les Feature Flags peuvent également servir à déployer progressivement une fonctionnalité sur une population d'utilisateurs _\(a.k.a. Canary Deployment\)._
{% endhint %}

{% hint style="warning" %}
Evitez les mécanisme de configuration de Feature Flags trop complexes !  
Le déploiement de configuration devient alors "error-prone" et plus délicat que le déploiement de code.
{% endhint %}

### Exemple

Sur Wishtack, nous avons implémenté la fonctionnalité permettant de **participer à une cagnotte** **avant** la fonctionnalité permettant **de récupérer la somme cumulée sur la cagnotte**.

Il n'était bien sûr pas envisageable d'activer la première fonctionnalité sans la deuxième pour le grand public par contre, chez Wishtack, nous pouvions déjà expérimenter la première fonctionnalité en production avec des vraies transactions.

