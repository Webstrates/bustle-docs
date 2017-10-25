# Tags

A tag is a simple textual label which can be referenced/related by arbitrary items. It can contain any number of properties.


{% method %}
## Creating a tag

Creating a tag is is done in an HTTP POST request. 

{% sample lang="bash" %}
A POST to `v1/tag` will create a new resource. 

```bash
$ curl -X POST .../v1/tag -d "{ 'name': 'My tag' }"
{ 'name': 'My tag', 'id': '0xfo1' }
```

{% endmethod %}

{% method %}
## Deleting a tag

Delete an existing tag with a DELETE request.

{% sample lang="bash" %}
DELETE to `v1/tag/<id>` will delete the given tag. 

```bash
$ curl -X DELETE .../v1/tag/0xfo1
```

{% endmethod %}


{% method %}
## Updating a tag

Updating a resource is is done in an HTTP PUT request. Supply `id` and `token` to update.

{% sample lang="bash" %}
A PUT to `v1/tag/<id>` will update the id'ed tag.

```bash
$ curl -X PUT .../v1/tag/0xfo1 -d "{ 'name': 'Another tag', }"
{ 'name': 'Anotheagr t', 'id': '0xfo1' }
```

{% endmethod %}


