# Resource

A resource is an item defined by its URI. It can be a webpage, webstrate, local file or virtually any other form digital artefact. A resource should (as a minimum) contain the following properties:

 * `name` a friendly name (does not have to be unique)
 * `url` an url to the resource 


{% method %}
## Creating a resource

Creating a resource is is done in an HTTP POST request. A `name` and `url` (and token) are required. 

{% sample lang="bash" %}
A POST to `v1/resource` will create a new resource. 

```bash
$ curl -X POST .../v1/resource -d "{ 'name': 'My file', 'url': 'https://somewhere.com/somefile.txt' }"
{ 'name': 'My file', 'url': 'https://somewhere.com/somefile.txt', 'id': '0xfo1' }
```

{% endmethod %}

{% method %}
## Deleting a resource

Delete an existing resource with a DELETE request.

{% sample lang="bash" %}
DELETE to `v1/resource/<id>` will delete the given resource. 

```bash
$ curl -X DELETE .../v1/resource/0xfo1
```

{% endmethod %}


{% method %}
## Updating a resource

Updating a resource is is done in an HTTP PUT request. Supply `id` and `token` to update.

{% sample lang="bash" %}
A PUT to `v1/individual/<id>` will update the id'ed resource.

```bash
$ curl -X PUT .../v1/resouce/0xfo1 -d "{ 'name': 'Another file', }"
{ 'name': 'Another file', 'url': 'https://somewhere.com/somefile.txt', 'id': '0xfo1' }
```

{% endmethod %}


