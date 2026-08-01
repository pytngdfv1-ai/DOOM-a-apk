💀 DOOM Mobile — Guía del Juego y Documentación Técnica

Adaptación web y móvil optimizada del legendario DOOM (1993) ejecutable en cualquier navegador o empaquetada como aplicación nativa para Android mediante Capacitor. Cuenta con controles táctiles avanzados, menú de trucos integrado, selector de armas de acceso rápido, botón de automapa y lienzo autoajustable al 100% de la pantalla.

📋 Tabla de Contenidos

📖 Manual y Guía del Juego Clásico

Historia y Argumento

Episodios

Arsenal de Armas

Bestiario Demoníaco

Códigos de Trucos

📱 Características de la Versión Móvil

🛠️ Estructura del Proyecto

🎨 Icono de la App (icon.png)

⚙️ Compilación Local y GitHub Actions

Compilación Local

Compilación Automática (APK Debug)

📜 Licencia y Créditos

📖 Manual y Guía del Juego Clásico

Historia y Argumento

Tomas el papel de un marine espacial (Doomguy). Tras ser castigado y enviado a las instalaciones militares de la UAC (Union Aerospace Corporation) en Fobos (luna de Marte), un experimento fallido de teletransportación abre un portal directo al Infierno. Los demonios invaden la base militar, masacrando a todo el personal. Tu único objetivo es sobrevivir, erradicar la horda demoníaca y cerrar el portal.

Episodios

Episodio 1: Knee-Deep in the Dead (Base militar de Fobos). Jefe: Bruiser Brothers.

Episodio 2: The Shores of Hell (Instalaciones corrompidas de Deimos). Jefe: Cyberdemon.

Episodio 3: Inferno (La superficie del Infierno). Jefe: Spider Mastermind.

Arsenal de Armas

N°

Arma

Munición

Uso Recomendado

1

Puño / Motosierra

Sin consumo

Combate cuerpo a cuerpo.

2

Pistola

Balas

Arma básica de inicio.

3

Escopeta

Cartuchos

Altamente efectiva a corta/media distancia.

4

Ametralladora (Chaingun)

Balas

Disparo rápido continuo; inmoviliza a los enemigos.

5

Lanzacohetes

Cohetes

Daño masivo de área (atención al daño cercano).

6

Rifle de Plasma

Células

Proyectiles energéticos ultrarrápidos.

7

BFG 9000

Células (40/disparo)

Devastación total de habitaciones completas.

Bestiario Demoníaco

Zombieman / Shotgun Guy: Soldados poseídos armados.

Imp: Demonios marrones que lanzan proyectiles de fuego.

Demon (Pinky) / Spectre: Bestias voraces (los espectros son semitransparentes).

Cacodemon: Demonios voladores rojos que disparan plasma.

Baron of Hell: Demonios gigantes con cuernos y fuego verde.

Cyberdemon: Híbrido demonio/máquina armado con lanzacohetes.

Spider Mastermind: Cerebro gigante cibernético con metralleta pesada.

Códigos de Trucos (Cheat Codes)

Puedes activarlos en cualquier momento desde el menú flotante de Trucos en la barra superior o ingresándolos por teclado:

IDDQD — Modo Dios (Invencibilidad total).

IDKFA — Armas, Llaves y Munición Máxima.

IDFA — Armas y Munición Máxima (Sin llaves).

IDCLIP — Atravesar Muros (Noclip).

IDBEHOLDS — Modo Berserk (Multiplica por 10 el daño de los puños).

IDBEHOLDV — Invulnerabilidad Temporal.

IDBEHOLDI — Invisibilidad Parcial.

IDBEHOLDA — Mapa Completo Revelado.

📱 Características de la Versión Móvil

Lienzo Autoajustable al 100%: El juego se centra dinámicamente (top: 50%, left: 50%) y se estira para cubrir completamente la pantalla del dispositivo en modo horizontal.

D-Pad táctil: Controles direccionales fluidos (Arriba, Abajo, Izquierda, Derecha).

Botonera de Acción: Botones dedicados para Fuego (s), Usar/Abrir puertas (w), Carrera (Space), Modificador Strafe (Alt), Enter y Esc.

Ajuste de Opacidad de Botones: Botón dedicado para alternar la transparencia de la interfaz táctil en 5 niveles (20%, 35%, 50%, 75%, 100%).

Panel de Selección de Armas: Desplegable superior para cambiar al instante a cualquier arma del 1 al 7.

Botón de Automapa (MAP): Alterna rápidamente la vista del mapa con un toque enviando la tecla Tab.

Soporte PWA / APK: Funciona sin instalación directa desde el navegador o dentro de un contenedor nativo Android con Capacitor.

🛠️ Estructura del Proyecto

DOOM-Mobile/
├── .github/
│   └── workflows/
│       └── build-apk.yml        # Workflow para generar APK en GitHub Actions
├── www/
│   └── index.html               # Juego web completo (HTML + CSS + JS)
├── icon.png                     # 📍 Icono oficial de la APK (1024x1024 px)
├── icon.svg                     # Versión vectorial del icono (opcional)
├── preview_icon.html            # Visualizador y exportador del icono a PNG
├── capacitor.config.json        # Configuración del contenedor nativo Capacitor
├── package.json                 # Dependencias Node / Capacitor
└── README.md                    # Documentación unificada


🎨 Icono de la App (icon.png)

Para que la APK generada tenga el icono personalizado:

El archivo icon.png debe estar ubicado en la raíz principal del repositorio (junto a package.json e index.html).

Debe ser una imagen cuadrada de alta resolución en formato PNG de 1024x1024 píxeles.

También puedes abrir preview_icon.html en un navegador web y hacer clic en "Descargar PNG (1024x1024)" para obtener la imagen exacta optimizada.

⚙️ Compilación Local y GitHub Actions

Compilación Local

# 1. Instalar dependencias
npm install

# 2. Generar iconos de Android desde icon.png
npx @capacitor/assets generate --iconAvailable icon.png

# 3. Añadir plataforma Android (si no existe)
npx cap add android

# 4. Sincronizar archivos de www/ con Android
npx cap sync android

# 5. Abrir en Android Studio para compilar APK
npx cap open android


Compilación Automática en GitHub Actions

El repositorio cuenta con el flujo automatizado .github/workflows/build-apk.yml.

Cada vez que realizas un git push a las ramas main o master:

GitHub Actions inicializa el entorno con Node 20 y Java JDK 17.

Detecta la presencia de icon.png en la raíz del repositorio y genera las resoluciones nativas (mipmap-*).

Sincroniza el proyecto con Capacitor y compila la APK debug mediante ./gradlew assembleDebug.

Sube la APK terminada como un Artefacto descargable (DOOM-Mobile-Debug-APK) en la sección Actions de tu repositorio.

📜 Licencia y Créditos

DOOM (1993): Desarrollado originalmente por John Carmack, John Romero, Adrian Carmack, Kevin Cloud y Sandy Petersen en id Software.

Motor Emulado: Impulsado en la web a través de JS-DOS.

Código Fuente de Doom: Publicado bajo la licencia GNU General Public License (GPL) en 1997.
