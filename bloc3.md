# Bloc 3: Viatge Temporal, Exorcisme del Codi i Publicació Remota

[⬅ Tornar a l'índex](README.md)

## Acció 3.11 — El commit infectat
He afegit al fitxer una funció que llança una excepció no controlada i l'he registrat a l'historial, simulant la corrupció del sistema.

```bash
git add main.js
git commit -m "feat: unhandled spectral exception"
```

## Acció 3.12 — Inspecció de la diferència
He comparat el commit infectat (`HEAD`) amb l'últim punt segur (`HEAD~1`) per veure exactament quin codi s'havia injectat.

```bash
git diff HEAD~1 HEAD
```

## Acció 3.13 — Exorcisme del codi
He executat una reversió amb `reset --hard`, que mou la branca a l'estat segur anterior, elimina el commit de l'historial i esborra el codi infectat de l'espai de treball. Com que el commit infectat no s'havia pujat a GitHub, l'historial remot no s'ha vist afectat.

```bash
git reset --hard HEAD~1
git log --oneline
```

## Acció 3.14 — Topologia final
He visualitzat gràficament l'arbre del repositori, on es veuen les branques, la fusió i la línia temporal purificada sense el commit infectat.

```bash
git log --oneline --graph --all
```

## Acció 3.15 — Publicació a GitHub
He vinculat el repositori local amb el repositori públic `halloween-git-rescue` i he pujat la branca `main` i les dues branques de treball.

```bash
git remote add origin https://github.com/ELTEUUSUARI/halloween-git-rescue.git
git push -u origin main
git push origin feature-nightmare feature-sanctuary
```

Enllaç al repositori: https://github.com/SGerona1/halloween-git-rescue