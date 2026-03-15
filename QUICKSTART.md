# ClickInmueble - GuÃ­a de Inicio RÃ¡pido

## Â¿QuÃ© es ClickInmueble?

ClickInmueble es una aplicaciÃ³n web completa de venta de departamentos con:
- CatÃ¡logo de propiedades con bÃºsqueda avanzada
- Panel administrativo seguro con autenticaciÃ³n JWT
- Base de datos MongoDB con 15 propiedades de ejemplo
- Interfaz moderna y responsiva

## Requisitos Previos

1. **Node.js** 14 o superior
2. **MongoDB** 4.4 o superior ejecutÃ¡ndose localmente

### Verificar instalaciÃ³n:
```bash
node --version      # Debe ser v14.0.0 o mayor
npm --version       # Debe estar disponible
mongod --version    # Debe estar instalado
```

## InstalaciÃ³n (3 pasos)

### 1. Instalar dependencias
```bash
cd ClickInmueble
npm install
```

### 2. Iniciar MongoDB
```bash
# En una terminal separada
mongod
```

### 3. Ejecutar servidor
```bash
npm start
```

DeberÃ­as ver:
```
âœ… MongoDB conectado exitosamente
ðŸš€ Servidor ClickInmueble ejecutÃ¡ndose en puerto 3000
```

## Primer Uso

### Abrir la aplicaciÃ³n
1. Abre http://localhost:3000 en tu navegador
2. Explora la pÃ¡gina principal con propiedades destacadas
3. Usa "Propiedades" para ver el catÃ¡logo completo con filtros

### Acceder al Panel Admin
1. Haz clic en "Admin" en la esquina superior derecha
2. Usa las credenciales:
   - Email: `admin@ClickInmueble.com`
   - ContraseÃ±a: `ClickInmueble2024!`
3. VerÃ¡s un dashboard con estadÃ­sticas y gestiÃ³n de propiedades

## Cargar Datos de Ejemplo

Ya vienen incluidos 15 departamentos de muestra, pero si quieres recargarlos:

```bash
npm run seed
```

Esto crearÃ¡:
- Admin predeterminado
- 15 departamentos en CDMX y Guadalajara
- InformaciÃ³n lista para exploreaciÃ³n

## Estructura RÃ¡pida

```
â”œâ”€â”€ server.js           â† Punto de entrada
â”œâ”€â”€ models/            â† Esquemas de MongoDB
â”œâ”€â”€ routes/            â† Endpoints de API
â”œâ”€â”€ middleware/        â† AutenticaciÃ³n JWT
â”œâ”€â”€ public/            â† Interfaz web
â”‚   â”œâ”€â”€ *.html         â† PÃ¡ginas principales
â”‚   â”œâ”€â”€ css/style.css  â† Estilos
â”‚   â””â”€â”€ js/            â† LÃ³gica del cliente
â””â”€â”€ seed/              â† Datos de ejemplo
```

## APIs Disponibles

### BÃºsqueda de Departamentos
```javascript
GET /api/apartments?city=CDMX&minPrice=1000000&limit=9&page=1
```

### Crear Contacto
```javascript
POST /api/contacts
{
  "name": "Juan",
  "email": "juan@example.com",
  "phone": "5512345678",
  "message": "Interesado en...",
  "apartmentId": "..."
}
```

### Login Admin
```javascript
POST /api/admin/login
{
  "email": "admin@ClickInmueble.com",
  "password": "ClickInmueble2024!"
}
```

## CaracterÃ­sticas Clave

### Frontend
âœ“ PÃ¡gina principal con hero section
âœ“ BÃºsqueda y filtros avanzados
âœ“ GalerÃ­a de imÃ¡genes
âœ“ Formulario de contacto
âœ“ DiseÃ±o responsivo (mobile/tablet/desktop)

### Backend
âœ“ API RESTful completa
âœ“ AutenticaciÃ³n JWT
âœ“ CRUD de departamentos
âœ“ GestiÃ³n de contactos
âœ“ Validaciones de datos

### Admin
âœ“ Dashboard con estadÃ­sticas
âœ“ GestiÃ³n de departamentos
âœ“ GestiÃ³n de contactos
âœ“ Modal para agregar/editar

## Desarrollo

### Modo desarrollo con recarga automÃ¡tica:
```bash
npm run dev
```

### Puntos de entrada Ãºtiles:
- **Frontend**: http://localhost:3000
- **API**: http://localhost:3000/api/apartments
- **Admin**: http://localhost:3000/admin.html

## SoluciÃ³n de Problemas

### "Error conectando a MongoDB"
- AsegÃºrate que MongoDB estÃ¡ corriendo: `mongod`
- Verifica que el URI en `.env` es correcto

### Puerto 3000 en uso
Cambia el puerto en `.env`:
```
PORT=3001
```

### Las imÃ¡genes no cargan
- Las imÃ¡genes vienen de picsum.photos
- Necesitas conexiÃ³n a internet

## PrÃ³ximos Pasos

1. **Explorar**: Abre http://localhost:3000 y navega por la app
2. **Admin**: Prueba el panel con las credenciales de ejemplo
3. **Datos**: Modifica/agrega departamentos desde el admin
4. **CÃ³digo**: Personaliza estilos en `public/css/style.css`

## Tech Stack

- Node.js + Express
- MongoDB + Mongoose
- HTML5 + CSS3 (Bootstrap 5)
- Vanilla JavaScript
- JWT Auth

## DocumentaciÃ³n Completa

Ver `README.md` para documentaciÃ³n detallada de:
- Estructura del proyecto
- Endpoints de API
- Variables de entorno
- Mejoras futuras

---

Â¿Preguntas? El cÃ³digo estÃ¡ bien comentado y listo para personalizar.

