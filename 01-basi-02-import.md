# Import

## less

```less
@import 'a-less-file.less';
@import 'as-less-file';
@import 'as-less-file.php';
@import 'as-css-file.css';
@import (optional) 'if-not-found-will-skip-errors.less';
@import (reference) 'will-be-not-included-in-css.less';
```

----

## sass

```scss
@import 'a-scss-file';
@import 'widget-01', 'widget-02';
```

##### nested imports

```scss
// file-to-import.scss
.example {
  color: red;
}

// another file
#main {
  @import 'file-to-import';
}
``

---

[Indice](README.md#lezioni)
