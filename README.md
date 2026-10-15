# Válvulas distribuidoras: animaciones de neumática e hidráulica

## 1. Qué es este proyecto y cómo se usa

Es una página web educativa, de un solo archivo (`index.html`), que muestra cómo funcionan ocho válvulas distribuidoras. Cada una tiene un corte longitudinal animado y su símbolo normalizado conectado a un circuito. No necesita internet ni instalar nada.

Las válvulas, en el mismo orden que la tabla de referencia del curso:

1. 2/2 normalmente cerrada (neumática, Pn), con botón y resorte, alimentando un motor neumático.
2. 2/2 normalmente abierta (Pn), con botón y resorte, alimentando un motor neumático.
3. 3/2 normalmente cerrada (Pn), con palanca y resorte, sobre un cilindro de simple efecto.
4. 3/2 normalmente abierta (Pn), con palanca y resorte, sobre un cilindro de simple efecto.
5. 4/2 monoestable (Pn), con una bobina y resorte, sobre un cilindro de doble efecto.
6. 5/2 biestable (Pn), con pilotaje 14 y 12, sobre un cilindro de doble efecto.
7. 4/3 centro cerrado (hidráulica, H), con solenoides Y1 y Y2 y centrado por resortes.
8. 5/3 centro abierto (H), con solenoides Y1 y Y2 y centrado por resortes.

Cómo usar la página:

- Arriba a la derecha hay un menú para elegir la válvula. También puedes cambiar de válvula editando el final de la dirección (por ejemplo `#5-3-centro-abierto`).
- Junto al menú está **Velocidad** (0.25× a 2×), que hace más lenta o más rápida toda la animación: corredera, cilindro, motor y flujo. El navegador recuerda la última velocidad elegida.
- Los botones **Corte**, **Símbolo** y **Ambos** deciden qué se ve. El corte muestra la corredera por dentro; el símbolo muestra la representación normalizada con el cilindro o el motor.
- Debajo hay botones de mando. En las válvulas de botón, palanca o una bobina, mantén presionado el botón: la válvula cambia de posición mientras lo sostienes y regresa sola al soltarlo. En la 5/2 hay un pulso para cada lado, y en las de tres posiciones hay tres botones (Energizar Y1, Centro, Energizar Y2).
- Debajo de los botones aparece el texto de la posición actual: qué puertos se conectan y qué hace el actuador.
- El panel **Tabla de referencia** muestra la imagen del profesor. Al cambiar de válvula se resalta su fila. Puedes acercar con los botones + y −, con la rueda del ratón (acerca hacia donde está el cursor) o pellizcando en pantallas táctiles. Arrastra para moverte. Doble clic o doble toque alterna el zoom. **Restablecer** muestra toda la tabla y **Ir a esta fila** acerca a la fila de la válvula que estás viendo. En el celular el panel queda debajo de la animación y se puede plegar.

## 2. Estructura de archivos

```
valvulas-distribuidoras/
├── index.html                       La página completa (diseño, animaciones y datos)
├── README.md                        Este archivo
└── assets/
    └── tabla-distribuidores.jpg     Imagen de la tabla de referencia
```

La carpeta `assets` debe quedar junto a `index.html` y con ese nombre exacto, porque la página busca la imagen en `assets/tabla-distribuidores.jpg`.

## 3. Crear la cuenta de GitHub y el repositorio

GitHub es un sitio donde se guardan proyectos y, además, se pueden publicar páginas web gratis. Un repositorio es la carpeta de tu proyecto dentro de GitHub.

1. Entra a https://github.com. Si ya tienes cuenta, inicia sesión y pasa al paso 4. Si no, pulsa **Sign up**, escribe tu correo, una contraseña y un nombre de usuario, y confirma el código que te llegue por correo. Tu nombre de usuario formará parte del enlace público de la página, así que elige uno que no te incomode compartir.
2. Una vez dentro, arriba a la derecha pulsa el botón **+** y elige **New repository**. También puedes pulsar el botón verde **New** en la página principal.
3. Llena el formulario así:
   - **Owner**: déjalo con tu usuario.
   - **Repository name**: escribe `valvulas-distribuidoras` (sin espacios ni acentos).
   - **Description** (opcional): `Animaciones de válvulas distribuidoras neumáticas e hidráulicas con corte y símbolo`.
   - **Public**: márcalo. Para publicar la página gratis con GitHub Pages el repositorio debe ser público.
   - **Add a README file**: NO lo marques, porque ya tenemos un `README.md` y se duplicaría.
   - **Add .gitignore**: deja `No .gitignore`.
   - **Choose a license**: es opcional. Puedes dejar `None` o elegir `MIT License` si quieres que otras personas puedan reutilizar el código.
4. Pulsa el botón verde **Create repository**. Llegarás a una página casi vacía con instrucciones; no necesitas seguirlas.

## 4. Subir los archivos desde el navegador

