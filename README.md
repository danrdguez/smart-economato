# Smart Economato 🛒

Smart Economato es una solución empresarial completa diseñada para economatos y centros educativos que necesitan gestionar inventario, compras, recepción de mercancía, distribución de stock y analítica operacional. El sistema permite a administradores, profesores y estudiantes colaborar de manera segura y eficiente mediante roles y permisos diferenciados.

---

## 🛠️ Tech Stack

- **Frontend:** React + TypeScript (Vite) + Nginx (Producción)
- **Backend:** NestJS (API REST)
- **Base de Datos:** PostgreSQL remoto alojado en Supabase
- **Infraestructura:** Docker & Docker Compose

---

## 🚀 Despliegue con Docker (Recomendado)

El proyecto está completamente contenedorizado. Tanto el frontend como el backend se levantan listos para producción con un solo comando:

```bash
docker-compose up --build
