# Arquitectura inicial

## Módulos previstos

- `src/widgets/`: activación e integración con Xbox Game Bar.
- `src/components/`: tarjetas de reloj, temporizador, cronómetro y configuración.
- `src/services/`: lógica de alertas, audio y almacenamiento local de presets.
- `src/styles/`: tema visual, colores y recursos de interfaz.
- `assets/`: captura de referencia e iconografía.
- `tests/`: pruebas de lógica aisladas de las APIs específicas de Windows.

## Restricciones a validar

La maqueta solicita tarjetas independientes, pin persistente, click-through mediante `WS_EX_TRANSPARENT`, HUD grande y opacidad individual. Antes de diseñar estas partes como capacidades del widget, hay que comprobar qué API proporciona Game Bar y qué operaciones permite el modelo de seguridad de UWP. Si alguna no está disponible, se documentará una alternativa compatible en lugar de prometer comportamiento nativo no soportado.
