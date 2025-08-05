# Instrucciones de Despliegue del Proyecto - HardSoft

Este proyecto incluye una aplicación completa de eCommerce desarrollada con frontend y backend separados.

---

## Requisitos Previos

- Node.js >= 16.x
- MongoDB (local o Atlas)
- Cuenta de envío de correos (ej: Gmail con contraseña de app)
- Cuentas para pasarelas de pago (Stripe, MercadoPago)
- Herramienta para ejecutar procesos (PM2 recomendado para backend)

---

## Estructura del Proyecto

- **frontend/** - Aplicación React + Vite
- **backend/** - API Express con control de usuarios, pedidos, productos, autenticación, seguridad, email, etc.

---

## Instalación

### 1. Clonar el proyecto

```bash
git clone https://tu-repo.git
cd proyecto
```

### 2. Configurar variables de entorno

Ve al directorio `/backend` y copia `.env.example` a `.env`, luego completa con tus datos reales:

```bash
cp backend/.env.example backend/.env
```

---

## Ejecución

### Frontend

Modo desarrollo:

```bash
cd frontend
npm install
npm run dev
```

Modo producción:

```bash
npm run build
npx serve dist
```

---

### Backend

Modo desarrollo:

```bash
cd backend
npm install
npm run dev
```

Modo producción:

```bash
pm2 start index.js --name hardsoft-backend
```

---

## Extras

- Ruta admin: `/admin`
- Acceso completo al perfil, seguridad, historial, cupones, direcciones y más
- Integrado con Stripe, MercadoPago (simulados o reales)
- Chat en vivo, notificaciones, favicon, íconos, protección de datos y más

---

## Desarrollado por

HardSoft — Reparación de hardware y software con tecnología de punta.
