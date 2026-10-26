# Bloc 1: Invocació del Repositori i Línia Base

[⬅ Tornar a l'índex](README.md)

## Acció 3.1 — Crear el repositori
He creat un directori buit anomenat `server-room-horror` i l'he inicialitzat com a repositori Git local, establint `main` com a branca principal.

```bash
mkdir server-room-horror
cd server-room-horror
git init -b main
```


## Acció 3.2 — Configurar la identitat
He configurat el nom i el correu perquè cada commit quedi associat a la meva identitat professional.

```bash
git config user.name "El teu Nom"
git config user.email "elteu@correu.com"
```



## Acció 3.3 — Primer commit
He creat el fitxer `main.js` amb l'estructura base de l'aplicació i l'he registrat a l'historial.

```bash
git add main.js
git commit -m "feat: crear estructura base de l'aplicació del servidor"
```



## Acció 3.4 — Sistema de seguretat
He aplicat dues modificacions successives al codi, cadascuna en un commit separat per mantenir la traçabilitat dels canvis.

```bash
git add main.js
git commit -m "feat: afegir control d'accés al sistema de seguretat"
```



```bash
git add main.js
git commit -m "feat: afegir alarma de temperatura a la sala de servidors"
```



## Acció 3.5 — Historial simplificat
He mostrat l'historial en una sola línia per verificar que la línia temporal inicial és estable i conté els tres commits.

```bash
git log --oneline
```

