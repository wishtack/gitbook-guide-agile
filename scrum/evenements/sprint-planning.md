# Sprint Planning

Chaque Sprint démarre avec un Sprint Planning lors duquel la Scrum Team doit définir :

* **what** : l'objectif du Sprint ou Spring Goal,
* **how** : puis comment atteindre cet objectif.

{% hint style="info" %}
Le Spring Planning **peut être divisé en deux parties** : Sprint Planning 1 et 2.
{% endhint %}

{% hint style="warning" %}
La durée maximum du Sprint Planning est de 2h pour un Sprint d'une semaine.
{% endhint %}

## What : Sprint Planning 1 et définition du Sprint Goal

La Scrum Team se réunit en entier _\(Product Owner, Development Team et Scrum Master\)_ pour définir le Sprint Goal.

1. Le Product Owner **décrit les User Stories** qu'il souhaiterait assigner au Sprint.
2. La Development Team **peut interroger le Product Owner** pour mieux comprendre le besoin.
3. Si une User Story est de taille importante, il s'agit alors d'une Epic et la Scrum Team peut alors décider de la décomposer en User Stories plus fines.
4. La Development Team **évalue** et **sélectionne** **à elle seule** les User Stories qu'elle **pense être capable de finir** d'ici la fin du Sprint.

{% hint style="info" %}
Pour optimiser le Sprint Planning en respectant le Timeboxing, pensez à dérouler ces étapes story par story.  
Ainsi, en cas de "timeout", l'équipe pourra commencer à travailler sur les premières stories.  
Si l'équipe accomplit sa mission avant la fin de l'itération, on pourra alors planifier un Backlog Refinement pour ajouter de nouvelles stories à l'itération.
{% endhint %}

### Décomposition des Epics

Durant le Sprint Planning, **les Epics seront décomposées** en User Stories plus fines.

## How : Sprint Planning 2

Suite au Sprint Planning 1, la Scrum Team peut libérer le Product Owner.

1. La Development Team **réfléchit et présente la conception / architecture / design de chaque User Story**. Cela peut se faire avec toute l'équipe ou par paire afin de paralléliser la reflexion si cela est vraiment nécessaire. Dans ce cas, la paire doit présenter le résultat de sa reflexion au reste de l'équipe.
2. Chaque User Story est ensuite **décomposée en tâches** techniques.
3. L' effort nécessaire pour chaque User Story **est ensuite estimé en points** par la Development Team.
4. Les membres de la Development Team doivent ensuite **se répartir naturellement** ces tâches.

{% hint style="danger" %}
Personne _\(ni le Product Owner, ni le Scrum Master, ni le Lead Super Hero Team Scrum Manager\)_ n'assigne les tâches aux membres de la Development Team.
{% endhint %}

{% hint style="warning" %}
L' effort nécessaire pour chacune des stories peut être estimé en heures mais il est préférable d'utiliser des points.
{% endhint %}

### Estimation de l'Effort

L' **effort** nécessaire pour réaliser chaque User Story est évalué avec un nombre de **points** suivant généralement une suite de Fibonacci _\(1, 2, 3, 5, 8 du plus simple au plus complexe\)_.  
En pratique, les valeurs 1, 2 et 3 suffisent et encouragent un découpage plus fin.

### Planning Poker

Pour encourager tous les membres de la Development Team à participer à l'estimation de l'effort associé aux User Stories, l'équipe peut utiliser un jeu de cartes grâce auquel chacun réfléchit à son estimation puis tout le monde dévoile sa carte simultanément.

### Répartition des Tâches

De nombreuses équipes ont le réflexe d'associer chaque tâche à l'expert du sujet.

Bien que cette approche puisse paraitre optimale, cela :

* décourage le partage de connaissances au sein de l'équipe,
* encourage le travail individuel plutôt que l'appropriation du produit par l'équipe,
* crée une dépendance forte envers certaines personnes dans l'équipe,
* n'encourage pas la remise en question et aboutit souvent à de la complexité artificielle.

{% hint style="warning" %}
Le code le moins maintenable est souvent produits par les experts et non les débutants.

Méfiez-vous des Lead Developers !
{% endhint %}

