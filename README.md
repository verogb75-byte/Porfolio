# 🎨 Portfolio Personal - Plantilla 

> Plantilla simple y moderna para crear tu portfolio web profesional usando solo HTML, CSS y JavaScript vanilla.

## 📋 Descripción

Este proyecto es una plantilla de portfolio diseñada para estudiantes que quieran mostrar sus proyectos de forma profesional y atractiva. **No utiliza frameworks complejos**, solo tecnologías web básicas que cualquier estudiante puede entender y modificar.

## ✨ Características

- ✅ **100% Responsive** - Se adapta a móviles, tablets y escritorio
- ✅ **Sin dependencias** - Solo HTML, CSS y JavaScript puro
- ✅ **Fácil de personalizar** - Código claro y bien comentado
- ✅ **Animaciones suaves** - Efectos profesionales al hacer scroll
- ✅ **Modal de imágenes** - Amplía las capturas de tus proyectos
- ✅ **Menú móvil funcional** - Hamburguesa menu responsive

## 🚀 Cómo usar

### 1. Descarga el proyecto
```bash
git clone https://github.com/vgb75/portfolio.git
cd portfolio
```

### 2. Abre el archivo HTML
Simplemente abre `main.html` en tu navegador favorito. ¡No necesitas instalar nada!

### 3. Personaliza tu información

#### Cambia tu nombre y enlaces
```html
<strong>Verónica García Bernardo</strong>
<li><a href="Proyectos"
<li><a href="https://github.com/verogb75-byte" target="_blank"">GitHub</a></li>
<li><a href="https://www.linkedin.com/in/ver%C3%B3nica-garc%C3%ADa-b8119b57/?skipRedirect=true" target="_blank">LinkedIn</a></li>
<li><a hrfe="https://www.canva.com/design/DAG7Ll-b2tM/r8LiBosPiMOhvldkZsOpFQ/view?utm_content=DAG7Ll-b2tM&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hf13dd85159" target="_blank">CV</a></li> 
```

#### Actualiza el Hero
```html
<h1 class="hero-title">CURRICULUM VITAE</h1>
<p class="hero-subtitle">PORTFOLIO</p>
```

#### Edita tus proyectos
Cada proyecto tiene esta estructura:
```html
<article class="project-card">
      <div class="project-image-container" onclick="openImageModal(this)">
        <img src="img/galería.png" alt="galería">
       </div>
      <div class="project-information">
        <h3 class="project-title">Mi Galería de Fotos</h3>
        <p class="project-description">
          Galería de Fotos relacionadas con Asturias 
        </p>
        <div class="technology-stack-list">
          <span class="technology-badge">HTML</span>
          <span class="technology-badge">CSS</span>
          <span class="technology-badge">JavaScript</span>
        </div>
        <a href="https://github.com/verogb75-byte/Mis_proyectos_1/tree/main/Mi-Galer-a-de-Fotos" target="_blank" class="button-primary">
          Ver en GitHub
        </a>
      </div>
    </article>
```

## 📁 Estructura del proyecto

```
portfolio/
│
├── main.html          # Archivo principal (TODO EN UNO)
├── README.md           # Este archivo
│
└── img/                # Carpeta para tus imágenes (crear)
    ├── galería.jpg
    ├── portuarios.jpg
    ├── tienda.jpg
    ├── fondo_1.jpg
    └── fondo_2.jpg
```

## 🎨 Personalización de colores

Puedes cambiar el color principal editando estas líneas en el CSS:

```css
/* Busca #e76f0d en el código y cámbialo por tu color favorito */
color: #e76f0d;        /* Naranja por defecto */
background: #e76f0d;   /* Naranja por defecto */

/* Ejemplos de otros colores:
   Azul:    #3498db
   Verde:   #2ecc71
   Morado:  #9b59b6
   Rojo:    #e74c3c
*/
```

## 🖼️ Añadir imágenes a tus proyectos

