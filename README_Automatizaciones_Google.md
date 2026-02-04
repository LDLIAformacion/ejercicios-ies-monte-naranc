# 🚀 Automatizaciones n8n para Centro Educativo
## Resumen y Casos de Uso de los Ejercicios

Este repositorio contiene **10 automatizaciones** diseñadas para la gestión de un centro educativo. A continuación se detallan los objetivos y ejemplos prácticos de uso para cada ejercicio.

---

## 📦 Listado de Ejercicios y Casos de Uso

| # | Automatización | Casos de Uso (Ejemplos) |
|---|----------------|-------------------------|
| **1** | **Resumen de Emails → Sheets** | • Registro automático de consultas de familias.<br>• Seguimiento de avisos de mantenimiento del centro. |
| **2** | **Respuesta Automática (Borrador)** | • Confirmar recepción de justificantes médicos.<br>• Respuesta estándar sobre plazos de matriculación. |
| **3** | **Adjuntos → Drive + Registro** | • Archivar DNIs o títulos enviados por alumnos.<br>• Guardar fotos de actividades extraescolares recibidas. |
| **4** | **Drive → Resumen IA** | • Resumen rápido de nuevas leyes publicadas en el boletín.<br>• Índice automático de actas de claustro extensas. |
| **5** | **Base de Datos Clasificada** | • Panel de control para ver el "sentimiento" del buzón.<br>• Alertas inmediatas para emails marcados como críticos. |
| **6** | **Etiquetado IA en Gmail** | • Separar "Publicidad" de "Comunicaciones Oficiales".<br>• Organizar el correo automáticamente por departamentos. |
| **7** | **Email → Google Calendar** | • Crear citas automáticas para tutorías con familias.<br>• Agendar cursos de formación recibidos por email. |
| **8** | **Recordatorios de Plazos** | • Aviso de fecha límite para entrega de memorias.<br>• Recordatorio de último día para solicitar becas. |
| **9** | **Gestión y Archivado** | • Limpieza de bandeja archivando facturas ya procesadas.<br>• Etiquetar y ocultar newsletters que no requieren acción. |
| **10** | **Resumen Semanal en Calendar** | • Informe para dirección sobre los temas más tratados.<br>• Repaso de lunes con lo más importante de la semana anterior. |

---

## 📋 Descripción Técnica de los Bloques

### Gestión Documental (1-5)
Enfocados en el procesamiento de la información entrante:
- **Centralización**: Todo queda registrado en Google Sheets sin intervención manual.
- **IA de Análisis**: Uso de modelos de lenguaje para sintetizar y clasificar el contenido.
- **Organización de Drive**: Estructura de archivos basada en la información del correo.

### Organización y Agenda (6-10)
Enfocados en la productividad del personal:
- **Productividad Visual**: Uso inteligente de etiquetas para priorizar el trabajo.
- **Sincronización Total**: El correo se convierte en agenda sin necesidad de copiar datos a mano.
- **Automatización del Seguimiento**: Sistema proactivo de avisos para no perder fechas clave.

---

## 🔧 Requisitos para Alumnos

Para que estos ejercicios funcionen en vuestro entorno n8n:
1. **Credenciales de Google**: OAuth2 configurado con acceso a Gmail, Calendar y Sheets.
2. **Credenciales de OpenAI**: API Key válida para el nodo de "IA Agent".
3. **IDs Personalizados**: Debéis sustituir los campos `TU_ID_...` por vuestros IDs reales de hojas de cálculo y carpetas.

---

*Actualizado para el curso de automatización n8n - Febrero 2026*
