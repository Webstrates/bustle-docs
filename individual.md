# Individual

An individual represents an entity which can actively participate in an activity. This can be a physical person but also a virtual assistant (e.g. a golem).

Supported properties on *individual* entities are:

* `name [String]`
* `email [String]`

{% method %}
## Creating an individual

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
A DELETE to `v1/individual/<id>` will delete and return the deleted individual.

```bash
$ curl -X DELETE .../v1/individual/0xfo1
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


{% method %}
## Finding an individual

Finding an individual can be done by querying for the values of properties or by 

{% sample lang="bash" %}
POST to `v1/find/individual/by` to do property value matches.

```bash
$ curl -X POST .../v1/find/individual/by -d "{ 'name': 'John .*', }"
[{ 'name': 'John Doe Sr', 'id': '0xfo1' }]
```

{% endmethod %}















