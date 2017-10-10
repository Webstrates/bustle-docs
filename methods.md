# Activities

The API for interacting with activities is defined below. The interface is RESTful most of the way.

{% method %}
## Creating an activity

Creating an activity is is done in an HTTP POST request. A `name` is the only required property for creating an activity. 

{% sample lang="bash" %}
A simple POST to `v1/activity` will create a new activity. The newly created activity will contain an id.

```bash
$ curl -X POST .../v1/activity -d "{ 'name': 'My Activity'}"
{ 'name': 'My activity', 'id': '0xab6' }
```

{% endmethod %}

{% method %}
## Deleting

Delete an activity via an HTTP DELETE.

{% sample lang="bash" %}
A simple DELETE to `v1/activity/<id>` will delete the activity with id `<id>`.


```bash
curl -X DELETE .../v1/activity/0xab6
```

{% endmethod %}

{% method %}
## Updating

Update an activity via an HTTP PUT.

{% sample lang="bash" %}
A simple PUT to `v1/activity/<id>` with some JSON body content will update the activity.


```bash
curl -X PUT .../v1/activity/0xab6 -d "{ 'start': 1507626697 }"
```

{% endmethod %}

{% method %}
## Relating an activity

Update an activity via an HTTP PUT.

{% sample lang="bash" %}
A simple PUT to `v1/activity/<id>` with some JSON body content will update the activity.


```bash
curl -X PUT .../v1/activity/0xab6 -d "{ 'start': 1507626697 }"
```

{% endmethod %}



















