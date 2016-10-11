# Variabili

## less

```less
@nice-white: #FFC;
@nice-blue: #5B83AD + #111;

.selector {
  color: @nice-blue;
}

.selector--second {
  background-color: @nice-blue;
  color: @nice-white;
}
```

----

## sass

```scss
$nice-white: #FFC;
$nice-blue: #5B83AD + #111;

.selector {
  color: $nice-blue;
}

.selector--second {
  background-color: $nice-blue;
  color: $nice-white;
}
```

---

## css

```css
:root {
  --nice-white: #FFC;
  --nice-blue: #6C94BE;
}

.selector {
  color: var(--nice-blue);
}

.selector--second {
  background-color: var(--nice-blue);
  color: var(--nice-white);
}
```

---

[Indice](README.md#lezioni)