# Transformation Etape par Etape

## Choix des Paramètres

### Durée des Itérations

Il faut d'abord définir la **durée des itérations** et **le jour de la semaine où chaque itération démarre**.

En général, il **est préférable d'opter pour la durée la plus courte** _\(une semaine\)_ pour les raisons suivantes :

* plus de transparence et réduction de l'effet tunnel,
* **feedback plus fréquent** du client,
* possibilité de **pivoter** et rectifier le tir plus **rapidement et fréquemment**,
* **favorisation d'un rythme régulier et durable** en évitant les coups de stress en fin d'itération,
* **calcul plus précis de la vélocité** et projection plus précise _\(e.g. : avec des itérations de 3 semaines, il faut attendre plus de 2 mois avant d'avoir la vélocité moyenne sur les 3 dernières itérations\)_,
* **si un membre de l'équipe rate un événement, cela devient problématique** car le prochain événement aura lieu dans plusieurs semaines,
* il est plus facile de **coordonner des équipes** qui démarrent **une nouvelle itération chaque lundi**. Autrement, les itérations s'enchevêtrent.

Si vous avez besoin d'itérations plus longues, posez-vous d'abord les questions suivantes :

* si vous constatez une volatilité importante de la vélocité ou effet tunnel _\(i.e. :  des itérations ne produisant aucune valeur suivies d'itérations produisant un nombre important de points\)_, est-ce possible de **découper les User Stories encore plus finement** ?
* est-ce possible de **réduire le** [**Work-In-Progress Limit**](kanban/workflow.md#work-in-progress-limit) ?
* si certains événements prennent trop de temps, est-ce que le Definition of Ready est bien respecté ? Est-ce possible d'améliorer le Collective Ownership pour raccourcir les discussions ?

{% hint style="warning" %}
**Des itérations plus longues nécessitent plus de préparation** et des [Sprint Planning](scrum/evenements/sprint-planning.md) plus longs. Si lors du [Spring Planning](scrum/evenements/sprint-planning.md), vous ne préparez qu'une partie de l'itération en attendant le prochain [Backlog Refinement](scrum/evenements/backlog-refinement.md), vous êtes peut-être en train de créer une itération au sein de l'itération 😉
{% endhint %}

### Échelle de Points _\(ou Point Scale\)_

Il est nécessaire de sélectionner un _Point Scale_ pour évaluer l'[effort](scrum/mesures-et-outils/story-points-vs-temps.md) nécessaire pour chaque [User Story](scrum/artefacts/user-story.md).

Nous vous recommandons les échelles :

* **1, 2, 3 & 8**
* ou **1, 3, 5 & 15**.

où la dernière valeur sert à estimer les [User Stories](scrum/artefacts/user-story.md) qui nécessiteront d'être découpées ultérieurement. **On ne démarre donc pas le développement d'une** [**User Story**](scrum/artefacts/user-story.md) **à 8 ou 15 points.**

Nous préférons ces échelles pour les raisons suivantes :

* en réduisant le nombre de valeurs possibles, vous réduisez également l'hésitation et la durée des [Spring Planning](scrum/evenements/sprint-planning.md) et [Backlog Refinement](scrum/evenements/backlog-refinement.md),
* ces échelles encouragent le découpage des [User Stories](scrum/artefacts/user-story.md), 
* l'échelle **S, M, L & XL** est également intéressante mais il faut reconvertir en points pour calculer la vélocité et la projection.

{% hint style="info" %}
**Astuce :**  dans le cas de planification moyen ou long terme, n'hésitez pas à **réduire  l'échelle** _\(e.g. : 1, 3 & 8\)_ afin d'**accélérer le temps d'estimation** en sacrifiant légèrement la précision qui sera probablement erronée dans tous les cas.
{% endhint %}

### Work-In-Progress Limit

Définir un [WIP limit](kanban/workflow.md#work-in-progress-limit) relativement bas encourage naturellement le Collective Ownership, le Pair Programming et favorise la communication.

A vous d'expérimenter, mesurer et trouver le WIP limit qui vous convient mais la formule suivante est généralement un bon point de départ :

$$
wiplimit = floor(teamsize / 2)
$$

## Definition of Done

L'équipe doit définir **son propre** [**Definition of Done**](scrum/artefacts/definition-of-done.md) puis l'**enrichir en fonction de son expérience** et ses erreurs.

## Definition of Ready

De même que pour le [Definition of Done](scrum/artefacts/definition-of-done.md), l'équipe doit définir et maintenir son [Definition of Ready](scrum/artefacts/definition-of-ready.md).

## Préparation de la Première Itération

### Premières _User Stories_

Définissez les premières [User Stories](scrum/artefacts/user-story.md) conformément au [Definition of Ready](scrum/artefacts/definition-of-ready.md) ; lors d'une session de [User Story Mapping](priorisation-and-planning/user-story-mapping.md) par exemple.

### Choix des Technologies et Outils _\(si applicable\)_

Si vous devez choisir les technologies et outils à utiliser, focalisez-vous sur la simplicité, la maintenabilité et la facilité de changer plus tard.

Pensez à vous faire accompagner dans ce choix.

### Recrutement _\(si applicable\)_

Recrutez progressivement !

Une **rencontre avec l'intégralité de l'équipe** pourrait être l'avant dernière étape de recrutement ; la dernière étant **une semaine d'essai au sein de l'équipe**.

### Indicateurs

Pensez à choisir et mesurer vos [indicateurs](indicateurs.md) avant de démarrer !

## Rencontre Directe avec le Client et les Utilisateurs

### **Pas d'Intermédiaires**

Le _Product Owner_ ne doit pas être un intermédiaire entre l'équipe et le client.

Généralement, il faut éviter les intermédiaires car inconsciemment **l'information sera toujours déformée et filtrée.**

Il est donc important que l'intégralité de l'équipe et le client puissent échanger au moins lors du [Sprint Review](scrum/evenements/sprint-review.md).

Faites tout de même **attention aux clients envahissants** !

### **Rencontrez vos Utilisateurs !**

Organiser des rencontres et échanges directs entre une sélection d'utilisateurs finaux et l'équipe permet de démystifier de nombreux aspects concernant l'utilisation du produit.

La rencontre fournit donc un indicateur qualitatif supplémentaire.

## Sprint Review

Organisez des [Sprint Review](scrum/evenements/sprint-review.md) même en l'absence du client et **invitez d'autres équipes** ou les curieux.

Certaines entreprises affichent les horaires de [Sprint Review](scrum/evenements/sprint-review.md) des différentes équipes dans leurs couloirs.

## Transparence et Propagation

Soyez transparents et sincères !

Expliquez votre approche avec les autres équipes et partagez votre expérience !

