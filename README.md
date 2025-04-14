🗂️ Descripción del Script: Organizador de la Carpeta "Descargas" en Python
Este script en Python automatiza la organización de los archivos dentro de la carpeta Descargas del usuario. Su funcionamiento se basa en identificar la extensión de cada archivo y moverlo a una subcarpeta temática, facilitando así la limpieza y orden del directorio.

🧠 ¿Cómo funciona?
Ubicación de la carpeta Descargas:
El script detecta automáticamente la ruta de la carpeta Descargas del usuario actual (~/Downloads).

Clasificación por categorías:
Define un diccionario de subcarpetas y extensiones asociadas:

Documentos: .pdf, .docx, .xlsx, .pptx, .txt

Imágenes: .jpg, .jpeg, .png, .gif

Vídeos: .mp4, .mov, .avi

Programas: .exe, .msi

Comprimidos: .zip, .rar, .7z

Otros: para extensiones no reconocidas

Procesamiento de archivos:

Recorre todos los archivos del directorio.

Verifica si son archivos (ignora carpetas).

Según su extensión, crea (si no existe) la carpeta correspondiente y mueve el archivo.

Si no encuentra coincidencia con ninguna categoría, lo mueve a la carpeta Otros.

🛠️ Librerías utilizadas:
os: Para navegación y manipulación del sistema de archivos.

shutil: Para mover archivos.

os.path: Para manejar rutas de forma multiplataforma.

✅ Características destacadas:
Totalmente automático y no destructivo (no borra nada).

Organiza archivos sin necesidad de intervención manual.

Compatible con Windows, macOS y Linux.

Fácil de extender: puedes añadir más categorías o tipos de archivo fácilmente.
