# 🚀 Automatizaciones N8N para Centro Educativo
## Integración con Google Suite (Gmail, Drive, Sheets)

Este paquete contiene **5 automatizaciones** listas para usar que cubren las necesidades solicitadas por el director.

---

## 📦 Contenido del Paquete

| # | Archivo | Descripción |
|---|---------|-------------|
| 1 | `auto_01_resumen_emails_sheets.json` | Resumen automático de emails con IA → Google Sheets |
| 2 | `auto_02_respuesta_automatica_borrador.json` | Respuesta inteligente guardada como borrador |
| 3 | `auto_03_adjuntos_drive_resumen.json` | Guardar adjuntos en Drive + registro |
| 4 | `auto_04_drive_resumen_automatico.json` | Resumen de documentos subidos a Drive |
| 5 | `auto_05_base_datos_emails_completa.json` | Base de datos completa de emails clasificados |
| - | `base_datos_emails.csv` | Plantilla para Google Sheets (emails) |
| - | `base_datos_documentos.csv` | Plantilla para Google Sheets (documentos) |

---

## ⚙️ Configuración Inicial Requerida

### 1. Credenciales de Google

Para todas las automatizaciones necesitas configurar las credenciales de Google en N8N:

1. Ve a **Settings → Credentials → Add Credential**
2. Busca **Google** y selecciona **OAuth2**
3. Sigue las instrucciones para conectar tu cuenta de Google
4. Asegúrate de dar permisos para:
   - Gmail (lectura y escritura)
   - Google Drive (lectura y escritura)
   - Google Sheets (lectura y escritura)

### 2. Credenciales de OpenAI

1. Ve a **Settings → Credentials → Add Credential**
2. Busca **OpenAI**
3. Introduce tu API Key de OpenAI

### 3. Crear Google Sheets

#### Hoja para Emails (`base_datos_emails.csv`):
1. Crea un nuevo Google Sheet llamado "Base de Datos Emails"
2. Importa el archivo CSV o crea las columnas manualmente:
   - ID, Fecha_Recepcion, Remitente, Asunto, Resumen_IA
   - Categoria, Prioridad, Estado, Tiene_Adjunto, Ruta_Adjunto

#### Hoja para Documentos (`base_datos_documentos.csv`):
1. Crea un nuevo Google Sheet llamado "Registro de Documentos"
2. Importa el CSV o crea las columnas:
   - ID, Fecha_Subida, Nombre_Archivo, Tipo_Archivo
   - Ubicacion_Drive, Resumen_IA, Palabras_Clave, Subido_Por, Origen

### 4. Crear Carpeta en Google Drive

1. Crea una carpeta llamada "Adjuntos_Emails" en tu Drive
2. Copia el ID de la carpeta (está en la URL)
3. Úsalo en las automatizaciones donde dice `TU_ID_CARPETA_DRIVE`

---

## 📋 Descripción de Cada Automatización

### Auto 01: Resumen de Emails → Sheets
```
Gmail (nuevo email) → Extraer datos → IA resume y clasifica → Insertar en Sheets
```
**Uso**: Crear automáticamente un registro de todos los emails con resúmenes inteligentes.

### Auto 02: Respuesta Automática (Borrador)
```
Gmail (nuevo email) → IA redacta respuesta → Crear BORRADOR en Gmail
```
**Uso**: Tener respuestas pre-redactadas para revisar y enviar. NO se envía automáticamente.

### Auto 03: Adjuntos → Drive + Registro
```
Gmail (email con adjunto) → Descargar adjunto → Subir a Drive → Registrar en Sheets
```
**Uso**: Archivar automáticamente todos los adjuntos recibidos por email.

### Auto 04: Documentos en Drive → Resumen
```
Drive (nuevo archivo) → Descargar → IA resume → Registrar en Sheets
```
**Uso**: Tener un índice automático de todos los documentos con resúmenes.

### Auto 05: Base de Datos Completa
```
Gmail → Extraer todo → IA clasifica (categoría, prioridad, sentimiento) → Sheets → Si urgente → Notificar
```
**Uso**: Sistema completo de gestión de emails con alertas de urgencia.

---

## 🔧 Cómo Importar las Automatizaciones

1. Abre N8N
2. Ve a **Workflows**
3. Clic en **Import from File**
4. Selecciona el archivo `.json` de la automatización
5. **IMPORTANTE**: Después de importar, debes:
   - Conectar tus credenciales de Google
   - Conectar tus credenciales de OpenAI
   - Cambiar los IDs de Google Sheets y Drive donde dice `TU_ID_...`

---

## ⚠️ Notas Importantes

### Seguridad
- La Auto 02 crea BORRADORES, no envía emails automáticamente
- Siempre revisa los borradores antes de enviar
- La Auto 05 envía notificaciones solo para emails URGENTES

### Costes
- Cada email procesado consume tokens de OpenAI
- Modelo recomendado: `gpt-4o-mini` (más económico)
- Coste estimado: ~$0.001-0.003 por email procesado

### Límites
- Gmail API tiene límites de uso diario
- Para alto volumen, considera espaciar las ejecuciones

---

## 📞 Soporte

Si tienes dudas sobre la configuración o el funcionamiento:
1. Revisa la Sticky Note dentro de cada workflow
2. Consulta la documentación de N8N: https://docs.n8n.io
3. Contacta con el formador del curso

---

## 🎯 Casos de Uso en el Centro Educativo

| Automatización | Quién la usa | Para qué |
|----------------|--------------|----------|
| Auto 01 | Secretaría | Registro automático de comunicaciones |
| Auto 02 | Secretaría | Agilizar respuestas a familias |
| Auto 03 | Administración | Archivo automático de documentación |
| Auto 04 | Jefatura | Índice de normativa y documentos |
| Auto 05 | Dirección | Visión global del buzón + alertas |

---

*Creado para el curso de automatización N8N - Febrero 2024*
