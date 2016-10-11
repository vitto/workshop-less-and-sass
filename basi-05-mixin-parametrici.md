# Mixin parametrici

## less

```less
.shadowed(@shadow-intensity: 0.1, @border-intensity: 0.05) {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, @border-intensity), 0 1px 3px rgba(0, 0, 0, @shadow-intensity);
}

.selector {
  background-color: white;
  .shadowed(0.15);
}
```

----

## sass

```scss
@mixin shadowed($shadow-intensity: 0.1, $border-intensity: 0.05) {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, $border-intensity), 0 1px 3px rgba(0, 0, 0, $shadow-intensity);
}

.selector {
  background-color: white;
  @include shadowed(0.15);
}
```

---

[Indice](README.md#lezioni)
