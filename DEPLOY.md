
# 🚀 Guía de Despliegue del Proyecto HardSoft

Este proyecto contiene un **frontend (React/Vite)** y un **backend (Node.js + Express + MongoDB)**, diseñados para ejecutarse por separado en producción o desarrollo.

---

## 📦 Contenido del ZIP
- `frontend.zip`: Código fuente del cliente
- `backend.zip`: Código fuente del servidor
- `README_DEPLOY.md`: Guía de despliegue
- `DEPLOY.md`: Esta guía extendida

---

## 🧪 Requisitos Previos
- Node.js (v18+)
- MongoDB (local o Atlas)
- Yarn o npm
- Git (opcional)
---

## ⚙️ Configuración Local

### 🔧 Backend

1. Descomprime `backend.zip`
2. En la raíz, copia `.env.example` a `.env` y configúralo.
3. Instala dependencias:
```bash
cd backend
npm install
```
4. Ejecuta en modo desarrollo:
```bash
npm run dev
```
5. Producción:
```bash
npm start
```

### 🌐 Frontend

1. Descomprime `frontend.zip`
2. Crea archivo `.env` y agrega:
```
VITE_API_URL=http://localhost:5000/api
```
3. Instala dependencias:
```bash
cd frontend
npm install
```
4. Ejecuta en modo desarrollo:
```bash
npm run dev
```
5. Construye para producción:
```bash
npm run build
```

---

## ☁️ Despliegue en Producción

### Frontend en Vercel

1. Ve a [vercel.com](https://vercel.com)
2. Nuevo proyecto → Sube carpeta del frontend
3. Establece la variable de entorno:
```
VITE_API_URL=https://tu-api-backend.com/api
```
4. Listo 🎉

### Backend en Railway

1. Ve a [railway.app](https://railway.app)
2. Nuevo proyecto → Subir carpeta del backend
3. Establece variables de entorno del archivo `.env`
4. Conecta a MongoDB (Railway o Atlas)
5. Obtendrás una URL pública para usar en el frontend

---

## 🛡️ Seguridad y Producción

- Usa HTTPS (automático en Vercel y Railway)
- Establece correctamente los CORS en el backend
- Configura tu dominio personalizado si lo deseas

---

## ✅ Funcionalidades Incluidas

- Registro/Login + recuperación de contraseña
- Administración de usuarios, productos y servicios
- Fondo configurable, icono de empresa y favicon
- Panel de administración completo
- Pasarelas de pago (MercadoPago/Stripe simuladas)
- Zona de perfil con historial, direcciones, cupones, etc.
- Secciones: productos, servicios, blog, ayuda, contacto, políticas y más

---

## 📂 Estructura Recomendable

- `/frontend` → Cliente
- `/backend` → API + DB
- Repositorio único o monorepo con Vite + Express

---

## 📬 Soporte

Si tienes dudas, consulta la documentación técnica o agrega herramientas como Postman, MongoDB Compass o PM2 en producción.

---

