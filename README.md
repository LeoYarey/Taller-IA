Sistema de Agendamiento de Citas

Sistema completo de calendario y gestión de reservas desarrollado con Next.js, TypeScript, React Big Calendar, TanStack Query y SQLite.

Características

Calendario interactivo con vistas mensual, semanal y diaria.

Creación, edición y cancelación de citas.

Administración de proveedores y servicios.

Validación de disponibilidad y detección automática de conflictos.

Interfaz moderna construida con Tailwind CSS.

Base de datos SQLite integrada, sin necesidad de configuración adicional.

Actualizaciones en tiempo real mediante React Query.

Tecnologías Utilizadas

Frontend: Next.js 16, React 19, TypeScript

Estilos: Tailwind CSS

Calendario: React Big Calendar

Formularios: React Hook Form y Zod

Estado del servidor: TanStack Query (React Query)

Base de datos: SQLite con better-sqlite3

Manejo de fechas: Day.js

Instalación

Las dependencias ya se encuentran instaladas. Si es necesario reinstalarlas:

npm install

Inicializar la Base de Datos

Para crear la base de datos con información de ejemplo, ejecutar:

npm run db:seed


Este proceso generará el archivo local.db con:

Tres proveedores de ejemplo

Cinco tipos de servicios

Horarios de disponibilidad (lunes a viernes, de 9:00 a 17:00)

Tres citas de demostración

Ejecución en Modo Desarrollo
npm run dev


El proyecto estará disponible en:
http://localhost:3000

Uso del Sistema
Crear una cita

Seleccionar “Nueva Cita” o dar clic en un espacio vacío del calendario.

Completar el formulario con los datos del cliente y la información de la cita.

Guardar la cita.

Ver detalles de una cita

Hacer clic sobre cualquier cita en el calendario.

Cancelar una cita

Abrir los detalles de la cita.

Seleccionar la opción “Cancelar cita”.

Base de Datos

El archivo local.db se encuentra en la raíz del proyecto.

Reiniciar la base de datos
rm local.db
npm run db:seed

Endpoints de la API

GET /api/appointments – Obtiene la lista de citas.

POST /api/appointments – Crea una nueva cita.

PUT /api/appointments/[id] – Actualiza una cita existente.

DELETE /api/appointments/[id] – Cancela una cita.

GET /api/availability – Obtiene los horarios disponibles.

GET /api/providers – Lista los proveedores.

GET /api/services – Lista los servicios.

Estructura del Proyecto
src/
├── app/              # App Router de Next.js
├── components/       # Componentes de la interfaz
├── db/               # Configuración de SQLite
├── hooks/            # Hooks basados en React Query
├── lib/              # Utilidades y validaciones
└── types/            # Tipos de TypeScript

Personalización
Modificar horarios de atención

En src/lib/business-rules.ts se pueden ajustar los horarios:

export const DEFAULT_BUSINESS_HOURS: BusinessHours = {
  start: '09:00',
  end: '17:00',
  daysOfWeek: [1, 2, 3, 4, 5], // Lunes a Viernes
};

Licencia

MIT