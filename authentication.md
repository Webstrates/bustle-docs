# Authentication

Authentication for all endpoints are done by including a token in either the header or as a query parameter.

{% method %}
{% sample lang="bash" %}
Provide the token in the header:

```bash
$ curl -X POST -H "Authorization : Bearer <token>" ...
```

Or in a query parameter:

```bash
$ curl -X POST "...?token=<token>"
```
{% endmethod %}



