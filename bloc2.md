# Bloc 2: Les Branques del Més Enllà i Resolució del Conflicte

[⬅ Tornar a l'índex](README.md)

## Acció 3.6 — Crear les branques
He creat les branques `feature-nightmare` i `feature-sanctuary`.

```bash
git branch feature-nightmare
git branch feature-sanctuary
git branch
```

**Justificació de la topologia:** he creat les dues branques des de l'últim commit estable de `main` perquè totes dues representen visions alternatives i independents del mateix codi. Així cada línia temporal evoluciona aïllada, sense heretar els canvis de l'altra, i en integrar-les a `main` es pot decidir quin codi és el definitiu.

## Acció 3.7 — La visió fosca
M'he desplaçat a `feature-nightmare` i he modificat la línia del missatge d'inici del servidor per injectar la lògica de la visió fosca.

```bash
git switch feature-nightmare
git add main.js
git commit -m "feat: injectar la lògica de la visió fosca al servidor"
```

## Acció 3.8 — El santuari
M'he desplaçat a `feature-sanctuary`. En aquesta branca el fitxer no conté el canvi de `feature-nightmare`, cosa que demostra l'aïllament entre branques. He modificat exactament la mateixa línia amb la lògica de protecció.

```bash
git switch feature-sanctuary
git add main.js
git commit -m "feat: establir la lògica de protecció del santuari"
```

## Acció 3.9 — Integració de les branques
He tornat a `main` i he integrat `feature-nightmare`. La fusió s'ha fet per *fast-forward*, perquè `main` no tenia commits nous des de la creació de