# avanzate

## nesting

##### combinator

```less
p, a, ul {
  border-top: 2px dotted #366;
  & + & {
    border-top: 0;
  }
}
```

##### order

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

---

[Indice](README.md#lezioni)
