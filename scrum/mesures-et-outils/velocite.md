# Vélocité

## Calcul de la vélocité

L'un des principaux intérêts des méthodes agiles est de pouvoir **évaluer l'avancement de la réalisation** d'un produit **pour mieux prévoir l'avenir**.

La vélocité d'un Sprint se calcule simplement en mesurant **le nombre de Story Points** réalisées lors de ce **Sprint**.

$$
vélocité = \sum(storypoints) / iterationCount
$$

## Workforce

Plus exactement, le calcul de la vélocité prend également en compte la notion de Workforce.

Lors de chaque Sprint, on évalue le Workforce qui est un pourcentage représentant la disponibilité de l'équipe.

$$
vélocité = \sum(iteration.storypoints / iteration.workforce) / iterationCount
$$

## Exemple de calcul de vélocité avec Workforce

Pour une équipe de développement de 5 personnes, si une personne est absente et qu'une autre travaille en parallèle à 50% sur un autre produit alors le Workforce sera de 85%.

A partir du calcul de vélocité et de Workforce des derniers Sprints _\(3 ou 4 généralement\)_, on prévoit la vélocité des itérations à venir ; ce qui permet de déduire les dates de livraison des User Stories à venir.

Sprint 1 : Workforce = 100%, Story Points = 14.

Sprint 2 : Workforce = 80%, Story Points = 8.

Sprint 3 : Workforce = 100%, Story Points = 12.

La vélocité des Sprints à venir sera estimée à :

$$
( 14 / 100\% + 8 / 80\% + 12 / 100\% ) / 3 = 12
$$

