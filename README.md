<h1>🧊 Organizador de la Carpeta "Descargas" en Python</h1>

<!-- Portada / Imagen -->
<p align="center">
  <img src="https://cdn.pixabay.com/photo/2014/04/03/10/34/rubiks-cube-310913_1280.png" alt="Rubik's Cube" width="300">
</p>

<p>
  Este script en <strong>Python</strong> organiza automáticamente los archivos de la carpeta <code>Descargas</code> del usuario, clasificándolos en subcarpetas según su tipo. Es una herramienta útil para mantener el directorio limpio, ordenado y facilitar la localización de archivos.
</p>

<h2>⚙️ ¿Cómo funciona?</h2>
<ol>
  <li>Detecta la ruta de la carpeta <code>Descargas</code> del usuario actual (<code>~/Downloads</code>).</li>
  <li>Clasifica los archivos por tipo de extensión en las siguientes categorías:
    <ul>
      <li><strong>Documentos</strong>: .pdf, .docx, .xlsx, .pptx, .txt</li>
      <li><strong>Imágenes</strong>: .jpg, .jpeg, .png, .gif</li>
      <li><strong>Vídeos</strong>: .mp4, .mov, .avi</li>
      <li><strong>Programas</strong>: .exe, .msi</li>
      <li><strong>Comprimidos</strong>: .zip, .rar, .7z</li>
      <li><strong>Otros</strong>: para archivos no clasificados</li>
    </ul>
  </li>
  <li>Crea las subcarpetas necesarias (si no existen).</li>
  <li>Mueve cada archivo a su carpeta correspondiente según su extensión.</li>
</ol>

<h2>📦 Requisitos</h2>
<ul>
  <li>Python 3.x</li>
  <li>Librerías estándar: <code>os</code>, <code>shutil</code></li>
</ul>

<h2>✅ Características</h2>
<ul>
  <li>Automatiza la organización de archivos en <code>Descargas</code>.</li>
  <li>Compatible con Windows, macOS y Linux.</li>
  <li>Fácil de modificar para adaptarse a nuevas extensiones.</li>
  <li>No elimina archivos, solo los mueve a carpetas temáticas.</li>
</ul>

<h2>🚀 Ejecución</h2>
<p>
  Solo necesitas ejecutar el script desde tu terminal o editor de código preferido:
</p>
<pre><code>python organizar_descargas.py</code></pre>

<h2>🛠 Tecnologías utilizadas</h2>
<ul>
  <li><code>os</code>: para navegación y gestión del sistema de archivos.</li>
  <li><code>shutil</code>: para mover archivos entre carpetas.</li>
</ul>

<h2>📁 Estructura esperada después de organizar</h2>
<pre><code>
Descargas/
│
├── Documentos/
├── Imágenes/
├── Vídeos/
├── Programas/
├── Comprimidos/
└── Otros/
</code></pre>

<h2>📌 Nota</h2>
<p>
  Este script está diseñado como una solución sencilla y personalizable. Puedes ampliarlo fácilmente para incluir nuevas categorías o integrarlo con tareas programadas para ejecutarlo automáticamente cada cierto tiempo.
</p>
