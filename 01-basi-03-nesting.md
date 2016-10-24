# nesting

## less

```less
.widget {
  background-color: white;
  a {
    display: block;
  }
}
```

#### parent

```less
.widget {
  background-color: white;
  &:hover {
    background-color: yellow;
  }
}
```

----

## sass

```scss
.widget {
  background-color: white;
  a {
    display: block;
  }
}
```

#### parent

```less
.widget {
  background-color: white;
  &:hover {
    background-color: yellow;
  }
}
```
---

[Indice](README.md#lezioni)
