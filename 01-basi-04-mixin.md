# mixin

## less

```less
.shadowed {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.selector {
  background-color: white;
  .shadowed;
}
```

#### mixin parametrico

```less
.shadowed() {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.selector {
  background-color: white;
  .shadowed;
}
```

----

## sass

```scss
@mixin shadowed {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.selector {
  background-color: white;
  @include shadowed;
}
```

#### Selettori estesi

```scss
.shadowed {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.selector {
  background-color: white;
  @extend .shadowed;
}
```

#### Selettori placeholder

```scss
%shadowed {
  box-shadow: 0 0 0 1px rgba(0, 0, 0, 0.05), 0 1px 3px rgba(0, 0, 0, 0.1);
}

.selector {
  background-color: white;
  @extend %shadowed;
}
```

---

[Indice](README.md#lezioni)
