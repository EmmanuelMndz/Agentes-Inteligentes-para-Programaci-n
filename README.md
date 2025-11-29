Sistema de Agendamiento de Citas
Sistema de calendario y reservas construido con Next.js, TypeScript, React Big Calendar, TanStack Query y SQLite.

⚫ Características Principales
⚫ Calendario interactivo: vistas mensual, semanal y diaria
⚫ Gestión de citas: crear, editar y cancelar
⚫ Administración de proveedores y servicios
⚫ Validación automática: disponibilidad y conflictos
⚫ Interfaz moderna con Tailwind CSS
⚫ Base de datos local SQLite, sin configuración adicional
⚫ Actualizaciones en tiempo real con React Query

Tecnologías

⚫ Frontend: Next.js 16, React 19, TypeScript
⚫ Estilos: Tailwind CSS
⚫ Calendario: React Big Calendar
⚫ Formularios: React Hook Form + Zod
⚫ Estado del servidor: TanStack Query
⚫ Base de datos: SQLite (better-sqlite3)
⚫ Fechas y tiempos: Day.js

Instalación & Inicio
# Instalar dependencias
npm install

# Inicializar base de datos con datos de ejemplo
npm run db:seed

# Ejecutar servidor de desarrollo
npm run dev

⚫ Abrir en navegador: http://localhost:3000

Uso Rápido
⚫ Crear cita
⚫ Clic en "Nueva Cita" o selecciona un espacio en el calendario
⚫ Completa los datos del cliente y detalles
⚫ Clic en "Guardar cita"
⚫ Ver detalles
⚫ Clic en cualquier cita del calendario
⚫ Cancelar cita
⚫ Abrir detalles de la cita → "Cancelar cita"

Base de Datos
Archivo: local.db en la raíz del proyecto
Reiniciar base de datos:
rm local.db
npm run db:seed

🌐 API Endpoints
Método	Ruta	Descripción
GET	/api/appointments	Listar citas
POST	/api/appointments	Crear cita
PUT	/api/appointments/[id]	Actualizar cita
DELETE	/api/appointments/[id]	Cancelar cita
GET	/api/availability	Slots disponibles
GET	/api/providers	Listar proveedores
GET	/api/services	Listar servicios

Estructura del Proyecto
src/
├── app/         # Next.js App Router
├── components/  # Componentes React
├── db/          # Base de datos SQLite
├── hooks/       # React Query hooks
├── lib/         # Utilidades y validaciones
└── types/       # Tipos TypeScript

Personalización

Cambiar horarios de atención:

// src/lib/business-rules.ts
export const DEFAULT_BUSINESS_HOURS: BusinessHours = {
  start: '09:00',
  end: '17:00',
  daysOfWeek: [1,2,3,4,5], // Lunes a Viernes
};

Licencia

MIT
