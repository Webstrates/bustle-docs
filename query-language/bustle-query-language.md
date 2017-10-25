# Bustle Query Language

## Activity examples

```
A = '1' AND -hastag->{name = 'MyTag'}
```

```
A = '1' AND <-participates-[{name = 'Some individual name'},{name = 'Some other dude'}]
```

```
A = '1' AND <-participates-['Some individual name', 'Some other dude']
```


```
start >= 12312312 AND <-participates-['Some individual name', 'Some other dude']
```

Indicate that we want to follow the *continiues* relation a variable number of steps. TODO - can this be done?

```
A = '1' AND -continues*->{name = 'MyTag'}
```





