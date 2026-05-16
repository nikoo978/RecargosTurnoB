# RecargosTurnoB - WebApp para Vercel

WebApp responsive para usar desde iPhone/iOS y enviar por WhatsApp los recargos, francos, francos posteriores, novedades y observaciones.

## Funciones incluidas

- Carga diaria desde el smartphone.
- Oficial de Servicio.
- Recargos con horario y detalle.
- Francos del día siguiente.
- Francos posteriores.
- Novedades.
- Observaciones.
- Generación de JPG desde el navegador.
- Historial mensual.
- Clasificación automática:
  - 07:00 a 13:00 = Mañana
  - 13:00 a 20:00 = Tarde
  - 20:00 en adelante = Noche
- Comparativo mensual por persona.
- Gestión de personal: agregar, editar y quitar.
- Respaldo JSON: exportar/importar datos.
- Evita duplicados: una fecha de guardia se guarda una sola vez; si se vuelve a generar, reemplaza el registro anterior.

## Importante sobre persistencia

Esta versión guarda los datos en `localStorage`, es decir, en el navegador del dispositivo.

Esto permite usarla inmediatamente en Vercel desde iPhone, pero:
- si se borra el historial del navegador, se pierden los datos;
- si se usa desde otro teléfono, no tendrá el mismo historial;
- para varios usuarios/dispositivos, conviene conectar una base de datos como Supabase, Neon, Vercel Postgres o Vercel KV.

## Instalar localmente

```bash
npm install
npm run dev
```

## Subir a Vercel

1. Crear un repositorio en GitHub con estos archivos.
2. En Vercel: Add New Project.
3. Seleccionar el repositorio.
4. Framework: Next.js.
5. Deploy.

## Instalar como app en iPhone

1. Abrir la URL de Vercel en Safari.
2. Tocar Compartir.
3. Elegir "Agregar a pantalla de inicio".
