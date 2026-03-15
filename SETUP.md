# ClickInmueble - ConfiguraciÃ³n RÃ¡pida

## InstalaciÃ³n RÃ¡pida (Menos de 5 minutos)

### Paso 1: Instalar Dependencias
```bash
npm install
```

### Paso 2: Iniciar MongoDB
Abre una terminal separada y ejecuta:
```bash
mongod
```

### Paso 3: Ejecutar Servidor
```bash
npm start
```

DeberÃ­as ver:
```
âœ… MongoDB conectado exitosamente
ðŸš€ Servidor ClickInmueble ejecutÃ¡ndose en puerto 3000
```

### Paso 4: Cargar Datos (Opcional)
Si quieres cargar 15 departamentos de ejemplo:
```bash
npm run seed
```

## Acceso

| PÃ¡gina | URL |
|--------|-----|
| Inicio | http://localhost:3000 |
| Propiedades | http://localhost:3000/propiedades.html |
| Admin | http://localhost:3000/admin.html |

## Login Admin

```
Email: admin@ClickInmueble.com
ContraseÃ±a: ClickInmueble2024!
```

## Desarrollo

Para desarrollo con reinicio automÃ¡tico:
```bash
npm run dev
```

## Estructura

```
ClickInmueble/
â”œâ”€â”€ server.js              â†’ Punto de entrada
â”œâ”€â”€ models/                â†’ Esquemas MongoDB
â”œâ”€â”€ routes/                â†’ Endpoints API
â”œâ”€â”€ public/                â†’ Interfaz web
â”‚   â”œâ”€â”€ *.html
â”‚   â”œâ”€â”€ css/style.css
â”‚   â””â”€â”€ js/
â””â”€â”€ seed/                  â†’ Datos de ejemplo
```

## Endpoints API

### Departamentos
- GET /api/apartments (listado)
- GET /api/apartments/:id (detalle)
- POST /api/apartments (crear, protegido)

### Contactos
- POST /api/contacts (crear)
- GET /api/contacts (listar, protegido)

### Admin
- POST /api/admin/login
- GET /api/admin/dashboard/stats

## SoluciÃ³n de Problemas

### MongoDB no conecta
- AsegÃºrate que `mongod` estÃ¡ corriendo
- Verifica la URI en `.env`

### Puerto 3000 ocupado
- Cambia PORT en `.env`
- O cierra la aplicaciÃ³n anterior

### Las imÃ¡genes no cargan
- Necesitas conexiÃ³n a internet (Picsum Photos)

## PersonalizaciÃ³n

- Colores: Ver `:root` en `public/css/style.css`
- Texto: Modificar archivos HTML
- LÃ³gica: Actualizar archivos JS
- Base de datos: Modificar modelos en `models/`

## ProducciÃ³n

1. Cambiar variables en `.env`
2. Usar MongoDB en la nube (Atlas)
3. Deployar en servidor (Heroku, AWS, etc.)

Ver `README.md` para documentaciÃ³n completa.

