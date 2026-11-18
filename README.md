# Party-GameTools

Widget táctico modular para Microsoft Xbox Game Bar. Su objetivo es ofrecer herramientas de tiempo configurables durante una partida, sin duplicar funciones que la plataforma ya proporciona.

> **Estado del proyecto:** prototipo conceptual y estructura documental. La aplicación todavía no está implementada; la integración con Game Bar, las herramientas de desarrollo y las capacidades reales del widget siguen pendientes de validación.

## Dirección visual

La identidad aprobada es **Glassmorphism Cyber-Deck**: paneles oscuros translúcidos, sensación de cristal esmerilado, acentos de neón cian y rosa, etiquetas sans-serif y contadores monoespaciados.

La imagen resume los estados principales del concepto: panel de herramientas, configuración avanzada de temporizadores, gestor de presets y alerta visual.

![Concepto visual de Party-GameTools: panel principal, temporizador, presets y alerta HUD](<docs/Party-GameTools GUIs.jpg>)

La referencia visual muestra la estética y los estados de la interfaz. Para el comportamiento final de los controles prevalece la especificación: cada tarjeta o ventana tendrá su propia barra de título con iconos individuales de Pin y Click-Through; el icono de opacidad abrirá un slider flotante propio.

## Funcionalidades previstas

- **Tarjetas independientes:** reloj con hora local y del servidor, temporizador y cronómetro de ronda. Cada módulo podrá presentarse como una tarjeta flotante autónoma.
- **Temporizador:** cuenta atrás con anillo de progreso y controles rápidos, como reiniciar y ajustar el tiempo.
- **Cronómetro:** medición de rondas o fases, con controles de inicio/detención y vueltas.
- **Controles por tarjeta y ventana:** Pin, Click-Through y control de opacidad propios. El slider de transparencia (0–100 %) aparece al activar el icono de opacidad.
- **Alertas configurables:** alerta visual de texto grande y alerta sonora con interruptores separados; texto personalizado y duración de fadeout para el aviso visual.
- **Prealertas y recurrencia:** aviso configurable antes del objetivo y repetición automática de ciclos mientras esté habilitada.
- **Presets:** guardar, describir, cargar y editar configuraciones para reutilizarlas en distintas sesiones y juegos.
- **Extensión futura:** espacio para módulos adicionales, por ejemplo notas, listas de objetivos o calculadoras.

El producto será agnóstico respecto al juego: los nombres de ejemplos que aparecen en los documentos o las imágenes no son etiquetas fijas de la interfaz.

## Consideraciones técnicas

La propuesta de diseño describe comportamientos deseados, no capacidades ya confirmadas de Xbox Game Bar. Antes de implementarlos hay que validar la plantilla, el SDK y el modelo de ejecución compatibles, en especial las tarjetas independientes, su permanencia al cerrar la superposición, Click-Through y el control individual de opacidad. No se debe asumir que APIs Win32 como `WS_EX_TRANSPARENT` están disponibles para un widget de Game Bar.

La tecnología y los pasos de instalación/despliegue se definirán tras revisar documentación y muestras oficiales para el entorno objetivo. No se presupone que Windows App SDK, UWP/XAML, .NET, JavaScript/TypeScript ni una herramienta concreta de empaquetado sean requisitos hasta completar esa comprobación.

## Documentación

- [Brief de concepto y prompt maestro](<docs/Party-GameTools Prototype.md>)
- [Transcripción de diseño y decisiones visuales](<docs/Party-GameTools - Gemini Chat Design.pdf>)
- [Referencia gráfica](<docs/Party-GameTools GUIs.jpg>)
- [Preparación del entorno](docs/01-setup.md)
- [Arquitectura inicial](docs/02-architecture.md)
- [Recursos visuales](assets/README.md)
