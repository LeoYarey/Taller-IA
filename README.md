# Sistema de Agendamiento de Citas 📅

Proyecto práctico desarrollado durante el webinar **"Agentes Inteligentes para Programación"**. Esta aplicación es una webapp completa de gestión de reservas construida utilizando elementos prefabricados y asistencia de IA para optimizar el desarrollo.


## 📋 Descripción del Proyecto

Este sistema permite la gestión integral de citas médicas o de servicios. Fue desarrollado para demostrar cómo la integración de herramientas modernas y asistentes de código puede acelerar la creación de software complejo.

**Funcionalidades principales:**
* **Calendario Interactivo:** Vistas mensual, semanal y diaria.
* **Gestión de Citas:** Creación, edición y cancelación con validaciones.
* **Lógica de Negocio:** Detección automática de conflictos de horario y validación de disponibilidad.
* **Persistencia:** Base de datos SQLite local para fácil despliegue y pruebas.

## 🛠 Tecnologías Utilizadas

El stack tecnológico fue seleccionado para maximizar la eficiencia y el rendimiento:

* **Frontend:** Next.js 16, React 19, TypeScript
* **Estilos:** Tailwind CSS
* **Calendario:** React Big Calendar
* **Estado y Datos:** TanStack Query (React Query)
* **Base de Datos:** SQLite (vía `better-sqlite3`)
* **Validación:** React Hook Form + Zod
* **Fechas:** Day.js

---

## 🚀 Instrucciones de Ejecución

Sigue estos pasos para ejecutar la aplicación en tu entorno local:

### 1. Instalación de Dependencias
Asegúrate de tener Node.js instalado. Luego, ejecuta:

```bash
npm install
