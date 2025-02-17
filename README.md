# YouTube Audio Downloader

Este proyecto es una **aplicación web** desarrollada en **Python** utilizando **Flask** y **yt-dlp** que te permite descargar el audio de videos de YouTube en diferentes formatos y calidades.

## Características
- Descarga solo el audio de videos de YouTube.
- Permite seleccionar entre varias calidades de audio disponibles.
- Convierte el audio a **MP3** por defecto (puedes modificarlo en el código).

## Requisitos

### Instalación de Python y dependencias

1. Asegúrate de tener Python instalado. Si no lo tienes, descárgalo desde [aquí](https://www.python.org/downloads/).

2. Clona este repositorio o descarga los archivos manualmente.

3. Instala las dependencias utilizando `pip` y el archivo `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

### Instalación de FFmpeg

Este proyecto requiere **FFmpeg** para convertir el audio descargado a diferentes formatos (como MP3). Sigue estos pasos para instalar **FFmpeg** y configurarlo en tu sistema:

1. **Descarga FFmpeg** desde el siguiente enlace:
   [Descargar FFmpeg (build más reciente)](https://github.com/GyanD/codexffmpeg/releases/download/2024-10-17-git-e1d1ba4cbc/ffmpeg-2024-10-17-git-e1d1ba4cbc-full_build.zip)

2. **Extrae el archivo ZIP** en una carpeta de tu elección, por ejemplo en `C:\ffmpeg`.

3. **Agregar FFmpeg al PATH** (Windows):

   - Presiona `Win + X` y selecciona **Sistema** o accede a **Configuración del sistema**.
   - Haz clic en **Configuración avanzada del sistema** en el panel de la izquierda.
   - En la ventana emergente, haz clic en **Variables de entorno**.
   - En **Variables del sistema**, selecciona `Path` y haz clic en **Editar**.
   - Haz clic en **Nuevo** y agrega la ruta a la carpeta `bin` dentro de la carpeta donde extrajiste FFmpeg, por ejemplo: `C:\ffmpeg\bin`.
   - Haz clic en **Aceptar** para cerrar todas las ventanas.

4. **Verifica la instalación** abriendo una terminal de comandos y ejecutando:

   ```bash
   ffmpeg -version
   ```

   Si ves detalles sobre la versión de **FFmpeg**, entonces está correctamente instalado y agregado al PATH.

## Ejecución del proyecto

1. Una vez instaladas las dependencias y configurado **FFmpeg**, ejecuta el servidor Flask con el siguiente comando:

   ```bash
   python server.py
   ```

2. Abre tu navegador web y ve a `http://localhost:5000`.

3. Pega el enlace de un video de YouTube, selecciona el formato de audio, y descarga el archivo MP3 generado.

## Personalización

- El formato de salida por defecto es **MP3**. Puedes cambiarlo modificando la línea en `app.py` que dice:

   ```python
   'preferredcodec': 'mp3',  # Cambia a 'opus', 'm4a', etc.
   ```

## Contribuir

1. Haz un fork del repositorio.
2. Crea una rama con una nueva funcionalidad (`git checkout -b feature/nueva-funcionalidad`).
3. Haz commit de tus cambios (`git commit -am 'Añadir nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un **Pull Request**.


## Instrucciones adicionales

Si necesitas más ayuda con **FFmpeg**, puedes consultar la documentación oficial en [FFmpeg.org](https://ffmpeg.org/).