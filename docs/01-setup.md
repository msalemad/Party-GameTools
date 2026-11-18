# Preparación del entorno

## Antes de instalar herramientas

La versión de Windows, la plantilla de proyecto y el paquete del Xbox Game Bar SDK deben verificarse juntos en la máquina de desarrollo. Comienza revisando la documentación vigente de Microsoft y las muestras oficiales de Xbox Game Bar; evita copiar manifiestos o comandos de versiones antiguas sin comprobarlos.

## Comprobaciones iniciales

1. Confirma que el equipo de desarrollo usa Windows 10/11 y que Xbox Game Bar está instalado y actualizado.
2. Instala Visual Studio 2022 con las herramientas de desarrollo UWP/Windows disponibles para la versión de Windows objetivo.
3. Instala un Windows SDK compatible con la muestra oficial seleccionada.
4. Revisa el README y los archivos del proyecto de una muestra oficial para identificar el SDK, NuGet, manifest declarations y pasos de ejecución que realmente requiere.
5. Solo instala Node.js/TypeScript si la arquitectura elegida usa una capa web; no es un requisito asumido para UWP/XAML.
6. Habilita las opciones de desarrollador o sideloading únicamente cuando vayas a probar un paquete local y siguiendo las instrucciones oficiales de Windows.

## Información que falta para fijar el proyecto

- Versión y edición de Windows
- Versión de Visual Studio y cargas de trabajo instaladas
- Muestra/versión del Game Bar SDK que se usará

No se crea aún un manifiesto de paquete inventado: sus extensiones deben corresponder al SDK y a la plantilla elegidos.
