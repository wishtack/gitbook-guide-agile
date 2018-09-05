# Exemple de Régression Naturelle

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



