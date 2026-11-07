# 💪 Mi Rutina

Página web estática para seguir una rutina full body de 3 días:

- Qué músculo trabaja cada ejercicio (principal y secundarios)
- Animación de ejemplo (fotos de inicio/fin alternadas) y link a videos de YouTube
- Registro de series, repeticiones y peso por día (se guarda en el navegador)
- Alternativas para cada ejercicio si no podés hacer el original
- Historial y exportar/importar datos en JSON

Sin frameworks: `index.html` + `data.js`. Se publica con GitHub Pages.

## Fuente de imágenes

[free-exercise-db](https://github.com/yuhonas/free-exercise-db) — más de 800 ejercicios, dominio público (Unlicense).

## Editar la rutina

La rutina está en `tools/build.py` (lista `DAYS`). Después de cambiarla:

```bash
curl -sL -o /tmp/exercises.json https://raw.githubusercontent.com/yuhonas/free-exercise-db/main/dist/exercises.json
python3 tools/build.py /tmp/exercises.json > data.js
```
