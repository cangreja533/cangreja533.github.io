# Recetario Web

Sitio estático (HTML + JS + Tailwind CSS) para explorar, filtrar y agregar recetas.

## Archivos
- `recetas.html` — página única (home, categorías, filtros, ficha de receta y formulario, todo por rutas con `#/...`)
- `app.js` — toda la lógica (routing, filtros, render, formulario)
- `recipes.json` — base de datos de recetas (207 recetas extraídas del proyecto)

## Cómo usarlo
Puedes abrir `recetas.html` directamente con doble clic (el sitio detecta si el navegador
bloquea la carga de `recipes.json` por el protocolo `file://` y usa una copia de respaldo
embebida). Para la mejor experiencia (recomendado), sírvelo con un servidor local, por ejemplo:

```
cd recetas-app
python3 -m http.server 8080
```

y abre `http://localhost:8080`.

## Categorías
Desayuno, Almuerzo, Cena, Ensalada, Postre, Zumos/Batidos — igual que el grid de referencia
(ícono + nombre), pero con las categorías reales de las recetas.

## Filtros (selectores)
- Categoría (tipo de comida)
- Tipo de alimentación (Paleo / Keto / Reset)
- Restricciones (Low Carb / Carbohidrato almidonado)
- Búsqueda por nombre

## Agregar recetas
El formulario en "Agregar receta" guarda la nueva receta en memoria mientras la pestaña
esté abierta. Usa el botón "Descargar recipes.json actualizado" para bajar un archivo con
todas las recetas (las originales + las agregadas) y reemplazar `recipes.json` si quieres
conservarlas de forma permanente.

## Nota sobre las imágenes
Los documentos de origen no incluían fotos reales de las recetas (solo links a reels de
Instagram). Por eso cada receta tiene un banner ilustrativo (degradado de color + emoji)
en vez de una foto real.
