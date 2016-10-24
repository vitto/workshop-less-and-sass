# less avanzato

## functions

##### image properties `node only`

Concatenare parametri divisi da **virgole** nelle singole regole

```less
.icon {
  @icon: 'icon.png';
  @size: image-size(@icon); // 32px 32px
  background-image: url(@icon);
  background-size: @size;
  height: image-height(@icon); // 32px
  width: image-width(@icon); // 32px
}
```

will output

```css
.icon {
  background-image: url('icon.png');
  background-size: 32px 32px;
  height: 32px;
  width: 32px;
}
```

---

##### data-uri `node only`

```less
.icon {
  background-image: data-uri('../data/image.jpg');
}

.icon-2 {
  background-image: data-uri('image/svg+xml;charset=UTF-8', 'image.svg');
}
```

will output

```css
.icon {
  background-image: url('data:image/jpeg;base64,bm90IGFjdHVhbGx5IGEganBlZyBmaWxlCg==');
}

.icon-2 {
  background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%3E%3Ccircle%20r%3D%229%22%2F%3E%3C%2Fsvg%3E");
}
```

---

##### convert

```less
.selector {
  width: convert(14cm, mm);
}
```

---

##### default

```less
.mixin (@value) when (ispixel(@value)) {
  width: @value;
}
.mixin (@value) when (default()) {
  height: @value;
}
.selector {
  .mixin(1em);
}
```

---

##### unit

```less
.selector {
  width: unit(4em, %) * 10;
}
```

---

##### get-unit

```less
.mixin (@value) when (get-unit(@value) = px) {
  width: @value;
}
.mixin (@value) when (get-unit(@value) = em) {
  height: @value;
}
.selector {
  .mixin(4em);
}
```

---

È possibile leggere tutte le funzioni disponibili su [LESS qui](less-functions).

[less-functions]: (http://lesscss.org/functions/#functions-overview)
[Indice](README.md#lezioni)
