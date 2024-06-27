# Sistema FBI

Este proyecto es una aplicación web simple que utiliza Node.js, Express y JSON Web Tokens (JWT) para la autenticación. Simula un sistema de inicio de sesión para agentes del FBI para acceder a información restringida.

## Características

- Autenticación de usuarios usando correo electrónico y contraseña.
- Generación y verificación de tokens JWT.
- Servir archivos estáticos para imágenes.
- HTML y CSS simples para el front-end.

## Instalación

1. Clona el repositorio:
    ```bash
    git clone https://github.com/Yistler/sistema-fbi.git
    cd sistema-fbi
    ```

2. Instala las dependencias:
    ```bash
    npm install
    ```

3. Inicia el servidor:
    ```bash
    node server.js
    ```

## Uso

1. Abre tu navegador web y navega a `http://localhost:3000`.

2. Ingresa tus credenciales para iniciar sesión. Utiliza uno de los usuarios predefinidos en `data/agentes.js`:
    ```json
    [
      {
        "email": "who@fbi.com",
        "password": "me"
      },
      {
        "email": "where@fbi.com",
        "password": "there"
      },
      {
        "email": "how@fbi.com",
        "password": "exactly"
      }
    ]
    ```

3. Después de iniciar sesión, recibirás un token y un botón para acceder al área restringida.

4. Haz clic en el botón para navegar al área restringida y ver la información secreta.

## Seguridad

- Esta aplicación genera una nueva clave secreta cada vez que se inicia el servidor. Para uso en producción, considera usar una clave secreta fija almacenada de manera segura.
- Las contraseñas están almacenadas en texto plano en este ejemplo. Para aplicaciones reales, siempre hashea y saltea las contraseñas utilizando una biblioteca como bcrypt.

## Dependencias

- [express](https://www.npmjs.com/package/express)
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
- [crypto](https://nodejs.org/api/crypto.html)
