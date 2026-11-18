# PROMPT MAESTRO DE INICIO Y ORQUESTACIÓN: Party-GameTools (Microsoft Game Bar Widget)

Actúa como Arquitecto de Software Senior y Desarrollador Principal especializado en extensiones y widgets para la Microsoft Game Bar (Windows 11 UWP/MSIX). Tu misión es inicializar, estructurar y guiar el desarrollo completo de "Party-GameTools", un widget táctico multipropósito de gestión temporal para juegos.

Las imágenes adjuntas en este prompt son la referencia visual absoluta (estética Glassmorphism Cyber-Deck, distribución modular y paneles de configuración). Todo debe implementarse exactamente como se ha proyectado.

---

## 1. STACK TECNOLÓGICO Y ENTORNO REQUERIDO
Antes de escribir cualquier línea de código, verifica o indícame los requisitos de instalación paso a paso de forma interactiva:
* Runtime / SDK: Windows App SDK, Microsoft Game Bar SDK (WinRT / .NET o JavaScript/HTML según el enfoque del widget UWP).
* Dev Tools: Visual Studio 2022 (con cargas de trabajo de desarrollo de aplicaciones universales de Windows y herramientas UWP), Node.js / TypeScript (si se usa framework web de soporte para la UI).
* Empaquetado: Herramientas MSIX Packaging Tool / Windows Store SDK para despliegue local de prueba.

---

## 2. ARQUITECTURA Y ESTRUCTURA DEL PROYECTO
Copilot/Claude: Debes iniciar el repositorio con la estructura base completa:
1. /src/widgets/ (Lógica de la Game Bar y ciclo de vida de las ventanas flotantes).
2. /src/components/ (Tarjetas modulares independientes: Reloj, Temporizador, Cronómetro).
3. /src/services/ (Motor de alertas, persistencia de presets en almacenamiento local, gestión de audio).
4. /src/styles/ (Diseño CSS/Xaml con soporte para Glassmorphism y opacidad dinámica).
5. /assets/ (Iconografía para Pin, Click-Through, Dial de Opacidad, Alertas).

---

## 3. ESPECIFICACIONES TÉCNICAS Y DE INTERFAZ (UI/UX)

### A. Estética Visual: "Glassmorphism Cyber-Deck"
* Paneles translúcidos con efecto esmerilado (frosted glass), bordes limpios con iluminación de acento en neón cian/azulado (#00F0FF), tipografía sans-serif geométrica para etiquetas y monoespaciada para los contadores de tiempo.

### B. Arquitectura Modular y Ventanas Independientes ("Popped-out Cards")
* Cada tarjeta o módulo (Reloj, Temporizador, Cronómetro) funciona como una entidad autónoma con su propia barra de título individual.
* **Controles Individuales obligatorios por tarjeta:**
  1. **Pin:** Ancla la tarjeta permanentemente sobre la pantalla del juego al cerrar la Game Bar.
  2. **Click-Through (Modo Fantasma):** Aplica la propiedad nativa de ventana transparente a eventos de ratón (`WS_EX_TRANSPARENT`) para que el usuario pueda disparar o interactuar con el juego a través del widget sin interferencias.
  3. **Control de Opacidad:** Un icono de dial que, al hacer clic, despliega un slider flotante individual para regular la transparencia (0% a 100%) de esa tarjeta específica en tiempo real.

### C. Motor de Alertas Avanzado (Configurable por Temporizador)
* **Alertas Duales:** Toggles independientes para Alerta Visual (Big Text HUD a pantalla completa) y Alerta Sonora. Se pueden usar por separado o juntas.
* **Personalización de Texto y Fadeout:** Textbox para definir el mensaje de texto gigante (ej. "¡REINICIO DEL SERVIDOR EN 15m!") y un control deslizante para la duración del fadeout en pantalla (1s a 10s).
* **Anticipación de Eventos (Pre-Alerta):** Selector de tiempo antes del evento objetivo (ej. avisar 5m, 10m, 15m antes).
* **Recurrencia Automática:** Opción de bucle para repetir ciclos automáticamente al llegar a cero (ej. temporizadores de reinicios de servidores cada 3 horas).

### D. Sistema de Gestión de Presets
* Panel modal independiente para guardar configuraciones completas de temporizadores asignándoles un **Nombre y una Descripción** (ej. *“Reinicio Servidor DayZ 3h - Avisar 15m, repetir”*).
* Permite cargar, editar o crear nuevos presets instantáneamente para evitar reconfiguraciones en futuras sesiones de juego.

---

## 4. FLUJO DE TRABAJO Y DESPLIEGUE LOCAL (PASO A PASO)

1. **Fase de Inicialización (Copilot):** Crea la estructura de carpetas, archivos de configuración del manifiesto de la Game Bar (`package.appxmanifest`), dependencias y esqueletos principales del código.
2. **Fase de Orquestación y Refinamiento (Claude):** Claude revisará el código generado, completará la lógica faltante del motor de alertas, el enlace de los sliders de opacidad y el sistema de presets.
3. **Instrucciones de Despliegue Local (Interactivas):** Durante el proceso, **dime paso a paso y de forma interactiva** cómo compilar, registrar e instalar el widget en la Microsoft Game Bar localmente por primera vez (incluyendo el modo de desarrollador de Windows, sideloading del paquete MSIX y los comandos o pasos necesarios en Visual Studio).