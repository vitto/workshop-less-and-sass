# Annidamento

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

#### combinator

```less
p, a, ul {
  border-top: 2px dotted #366;
  & + & {
    border-top: 0;
  }
}
```

#### order `less`

```less
.header {
  .menu {
    border-radius: 5px;
    .no-border-radius & {
      background-image: url('images/button-background.png');
    }
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
