# BotaniCo

BotaniCo es una página web estática que presenta una plataforma para conectar a personas que necesitan ayuda con sus plantas con personas dispuestas a cuidarlas. La página muestra solicitudes en tarjetas interactivas y explica cómo participar en la comunidad.

> Proyecto académico de diseño y desarrollo web realizado en equipo por tres personas.

## Despliegue en vivo
[![Ver en GitHub Pages](https://img.shields.io/badge/Ver_Web-GitHub_Pages-2ea44f?style=for-the-badge&logo=github)](https://deterry69.github.io/BotaniCo/)

## Diseño

Algunos de los recursos visuales utilizados en la página:

| Identidad visual | Fondo de la página |
| --- | --- |
| ![Logotipo de BotaniCo](assets/logo.png) | ![Ilustración botánica del fondo](assets/background.png) |

Ejemplo de imagen utilizada en una tarjeta de solicitud:

![Monstera utilizada en una tarjeta de BotaniCo](https://res.cloudinary.com/da9tytxsu/image/upload/v1791482421/monstera_zmnyls.png)

## Funcionalidades

- Navegación principal y sección de presentación con un formulario visual de búsqueda.
- Tarjetas de solicitudes de cuidado con información de la planta, ubicación aproximada, disponibilidad y perfil de quien publica.
- Giro de las tarjetas para consultar la descripción y los detalles de cada solicitud.
- Secciones informativas sobre cómo funciona la plataforma y cómo ofrecer ayuda.
- Maquetación adaptable a distintos tamaños de pantalla.

La búsqueda, los filtros, el inicio de sesión y el registro forman parte de la interfaz visual; no están conectados a un servidor ni a una base de datos en esta versión.

## Requisitos

- Un navegador web moderno.
- Git para clonar el repositorio.
- Python 3 **o** la extensión Live Server de Visual Studio Code para servir la página localmente.
- Conexión a internet para cargar las fuentes, algunos iconos y las imágenes alojadas en servicios externos.

No hace falta instalar paquetes ni compilar el proyecto.

## Instalación y uso

Clona el repositorio y entra en la carpeta del proyecto:

```bash
git clone https://github.com/deterry69/BotaniCo.git
cd BotaniCo
```

Inicia un servidor local desde esa carpeta:

```bash
python3 -m http.server 8000
```

En Windows también puedes usar:

```powershell
py -m http.server 8000
```

Abre [http://localhost:8000](http://localhost:8000) en el navegador. Para detener el servidor, vuelve a la terminal y pulsa `Ctrl+C`.

Como alternativa, abre la carpeta del proyecto en Visual Studio Code y selecciona **Open with Live Server** sobre `index.html`.

### Variables de entorno

Esta versión es estática y no utiliza backend, claves ni configuración local: **no necesita un archivo `.env`**. No crees uno para ejecutar el proyecto. Si en el futuro se incorporan servicios que requieran credenciales, deben documentarse las variables necesarias en un `.env.example` y mantener los valores secretos fuera del repositorio.

## Arquitectura del proyecto

La aplicación es una página única construida con HTML, CSS y un pequeño fragmento de JavaScript integrado en `index.html`.

```text
BotaniCo/
├── assets/
│   ├── background.png
│   ├── logo.png
│   └── icons/
├── index.html
├── styles.css
└── README.md
```

- **`index.html`** contiene la estructura semántica de la página: navegación, presentación y formulario, tarjetas, sección informativa y pie de página. También contiene la función JavaScript que activa el giro de las tarjetas.
- **`styles.css`** define la identidad visual, los componentes, la disposición adaptable y las animaciones. Las tarjetas usan transformaciones 3D y una clase que alterna JavaScript.
- **`assets/`** contiene el logotipo, el fondo y los iconos SVG de cuidados.
- **Recursos externos:** las fuentes se cargan desde Google Fonts, algunos de los iconos de interfaz desde Font Awesome y las fotografías de las tarjetas desde Cloudinary.

### Convención CSS: BEM

Los nombres de clase CSS siguen la convención **BEM** (*Block, Element, Modifier*): `bloque__elemento--modificador`. El bloque representa un componente independiente; el elemento, una parte de ese bloque; y el modificador, una variante o estado. Por ejemplo, `cards__card` identifica una tarjeta del bloque `cards`, y `cards__card--flipped` representa su estado girado.

## Organización del equipo

El trabajo se repartió entre tres integrantes y se integró mediante ramas de Git:

| Rama | Trabajo |
| --- | --- |
| `nav-hero` | Navegación y sección de presentación (nav-hero) |
| `cards-section` | Sección de tarjetas |
| `how-it-works-footer` | Sección how-it-works y footer|
| `dev` | Rama de integración del desarrollo. |
| `main` | Rama principal del repositorio. |

Figma se utilizó para el diseño, Visual Studio Code para el desarrollo y Trello para organizar el trabajo. La planificación se basó en sprints semanales durante dos semanas, con reparto de tareas y puesta en común del avance.

## Próximos pasos

- Conectar la búsqueda y los filtros de cuidados a solicitudes reales.
- Implementar el registro, el inicio de sesión y las acciones de contacto y favoritos.
- Completar o ajustar las secciones de destino de los enlaces de navegación.
- Añadir pruebas de accesibilidad y comprobar la experiencia en distintos dispositivos y navegadores.
- Valorar la separación del JavaScript y la gestión de imágenes y otros recursos externos.

## Miembros

- Daniel Pavón Téllez [GitHub](https://github.com/Daaniel-Sans) 
- Luis Ruiz Hinojosa [GitHub](https://github.com/Hiiinojosaa) 
- Alfonso José de Terry Pérez [GitHub](https://github.com/deterry69)