1. Crea una carpeta llamada `img/` en tu proyecto
2. Guarda las capturas de tus proyectos allí
3. En el HTML, descomenta y actualiza:
```html
<!-- Cambiar esto: -->
🖥️

<!-- Por esto: -->
<img src="img/galería.png" alt="galería">
```

 ## Funcionalidades JavaScript

📱 **Menú de Navegación Móvil**
```js
toggleMobileMenu()
```
Abre o cierra el menú de navegación en dispositivos móviles.
Funcionamiento:
Busca el elemento con ID navigationMenu.
Alterna la clase is-active para mostrar u ocultar el menú.
```js
function toggleMobileMenu()
```

🖼️ **Modal de Imágenes**
```js
openImageModal(element)
```
Abre un modal mostrando la imagen contenida dentro del elemento seleccionado.
Funcionamiento:
Busca una etiqueta <img> dentro del elemento clicado.
Copia la fuente (src) de la imagen al modal.
Activa el modal agregando la clase is-active.
Parámetro:
element: contenedor HTML que incluye una imagen.
```js
function openImageModal(element)
```
```js
closeImageModal()
```
Cierra el modal de imagen.
Funcionamiento:
Elimina la clase is-active del modal.
```js
function closeImageModal()
```

✨ **Animaciones al Hacer Scroll**
**Intersection Observer**
Se utiliza la API IntersectionObserver para animar elementos cuando entran en pantalla.
Funcionamiento:
Observa elementos con la clase .project-card.
Cuando un elemento es visible al menos un 10%, se le añade la clase is-visible.
```js
const scrollObserver = new IntersectionObserver(...)
```
Esto permite aplicar animaciones CSS de forma eficiente.

📌 **Observación de Tarjetas de Proyectos**
Todas las tarjetas con la clase .project-card son observadas para activar animaciones al hacer scroll.
```js
const projectCards = document.querySelectorAll('.project-card');
```

🔗 **Cierre Automático del Menú al Navegar**
Al hacer clic en cualquier enlace del menú de navegación:
Funcionamiento:
Se elimina la clase is-active del menú.
Mejora la experiencia de usuario en dispositivos móviles.
```js
const navigationLinks = document.querySelectorAll('.navigation-menu a');
```

🚀 **Notas Finales**
El script es ligero y eficiente.


## 📚 Tecnologías utilizadas

- **HTML5** - Estructura semántica
- **CSS3** - Estilos y animaciones
  - Flexbox
  - CSS Grid
  - Media Queries
  - Animations
- **JavaScript** - Interactividad
  - Intersection Observer API
  - Event Listeners
  - DOM Manipulation

## 🎓 Proyecto educativo

Esta plantilla fue diseñada para:
- **Estudiantes de desarrollo web** que están aprendiendo
- **Bootcamps y cursos** de programación
- **Programadores junior** que necesitan un portfolio rápido
- **Proyectos escolares** de informática

## 📝 Licencia

Este proyecto es de uso libre para fines educativos. Siéntete libre de modificarlo y adaptarlo a tus necesidades.

## 🤝 Contribuciones

¿Encontraste algún error o tienes una mejora? ¡Las contribuciones son bienvenidas!

1. Haz un Fork del proyecto
2. Crea una rama para tu mejora (`git checkout -b mejora/nueva-funcionalidad`)
3. Haz commit de tus cambios (`git commit -m 'Añade nueva funcionalidad'`)
4. Sube los cambios (`git push origin mejora/nueva-funcionalidad`)
5. Abre un Pull Request

## 💬 Contacto

Si tienes dudas o sugerencias:
- 📧 Email: verogb75@gmail.com
- 💼 LinkedIn:https://www.linkedin.com/in/ver%C3%B3nica-garc%C3%ADa-b8119b57/?skipRedirect=true
- 🐙 GitHub: https://github.com/verogb75-byte

---



Hecho con ❤️ 
