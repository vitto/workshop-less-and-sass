# avanzate

## variable interpolation

##### less

```less
.status-message(@modifier, @color) {
  &--@{modifier} {
    color: darken(@color, 30%);
    background-color: @color;
  }
}
.message {
  display: block;
  border-radius: 4px;
  .status-message(info, rgb(62, 184, 205));
  .status-message(success, rgb(114, 184, 89));
  .status-message(warning, rgb(223, 181, 32));
  .status-message(error, rgb(205, 92, 62));
}
```

---

##### sass

```scss
@mixin status-message($modifier, $color) {
  &--#{$modifier} {
    color: darken($color, 30%);
    background-color: $color;
  }
}
.message {
  display: block;
  border-radius: 4px;
  @include status-message('info', rgb(62, 184, 205));
  @include status-message('success', rgb(114, 184, 89));
  @include status-message('warning', rgb(223, 181, 32));
  @include status-message('error', rgb(205, 92, 62));
}

```

---

[Indice](README.md#lezioni)
