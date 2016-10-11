# less avanzato

## mixin

### pattern matching mixins

```less
.mixin(dark; @color) {
  color: darken(@color, 10%);
}
.mixin(light; @color) {
  color: lighten(@color, 10%);
}
.mixin(@_; @color) {
  display: block;
}

.selector {
  .mixin(dark, #4e4eee);
}
```

### mixin condizionali

```less
.mixin (@a) when (lightness(@a) >= 50%) {
  background-color: black;
}
.mixin (@a) when (lightness(@a) < 50%) {
  background-color: white;
}
.mixin (@a) when not (@a = #fff) {
  border-color: white;
}

.mixin (@a) when (iscolor(@a)) {
  /* is a color */
}
.mixin (@a) {
  color: @a;
}

.selector {
  .mixin(#4e4eee);
}
```

## mixin come funzione

##### variabili condivise

```less
.mixin() {
  @width:  100%;
  @height: 200px;
}

.caller {
  .mixin();
  width:  @width;
  height: @height;
}
```

##### mixin condivisi

```less
.unlock(@value) { // outer mixin
  .doSomething() { // nested mixin
    declaration: @value;
  }
}

#namespace {
  .unlock(5); // unlock doSomething mixin
  .doSomething(); //nested mixin was copied here and is usable
}
```


## rulesets

```less
.desktop-and-old-ie(@rules) {
  @media screen and (min-width: 1200px) {
    @rules();
  }
  html.lt-ie9 & {
    @rules();
  }
}

header {
  background-color: blue;

  .desktop-and-old-ie({
    background-color: red;
  });
}
```

##### var scoping

```less
@detached-ruleset: {
  caller-variable: @caller-variable; // variable is undefined here
  .caller-mixin(); // mixin is undefined here
};

.selector {
  // use detached ruleset
  @detached-ruleset();

  // define variable and mixin needed inside the detached ruleset
  @caller-variable: value;
  .caller-mixin() {
    variable: declaration;
  }
}
```

---

[Indice](README.md#lezioni)
