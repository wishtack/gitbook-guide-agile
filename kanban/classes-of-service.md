# Classes of Service

Dans la plupart des organisations, tous les éléments n'ont pas la même **notion de priorité ou d'échéance**.

Les éléments **ne peuvent donc pas être traitées de façon homogène** ; il faut appliquer **des contraintes de Workflow différentes** par catégorie d'éléments.

Les Classes of Service permettent de catégoriser les éléments afin de refléter la **priorisation en fonction des risques et de la valeur de l'élément.**

## Standard Class of Service

Cette classe regroupe les éléments qui ne sont pas associés aux classes décrites ci-dessous.

Après priorisation, ces éléments sont traités avec une approche "FIFO" _\(First In / First Out\)_.

## Expedite Class of Service

Cette classe est attribuée aux **éléments prioritaires**.

{% hint style="success" %}
Pour éviter de perturber l'avancement général du Workflow, il est recommandé d'**attribuer une limite de Work-In-Progress spécifique** pour les éléments de cette classe.
{% endhint %}

{% hint style="danger" %}
Un **nombre important d'éléments** dans cette classe révèle un **manque de confiance** en la capacité de livraison.
{% endhint %}

## Fixed Delivery Date Class of Service

Cette classe est attribuée aux éléments devant être **livrés à une date spécifique**.

Les éléments de cette classe doivent être mis dans la file Work-In-Progress **suffisamment en avance pour respecter l'échéance**.

{% hint style="success" %}
Les éléments de cette classe doivent avoir une **date d'échéance définie par une contrainte extérieure** _\(e.g. : mise en conformité, migration ou compatibilité technique...\)_.  
Autrement, le Kanban serait utilisé comme un diagramme de Gantt.
{% endhint %}

## Intangible Class of Service

Cette classe est attribuée aux éléments dont il est **difficile d'évaluer la valeur apportée à l'utilisateur** _\(bug fixes, chores, optimisations, changement de design, etc...\)_.

Cette classe a **la priorité la plus basse**.

