# Shining and the Darkness — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/mega-drive/shining-and-the-darkness)**.

Traducción al **español de España** de *Shining and the Darkness* (Mega Drive, 1991), el RPG de mazmorras
en primera persona de Climax Entertainment publicado por SEGA (en Occidente, *Shining in the Darkness*).

La traducción se distribuye como **parche**: necesitas tu propia copia de la ROM japonesa original.
Este repositorio contiene únicamente este README; el parche está en **[Releases](../../releases)**.

## Estado

Última versión: **[v1.1](../../releases/tag/v1.1)**.

Traducción nueva realizada directamente desde los textos japoneses de la ROM, con biblia de términos,
glosarios y revisión editorial cruzada. Incluye:

| Parte | Estado |
|---|---|
| Diálogos y mensajes | Los **1.280 mensajes** del juego (historia, combate, tiendas, taberna, iglesia…) |
| Nombres | 146 hechizos y objetos, 126 monstruos y 33 rótulos de lugares y personajes |
| Menús | Campo, combate, Estado, Equipo, tiendas y pantalla de nombre (rejilla latina con «Espacio / Borrar / Fin») |
| Gráficos | Globos del viejo («Nueva / Seguir / Borrar / Copiar», «Rápido / Lento»), rueda de órdenes, «Equipado» e indicador ▼ de «continuar» |
| Fuente | Fuente latina de ancho variable con tildes, ñ, ¡ y ¿ |

### Qué se ha comprobado y qué no

Probado en **Genesis Plus GX** (libretro, Linux), siempre desde partida nueva con la ROM exacta del parche: arranque,
el viejo y sus globos, pantalla de nombre, escena del trono y de Mefisto, mapa, entrada al templo, unos 12 combates
(incluidos varios monstruos iguales y el game over con vuelta desde la iglesia), menú de campo, Estado, Usar / Equipar / Tirar / Dar,
las cuatro tiendas del pueblo (comprar y vender), taberna, iglesia, guardar y cargar (con reinicio), Copiar y Borrar.

**No se ha jugado el juego completo.** Quedan sin comprobar en pantalla: los pisos inferiores y el resto de la historia, la magia con MP,
los compañeros que se unen al grupo, los objetos malditos, la subida de nivel con varios personajes y los finales. Sus textos están traducidos y
validados de forma automática (caracteres, códigos de control, longitud de línea medida con la fuente real), pero no se han visto en el juego.
No se ha probado en consola física ni en flashcart. La traducción y su revisión han contado con **asistencia de IA**;
no es una localización oficial ni una revisión humana profesional.

### Limitaciones conocidas

- El nombre del héroe admite **5 letras**, como en el original.
- Los menús dibujados con la fuente de 8 píxeles usan letras monoespaciadas y se ven más separadas; los nombres de objeto en esos
  menús van **abreviados** (máximo 10 caracteres, p. ej. «Dag.bronce»); en los diálogos aparece el nombre completo.
- Se conservan los rótulos de marca y el texto en inglés del original (SEGA, CLIMAX, título, copyright, «WELCOME BACK…») y los carteles
  pintados con alfabeto decorativo inventado (estandarte del mapa, carteles de tienda), que no es japonés.

## Biblia de términos y estilo

Castellano de España, tuteo salvo en el trato formal de la corte y los comerciantes mayores, y voces diferenciadas por personaje
(el viejo del inicio, el rey, los tenderos, el villano Mefisto…). Nombres propios transcritos del japonés (Bilbo, Merlín, Claire, Mortred, Mefisto,
Tristán, Ward). Ortotipografía española: «…», ¡!, ¿?.

## Cómo aplicar el parche

1. Descarga **[Shining-and-the-Darkness-es-ES-v1.1.xdelta](../../releases/download/v1.1/Shining-and-the-Darkness-es-ES-v1.1.xdelta)**.
2. Comprueba que tienes la ROM japonesa **original, sin cabecera adicional y sin otros parches**:

   | Dato | Valor |
   |---|---|
   | Archivo de referencia | `Shining and the Darkness (Japan).md` |
   | Tamaño | 1.048.576 bytes (1 MiB) |
   | CRC32 | `496AF51C` |
   | MD5 | `380741cee5ff1c89498270d45af7521a` |
   | SHA-256 | `c3b4b6daf4b8cf4d3beb469c7dd89d179983b0bcf3538803e78d47af155e4fe6` |

3. Aplica el parche con **[Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)** o con `xdelta3`:

   ```bash
   xdelta3 -d -s "Shining and the Darkness (Japan).md" Shining-and-the-Darkness-es-ES-v1.1.xdelta "Shining and the Darkness (es-ES).md"
   ```

4. La ROM resultante ocupa **2.097.152 bytes (2 MiB)**. Su MD5 debe ser `15f02176d49f5259774d1721a9db578f` y su SHA-256 `ab4a58a4ceda0a42de665b614a5cba8ef5612c23670bcf60852f0e3e1f0f105d`.
5. Juega en modo **Mega Drive japonesa, NTSC a 60 Hz**. La ROM ampliada a 2 MiB conserva la memoria de guardado del original.

Aplica cada versión sobre el **original japonés**, no sobre una ROM traducida. No cargues un estado de emulador creado con otra versión del juego.

## Créditos y licencias

- Fuente latina: *Misc Fixed 5x8 y 6x12* del proyecto X11 (dominio público), recortada a ancho variable.
- Herramientas propias de extracción, reinserción y compresión gráfica; no se distribuyen ROMs ni herramientas con texto del juego.

## Aviso

Proyecto de traducción por afición, sin ánimo de lucro y sin relación con SEGA ni Climax Entertainment.
No se distribuye la ROM, solo un parche para una copia propia. Se mantienen los nombres y créditos del equipo original.
Si eres titular de los derechos y quieres que lo retire, abre una incidencia.

## Cambios

- **v1.1** (2026-11-03): el recuadro del cursor en la pantalla de nombre ya no se sale; las siglas HP/MP/LV pasan a PV/PM/NV; «Atac» pasa a «Ata.»; el cuadro de monedas de la posada, que seguía en japonés, dice «Monedas» (sin comprobar en pantalla: la posada solo sale con la historia avanzada); corregido un píxel suelto en la «y» de los rótulos de 8 píxeles. Corrige lo comunicado por un usuario.
- **v1.0** (2026-10-30): primera publicación.
