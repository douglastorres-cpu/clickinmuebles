# ClickInmueble - Plataforma de Venta de Departamentos

ClickInmueble es una plataforma completa de venta de departamentos construida con Node.js, Express.js, MongoDB y Vanilla JavaScript. Ofrece una interfaz moderna para listar, buscar y contactar sobre propiedades residenciales en MÃ©xico.

## CaracterÃ­sticas

- **CatÃ¡logo de Propiedades**: Listado completo de departamentos con filtros avanzados
- **BÃºsqueda y Filtros**: Filtrar por ciudad, precio, recÃ¡maras, tipo de propiedad
- **GalerÃ­a de ImÃ¡genes**: Vista detallada de cada propiedad con mÃºltiples imÃ¡genes
- **Panel Admin**: GestiÃ³n completa de departamentos y contactos
- **Sistema de Contactos**: Formularios para que los clientes se comuniquen
- **AutenticaciÃ³n JWT**: Panel administrativo protegido con tokens JWT
- **Base de Datos MongoDB**: Almacenamiento robusto con Mongoose
- **DiseÃ±o Responsivo**: Interfaz optimizada para desktop, tablet y mÃ³vil
- **EstadÃ­sticas**: Dashboard con mÃ©tricas de propiedades y contactos

## Requisitos

- Node.js 14+
- MongoDB 4.4+
- npm o yarn

## InstalaciÃ³n

1. Clona o navega al directorio del proyecto:
```bash
cd ClickInmueble
```

2. Instala las dependencias:
```bash
npm install
```

3. Configura las variables de entorno (archivo `.env` incluido con valores por defecto):
```
PORT=3000
MONGODB_URI=mongodb://localhost:27017/ClickInmueble
JWT_SECRET=ClickInmueble_secret_2024_xyz
ADMIN_EMAIL=admin@ClickInmueble.com
ADMIN_PASSWORD=ClickInmueble2024!
```

4. AsegÃºrate que MongoDB estÃ¡ ejecutÃ¡ndose:
```bash
# En macOS con Homebrew
brew services start mongodb-community

# O ejecuta mongod directamente
mongod
```

5. Siembra la base de datos con datos de ejemplo:
```bash
npm run seed
```

6. Inicia el servidor:
```bash
npm start
```

El servidor estarÃ¡ disponible en `http://localhost:3000`

## Desarrollo

Para desarrollo con reinicio automÃ¡tico:
```bash
npm run dev
```

## Estructura del Proyecto

```
ClickInmueble/
â”œâ”€â”€ models/                 # Modelos de Mongoose
â”‚   â”œâ”€â”€ Apartment.js       # Modelo de departamentos
â”‚   â”œâ”€â”€ Contact.js         # Modelo de contactos
â”‚   â””â”€â”€ Admin.js           # Modelo de administradores
â”œâ”€â”€ routes/                 # Rutas de API
â”‚   â”œâ”€â”€ apartments.js      # Endpoints de departamentos
â”‚   â”œâ”€â”€ contacts.js        # Endpoints de contactos
â”‚   â””â”€â”€ admin.js           # Endpoints de autenticaciÃ³n y admin
â”œâ”€â”€ middleware/             # Middleware personalizado
â”‚   â””â”€â”€ auth.js            # VerificaciÃ³n de JWT
â”œâ”€â”€ seed/                   # Datos de semilla
â”‚   â””â”€â”€ seed.js            # Script para popular la BD
â”œâ”€â”€ public/                 # Archivos estÃ¡ticos
â”‚   â”œâ”€â”€ index.html         # PÃ¡gina principal
â”‚   â”œâ”€â”€ propiedades.html   # Listado de propiedades
â”‚   â”œâ”€â”€ detalle.html       # Detalle de propiedad
â”‚   â”œâ”€â”€ contacto.html      # PÃ¡gina de contacto
â”‚   â”œâ”€â”€ admin.html         # Panel administrativo
â”‚   â”œâ”€â”€ css/
â”‚   â”‚   â””â”€â”€ style.css      # Estilos principales
â”‚   â””â”€â”€ js/
â”‚       â”œâ”€â”€ main.js        # Funciones compartidas
â”‚       â”œâ”€â”€ propiedades.js # LÃ³gica de listado
â”‚       â”œâ”€â”€ detalle.js     # LÃ³gica de detalle
â”‚       â”œâ”€â”€ contacto.js    # LÃ³gica de contacto
â”‚       â””â”€â”€ admin.js       # LÃ³gica de admin panel
â”œâ”€â”€ server.js              # Punto de entrada
â”œâ”€â”€ package.json           # Dependencias
â”œâ”€â”€ .env                   # Variables de entorno
â””â”€â”€ README.md              # Este archivo
```

