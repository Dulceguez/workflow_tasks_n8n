# Task Automation System – n8n

Sistema de automatización de tareas construido con **n8n**, **Google Sheets** y **correo electrónico**.  
Permite crear nuevas tareas desde un formulario HTML, notificar su creación por correo y enviar recordatorios diarios.

---

## 🔹 Workflows

### 1. Create Task Workflow
- Recibe nuevas tareas desde un **formulario HTML** 
- Convierte la prioridad en un **emoji** usando un **Function node** (🔴 alta, 🟠 media, 🟢 baja)
- Guarda las tareas en **Google Sheets**  
- Envía un **correo electrónico** notificando la creación de la tarea  

**Archivo:** `workflows/create-task-workflow.json`  
**Interfaz:** `html/tracker_tareas.html`

### 2. Daily Reminder Workflow
- Se ejecuta todos los días a las **9:00 AM**  
- Revisa las tareas de hoy en Google Sheets  
- Envía un **correo recordatorio** por cada tarea  

**Archivo:** `workflows/daily-reminder-workflow.json`

---

## 🛠 Tech Stack
- **n8n**  
- **Google Sheets** (almacenamiento de tareas)  
- **Email node** (Gmail)  
- **HTML** (formulario de creación de tareas)  
- **Function nodes** (JavaScript) para lógica personalizada  

---

## ⚙️ Cómo usar
1. Importa los workflows desde la carpeta `/workflows` en tu instancia de n8n.  
2. Configura tus credenciales de Google Sheets y Gmail en n8n.  
3. Sube el HTML a un servidor o abre localmente para enviar tareas.  
4. Ajusta triggers según tu zona horaria si es necesario.  

---

## 🎥 Workflow Demo 

Este video muestra como el workflow crea una tarea automaticamente y la envia por Gmail.

[▶ Ver demo](./create_task_recording.mp4)

