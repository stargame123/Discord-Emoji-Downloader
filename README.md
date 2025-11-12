# 🎭 Discord Emoji Downloader

> Descarga emojis y stickers de tus servidores Discord de forma masiva en un único archivo ZIP.

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/stargame123/Discord-Emoji-Downloader?style=social)](https://github.com/stargame123/Discord-Emoji-Downloader)

## 🚀 Características

✨ **Descarga Masiva de Emojis**
- Descarga todos los emojis personalizados de tus servidores
- Selecciona los emojis que deseas descargar
- Obtén imágenes de alta calidad en formato PNG

🎨 **Soporte para Stickers**
- Descarga stickers de los servidores Discord
- Selecciona stickers individuales
- Imágenes en formato WebP de alta resolución

🔐 **Seguridad y Privacidad**
- Token almacenado localmente en el navegador
- No se almacenan datos en servidores externos
- Código de fuente abierta verificable
- Funcionamiento 100% local

⚡ **Interfaz Moderna y Rápida**
- Diseño responsivo y atractivo
- Interfaz intuitiva paso a paso
- Indicadores de progreso en tiempo real
- Navegación fluida entre pasos

📦 **Descarga Organizada**
- Los archivos se descargan en un ZIP organizado
- Carpetas separadas para emojis y stickers
- Nombres descriptivos para cada archivo
- Timestamp automático en el nombre del archivo

## 📋 Requisitos

- Navegador web moderno (Chrome, Firefox, Safari, Edge)
- Token de usuario de Discord
- Conexión a Internet

## 🔧 Cómo Obtener tu Token de Discord

1. Abre Discord en tu navegador (o la aplicación)
2. Abre las herramientas de desarrollador: `Ctrl + Shift + I` (Windows) o `Cmd + Option + I` (Mac)
3. Ve a la pestaña **Console**
4. Ejecuta este comando:
```javascript
setInterval(() => {
  fetch('https://canary.discord.com/api/v10/users/@me', {
    headers: {'Authorization': 'Bearer [TU_TOKEN]'}
  })
}, 50000);
```
5. Abre la pestaña **Network**
6. En los headers de cualquier solicitud, busca el header `Authorization`
7. Copia el valor (es tu token)

> **⚠️ IMPORTANTE:** Nunca compartas tu token con nadie. Solo úsalo en esta aplicación de confianza.

## 📖 Instrucciones de Uso

### Opción 1: Usar la Aplicación Web

1. **Abre la aplicación**: Ve a [stargame123.github.io/Discord-Emoji-Downloader](https://stargame123.github.io/Discord-Emoji-Downloader/)

2. **Paso 1 - Autenticación**
   - Ingresa tu token de usuario de Discord
   - Haz clic en "Continuar"

3. **Paso 2 - Selecciona Servidor**
   - Elige el servidor del que deseas descargar emojis
   - Haz clic en "Continuar"

4. **Paso 3 - Selecciona Emojis**
   - Visualiza todos los emojis disponibles del servidor
   - Selecciona los emojis que deseas descargar
   - Usa "Seleccionar todos" para elegir todos a la vez
   - Usa "Desmarcar todos" para deseleccionar
   - Haz clic en "Continuar"

5. **Paso 4 - Selecciona Stickers**
   - Visualiza todos los stickers disponibles
   - Selecciona los stickers que deseas descargar
   - Usa los botones de selección rápida si lo necesitas
   - Haz clic en "Continuar"

6. **Paso 5 - Vista Previa**
   - Revisa los emojis y stickers seleccionados
   - Verifica que todo sea correcto
   - Haz clic en "Descargar ZIP" para obtener tu archivo

7. **Recibe tu Descarga**
   - El archivo ZIP se descargará automáticamente
   - Nombre: `discord-emojis-[timestamp].zip`
   - Contiene dos carpetas: `emojis/` y `stickers/`

### Opción 2: Ejecutar Localmente

```bash
# Clonar el repositorio
git clone https://github.com/stargame123/Discord-Emoji-Downloader.git

# Entrar al directorio
cd Discord-Emoji-Downloader

# Abrir en navegador (desde la carpeta raíz)
open index.html
```

## 🏗️ Estructura del Proyecto

```
Discord-Emoji-Downloader/
├── index.html          # Aplicación web principal
├── README.md           # Este archivo
└── package.json        # Información del proyecto
```

## 💻 Stack Tecnológico

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **API**: Discord API v10
- **Librerías**:
  - JSZip: Para crear archivos ZIP
  - Fetch API: Para realizar solicitudes HTTP
- **Almacenamiento**: SessionStorage (local del navegador)

## 🔄 Flujo de la Aplicación

```
┌─────────────────────┐
│  Paso 1: Login      │  → Valida token de Discord
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Paso 2: Servidores  │  → Lista tus servidores
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  Paso 3: Emojis     │  → Selecciona emojis
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Paso 4: Stickers    │  → Selecciona stickers
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ Paso 5: Descarga    │  → Descarga como ZIP
└─────────────────────┘
```

## 🎯 Funcionalidades Principales

### Autenticación Segura
- Valida tokens directamente con Discord API
- Almacenamiento local (no en servidores)
- Sin almacenamiento persistente

### Gestión de Servidores
- Lista todos tus servidores Discord
- Muestra iconos de servidor
- Selección fácil por radio button

### Selección Avanzada
- Checkboxes individuales para cada emoji/sticker
- Botones "Seleccionar todos" para rapidez
- Botones "Desmarcar todos" para limpiar
- Contadores en tiempo real
- Estado visual de selección

### Descarga Inteligente
- Progreso en tiempo real durante la descarga
- Organización automática en carpetas
- Nombres descriptivos de archivos
- Formato ZIP comprimido

### Navegación Fluida
- Botones "Atrás" en todos los pasos
- Retorno al inicio en cualquier momento
- Preservación de selecciones al navegar

## 🖼️ Formatos de Descarga

| Tipo | Formato | Ubicación |
|------|---------|----------|
| Emojis | PNG | `/emojis/` |
| Stickers | WebP | `/stickers/` |

## ⚙️ Configuración Técnica

### Endpoints de Discord API Utilizados

```javascript
GET  /users/@me                    // Obtener info del usuario
GET  /users/@me/guilds             // Listar servidores
GET  /guilds/{id}                  // Obtener datos del servidor
GET  /guilds/{id}/stickers         // Obtener stickers del servidor
```

### CDN de Discord

```
Emojis: https://cdn.discordapp.com/emojis/{id}.png
Stickers: https://media.discordapp.net/stickers/{id}.webp
```

## 🔒 Privacidad y Seguridad

- ✅ Los tokens NO se envían a servidores terceros
- ✅ Todo funciona en tu navegador local
- ✅ SessionStorage se limpia al cerrar la sesión
- ✅ Código verificable de fuente abierta
- ✅ HTTPS en la aplicación web

## 🐛 Solución de Problemas

### "Token inválido o error de conexión"
- Verifica que tu token sea correcto
- Asegúrate de que Discord API sea accesible
- Intenta obtener un nuevo token

### "Error al descargar"
- Verifica tu conexión a Internet
- Intenta con menos archivos
- Recarga la página e intenta de nuevo

### "Los emojis no cargan"
- Algunos emojis pueden estar fuera de servicio
- Intenta refrescar la página
- Verifica que tengas permisos en el servidor

## 🚧 Roadmap Futuro

- [ ] Descarga individual de emojis/stickers
- [ ] Filtro por tipo de emoji
- [ ] Vista previa en tiempo real
- [ ] Soporte para más formatos
- [ ] Exportación a diferentes formatos
- [ ] Interfaz multiidioma

## 📝 Licencia

Este proyecto está bajo la licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios grandes:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📞 Soporte

Si encuentras problemas o tienes sugerencias:

- Abre un [Issue](https://github.com/stargame123/Discord-Emoji-Downloader/issues)
- Incluye detalles de tu problema
- Proporciona pasos para reproducir el error

## 👨‍💻 Autor

**stargame123** - Discord Emoji Downloader

- GitHub: [@stargame123](https://github.com/stargame123)
- Proyecto: [Discord-Emoji-Downloader](https://github.com/stargame123/Discord-Emoji-Downloader)

## ⭐ Agradecimientos

- Discord API por proporcionar acceso a los datos
- JSZip por la funcionalidad de compresión ZIP
- Comunidad de GitHub por el feedback

---

<div align="center">

**Hecho con ❤️ por [stargame123](https://github.com/stargame123)**

[⬆ volver arriba](#-discord-emoji-downloader)

</div>
