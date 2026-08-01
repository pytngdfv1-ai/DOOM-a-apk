💀 DOOM (1993) — Guía y Manual del Juego Clásico

DOOM es un videojuego de disparos en primera persona (FPS) pionero, desarrollado por id Software y lanzado originalmente en 1993. Definó las bases del género y se convirtió en uno de los títulos más influyentes en la historia de los videojuegos.

📜 Historia y Argumento

Tomas el papel de un marine espacial sin nombre (popularmente conocido como Doomguy). Tras agredir a un oficial superior que ordenó disparar contra civiles desarmados, eres transferido como castigo a la base militar de la UAC (Union Aerospace Corporation) en Fobos, una de las lunas de Marte.

La UAC realizaba experimentos secretos de teletransportación entre Fobos y Deimos. Algo sale catastróficamente mal: los portales se abren de par en par al mismísimo Infierno, permitiendo que hordas de demonios invadan las instalaciones y masacren a todo el personal. Tu objetivo es sobrevivir, erradicar la amenaza demoníaca y cerrar las puertas del Infierno.

🎮 Episodios del Juego

Episodio 1: Knee-Deep in the Dead (Hasta el cuello con los muertos)

Escenario: Base militar de Fobos.

Jefe Final: Los Bruiser Brothers (dos Barones del Infierno en E1M8).

Episodio 2: The Shores of Hell (Las orillas del Infierno)

Escenario: Instalaciones de Deimos corrompidas por la biomasa demoníaca.

Jefe Final: El Cyberdemon (E2M8).

Episodio 3: Inferno (Infierno)

Escenario: La superficie misma del Infierno.

Jefe Final: El Spider Mastermind (E3M8).

🔫 Arsenal de Armas

N°

Arma

Tipo de Munición

Descripción

1

Puño / Motosierra

Sin consumo

Combate cuerpo a cuerpo. La motosierra destroza enemigos pequeños.

2

Pistola

Balas

Arma inicial básica. Precisa a larga distancia.

3

Escopeta

Cartuchos

Arma principal a corta/media distancia. Devastadora en grupos de enemigos.

4

Ametralladora (Chaingun)

Balas

Disparo continuo rápido. Inmoviliza enemigos al ser atacados rápidamente.

5

Lanzacohetes

Cohetes

Gran daño de área. ¡Cuidado con el daño por explosión cercana!

6

Rifle de Plasma

Células de energía

Dispara ráfagas veloces de proyectiles de energía azul.

7

BFG 9000

Células de energía (40 por disparo)

La máxima arma de destrucción. Limpia habitaciones enteras de un disparo.

👹 Bestiario Demoníaco

Zombieman / Shotgun Guy / Heavy Weapon Dude: Antiguos soldados humanos poseídos.

Imp: Demonios marrones que lanzan bolas de fuego.

Demon (Pinky) / Spectre: Bestias cuadrúpedas voraces (los espectros son invisibles).

Cacodemon: Esferas voladoras rojas de un solo ojo que lanzan bolas de plasma.

Baron of Hell: Demonios gigantes con cuernos que lanzan fuego verde.

Cyberdemon: Híbrido demonio/máquina gigante con un lanzacohetes en el brazo.

Spider Mastermind: Cerebro gigante montado sobre patas mecánicas con ametralladora pesada.

🧪 Códigos de Trucos (Cheat Codes)

Ingresa estos códigos en cualquier momento durante la partida para activar ventajas:

IDDQD — Modo Dios (Invencibilidad total y ojos amarillos en la interfaz).

IDKFA — Armas, Llaves y Munición Máxima (Otorga todo el arsenal y tarjetas de acceso).

IDFA — Armas y Munición Máxima (Sin otorgar llaves).

IDCLIP — Atravesar Paredes (Permite caminar a través de muros y obstáculos).

IDBEHOLDS — Modo Berserk (Multiplica por 10 el daño de los puños).

IDBEHOLDV — Invulnerabilidad Temporal.

IDBEHOLDI — Invisibilidad Parcial (Los enemigos tienen dificultades para apuntarte).

IDBEHOLDA — Revelar Mapa Completo.

IDCLEVxy — Salto de Nivel (donde x es el episodio e y el nivel; ej: IDCLEV11 para E1M1).

📜 Licencia y Créditos

DOOM fue creado por John Carmack, John Romero, Adrian Carmack, Kevin Cloud y Sandy Petersen. El código fuente de Doom fue liberado bajo la licencia GPL en 1997.