## API Endpoints

### Departamentos
- `GET /api/apartments` - Listar con filtros y paginaciÃ³n
- `GET /api/apartments/featured` - Obtener destacados
- `GET /api/apartments/stats` - EstadÃ­sticas
- `GET /api/apartments/:id` - Detalle de departamento
- `POST /api/apartments` - Crear (protegido)
- `PUT /api/apartments/:id` - Actualizar (protegido)
- `DELETE /api/apartments/:id` - Eliminar (protegido)

### Contactos
- `POST /api/contacts` - Crear contacto
- `GET /api/contacts` - Listar contactos (protegido)
- `PUT /api/contacts/:id` - Actualizar estado (protegido)

### Admin
- `POST /api/admin/login` - Login de administrador
- `GET /api/admin/me` - Perfil actual (protegido)
- `GET /api/admin/dashboard/stats` - EstadÃ­sticas del dashboard (protegido)

## Credenciales de Prueba

Email: `admin@ClickInmueble.com`
ContraseÃ±a: `ClickInmueble2024!`

## TecnologÃ­as Utilizadas

- **Backend**: Node.js, Express.js
- **Base de Datos**: MongoDB, Mongoose ODM
- **AutenticaciÃ³n**: JWT (jsonwebtoken)
- **Seguridad**: bcryptjs para hash de contraseÃ±as
- **Frontend**: HTML5, CSS3, Bootstrap 5, Vanilla JavaScript
- **Iconos**: Font Awesome 6
- **TipografÃ­a**: Google Fonts (Poppins)

## Funcionalidades Principales

### Lado Cliente
- PÃ¡gina principal con propiedades destacadas
- BÃºsqueda y filtrado avanzado
- Vistas de detalle de propiedades con galerÃ­a
- Sistema de contacto para consultas
- Formularios responsivos

### Lado Admin
- AutenticaciÃ³n segura con JWT
- GestiÃ³n de departamentos (CRUD)
- VisualizaciÃ³n y gestiÃ³n de contactos
- Dashboard con estadÃ­sticas
- Modal para agregar/editar propiedades

## Notas de Desarrollo

- Todos los precios estÃ¡n en MXN (pesos mexicanos)
- Las imÃ¡genes usan Picsum Photos API para datos de prueba
- El sistema estÃ¡ completamente funcional sin necesidad de validaciÃ³n adicional
- El frontend es completamente responsivo
- Las bÃºsquedas soportan bÃºsqueda de texto en tÃ­tulo, descripciÃ³n y vecindario
- Los tokens JWT expiran en 24 horas

## Mejoras Futuras

- IntegraciÃ³n con pasarelas de pago
- Sistema de favoritos/guardados
- Notificaciones por email
- IntegraciÃ³n de mapas reales
- GalerÃ­a mejorada con zoom
- Reportes avanzados
- IntegraciÃ³n con redes sociales
- Sistema de calificaciones y reseÃ±as

## Soporte

Para preguntas o soporte, contacta a: info@ClickInmueble.com

## Licencia

Todos los derechos reservados. ClickInmueble 2024.

