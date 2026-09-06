# HACKdeck

### Encuentra el evento adecuado. Visualiza las fechas. Reserva tiempo para crear.

[Explorar HACKdeck](https://hackdeck-app.vercel.app/) · [English](README.md) · [简体中文](README.zh-CN.md)

HACKdeck es una plataforma multilingüe para descubrir hackatones, build weeks y programas para desarrolladores. Organiza anuncios dispersos en una colección cronológica de tarjetas para comparar oportunidades antes de comprometer tiempo.

## Funciones

- Línea de tiempo desplazable con tarjetas ordenadas por fecha.
- Filtros por organizador, ubicación, participación remota, fechas, plazos, premios, requisitos, formato y estado.
- Detalles con enlaces a fuentes oficiales o de la organización.
- Interfaces en inglés, chino mandarín simplificado y español.
- Eventos guardados en el navegador sin crear una cuenta.
- Exportación e importación JSON para trasladar una selección a otro navegador o dispositivo.
- Diseño adaptable a pantallas grandes y pequeñas.

## Enfoque del producto

Un directorio muestra qué eventos existen. Para planificar también hay que entender los plazos, los solapamientos, las modalidades de participación y los requisitos. HACKdeck reúne esos detalles en una línea de tiempo visual para facilitar la comparación y la selección.

## Cómo usarlo

Abre el sitio, elige un idioma y ajusta los filtros. Explora las tarjetas y consulta los detalles. Comprueba la información actual del organizador antes de solicitar una plaza. Guarda los eventos que te interesen y exporta un archivo JSON si cambias de navegador.

## Fuentes y actualización

El catálogo se selecciona a partir de fuentes oficiales de empresas, universidades y organizadores. Una organización supervisada es una pista de búsqueda, no un evento confirmado.

El catálogo no garantiza información en tiempo real. Las fechas, los requisitos, los premios y las reglas pueden cambiar. Consulta siempre la fuente original. El validador señala registros que necesitan mantenimiento, incluidos eventos finalizados pendientes de archivar.

## Implementación

El proyecto utiliza React 19, Vite, Tailwind CSS, Radix UI, iconos Lucide y efectos visuales OGL.

- `src/App.jsx`: línea de tiempo, filtros, detalles y selección guardada.
- `src/data/events.js`: eventos y metadatos de las fuentes.
- `src/data/i18n.js`: traducciones de la interfaz.
- `scripts/validate-events.mjs`: comprobaciones del catálogo.

## Desarrollo local

Requiere Node.js 20 o posterior y pnpm.

```bash
pnpm install --frozen-lockfile
pnpm dev
```

Abre la dirección local indicada por Vite.

```bash
pnpm validate:data
pnpm build
pnpm preview
```

La validación de datos y la compilación son comprobaciones distintas. Revisa los hallazgos del catálogo contra las fuentes originales antes de publicar cambios en los eventos.

## Privacidad

Los eventos guardados permanecen en el almacenamiento local del navegador; no se necesita una cuenta ni se carga esa selección en un servidor. Borrar el almacenamiento puede eliminarla. La exportación e importación JSON permiten realizar copias de seguridad, pero no proporcionan sincronización automática entre dispositivos.

## Contribuir

Para añadir o corregir un evento, incluye una fuente oficial, conserva los datos desconocidos, revisa identificadores y enlaces duplicados, y archiva los eventos finalizados. Los cambios de interfaz deben mantener el acceso por teclado, las etiquetas claras, el diseño adaptable y los tres idiomas.

## Copyright

Copyright © 2026 Jiexi Yang. All rights reserved.
This project is publicly available for viewing and portfolio evaluation only.