📱 DOOM Mobile Edition (Capacitor & WebApp)

Esta es una versión web y nativa para Android/iOS de DOOM (1993) emulada con js-dos v6.22 (DOSBox compilado a WebAssembly) y empaquetada con Capacitor para ejecutarse como una aplicación móvil nativa a pantalla completa.

🚀 Características de esta Versión Móvil

Pantalla Adaptativa y Centrada:

El lienzo <canvas> se escala dinámicamente y se ubica de forma absolutamente centrada en el dispositivo mediante coordenadas CSS (top: 50%, left: 50%, transform: translate(-50%, -50%)).

Soporta 3 modos de visualización intercambiables en tiempo real:

Estirar (100%): Llena toda la pantalla del teléfono sin barras negras.

Zoom Inteligente: Maximiza el área manteniendo cobertura total.

Clásica (4:3): Conserva la relación de aspecto original de MS-DOS.

Controles Táctiles Integrados:

D-Pad (Cruceta) para movimiento preciso.

Botones táctiles dedicados para Fuego, Usar (W), Correr (Shift/Space), Alt (Strafe), Enter y Esc.

Nuevo Selector de Arma: Botón conmutador que permite rotar secuencialmente entre las armas (1 al 7) con un solo toque.

Control de Atenuación de Botones (Opacidad):

Ajuste rápido de transparencia de la interfaz táctil (20%, 35%, 50%, 75%, 100%) para evitar tapar la visibilidad de la acción.

Respuesta táctil visual con encendido luminoso al presionar cualquier botón.

Panel de Trucos Táctil:

Menú desplegable en la barra superior con botones para ejecutar automáticamente los comandos principales (IDDQD, IDKFA, IDCLIP, IDBEHOLD, etc.).

Bloqueo de Orientación:

Pantalla de advertencia automática para forzar al usuario a colocar el teléfono en modo horizontal (Landscape).

📂 Estructura del Proyecto

doom-mobile-app/
├── .github/
│   └── workflows/
│       └── build-apk.yml        # Workflow para generar APK automáticamente en GitHub Actions
├── www/
│   └── index.html               # Aplicación web completa (HTML + CSS + JS en un solo archivo)
├── capacitor.config.json        # Configuración del contenedor nativo de Capacitor
├── native-patches/              # Ajustes de AndroidManifest.xml y permisos
├── package.json                 # Dependencias del proyecto Node/Capacitor
└── README.md                    # Este archivo de documentación


🛠️ Tecnologías Utilizadas

HTML5 Canvas & WebGL: Renderizado gráfico del motor de DOS.

js-dos 6.22 / wdosbox.js: Emulación de MS-DOS ejecutable en navegador vía WebAssembly.

Capacitor (Ionic Framework): Encapsulamiento del código web en una App Nativa de Android (.apk).

FontAwesome 6.4: Iconografía ligera para controles táctiles y barra superior.

📦 Compilación y Empaquetado

Requisitos Previos

Node.js (v18+)

Android Studio y SDK de Android (para compilación local)

Comandos de Compilación Local

# 1. Instalar dependencias
npm install

# 2. Inicializar plataforma Android (si aún no está creada)
npx cap add android

# 3. Sincronizar los cambios de la carpeta /www con el proyecto Android
npx cap sync android

# 4. Abrir en Android Studio para compilar la APK final
npx cap open android


Compilación Automática con GitHub Actions

El repositorio incluye un workflow que compila el APK en la nube cada vez que realizas un push a la rama principal:

Ve a la pestaña Actions en tu repositorio de GitHub.

Selecciona el flujo Enhance APK build workflow.

Descarga el artefacto app-debug.apk generado al finalizar la compilación.

📱 Mapa de Teclas Interno (JS-DOS Mapping)

Botón Táctil

Tecla Simulada en DOS

Función en el Juego

D-Pad

ArrowUp, ArrowDown, ArrowLeft, ArrowRight

Desplazamiento y giro

Fuego

S

Disparar arma actual

Usar

W

Abrir puertas / activar interruptores

Arma [1-7]

1, 2, 3, 4, 5, 6, 7

Cambiar de arma secuencialmente

Run

Space / Shift

Mantener para correr

Alt

Alt

Modificador de strafe (desplazamiento lateral)

Enter

Enter

Confirmar en menús

Esc

Escape

Pausa y menú principal

📄 Licencia

Distribución libre para fines educativos y de preservación de software clásico. El motor de juego utiliza la versión shareware liberada de DOOM 1.9.
