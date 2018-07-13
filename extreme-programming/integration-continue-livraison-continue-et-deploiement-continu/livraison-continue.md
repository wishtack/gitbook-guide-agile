# Livraison Continue

En plus de tout ce que l'[intégration continue](integration-continue.md) propose, la **livraison continue** ajoute une dernière étape au process permettant aux parties prenantes autorisées de **déployer** la dernière version **en production par simple clic** mais également de **rollback** à la version précédente en cas de problème.

En plus de cette fonctionnalité, la livraison continue **implique surtout une façon de concevoir et de développer** les produits respectant les règles suivantes :

* Le code de l'environnement d'intégration doit fonctionner en production.
* L'intégralité du déploiement doit se faire automatiquement _\(y compris les migrations de base de données par exemple\)_.
* Le déploiement ne doit pas causer d'interruption de service.

![Continuous Delivery](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LHD4wSD1i9v5yCa767m%2F-LHJ4GPYKCKTQ1Xvm1al%2F-LHJDAedZr6u4V5h5w3U%2Fcontinuous-delivery.png?alt=media&token=70ff30f6-1a89-498c-a723-569d98ed7934)



_Several benefits of continuous delivery have been reported._

* _Accelerated Time to Market: CD lets an organization deliver the business value inherent in new software releases to customers more quickly. This capability helps the company stay a step ahead of the competition._
* _Building the Right Product: Frequent releases let the application development teams obtain user feedback more quickly. This lets them work on only the useful features. If they find that a feature isn’t useful, they spend no further effort on it. This helps them build the right product._
* _Improved Productivity and Efficiency: Significant time savings for developers, testers, operations engineers, etc. through automation._
* _Reliable Releases: The risks associated with a release have significantly decreased, and the release process has become more reliable. With CD, the deployment process and scripts are tested repeatedly before deployment to production. So, most errors in the deployment process and scripts have already been discovered. With more frequent releases, the number of code changes in each release decreases. This makes finding and fixing any problems that do occur easier, reducing the time in which they have an impact._
* _Improved Product Quality: The number of open bugs and production incidents has decreased significantly._
* _Improved Customer Satisfaction: A higher level of customer satisfaction is achieved._

_Obstacles have also been investigated._

* _Customer preferences: Some customers do not want continuous updates to their systems. This is especially true at the critical stages in their operations._
* _Domain restrictions: In some domains, such as telecom and medical, regulations require extensive testing before new versions are allowed to enter the operations phase._
* _Lack of test automation: Lack of test automation leads to lack developer confidence and can prevent using continuous delivery._
* _Differences in environments: Different environments used in development, testing and production can result in undetected issues slipping to the production environment._
* _Tests needing a human oracle: Not all quality attributes can be verified with automation. These attributes require humans in the loop, slowing down the delivery pipeline._