1. En la página del repositorio recién creado, busca el texto **uploading an existing file** (aparece en la sección de configuración rápida) y pulsa ese enlace. Si no lo ves, pulsa el botón **Add file** y luego **Upload files**.
2. Abre en tu computadora la carpeta donde guardaste el proyecto. Selecciona `index.html`, `README.md` y la carpeta `assets` completa, y arrástralos a la zona que dice **Drag files here**. La carpeta `assets` debe conservarse como carpeta, con la imagen adentro.
3. Si tu navegador no te deja arrastrar carpetas, sube primero `index.html` y `README.md`. Luego pulsa **Add file > Create new file**, escribe en el nombre `assets/LEEME.txt` (al teclear la diagonal GitHub crea la carpeta `assets`), pon cualquier texto y pulsa **Commit changes**. Después entra a la carpeta `assets` en GitHub, pulsa **Add file > Upload files** y arrastra ahí `tabla-distribuidores.jpg`. Lo importante es que la imagen termine en `assets/tabla-distribuidores.jpg`.
4. Espera a que cada archivo muestre su barra de carga completa. Abajo, en el cuadro **Commit changes**, escribe un mensaje, por ejemplo `Agrego animaciones de válvulas y tabla de referencia`.
5. Deja marcada la opción **Commit directly to the main branch** y pulsa el botón verde **Commit changes**.
6. Comprueba que en la página del repositorio se vean `index.html`, `README.md` y la carpeta `assets`. Entra a `assets` para confirmar que está la imagen.

## 5. Publicar con GitHub Pages

1. En la página del repositorio pulsa la pestaña **Settings** (Configuración), arriba a la derecha de las pestañas.
2. En el menú de la izquierda pulsa **Pages**.
3. En la sección **Build and deployment**, en **Source**, elige **Deploy from a branch**.
4. En **Branch**, elige `main` en el primer menú y `/ (root)` en el segundo. Pulsa **Save**.
5. Espera de 1 a 3 minutos. Recarga la página de **Pages** de vez en cuando. Cuando esté listo, arriba aparece un mensaje que dice **Your site is live at** seguido del enlace.
6. El enlace tiene este formato, cambiando USUARIO por tu nombre de usuario de GitHub: `https://USUARIO.github.io/valvulas-distribuidoras/`
7. Para ver el avance, entra a la pestaña **Actions** del repositorio. Ahí aparece un proceso llamado **pages build and deployment**. Si tiene un círculo amarillo, sigue trabajando; con una palomita verde, ya terminó; con una cruz roja, hubo un problema (revisa la sección 8).

## 6. Verlo sin internet

1. Descarga los archivos: en la página del repositorio pulsa el botón verde **Code** y luego **Download ZIP**.
2. Descomprime el ZIP en una carpeta.
3. Abre `index.html` con doble clic. Se abrirá en tu navegador y funciona sin conexión, siempre que la carpeta `assets` siga junto a `index.html`.

## 7. Compartirlo con el profesor y actualizarlo

- Para compartirlo, envía el enlace de la página (`https://USUARIO.github.io/valvulas-distribuidoras/`). Si además quieres que vea el código, envía el enlace del repositorio (`https://github.com/USUARIO/valvulas-distribuidoras`).
- Para actualizar un archivo, entra al repositorio, pulsa **Add file > Upload files** y sube de nuevo el archivo con exactamente el mismo nombre (y dentro de la misma carpeta si es la imagen). GitHub lo reemplaza. Escribe un mensaje de commit y pulsa **Commit changes**. La página se vuelve a publicar sola en uno o dos minutos.

## 8. Problemas comunes

- **Aparece un 404 justo después de publicar.** Es normal los primeros minutos. Espera 3 minutos, revisa que la pestaña **Actions** muestre la palomita verde y recarga. Confirma también que `index.html` esté en la raíz del repositorio y no dentro de otra carpeta, y que en Pages esté elegida la rama `main` con `/ (root)`.
- **La imagen de la tabla no carga.** El panel mostrará un aviso. Revisa que la carpeta se llame `assets` y el archivo `tabla-distribuidores.jpg`, todo en minúsculas y sin espacios. GitHub distingue mayúsculas de minúsculas: `Assets` o `Tabla-Distribuidores.JPG` no funcionarán. Revisa también que la carpeta `assets` esté al mismo nivel que `index.html`.
- **Subí un cambio pero no lo veo.** El navegador guarda copias. Recarga forzando con Ctrl + F5 (en Mac, Cmd + Shift + R), o abre la página en una ventana de incógnito. En el celular, cierra la pestaña y vuelve a abrir el enlace.
- **El repositorio no me deja activar Pages.** Verifica que sea público (**Settings > General**, al final, en **Danger Zone**, aparece su visibilidad).

## 9. Créditos

La tabla de referencia fue tomada del material del curso de Hidráulica. Las animaciones se hicieron con ayuda de Claude.
