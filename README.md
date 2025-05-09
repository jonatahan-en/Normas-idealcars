# Normas-idealcars

## Introducción

IdealCars es una plataforma diseñada para facilitar la compra, venta y gestión de anuncios de vehículos. Este proyecto tiene como objetivo ofrecer una experiencia intuitiva y funcional tanto para propietarios como para compradores.

## Normas del Proyecto

1. **Cumplir con los plazos:** Respetar los tiempos establecidos para cada tarea.
2. **Trabajo en ramas:** Todo el código que trabajemos debe estar en una rama creada a partir de `develop`.
3. **Merge a `develop`:** Solo se realizará un merge a la rama `develop` cuando el trabajo esté completo, funcione correctamente y haya sido testeado.
4. **Colaboración:** Es muy importante que los 5 contribuyamos al proyecto, ya que al final todos dependemos de todos.
5. **reuniones** reuniones de 30 minutos maximo para informar de los avances, dudas y sobre todo si  vamos por el mismo camino toods

## Objetivos del Proyecto

### Objetivos Básicos (MVP)

1. **Register:** Permitir a los usuarios registrarse en la plataforma.
2. **Login:** Autenticar a los usuarios para acceder a sus cuentas.
3. **Editar anuncio:** Los propietarios podrán modificar o eliminar sus anuncios.
4. **Lista de anuncios:** Mostrar todos los anuncios disponibles en la plataforma.
5. **Crear anuncio:** Permitir a los usuarios publicar nuevos anuncios.
6. **Logout:** Cerrar sesión de manera segura.
7. **Contacto con el usuario:**
   - **Por email:** Enviar mensajes directamente desde la plataforma.
   - **Por chat:** Comunicación en tiempo real entre usuarios.
8. **Detalle de anuncio** Crear una pagina donde podamos ver los detalles del anuncio

9. **css** en el css es muy importante dejar los botones enlaces para los diferentes funciones que vamos añadir


### implementacion terminada 

1. **Baja de usuario** Crear un boton para dar de baja al usuario de la plataforma 

### Objetivos Extras (Funcionalidades Adicionales)

1. Recuperación de contraseña.
2. Compartir anuncio en redes sociales.

3. Actualización de datos de usuario.
4. Crear un Facebook y Twitter para redirigir desde el footer.
5. Marcar y desmarcar anuncio como reservado.
6. Marcar y desmarcar anuncio como favorito.

## Guía de Git

### Crear una nueva rama

1. Cambiar a la rama `develop`

   ```bash
   git checkout develop
   ```

2. Actualizar la rama `develop`

    ```bash
    git pull origin develop
    ```

3. Crear una nueva rama

    ```bash
    git checkout -b nombre-de-tu-rama
    ```

### subir cambios

```bash
git add .
git commit -m "description"
git push origin nombre-de-tu-rama
```

### Hacer un merge`develop`

1. cambiar de rama 
2. actualizar la rama
3. hacer un merge de tu rama
4. subir los cambios a develop

```bash
git checkout develop
git pull origin develop
git merge nombre de tu rama
git push origin develop
```

### Actualizar tu rama

1. cambiar a tu rama 
2. bajar los cambios 

```bash
git checkout nombre-de-tu-rama
git pull origin develop

```


## Trabajos a realizar :

1. *Ruben y Juan* Realizar stylos de  pagina principal,estylos en las paginas login,crear-product, registro ,  este proceso incluye "Responsive Desing"
2. *Jorge*  Realiza la implementaicon del imail de contacto entre usuarios 
3. *Jose* Realiza la implementacion del detalle del anuncio
4. *Jonathan* Realiza la implementacion del chat entre usuarios 

```bash
# System Context

## I am working on a software system with the following directory structure, architecture, and analyzed files:

## Directory Structure
```
idealCars
├── Controllers
│   ├── api
│   │   ├── user
│   │   │   ├── loginApiController.js
│   │   │   ├── ProfileApiController.js
│   │   │   ├── signoutApiController.js
│   │   │   └── signupApiController.js
│   │   └── apiProductsController.js
│   ├── chatController.js
│   ├── contactController.js
│   ├── homeController.js
│   ├── loginController.js
│   ├── myProductsController.js
│   ├── productController.js
│   ├── profileController.js
│   ├── signoutController.js
│   └── signupController.js
├── lib
│   ├── connectMongoose.js
│   ├── emailManager.js
│   ├── i18nConfigure.js
│   ├── jwtAuthMiddlewere.js
│   ├── sessionManager.js
│   ├── uploadConfigure.js
│   └── utils.js
├── locales
│   ├── en.json
│   ├── es.json
│   └── pt.json
├── models
│   ├── Message.js
│   ├── Products.js
│   └── User.js
├── public
│   ├── css
│   │   ├── chat.css
│   │   ├── email.css
│   │   ├── myProduct.css
│   │   ├── product-detail.css
│   │   ├── splash.css
│   │   └── styles.css
│   ├── flags
│   │   ├── en.png
│   │   ├── es.png
│   │   ├── fr.png
│   │   ├── prt.png
│   │   └── ro.png
│   ├── imagenes
│   │   └── .gitignore
│   ├── logo
│   │   ├── Logo_IdealCars.png
│   │   ├── logo.png
│   │   └── logo.svg
│   └── redes sociales
│       ├── IG_bd_black.png
│       ├── IG_bd_white.png
│       ├── tw_bd_black.png
│       └── tw_bd_white.png
├── views
│   ├── chat.ejs
│   ├── editProduct.ejs
│   ├── email.ejs
│   ├── error.ejs
│   ├── footer.ejs
│   ├── header.ejs
│   ├── home.ejs
│   ├── login.ejs
│   ├── myProduct.ejs
│   ├── new-product.ejs
│   ├── product-detail.ejs
│   ├── profile.ejs
│   ├── signout.ejs
│   └── signup.ejs
├── app.js
├── initDB.js
├── package-lock.json
├── package.json
├── server.js
└── webSocketServer.js

