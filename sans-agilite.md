# Sans Agilité

## "Cycle" en racine carrée

### Le client exprime son besoin

> Je veux une application mobile pour un réseau social avec du rouge en couleur dominante. Rendez-vous dans 6 mois.

... ou avec un cahier des charges.

### 3 mois plus tard...

* Retards.
* Client déçu par la version beta.
* Trop tard pour tout remettre en question.
* Tensions avec le client et au sein de l'équipe.
* Le "lead developer" quitte l'entreprise.
* 3 nouveaux développeurs rejoignent l'équipe en renfort.
* Le renfort ralentit encore plus l'équipe.

![Cycle en racine carr&#xE9;e de Michel ARBOI](.gitbook/assets/image%20%285%29.png)

## Coût du changement

Avec le cycle en V, le coût du changement augmente au fil du temps à travers le Software Development Life Cycle.

Il est donc plus difficile et plus cher de remédier à une erreur de conception à la livraison qu'au début des développements.

De même, sans méthode de développement, plus le développement avance, plus le code devient complexe et plus le changement est couteux.



![Cost of change](.gitbook/assets/cost-of-change.gif)

## Conséquences techniques

* Peur du changement.
* Développement empirique.
* Complexité artificielle \(i.e. : développement inutile ou inutilisable\).
* L'équipe est débordée par la correction de bugs.
  * La correction d'un bug en provoque un autre.

## Conséquences organisationnelles

* Dé-responsabilisation des développeurs.
* Problèmes de priorisation des tâches.
* Plusieurs personnes qui réimplementent la même fonctionnalité.
* Le "deadlock" humain.

## Bottom-up vs Top-down

### Bottom-up 

La tradition académique veut que l'on conçoive et que l'on développe les applications de bas en haut.

1. On développe une couche générique. 
2. On essaie de répondre à tous les besoins que l'on peut imaginer et qui finissent souvent par être surréalistes.
3. On perd donc beaucoup de temps pour du développement superflu.
4. On se retrouve avec une interface inutilisable.

```python
SocialNetworkMessage(
    recipient_group_list=[
        RecipientGroup(
            can_edit=False,
            can_reply=False,
            is_anonymous=False,
            private=True,
            recipient_list=[user1, user2]
        ),
        RecipientGroup(
            can_edit=True,
            can_reply=True,
            is_anonymous=True,
            private=False,
            recipient_list=[user3, user4]
        )
    ],
    is_embeddable=False,
    message_expiration=datetime(2025, 10, 1),
    show_thumbnail=True,
    ...
)
```

... ou sans named parameters

```python
SocialNetworkMessage(
    [
        RecipientGroup(
            False,
            False,
            False,
            True,
            [user1, user2]
        ),
        RecipientGroup(
            True,
            True,
            True,
            False,
            [user3, user4]
        )
    ],
    False,
    datetime(2025, 10, 1),
    True,
    ...
)
```

{% hint style="danger" %}
Attention à l'"Over-Thinking"
{% endhint %}

### Top-down

Dans le bâtiment, il n'est pas évident de construire des escaliers de haut en bas mais dans l'univers virtuel du développement, on peut.

Peu importe le point de départ de l'escalier, ce qui compte est que celui-ci arrive au 1er étage. Dans ce cas, il est préférable de commencer par le point d'arrivée c'est à dire l'étage; ainsi nous sommes sûrs que l'escalier arrivera bien au bon niveau et non quelques centimètres plus bas ou plus haut car nous avons oublié de prendre en compte l'épaisseur du carrelage.

L'approche **top-down** permet de garantir que le développement répond au besoin et uniquement au besoin, évitant ainsi le développement superflu.

## La régression naturelle et l'approche Code & Fix

{% tabs %}
{% tab title="Day 1" %}
```python
class User:

    def message_list():
        return DataSource().message_list(user_id=self.id)
```
{% endtab %}

{% tab title="Day 2" %}
```python
class User:

    def message_list():

        if os.environ.ENV == "stage":
            data_source = DataSource(host="10.45.23.10")
        else:
            data_source = DataSource()

        return data_source.message_list(user_id=self.id)
```
{% endtab %}

{% tab title="Day 3" %}
```python
class User:

    def message_list():

        if os.environ.ENV in ["stage", "STAYGE"]:
            data_source = DataSource(host="10.45.23.10")
        else if int(os.environ.HOST_NAME[-1]) % 2:
            data_source = DataSource(host="10.33.35.15")
        else:
            data_source = DataSource()

        return data_source.message_list(user_id=self.id)
```
{% endtab %}

{% tab title="Day 4" %}
```python
class User:

    def message_list():

        if os.environ.ENV in ["stage", "STAYGE"]:
            data_source = DataSource(host="10.45.23.10")
        else if os.environ.HOST_NAME[-1] % 2:
            data_source = DataSource(host="10.33.35.15")
        else:
            data_source = DataSource()

        if self.id.startswith("xft"):
            if self.country == "FR":
                if self.partner_id.startswith("RT")
                    self.xrb = 43
            else:
                self.xbe = 56

        return data_source.message_list(user_id=self.id, xrb=self.xrb, xbe=self.xbe)
```
{% endtab %}
{% endtabs %}

