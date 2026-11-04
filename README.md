# Calculadora de viernes libres

Herramienta interna de Cloud District para estimar cuántos **viernes libres** corresponden a una persona en el año según su fecha de incorporación, sus ausencias y su jornada, dentro del beneficio de reducción de jornada de la empresa.

🔗 **Sitio publicado:** https://clouddistrict-people.github.io/calculadora-viernes-libre/

## Cómo se calcula

Prorrata por días laborables:

> viernes = 15 × (días laborables trabajados − día extra − cumpleaños) ÷ (días laborables del año − día extra − cumpleaños)

- **Un año completo son 15 viernes libres.**
- **Día extra y cumpleaños:** se descuentan siempre completos (1 día cada uno, desactivables), aunque haya alta tardía o ausencia. Con un año completo no cambian el resultado; con altas tardías o ausencias lo ajustan ligeramente.
- **Días laborables:** de lunes a viernes, sin festivos.
- **Incorporación a mitad de año:** no cuentan los días anteriores al alta; el cálculo llega hasta el 31 de diciembre.
- **Bajas y otras ausencias** (baja médica, nacimiento y cuidado del menor, etc.): cada día laborable de ausencia resta lo mismo, sea cual sea la época del año. Cada ausencia tiene un interruptor «cuenta como tiempo trabajado» para las que no deban restar. Si la baja sigue abierta, se deja sin fecha de fin (cuenta hasta el 31 de diciembre) y se actualiza al alta.
- **Redondeo:** a días enteros; hasta x,5 se redondea hacia abajo y desde x,6 hacia arriba.
- **Jornada parcial:** mismo número de viernes que con jornada completa. La herramienta los traduce a horas según las horas semanales (referencia de jornada completa: 40 h): cada viernes vale horas semanales ÷ 5. Si la persona no trabaja los viernes, muestra también el equivalente en jornadas.
- **Saldo:** opcionalmente se indican los viernes ya disfrutados; si el saldo sale negativo lo asume la empresa.
- **Festivos:** precargados para Madrid capital. Los de 2026 son los oficiales (BOCM); para el resto de años se autogeneran (Semana Santa calculada con el algoritmo de Gauss; el 1 de noviembre y el 6 de diciembre pasan al lunes si caen en domingo) y se marcan como «provisional» hasta que haya decreto oficial. Se pueden editar a mano.

## Cómo usarla

Solo hace falta abrir la URL publicada: no requiere instalación ni backend, todo corre en el navegador.

1. Escribe la fecha de incorporación, o haz clic en un día del calendario (también hay un botón **Hoy**).
2. Si procede, añade ausencias y elige la jornada (completa o parcial).
3. El resultado y el desglose se actualizan solos.

## Cómo actualizar el sitio

Este repo tiene un único archivo, `index.html`, autocontenido (HTML + CSS + JS, sin dependencias externas salvo las fuentes de Google Fonts). GitHub Pages sirve directamente ese archivo.

Para publicar cambios:
1. Edita `index.html` desde el icono del lápiz en GitHub, o súbelo de nuevo con **Add file → Upload files** para sustituirlo entero.
2. Confirma el commit.
3. GitHub Pages se actualiza solo en 1-2 minutos — no hace falta tocar nada más.

## Notas

- Repositorio **privado**: solo lo ven las personas añadidas como colaboradoras en *Settings → Collaborators and teams*.
- Look & feel de clouddistrict.com: tipografías Archivo, Archivo Black e IBM Plex Mono, y logo y favicon oficiales de la web.
- Cualquier duda o petición de cambio, contacta con tu manager o con People.
