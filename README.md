Aplicación web para que una empresa de telecomunicaciones gestione el inventario de equipos y materiales entregados a sus técnicos de instalaciones de fibra óptica.

🚀 Tecnologías utilizadas

Backend: Node.js + Express con TypeScript

Base de datos: MySQL/MariaDB (desarrollo en XAMPP, despliegue en servicio remoto)

Validación: Zod

Autenticación: Sesiones con express-session

Frontend: HTML estático + Bootstrap 5
 + JavaScript (fetch API)

⚙️ Funcionalidades principales
👨‍💼 Administrador

Transferir material a un técnico (requiere aceptación).

Retirar material a un técnico (requiere aceptación).

Crear técnicos y nuevos materiales.

Consultar stock de técnicos y del almacén.

Listar órdenes de trabajo por técnico/fecha/nº orden.

🧑‍🔧 Técnico

Consultar su stock propio.

Transferir materiales a compañeros (requiere aceptación del receptor).

Crear órdenes de trabajo e imputar materiales (se descuentan del stock).

📂 Estructura del proyecto
src/
 ├─ config/        # Configuración (env, base de datos)
 ├─ controllers/   # Lógica de controladores
 ├─ middlewares/   # Middlewares de autenticación y permisos
 ├─ routes/        # Definición de rutas
 ├─ services/      # Servicios y lógica de negocio
 ├─ utils/         # Validaciones, helpers
public/            # Archivos frontend (HTML, JS, CSS, Bootstrap)
scripts/           # schema.sql y seed.sql para la BD

🛠️ Instalación y uso

Clonar el repositorio

git clone https://github.com/TU-USUARIO/inventario-fibra.git
cd inventario-fibra


Instalar dependencias

npm install


Configurar variables de entorno
Crea un archivo .env en la raíz con el siguiente contenido:

PORT=3000
SESSION_SECRET=supersecreto
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=inventario
DB_PORT=3306


Crear base de datos

Arranca MySQL (ej: XAMPP).

Crea la base de datos inventario.

Importa scripts/schema.sql y scripts/seed.sql desde phpMyAdmin o terminal.

Ejecutar en modo desarrollo

npm run dev


Acceder en el navegador:

http://localhost:3000/health
 → Comprobación del servidor

http://localhost:3000/login.html
 → Pantalla de login

🔐 Usuarios de prueba (seed.sql)

Administrador

Email: admin@example.com

Password: Admin123!

Técnico 1

Email: tec1@example.com

Password: Tec123!

Técnico 2

Email: tec2@example.com

Password: Tec123!

(las contraseñas deben reemplazarse por los hashes bcrypt en el seed.sql)

📌 Notas

Proyecto desarrollado en entorno local con XAMPP.

Preparado para desplegar en la nube con un servicio de base de datos remoto.

Toda acción queda registrada en movimientos y logs para trazabilidad.

✨ Proyecto creado como trabajo final de FP en Desarrollo de Aplicaciones Web por [Tu nombre].
