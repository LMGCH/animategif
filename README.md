# 🚀 LinkedIn Animated GIF Card Generator

¡Haz que tu perfil destaque en el feed de LinkedIn! Esta es una aplicación web minimalista, ligera y **100% Client-Side** (ejecutada en el navegador) que transforma una foto de perfil estática en una tarjeta animada profesional en formato GIF con un efecto dinámico de radar y mensajes alternos.

Ideal para compartir en publicaciones, artículos o mensajes directos y captar la atención de reclutadores y conexiones estratégicas.

---

## 📸 Demostración Visual

Así es como se ve la tarjeta animada final generada por la herramienta:

<p align="center">
  <img src="https://github.com/LMGCH/animategif/blob/main/mi-presentacion-Red.gif?raw=true" alt="LinkedIn GIF Demo" width="400" style="border-radius: 12px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
</p>

---

## ✨ Características Principales

*   **Procesamiento 100% Local (Client-Side):** No requiere bases de datos, servidores backend ni almacenamiento en la nube. La privacidad del usuario está garantizada, ya que las imágenes se procesan directamente en la memoria temporal del navegador mediante `FileReader` y `Canvas`.
*   **Sin Web Workers (Ultra Compatible):** Configurado específicamente de forma síncrona nativa para evitar bloqueos por rutas relativas en entornos estáticos de hosting.
*   **Despliegue Gratuito e Instantáneo:** Listo para ser alojado en **GitHub Pages** con un solo clic.
*   **Optimizado para LinkedIn:** Genera un archivo binario `.gif` cuadrado de 500x500 píxeles, con un peso menor a 300 KB, asegurando una reproducción fluida e instantánea en el scroll móvil sin ralentizaciones.

---

## 🛠️ Tecnologías Utilizadas

*   **HTML5 & CSS3:** Interfaz moderna optimizada con variables de entorno CSS (`:root`) para alternar estilos de contraste premium y un fondo estilo *Modo Oscuro* (Gris antracita corporativo `#1d2226`).
*   **Canvas API (2D Context):** Renderizado dinámico fotograma a fotograma (patrones de ondas en expansión, máscaras circulares de recorte de imagen y trazados tipográficos adaptables).
*   **JSGif (GIFEncoder.js):** Codificación binaria local de píxeles (`ctx.getImageData`) convertida en flujos estables de objetos URL (`Blob`).

---

## 🚀 Despliegue en 3 Pasos (GitHub Pages)

Si quieres alojar tu propio generador de forma gratuita:

1.  **Clona o haz un Fork** de este repositorio en tu cuenta de GitHub.
2.  Ve a los **Settings** (Ajustes) de tu repositorio.
3.  En el menú lateral izquierdo, selecciona **Pages**. En la sección *Build and deployment*, elige la rama `main` (o `master`) y la carpeta `/root`. Haz clic en **Save**.

¡Listo! En un par de minutos tendrás tu enlace público del tipo `https://github.io`.

---

## 📋 Requisitos del Archivo de Entrada

Para garantizar que el codificador gráfico procese la imagen correctamente, la interfaz web valida e instruye al usuario con las siguientes pautas:
*   **Formatos admitidos:** Únicamente imágenes planas estándar (`.jpg`, `.jpeg`, `.png`).
*   **Formatos restringidos:** Se bloquean formatos pesados de mapa de bits puro (`.bmp`) o impresión (`.tiff`) para evitar congelamiento de la UI.
*   **Peso recomendado:** Archivos de imagen menores a **4 MB** para agilizar los tiempos de renderizado síncrono.

---

## 💡 Buenas Prácticas Implementadas

*   **`encoder.setSize(500, 500)`:** Inicialización obligatoria de dimensiones en el constructor de píxeles para evitar excepciones críticas en el motor de renderizado de la librería.
*   **`URL.createObjectURL(blob)`:** Generación de enlaces de descarga locales eficientes en lugar de cadenas Base64 pesadas, optimizando el rendimiento de la memoria del navegador.
*   **Aislamiento de Ámbitos CSS:** Separación estricta de herencias cromáticas para mantener la legibilidad oscura dentro del formulario (`label`) frente al fondo exterior antracita del sitio web.

---

## 🤝 Contribuciones

Las contribuciones, sugerencias de mejoras visuales o reportes de errores son bienvenidos. Siéntete libre de abrir un *Issue* o enviar un *Pull Request*.

Si este proyecto te ha resultado útil para dinamizar tu red de contactos, ¡no olvides dejar una ⭐ en este repositorio!
