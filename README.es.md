# FITS Header Editor

> Una herramienta basada en navegador, rápida y segura para inspeccionar, editar, añadir y exportar metadatos de cabecera astronómicos **FITS** (`.fits`, `.fit`, `.fts`) directamente en el lado del cliente.
>
> 🔗 **Herramienta Online**: [https://abctool.info/fits-header-editor-online/es/](https://abctool.info/fits-header-editor-online/es/)
>
> 🌐 [English](README.md) | **Español** | [中文](README.zh.md) | [日本語](README.ja.md)

---

## Descripción General

Tradicionalmente, visualizar y editar los metadatos astronómicos de archivos FITS requería instalar software de escritorio pesado (como SAOImage DS9, AstroImageJ, PixInsight) o ejecutar scripts de Python con `astropy.io.fits`.

**[FITS Header Editor Online](https://abctool.info/fits-header-editor-online/es/)** lleva la capacidad completa de visualización y edición de cabeceras FITS directamente a su navegador web:
- **100% en el lado del cliente y privado**: Los archivos se analizan y procesan completamente en su navegador. Ningún dato astronómico se sube a servidores externos.
- **Sin instalación**: Funciona de forma instantánea en cualquier dispositivo (Windows, macOS, Linux, tablet) con un navegador web moderno.
- **Edición en tiempo real**: Añada, modifique, reordene o elimine tarjetas estándar de 80 caracteres en tiempo real.
- **Exportación flexible**: Guarde y descargue archivos `.fits` modificados al instante, o exporte los metadatos en formatos JSON y TXT.

---

## Guía de Uso

### 1. Cargar el Archivo FITS

Abra [FITS Header Editor Online](https://abctool.info/fits-header-editor-online/es/). Verá la pantalla inicial de carga:

![FITS Header Editor Online - Pantalla de carga](./src/img/1-fits-header-viewer-editor.png)

- **Seleccionar o arrastrar archivo**: Arrastre y suelte su archivo `.fits`, `.fit` o `.fts` en el área designada, o haga clic en **Select FITS File**.
- **Archivo de ejemplo**: ¿Desea probar la herramienta primero? Haga clic en **Load Sample FITS** para cargar un archivo astronómico de ejemplo preconfigurado (`13838SgrA.fits`) con un solo clic.

---

### 2. Inspeccionar y Buscar Metadatos

Una vez cargado el archivo, aparecerá la tabla interactiva del editor de cabeceras:

![FITS Header Editor Online - Interfaz del editor](./src/img/2-fits-header-editor-ui.png)

- **Resumen del archivo**: La barra superior muestra información esencial, como el nombre del archivo, tamaño, número total de tarjetas de cabecera y el tipo de HDU (por ejemplo, `Primary HDU`).
- **Búsqueda instantánea**: Utilice el campo de búsqueda (`Search keywords, values, comments...`) para localizar rápidamente tarjetas por nombre de palabra clave, valor o comentario.
- **Filtros por categoría**: Filtre tarjetas según categorías funcionales estandarizadas:
  - **All**: Vea todas las tarjetas existentes en orden.
  - **Target & Coord**: Nombres de objetos, coordenadas RA/DEC, época astronómica, etc.
  - **Camera & Optics**: Tiempo de exposición, ganancia, filtro, distancia focal y dimensiones de píxel.
  - **WCS Coordinates**: Parámetros de proyección astrométrica (CRVAL, CRPIX, matriz CD).
  - **Structural**: Tarjetas estructurales estándar de FITS (SIMPLE, BITPIX, NAXIS, EXTEND).

---

### 3. Editar, Añadir y Organizar Palabras Clave

La tabla de edición ofrece un control granular completo sobre cada tarjeta:

- **Editar valores y tipos**: Modifique los valores directamente en la fila. Los valores booleanos cuentan con menús desplegables intuitivos (`T (True)` / `F (False)`), mientras que los textos y números se pueden editar en línea.
- **Accesos directos (Quick Helpers)**: Haga clic en botones predefinidos para insertar rápidamente palabras clave astronómicas habituales:
  - `+ OBJECT` (Nombre del objeto celeste)
  - `+ EXPTIME` (Tiempo de exposición en segundos)
  - `+ FILTER` (Filtro óptico)
  - `+ BAYERPAT` (Patrón de matriz Bayer)
  - `+ GAIN` (Ganancia del sensor)
  - `+ FOCALLEN` (Distancia focal del telescopio)
  - `+ PIXSIZE` (Tamaño físico del píxel)
  - `+ OBSERVER` (Nombre del observador o astrofotógrafo)
- **Palabras clave personalizadas**: Haga clic en **+ Add Keyword** para crear cualquier tarjeta FITS con tipos, valores y comentarios personalizados.
- **Reordenar y eliminar**: Use las flechas arriba/abajo (`↑`, `↓`) para cambiar el orden de las tarjetas o haga clic en (`✕`) para eliminar tarjetas innecesarias.
- **Restablecer**: Haga clic en **Reset** en cualquier momento para descartar cambios no guardados y restaurar el archivo original.

---

### 4. Guardar y Exportar

Una vez terminadas las modificaciones:
- **Save & Download FITS**: Vuelve a empaquetar la cabecera actualizada junto con los datos binarios originales en un archivo `.fits` estándar y descárguelo a su dispositivo.
- **Export JSON**: Exporte todas las tarjetas de cabecera como un documento estructurado JSON clave-valor para automatización y análisis por script.
- **Export TXT**: Exporte la representación de texto estándar y limpia de las cabeceras FITS.

---

## Formatos Compatibles y Especificaciones

| Característica | Detalles |
| :--- | :--- |
| **Extensiones compatibles** | `.fits`, `.fit`, `.fts` |
| **Soporte de HDU** | Primary HDU y extensiones de imagen estándar |
| **Cumplimiento de estándares** | Formato estándar de tarjetas de 80 columnas FITS (estándar NASA / IAU) |
| **Seguridad y privacidad** | Ejecución 100% en el navegador (WebAssembly / JavaScript); sin cargas a la nube |

---

## Acceder a la Herramienta

👉 Utilice la herramienta directamente en su navegador: **[https://abctool.info/fits-header-editor-online/es/](https://abctool.info/fits-header-editor-online/es/)**
