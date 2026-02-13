# Popular Dictionary Methods

## Creating Dictionary

```
d = {1: 'a', 2: 'b'}
```

Using zip:

```
d = dict(zip(keys, values))
```

## Access

```
d[key]
d.get(key)
```

## Add / Update

```
d['new'] = value
```

## Delete

```
del d[key]
```

## Methods

| Method   | Description      |
| -------- | ---------------- |
| keys()   | All keys         |
| values() | All values       |
| items()  | Key-value pairs  |
| get()    | Safe access      |
| pop(key) | Remove key       |
| update() | Merge dictionary |
| clear()  | Remove all       |

## Loop

```
for k, v in d.items():
    print(k, v)
```

Dictionaries are **mutable** and keys must be unique.
