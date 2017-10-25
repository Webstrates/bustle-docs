# Activities

The API for interacting with activities is defined below. The interface is RESTful most of the way.

The supported properties on activites are:

 * `name: String`
 * `start: Int` - unix epoch
 * `stop: Int`

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

Relate an existing activity to another entity is done with an HTTP PUT. The relation needs a type (or label), an origin and a destination. The origin and destination can only be of the types designated by the  The built-in relation-types are:

 * *activity* -- continues -> *activity* - the meaning here is that the activity is a continuation of a previous activity
 * *individual* -- participates -> *activity*
 * *activity* -- includes --> *resource*
 
 
Relations are one-way. This means that when activity A *continues* activity B then B **does not automatically** *continue* A. You can only create relations which originate in an activity on an activity.

{% sample lang="bash" %}
A simple PUT to `v1/activity/<id>` with some JSON body content will update the activity.


```bash
curl -X PUT .../v1/activity/0xab6/--continues->/0xab5
```

Or the short-hand version.

```bash
curl -X PUT .../v1/activity/0xab6/c/0xab5
```

For a complete list of relations see the [Relations](content/relations.html) section.

{% endmethod %}


## Finding activities

The query methods described here take their outset in the [query language](content/query-language/bustle-query-language.html) but adds a easier-to-use API layer for frequently used queries.



### By participation of individuals

Find activities participated by certain individuals.

{% method %}
#### Any

Find activities in which any of the given participants have participated in. The union of all their activities in other words.

{% sample lang="bash" %}

```bash
curl -X POST .../v1/find/activity/participant/any -d "{ 'participants': ['0xfo0'] }"
```

{% endmethod %}

{% method %}
#### All

Find activities in which all the given participants have participated in. The shared set of all their activities in other words.

{% sample lang="bash" %}
```bash
curl -X POST .../v1/find/activity/participant/all -d "{ 'participants': ['0xfo0'] }"
```

{% endmethod %}

### By time

Find activities occurring within a given time-frame.

{% method %}
#### After

All activities occurring after the given time.

{% sample lang="bash" %}
```bash
curl -X POST .../v1/find/activity/participant/all -d "{ 'participants': ['0xfo0'] }"
```




{% endmethod %}

{% method %}
### By related activities

{% endmethod %}

{% method %}
### By relation

{% endmethod %}