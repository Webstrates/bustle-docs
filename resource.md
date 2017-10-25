# Resource

A resource is an item defined by its URI. It can be a webpage, webstrate, local file or virtually any other form digital artefact.

{% method %}
## Creating resource

Creating an individual is is done in an HTTP POST request. A `name` and `email` are required for creating an individual. 

{% sample lang="bash" %}
A simple POST to `v1/individual` will create a new individual. The newly created indvidual will contain an id.

```bash
$ curl -X POST .../v1/individual -d "{ 'name': 'John Doe', }"
{ 'name': 'John Doe', 'id': '0xfo1' }
```

{% endmethod %}

{% method %}
## Deleting an individual

Creating an individual is is done in an HTTP DELETE request. Supply `id` and `token` to delete.

{% sample lang="bash" %}
A simple POST to `v1/individual` will create a new individual. The newly created indvidual will contain an id.

```bash
$ curl -X POST .../v1/individual -d "{ 'name': 'John Doe', }"
{ 'name': 'John Doe', 'id': '0xfo1' }
```

{% endmethod %}


{% method %}
## Updating an individual

Updating an individual is is done in an HTTP PUT request. Supply `id` and `token` to update.

{% sample lang="bash" %}
A simple PUT to `v1/individual/<id>` will update the id'ed individual.

```bash
$ curl -X PUT .../v1/individual/0xfo1 -d "{ 'name': 'John Doe Sr', }"
{ 'name': 'John Doe Sr', 'id': '0xfo1' }
```

{% endmethod %}


