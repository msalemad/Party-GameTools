# Party-GameTools

Widget táctico multipropósito para Xbox Game Bar, con reloj, temporizadores, cronómetro, alertas y presets.

## Referencia visual de la GUI

La captura adjunta al proyecto define la dirección visual prevista: paneles modulares de estética **Glassmorphism Cyber-Deck**, acentos cian/rosa, configuración avanzada del temporizador, gestor de presets y alerta HUD.

![Referencia visual de la GUI esperada](assets/gui-reference.png)

> La imagen original debe guardarse como `assets/gui-reference.png`. El entorno de edición de este cambio no proporciona los bytes de la imagen adjunta para subirla al repositorio; por eso el enlace queda preparado, pero la captura aún no está incluida en Git. Consulta [assets/README.md](assets/README.md) para añadirla.

## Estructura

```text
assets/                 Recursos visuales e iconos
src/
  components/            Tarjetas de reloj, temporizador y cronómetro
  services/              Alertas, audio y persistencia de presets
  styles/                Recursos de estilo y tema
  widgets/               Integración y ciclo de vida del widget

docs/                    Requisitos, arquitectura y guía de desarrollo
tests/                   Pruebas
```

## Estado y siguientes fases

- [x] Estructura inicial del repositorio y documentación de preparación
- [ ] Incorporar la captura original en `assets/gui-reference.png`
- [ ] Verificar las plantillas y APIs vigentes del Xbox Game Bar SDK en el entorno Windows
- [ ] Crear el proyecto UWP/XAML y su manifiesto a partir de una muestra oficial compatible
- [ ] Implementar la interfaz y validar las capacidades permitidas por Game Bar
- [ ] Añadir temporizadores, alertas y presets; compilar y probar el paquete MSIX

## Requisitos de desarrollo

El desarrollo y las pruebas de empaquetado se realizan en Windows con Visual Studio y los componentes UWP/Windows SDK que requiera la versión del Game Bar SDK elegida. Revisa [la guía de preparación](docs/01-setup.md) antes de instalar herramientas o crear el manifiesto. No se presupone que Windows App SDK, Node.js o `WS_EX_TRANSPARENT` sean requisitos o capacidades compatibles del widget sin verificarlo contra documentación y muestras oficiales.
