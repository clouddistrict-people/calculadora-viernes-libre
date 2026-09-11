# Calculadora de viernes libres

Herramienta interna de Cloud District para estimar cuántos **viernes libres** corresponden a una nueva incorporación según su fecha de alta, dentro del beneficio de reducción de jornada de la empresa.

🔗 **Sitio publicado:** `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/` *(actualiza este enlace cuando lo tengas)*

## Qué hace

A partir de la fecha de incorporación de una persona, calcula:

- las **SAH brutas** (horas de calendario) desde esa fecha hasta el 31 de diciembre del mismo año,
- descontando vacaciones proporcionales, día extra de empresa y día de cumpleaños,
- comparándolas con la **SAH objetivo** (calibrada automáticamente para que un año completo dé siempre **15 viernes libres**, el precepto fijo de la empresa),
- y convierte el excedente de horas en el número de viernes libres correspondiente.

Tiene en cuenta:
- **Jornada normal:** 8,5h de lunes a jueves, 6,5h los viernes.
- **Jornada intensiva de verano:** 7,5h de lunes a viernes, siempre del 15 de junio al 15 de septiembre (fijo, no se mueve con el calendario).
- **24 y 31 de diciembre:** media jornada.
- **Festivos:** precargados para Madrid capital; para 2026 son los oficiales (BOCM), para el resto de años se autogeneran (incluida la Semana Santa, calculada con el algoritmo de Gauss) y se marcan como "provisional" hasta que haya decreto oficial. Editables a mano en cualquier momento.

## Cómo usarla

Solo hace falta abrir la URL publicada — no requiere instalación ni backend, todo corre en el navegador:

1. Escribe la fecha de incorporación (o haz clic directamente en un día del calendario) — también hay un botón **"Hoy"**.
2. Introduce los días de vacaciones proporcionales (se copian de Factorial, no se calculan aquí).
3. El resultado y el desglose del cálculo se actualizan solos.

## Cómo actualizar el sitio

Este repo tiene un único archivo, `index.html`, autocontenido (HTML + CSS + JS, sin dependencias externas salvo las fuentes de Google Fonts). GitHub Pages sirve directamente ese archivo.

Para publicar cambios:
1. Edita `index.html` desde el icono del lápiz en GitHub, o súbelo de nuevo con **Add file → Upload files** para sustituirlo entero.
2. Confirma el commit.
3. GitHub Pages se actualiza solo en 1-2 minutos — no hace falta tocar nada más.

## Notas

- Repositorio **privado**: solo lo ven las personas añadidas como colaboradoras en *Settings → Collaborators and teams*.
- Identidad visual de Cloud District (Purple Black `#090017`, Lima `#AFFC41`, tipografía Poppins) aplicada según el brandbook 2025 y la skill de identidad de marca.
- Cualquier duda o petición de cambio, contacta con [tu nombre / equipo de People].
