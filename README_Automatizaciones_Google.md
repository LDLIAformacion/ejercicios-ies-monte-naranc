# 🚀 Automatizaciones n8n para Centro Educativo
## Resumen de Ejercicios de Automatización

Este repositorio contiene una colección de **10 automatizaciones** diseñadas para agilizar la gestión administrativa y académica de un centro educativo utilizando n8n, Gmail, Google Calendar y Google Sheets.

---

## 📦 Listado de Ejercicios

| # | Archivo | Descripción resumida |
|---|---------|-------------|
| 1 | `auto_01_resumen_emails_sheets.json` | Resumen automático de emails con IA → Google Sheets |
| 2 | `auto_02_respuesta_automatica_borrador.json` | IA redacta una respuesta profesional (Borrador) |
| 3 | `auto_03_adjuntos_drive_resumen.json` | Guarda adjuntos en Drive y los registra en Sheets |
| 4 | `auto_04_drive_resumen_automatico.json` | Resumen automático de documentos nuevos en Drive |
| 5 | `auto_05_base_datos_emails_completa.json` | Clasificación avanzada y base de datos de correos |
| 6 | `auto_06_etiquetar_emails_ia.json` | Etiquetado automático de emails basado en contenido |
| 7 | `auto_07_email_a_evento_calendar.json` | Detección de reuniones en emails → Evento en Calendar |
| 8 | `auto_08_recordatorio_email_calendar.json` | Crea recordatorios de seguimiento para emails con plazos |
| 9 | `auto_09_etiquetas_y_archivado.json` | Gestión integral: etiquetado, archivado y registro |
| 10| `auto_10_agenda_semanal_emails.json` | Resumen semanal de actividad → Informe en Calendar |

---

## 📋 Descripción de las Automatizaciones

### 1-5: Gestión Documental y Respuesta
- **Resumen e IA**: Procesamiento de texto entrante para generar síntesis ejecutivas.
- **Borradores Inteligentes**: Redacción asistida de respuestas para agilizar la secretaría.
- **Control de Adjuntos**: Organización automática de archivos recibidos por email en carpetas de Drive.
- **Análisis de Drive**: Vigilancia de carpetas para resumir automáticamente normativa o actas.

### 6-10: Organización y Calendario
- **Etiquetado Inteligente**: Clasificación visual en Gmail (Familias, Profesorado, Urgente).
- **Integración con Calendar**: Extracción de fechas y horas para asegurar que ninguna reunión se pase por alto.
- **Seguimiento de Plazos**: Recordatorios automáticos para emails que requieren una acción futura.
- **Informes Semanales**: Visión global de la carga de trabajo y temas destacados de la semana.

---

## 🔧 Configuración General

Para utilizar estos flujos, se requiere:
1. **n8n** instalado y funcionando.
2. **Credenciales de Google** (OAuth2) con permisos para Gmail, Calendar y Sheets.
3. **Credenciales de OpenAI** para las funciones de Inteligencia Artificial.
4. Ajustar los **IDs de Google Sheets y Carpetas** en los nodos correspondientes.

---

*Creado para el curso de automatización n8n - Febrero 2026*
