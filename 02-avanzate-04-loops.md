# avanzate

## generate a column set

##### less

```less
.generate-columns(@n, @i: 1) when (@i =< @n) {
  .column-@{i} {
    width: (@i * 100% / @n);
  }
  .generate-columns(@n, (@i + 1));
}

.generate-columns(6);
```

##### sass

```sass
@mixin generate-columns($columns) {
  $i: 1;
  @while $i <= $columns {
    .column-#{$i} {
      width: ($i * 100% / $columns);
    }
    $i: $i + 1;
  }
}

@include generate-columns(6);
```

---

[Indice](README.md#lezioni)
