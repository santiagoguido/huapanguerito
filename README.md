# Huapanguerito Multiplicador

Juego en pixel art para niñas y niños de 10 años que sirve para **repasar** y **evaluar** las tablas de multiplicar (del 2 al 10), ambientado en Xichú, Guanajuato.

Todo el juego vive en un solo archivo: `index.html`. No necesita instalar nada.

## Cómo publicarlo en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `huapanguerito-multiplicador`) y márcalo como **público**.
2. Sube el archivo `index.html` (y este README si quieres) a la raíz del repositorio, en la rama `main`.
3. Entra a **Settings → Pages**.
4. En **Build and deployment**, elige **Source: Deploy from a branch**, rama **main** y carpeta **/(root)**. Guarda.
5. En uno o dos minutos el juego estará en:
   `https://TU-USUARIO.github.io/huapanguerito-multiplicador/`

Comparte ese enlace con los niños. Funciona en computadora, tableta y celular.

## Qué tiene el juego

**Repasar tablas.** El niño camina con su huapanguerito por un mapa grande de Xichú. La cámara lo sigue de cerca y las comunidades van apareciendo conforme avanza; cada una muestra su nombre, su tabla y sus estrellas. Un minimapa en la esquina indica dónde va. El recorrido es: Casitas (2, en la cima del cerro), Álamo (3) y La Misión (4) juntas y con sus álamos, La Sábila (5), El Rucio (6), El Aguacate (7), El Huamúchil (8, a la orilla del río), La Laja (9, junto al río y cerca de El Huamúchil) y El Platanal (10, a la orilla del río, lejos de las otras dos). El camino termina en el centro del mapa, en La Topada: una plaza con la iglesia, los dos estrados y gente bailando. Se camina tocando una comunidad en el mapa, con las flechas del teclado o con los botones Anterior/Siguiente.

Al entrar a una comunidad, el niño ve la tabla, la cuenta "de N en N" y un truco; también puede escucharla en voz alta. Luego atrapa la fruta (pitaya, mango, plátano, aguacate o chilcuague) con la respuesta correcta. Si se equivoca, recibe una pista y esa multiplicación se le vuelve a preguntar al final. Gana de 1 a 3 estrellas.

**La Topada (evaluación).** Inspirada en los duelos de trovadores del huapango arribeño: cada trovador toca con sus músicos en su propio estrado enramado, frente a la iglesia, mientras la gente baila entre los dos. Se eligen las tablas, el número de preguntas (20, 30, 50 o todas) y el tiempo por pregunta (15, 10 o 6 segundos). El niño escribe la respuesta con un teclado en pantalla (o el del equipo). Al final muestra:

- Aciertos, tiempo promedio y una medalla.
- Un mapa de calor de todas las tablas: verde = memorizada (correcta en 5 s o menos), amarillo = correcta pero lenta, rojo = fallada o sin tiempo.
- La lista de multiplicaciones para repasar y un botón que arma un repaso solo con esas.
- Un botón para **copiar el reporte** como texto (útil para mandarlo por WhatsApp a la maestra o a los papás).

Los resultados y estrellas se guardan en el navegador de cada dispositivo (no hay servidor ni cuentas).

## Cómo personalizarlo

Abre `index.html` y busca el bloque `DATOS DE XICHÚ` al inicio del código. (La posición de cada comunidad en el mapa está en `OW_ROUTE` y lo que la rodea en `OW_LAND`.) Ahí puedes cambiar:

- `nombre`: el nombre de la comunidad de cada tabla.
- `fruta`: `pitaya`, `mango`, `chilcuague`, `platano` o `aguacate`.
- `props`: lo que aparece en el paisaje (`pitayo`, `mango`, `platano`, `sabila`, `huamuchil`, `pino`, `casita`, `capilla`, `kiosko`, `alamo`, `aguacate`, `laja`). El primero de la lista es el emblema de la comunidad: es el que más aparece y su ícono en el mapa.
- `tema`: el cielo (0 atardecer, 1 noche azul, 2 atardecer rosa, 3 noche verde).
- `intro`: el texto que lee el niño al llegar.

Justo debajo están los trucos de cada tabla (`TRUCOS`) y las frases de ánimo (`OK_LINES`, `TOP_OK`, etc.). La constante `MEM_MS` define cuántos milisegundos cuentan como "memorizada" (5000 = 5 s).

La música es una melodía original en 6/8 generada en el navegador; se puede apagar con el botón **Música**.
