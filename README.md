# Migrar TrueNAS de USB a USB · Migrate TrueNAS from USB to USB

🇪🇸 [Español](#español) · 🇬🇧 [English](#english)

---

## Español

Guía visual paso a paso para **reemplazar el dispositivo de arranque de TrueNAS** (USB, DOM o SSD pequeño) conservando pools ZFS, datasets, shares, usuarios y configuración.

### Contenido

| Paso | Qué cubre |
|------|-----------|
| Visión general | Por qué el SO y los datos son independientes |
| 01 | Backup de la configuración (con *Export Password Secret Seed*) |
| 02 | Anotar pools y estado de discos |
| 03 | Apagado limpio |
| 04 | Crear el instalador (Etcher / Rufus / `dd`) e instalar |
| 05 | Importar las pools ZFS (WebUI y consola) |
| 06 | Restaurar la configuración |
| 07 | Verificación final y *scrub* |
| Extra | Problemas comunes y tips (espejo de arranque, backup automático por cron) |

### Idioma

La página está en **español e inglés**. Usa el selector **ES / EN** (arriba a la derecha) o el parámetro `?lang=en` / `?lang=es`. Sin preferencia guardada se usa el idioma del navegador.

### Ver la guía

- Online (si GitHub Pages está activo en el repo): https://serverheaven.github.io/Migrate-TrueNas-Scale/?lang=en
- En local: abre `index.html` o ejecuta `python3 -m http.server 8000` y visita <http://localhost:8000>. Solo carga tipografías de Google Fonts; sin conexión usa las del sistema.

### Estructura

Un único `index.html` autocontenido (HTML + CSS + JS). Las traducciones al inglés están en el bloque `<script id="i18n-data">` al final del archivo, indexadas por el texto original en español: si editas un texto en español, añade/actualiza su entrada para que también cambie en inglés.

### Referencias oficiales

- [Manage Configuration (TrueNAS Docs)](https://www.truenas.com/docs/scale/25.10/scaletutorials/systemsettings/advanced/managesysconfig/)
- [Descargas de TrueNAS](https://www.truenas.com/download/)
- [TrueNAS Documentation Hub](https://www.truenas.com/docs/)

> ⚠️ Material comunitario, **no es documentación oficial** de iXsystems. Haz siempre backup de la configuración y verifica con la documentación de tu versión antes de actuar sobre datos reales.

---

## English

Visual step-by-step guide to **replace the TrueNAS boot device** (USB, DOM or small SSD) while keeping your ZFS pools, datasets, shares, users and configuration.

### Contents

| Step | Covers |
|------|--------|
| Overview | Why the OS and the data are independent |
| 01 | Configuration backup (with *Export Password Secret Seed*) |
| 02 | Noting pools and disk status |
| 03 | Clean shutdown |
| 04 | Creating the installer (Etcher / Rufus / `dd`) and installing |
| 05 | Importing the ZFS pools (WebUI and console) |
| 06 | Restoring the configuration |
| 07 | Final verification and *scrub* |
| Extra | Common problems and tips (boot mirror, automatic cron backup) |

### Language

The page is **bilingual (Spanish / English)**. Use the **ES / EN** switch (top right) or the `?lang=en` / `?lang=es` parameter. With no saved preference it follows the browser language.

### Viewing the guide

- Online (if GitHub Pages is enabled on the repo): `https://serverheaven.github.io/migrate-truenas-scale/`
- Locally: open `index.html`, or run `python3 -m http.server 8000` and visit <http://localhost:8000>. It only loads Google Fonts; offline it falls back to system fonts.

### Structure

A single self-contained `index.html` (HTML + CSS + JS). The English translations live in the `<script id="i18n-data">` block at the end of the file, keyed by the original Spanish text: if you edit a Spanish string, add/update its entry so the English version changes too.

### Official references

- [Manage Configuration (TrueNAS Docs)](https://www.truenas.com/docs/scale/25.10/scaletutorials/systemsettings/advanced/managesysconfig/)
- [TrueNAS downloads](https://www.truenas.com/download/)
- [TrueNAS Documentation Hub](https://www.truenas.com/docs/)

> ⚠️ Community material, **not official iXsystems documentation**. Always back up your configuration and check the docs for your version before acting on real data.
