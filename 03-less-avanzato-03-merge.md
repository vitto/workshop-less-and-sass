# less avanzato

## merge

##### virgole

Concatenare parametri divisi da **virgole** nelle singole regole

```less
.mixin() {
  box-shadow+: inset 0 0 10px #555;
}
.myclass {
  .mixin();
  box-shadow+: 0 0 20px black;
}
```

##### spazi

Concatenare parametri divisi da **spazi** nelle singole regole 

```less
.mixin() {
  transform+_: scale(2);
}
.myclass {
  .mixin();
  transform+_: rotate(15deg);
}
```

---

[Indice](README.md#lezioni)
