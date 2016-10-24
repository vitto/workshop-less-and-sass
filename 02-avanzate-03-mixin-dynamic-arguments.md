# avanzate

## mixin dynamic arguments

##### less

```less
.box-shadow(@x: 0; @y: 0; @blur: 1px; @color: #000) {
    -webkit-box-shadow: @arguments;
    -moz-box-shadow: @arguments;
    -ms-box-shadow: @arguments;
    -o-box-shadow: @arguments;
    box-shadow: @arguments;
}
.box {
  .box-shadow(2px; 5px);
}
```

---

##### sass

```scss
@mixin box-shadow($params...) {
  -webkit-box-shadow: $params;
  -moz-box-shadow: $params;
  -ms-box-shadow: $params;
  -o-box-shadow: $params;
  box-shadow: $params;
}
.box {
  @include box-shadow(1px 1px 2px rgba(0, 0, 0, 0.3), inset 0 0 1px rgba(0, 0, 0, 0.6));
}
```

---

[Indice](README.md#lezioni)
