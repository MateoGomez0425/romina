# Romina Honeker — Numeróloga · Diseñadora Humana

Página web con scheduler de turnos para sesiones de numerología y diseño humano.

## 🚀 Instalación

1. **Cloná el repositorio** (solo archivos públicos):
   ```bash
   git clone <repo-url>
   cd Romina
   ```

2. **Configurá los secretos locales:**
   ```bash
   cp config.example.js config.js
   ```
   Editá `config.js` y pegá la URL de tu Google Apps Script.

3. **Abrí `index.html`** en tu navegador o subilo a tu servidor web.

## 🔒 Archivos ignorados por Git

| Archivo | Contenido | ¿Por qué se ignora? |
|---------|-----------|---------------------|
| `config.js` | URL del Web App | Expone la URL del script |
| `code.gs` | Código del Apps Script con emails | Contiene `CALENDAR_ID` (`rh.esenciasyluz@gmail.com`) y `NOTIFICATION_EMAIL` |
| `appsscript.json` | Config del Apps Script | Expone los scopes y servicios habilitados |

## 🔧 Configuración del Google Apps Script

1. Andá a [https://script.google.com](https://script.google.com)
2. Creá un proyecto nuevo, pegá el contenido de `code.gs`
3. Activá **Calendar API** en Servicios (menú izquierdo > "+" > Calendar API v3)
4. **Settings > Project Settings > Show `appsscript.json` manifest file**
5. Pegá el contenido de `appsscript.json`
6. Ejecutá `doPost` para autorizar permisos
7. **Deploy > New deployment > Web app** (Execute as: Me, Who has access: Anyone)
8. Copiá la URL y pegala en `config.js`

## 📁 Estructura del proyecto

```
Romina/
├── index.html           # Página web principal
├── config.js            # Config local (NO subir a GitHub)
├── config.example.js    # Template de configuración
├── code.gs              # Google Apps Script (NO subir a GitHub)
├── appsscript.json       # Manifest de Apps Script (NO subir a GitHub)
└── .gitignore           # Archivos ignorados
```

## 🛠 Tecnologías

- HTML + CSS + JavaScript (vanilla, sin frameworks)
- Google Apps Script (backend sin servidor)
- Google Calendar API v3
- Google Fonts (Playfair Display + Montserrat)