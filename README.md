# 🔐 Credentials - Sistema de Gestión de Usuarios

Una aplicación web moderna de gestión de autenticación de usuarios, desarrollada con Angular 19 y Tailwind CSS. Esta aplicación permite a los usuarios registrarse, iniciar sesión y gestionar sus credenciales de forma segura utilizando localStorage.

![Angular](https://img.shields.io/badge/Angular-19.2-DD0031?style=for-the-badge&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.7-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## 📋 Tabla de Contenidos

- [Características](#-características)
- [Tecnologías](#-tecnologías)
- [Requisitos Previos](#-requisitos-previos)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Estructura del Proyecto](#-estructura-del-proyecto)
- [Comandos Disponibles](#-comandos-disponibles)
- [Funcionalidades](#-funcionalidades)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

## ✨ Características

- ✅ **Registro de Usuarios**: Sistema completo de registro con validación de datos
- 🔑 **Autenticación**: Login seguro con validación de credenciales
- 🛡️ **Protección de Rutas**: Guard de autenticación para rutas protegidas
- 👥 **Dashboard de Usuarios**: Visualización de todos los usuarios registrados
- 💾 **Persistencia Local**: Almacenamiento de datos en localStorage
- 📱 **Diseño Responsivo**: Interfaz adaptable a diferentes dispositivos
- 🎨 **UI Moderna**: Diseño limpio y moderno con Tailwind CSS
- ⚡ **Componentes Standalone**: Arquitectura moderna de Angular
- 🔒 **Validación de Formularios**: Validación reactiva de formularios con feedback en tiempo real

## 🛠️ Tecnologías

Este proyecto está construido con las siguientes tecnologías:

- **[Angular 19.2](https://angular.dev/)** - Framework principal
- **[TypeScript 5.7](https://www.typescriptlang.org/)** - Lenguaje de programación
- **[Tailwind CSS 3.4](https://tailwindcss.com/)** - Framework CSS
- **[RxJS 7.8](https://rxjs.dev/)** - Programación reactiva
- **[Angular Router](https://angular.dev/guide/routing)** - Navegación y routing
- **[Angular Forms](https://angular.dev/guide/forms)** - Formularios reactivos
- **[Jasmine](https://jasmine.github.io/)** - Framework de testing
- **[Karma](https://karma-runner.github.io)** - Test runner

## 📦 Requisitos Previos

Antes de comenzar, asegúrate de tener instalado:

- **Node.js** (versión 18.x o superior)
- **npm** (versión 9.x o superior)
- **Angular CLI** (versión 19.x)

Para instalar Angular CLI globalmente:

```bash
npm install -g @angular/cli
```

## 🚀 Instalación

1. **Clonar el repositorio**

```bash
git clone https://github.com/Mariogarluu/Credentials_Angular.git
cd Credentials_Angular
```

2. **Instalar dependencias**

```bash
npm install
```

3. **Iniciar el servidor de desarrollo**

```bash
npm start
# o
ng serve
```

4. **Abrir en el navegador**

Navega a `http://localhost:4200/`. La aplicación se recargará automáticamente cuando realices cambios en los archivos fuente.

## 💻 Uso

### Registro de Usuario

1. Navega a la página de registro en `/register`
2. Completa el formulario con:
   - Nombre completo
   - Email válido
   - Contraseña (mínimo 8 caracteres)
   - Confirmación de contraseña
3. Haz clic en "Registrarse"

### Inicio de Sesión

1. Navega a la página de login en `/login`
2. Ingresa tu email y contraseña
3. Haz clic en "Iniciar Sesión"
4. Serás redirigido al dashboard

### Dashboard

- Visualiza tu información de usuario
- Consulta la lista de todos los usuarios registrados
- Cierra sesión o registra un nuevo usuario

## 📁 Estructura del Proyecto

```
Credentials_Angular/
├── src/
│   ├── app/
│   │   ├── core/
│   │   │   ├── guards/
│   │   │   │   └── auth.guard.ts          # Guard de autenticación
│   │   │   ├── models/
│   │   │   │   └── credentials.ts         # Modelos de datos
│   │   │   └── services/
│   │   │       └── auth.service.ts        # Servicio de autenticación
│   │   ├── pages/
│   │   │   ├── dashboard/
│   │   │   │   ├── dashboard.component.ts
│   │   │   │   ├── dashboard.component.html
│   │   │   │   └── dashboard.component.scss
│   │   │   ├── login/
│   │   │   │   ├── login.component.ts
│   │   │   │   ├── login.component.html
│   │   │   │   └── login.component.scss
│   │   │   └── register/
│   │   │       ├── register.component.ts
│   │   │       ├── register.component.html
│   │   │       └── register.component.scss
│   │   ├── app.component.ts               # Componente raíz
│   │   ├── app.config.ts                  # Configuración de la app
│   │   └── app.routes.ts                  # Configuración de rutas
│   ├── index.html
│   ├── main.ts
│   └── styles.scss                        # Estilos globales
├── public/                                # Archivos estáticos
├── angular.json                           # Configuración de Angular
├── tailwind.config.js                     # Configuración de Tailwind
├── tsconfig.json                          # Configuración de TypeScript
└── package.json                           # Dependencias del proyecto
```

## 🔧 Comandos Disponibles

### Desarrollo

```bash
# Iniciar servidor de desarrollo
npm start
# o
ng serve

# Iniciar con configuración específica
ng serve --configuration development
```

### Construcción

```bash
# Build de producción
npm run build
# o
ng build

# Build de desarrollo
ng build --configuration development

# Build en modo watch
npm run watch
```

### Testing

```bash
# Ejecutar tests unitarios
npm test
# o
ng test

# Tests con coverage
ng test --code-coverage
```

### Generación de Código

```bash
# Generar un componente
ng generate component nombre-componente

# Generar un servicio
ng generate service nombre-servicio

# Generar un guard
ng generate guard nombre-guard

# Ver ayuda de generación
ng generate --help
```

## 🎯 Funcionalidades

### Servicio de Autenticación

El `AuthService` proporciona:

- `register(data: RegisterData)`: Registra un nuevo usuario
- `login(credentials: Credentials)`: Autentica un usuario
- `logout()`: Cierra la sesión del usuario
- `isAuthenticated()`: Verifica si hay un usuario autenticado
- `getAllUsers()`: Obtiene la lista de todos los usuarios
- `user`: Signal que contiene los datos del usuario actual

### Guard de Autenticación

El `authGuard` protege las rutas que requieren autenticación:

- Redirige a `/login` si el usuario no está autenticado
- Permite el acceso si el usuario tiene una sesión válida

### Validaciones de Formularios

- **Email**: Campo requerido y formato de email válido
- **Contraseña**: Campo requerido, mínimo 8 caracteres
- **Confirmación**: Las contraseñas deben coincidir
- **Nombre**: Campo requerido para el registro

## 🤝 Contribuir

Las contribuciones son bienvenidas. Para contribuir:

1. Haz un Fork del proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📝 Licencia

Este proyecto es de código abierto y está disponible para uso educativo y de aprendizaje.

---

## 📞 Contacto

**Mariogarluu** - [@Mariogarluu](https://github.com/Mariogarluu)

Proyecto: [https://github.com/Mariogarluu/Credentials_Angular](https://github.com/Mariogarluu/Credentials_Angular)

---

## 🙏 Recursos Adicionales

- [Documentación de Angular](https://angular.dev/)
- [Guía de Angular CLI](https://angular.dev/tools/cli)
- [Documentación de Tailwind CSS](https://tailwindcss.com/docs)
- [Guía de TypeScript](https://www.typescriptlang.org/docs/)

---

⭐ Si este proyecto te ha sido útil, considera darle una estrella en GitHub!
