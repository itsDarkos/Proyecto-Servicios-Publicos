# Proyecto React con Autenticación y Roles

Este es el frontend de una aplicación web construida con React. La aplicación cuenta con un sistema de autenticación de usuarios, gestión de sesiones y control de acceso basado en roles (administradores y usuarios regulares).

## ✨ Características

- **Autenticación de Usuarios:** Sistema completo de registro e inicio de sesión.
- **Rutas Protegidas:** Ciertas secciones de la web solo son accesibles para usuarios autenticados.
- **Control de Acceso por Roles:**
  - Rutas exclusivas para administradores.
  - Rutas para usuarios regulares.
- **Gestión de Perfil de Usuario:** Los usuarios pueden ver y gestionar la información de su cuenta.
- **Diseño Responsivo:** Interfaz adaptable a diferentes tamaños de pantalla gracias a Bootstrap.

## 🚀 Tecnologías Utilizadas

Este proyecto es una aplicación de una sola página (SPA) construida con las siguientes tecnologías:

### Frontend

- **React:** Biblioteca principal para la construcción de la interfaz de usuario.
- **React Router DOM:** Para la gestión de rutas en la aplicación.
- **React Hook Form:** Para la gestión de formularios y validaciones.
- **Axios:** Para realizar peticiones HTTP al backend.
- **Bootstrap y React-Bootstrap:** Para el diseño y los componentes de la interfaz.
- **Styled-components:** Para estilos personalizados a nivel de componentes.

### Backend (Asumido)

Aunque el código del backend no se encuentra en este repositorio, el `package.json` sugiere que está construido con:

- **Node.js con Express:** Como entorno de ejecución y framework para el servidor.
- **MongoDB con Mongoose:** Como base de datos y ODM para modelar los datos.
- **bcrypt:** Para el hasheo y la seguridad de las contraseñas.

## 🔧 Instalación y Puesta en Marcha

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

1. **Clona el repositorio:**

   ```bash
   git clone <URL-DEL-REPOSITORIO>
   ```

2. **Navega al directorio del proyecto:**

   ```bash
   cd <NOMBRE-DEL-DIRECTORIO>
   ```

3. **Instala las dependencias:**

   Asegúrate de tener [Node.js](https://nodejs.org/) y [npm](https://www.npmjs.com/) instalados.

   ```bash
   npm install
   ```

## 📜 Scripts Disponibles

En el directorio del proyecto, puedes ejecutar los siguientes comandos:

### `npm start`

Ejecuta la aplicación en modo de desarrollo.
Abre [http://localhost:3000](http://localhost:3000) para verla en tu navegador.

La página se recargará automáticamente si realizas cambios en el código.

### `npm test`

Lanza el corredor de pruebas en modo interactivo.

### `npm run build`

Construye la aplicación para producción en la carpeta `build`.
Empaqueta React correctamente en modo de producción y optimiza la compilación para obtener el mejor rendimiento.

## 📁 Estructura del Proyecto

El código fuente de la aplicación se encuentra en el directorio `src`. Aquí tienes un resumen de la estructura:

```
src/
├── assets/         # Imágenes, iconos y otros recursos estáticos
├── Components/     # Componentes reutilizables de React
│   ├── Auth/       # Lógica de autenticación (AuthProvider, useAuth)
│   ├── Cards/      # Componentes de tarjetas
│   ├── Hooks/      # Hooks personalizados
│   ├── Layout/     # Componente principal de la estructura (Layout)
│   ├── Navigations # Barra de navegación
│   ├── Routers/    # Configuración de rutas (públicas y privadas)
│   └── ...
├── pages/          # Vistas principales de la aplicación
│   ├── Home/
│   ├── Login/
│   ├── Register/
│   ├── Consulta/   # Página para usuarios regulares
│   ├── CRUD/       # Páginas de administrador
│   └── Usuario/    # Perfil del usuario
├── index.js        # Punto de entrada de la aplicación
└── App.js          # Componente raíz que carga el enrutador
```

## 🗺️ Rutas de la Aplicación

La aplicación utiliza `react-router-dom` para gestionar la navegación. Las rutas principales son:

- **Rutas Públicas:**
  - `/`: Página de inicio.
  - `/login`: Página de inicio de sesión.
  - `/register`: Página de registro de nuevos usuarios.

- **Rutas Privadas (Requieren autenticación):**
  - `/mi-cuenta`: Perfil del usuario.
  - `/consultas`: Accesible solo para usuarios con rol `regular`.
  - `/admin/users`: Accesible solo para usuarios con rol `admin`.

- **Ruta Comodín:**
  - `*`: Cualquier otra ruta no definida redirige a la página de inicio.
