# 🏪 Smart Economato

[![Node.js](https://img.shields.io/badge/Node.js-18+-green)](https://nodejs.org)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org)
[![React](https://img.shields.io/badge/React-18-61dafb)](https://react.dev)
[![NestJS](https://img.shields.io/badge/NestJS-10-ea284e?logo=nestjs&logoColor=white)](https://nestjs.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-336791)](https://www.postgresql.org)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED)](https://www.docker.com)

> **Sistema integral de gestión de inventario, compras y analítica para economatos educativos**

## 🎯 ¿Qué es Smart Economato?

Smart Economato es una solución full-stack diseñada para **gestionar inventario, compras, recepción y analítica** en centros educativos culinarios. Permite que administradores, profesores y estudiantes colaboren de forma segura con roles diferenciados.

### ⭐ Características principales

- ✅ **Autenticación segura** — JWT con registro y verificación de usuarios
- 📦 **Gestión de inventario** — Stock, lotes con caducidad y alertas automáticas
- 🛒 **Compras inteligentes** — Gestión de proveedores y recepción de mercancía
- 🏭 **Operaciones avanzadas** — Distribución, bajas y auditoría completa
- 📊 **Analítica en tiempo real** — Rendimiento, escandallos, informes financieros
- 🔄 **Sincronización offline** — Caché y actualizaciones en vivo
- 🎨 **UI moderna y responsiva** — Diseño profesional y accesible

## 🛠️ Stack tecnológico

| Capa | Tecnología |
|------|-----------|
| **Frontend** | React 18 + TypeScript + Vite + Tailwind |
| **Backend** | NestJS + Node.js |
| **Base de datos** | PostgreSQL (Supabase) |
| **Infraestructura** | Docker + Nginx |
| **UI/UX** | Radix UI + TanStack Table + Recharts |

## 👥 Roles de usuario

| Rol | Acceso |
|-----|--------|
| 🔴 **Administrador** | Control total, gestión de usuarios, aprobaciones |
| 🟡 **Profesor** | Recepción, distribución, pedidos, bajas |
| 🟢 **Estudiante** | Consulta de inventario, análisis, coste de recetas |

## 🚀 Inicio rápido

### Requisitos previos

- **Docker & Docker Compose** (recomendado) O
- **Node.js 18+** + **PostgreSQL** (desarrollo local)

### Con Docker (⭐ recomendado)

```bash
# Clonar y entrar en el directorio
git clone https://github.com/danrdguez/smart-economato.git
cd smart-economato

# Levantar los servicios
docker-compose up --build
```

✅ **La app estará disponible en:**
- 🌐 Frontend: http://localhost:8081
- 🔌 API: http://localhost:3000/api

> **Nota:** Si tienes XAMPP/Apache en puerto 8080, detenlo primero o cambia el puerto en `docker-compose.yml`

### Desarrollo local (sin Docker)

#### 1️⃣ Backend (NestJS - puerto 3000)
```bash
cd backend
cp .env.example .env  # Configura tus variables
npm install
npm run start:dev
```

#### 2️⃣ Frontend (React - puerto 8081)
```bash
cd frontend
cp .env.example .env
npm install
npm run dev
```

Abre http://localhost:8081 en tu navegador.

## ⚙️ Configuración

### Variables de entorno

**Backend** (`backend/.env`):
```env
DB_HOST=tu-host-postgres
DB_PORT=5432
DB_NAME=smart_economato
DB_USER=postgres
DB_PASS=tu-contraseña
JWT_SECRET=tu-secret-key
JWT_EXPIRES_IN=24h
ALLOWED_ORIGINS=http://localhost:8081
```

### Base de datos

La BD está en **Supabase** (PostgreSQL remoto). Para restaurar localmente:

```bash
psql -h localhost -U postgres -d smart_economato -f proyecto_completo.sql
```

## 🔑 Credenciales de demo

| Rol | Email | Contraseña |
|-----|-------|-----------|
| 🔴 Admin | `admin@smarteconomato.local` | `Admin1234!` |
| 🟡 Profesor | `profesor@smarteconomato.local` | `Profesor1!` |
| 🟢 Alumno | `alumno@smarteconomato.local` | `Alumno1234!` |

⚠️ **Solo para desarrollo. Cambiar credenciales en producción.**

## 📁 Estructura del proyecto

```
smart-economato/
├── frontend/              # React + TypeScript (Vite)
│   ├── src/
│   ├── public/
│   └── package.json
├── backend/               # NestJS + Express
│   ├── src/
│   ├── test/
│   └── package.json
├── docs/                  # Documentación completa
│   └── Importante/        # Guías paso a paso
├── proyecto_completo.sql  # Export completo de BD
└── docker-compose.yml     # Orquestación
```

## 📚 Documentación

La documentación completa está en `docs/Importante/` (más de 30 guías):

- 📖 [Visión general](docs/Importante/01_VISION_GENERAL.md)
- 🚀 [Puesta en marcha](docs/Importante/02_PUESTA_EN_MARCHA_Y_DESARROLLO_LOCAL.md)
- 🏗️ [Arquitectura](docs/Importante/04_ARQUITECTURA_Y_MODELO_DE_DATOS.md)
- 🔐 [Autenticación](docs/Importante/09_AUTENTICACION_BACKEND_JWT_SEGURIDAD.md)
- 📦 [Inventario](docs/Importante/11_GESTION_DE_INVENTARIO.md)
- 📊 [Analítica](docs/Importante/22_ANALITICA_E_INFORMES.md)

**[Ver documentación completa →](docs/Importante)**

## ✅ Verificación de salud

```bash
# Health check del API
curl http://localhost:3000/api/health
```

## 🧪 Testing

```bash
# Backend
cd backend
npm run test          # Tests unitarios
npm run test:e2e      # Tests E2E

# Frontend
cd frontend
npm run test          # Vitest
```

## 🚢 Deployment

Consulta [Despliegue y CI/CD](docs/Importante/03_DESPLIEGUE_Y_CICD.md) para instrucciones de producción.

## 📝 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).

