# Bottom-up vs Top-down

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