```

## Mermaid Diagram
```mermaid
graph TD

    2108["End User<br>External Actor"]
    2109["MongoDB Database<br>NoSQL RDBMS"]
    2110["External Email Service<br>SMTP/API Provider"]
    2111["WebSocket Clients<br>User Browsers/Apps"]
    subgraph 2103["IdealCars Platform"]
        subgraph 2104["IdealCars Application Container"]
            2107["Application Logic"]
            2112["Web Server &amp; App Core<br>Node.js, Express.js"]
            2113["WebSocket Handler<br>Socket.IO"]
            2125["Database Initialization Utility<br>Node.js Script"]
            subgraph 2105["Core Services & Libraries"]
                2119["Database Connector<br>Mongoose"]
                2120["Session Management<br>Express Session, MongoDB Store"]
                2121["Authentication Middleware<br>JWT Guard"]
                2122["Email Utility<br>Nodemailer (assumed)"]
                2123["I18n Configuration<br>i18n"]
                2124["File Upload Configuration<br>Multer (assumed)"]
            end
            subgraph 2106["Domain Models"]
                2116["User Model<br>Mongoose Schema"]
                2117["Product Model<br>Mongoose Schema"]
                2118["Message Model<br>Mongoose Schema"]
            end
        end
    end
    %% Edges at this level (grouped by source)
    2108["End User<br>External Actor"] -->|sends HTTP requests to| 2112["Web Server &amp; App Core<br>Node.js, Express.js"]
    2108["End User<br>External Actor"] -->|establishes WebSocket connection with| 2113["WebSocket Handler<br>Socket.IO"]
    2113["WebSocket Handler<br>Socket.IO"] -->|communicates with| 2111["WebSocket Clients<br>User Browsers/Apps"]
    2119["Database Connector<br>Mongoose"] -->|connects to| 2109["MongoDB Database<br>NoSQL RDBMS"]
    2120["Session Management<br>Express Session, MongoDB Store"] -->|stores session data in| 2109["MongoDB Database<br>NoSQL RDBMS"]
    2122["Email Utility<br>Nodemailer (assumed)"] -->|sends emails via| 2110["External Email Service<br>SMTP/API Provider"]

```

## Analyzed Files


1. Introducción
Nombre del Proyecto: IdealCars
. Objetivo: Explica brevemente el propósito del proyecto. Ejemplo: "IdealCars es una API diseñada para gestionar información de vehículos y facilitar la interacción entre usuarios y concesionarios."
. Equipo: Menciona quiénes participaron en el desarrollo.
2. Funcionalidades Principales
. Gestión de Vehículos: Describe cómo se manejan los datos de los vehículos (creación, actualización, eliminación, etc.).
. WebSocket Server: Explica cómo se utiliza para comunicación en tiempo real.
. Autenticación: Si implementaron autenticación, menciona cómo se asegura la seguridad de los usuarios.
. Otros Módulos: Enumera otras características importantes.
3. Herramientas y Tecnologías Utilizadas
Backend:
Node.js
Express.js
WebSocket (para comunicación en tiempo real)
Base de Datos: Menciona si usaron MongoDB,(mongoose)
Entorno de Desarrollo:
Visual Studio Code
Git/GitHub para control de versiones
Otros:
Dotenv para configuración de variables de entorno
Debug para depuración
añadir mas herramientas 
4. Arquitectura del Proyecto
. Explica cómo está estructurado el proyecto:
server.js: Punto de entrada principal.
app.js: Configuración de rutas y middlewares.
. webSocketServer.js: Configuración del servidor WebSocket.
. Muestra un diagrama simple si es posible.
5. Retos y Soluciones
. Habla de los desafíos que enfrentaron durante el desarrollo (por ejemplo, manejo de errores, configuración del servidor).
. Explica cómo los resolvieron.
6. Conclusión
. Impacto: ¿Qué valor aporta IdealCars a los usuarios?
. Próximos Pasos: Menciona posibles mejoras o funcionalidades futuras.
7. Demostración (Opcional)
. Si es posible, muestra una demo rápida del proyecto en funcionamiento.
. Consejos para la Presentación
. Usa diapositivas simples y visuales (puedes usar PowerPoint, Google Slides o Canva).
. Incluye capturas de pantalla del código o del proyecto en funcionamiento.
ALGO MUY IMPORTANTE QUE COMENTO JOANA AYER ES QUE TENGAMOS UN VIDELO DE LA DEMO POR SI FALLA ALGO 
```