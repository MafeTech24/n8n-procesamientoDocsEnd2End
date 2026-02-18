# 🤖 Sistema Backend de Procesamiento Documental con Gemini AI (n8n)

Pipeline backend **API-First** para la ingesta, procesamiento y extracción estructurada de documentos (facturas/recibos) utilizando **n8n**, **Gemini 2.5 Flash**, **Supabase** y **Google Sheets**.  
Incluye **detección de duplicados (hashing)**, **confidence scoring**, persistencia estructurada y **monitoreo en tiempo real**.


---

## 🎯 Problema

El procesamiento manual de facturas y documentos administrativos presenta limitaciones típicas:

- Alto consumo de tiempo operativo
- Propensión a errores humanos
- Falta de trazabilidad y auditoría
- Riesgo de duplicación de documentos
- Ausencia de validación automática
- Dificultad para escalar el proceso

---

## ✅ Solución

Se desarrolló un pipeline backend con **n8n** que:

- Recibe documentos vía **Webhook**
- Normaliza los datos de entrada
- Detecta duplicados mediante **hashing**
- Persiste datos y estados en **Supabase**
- Extrae texto (OCR)
- Procesa y estructura información con **Gemini 2.5 Flash**
- Calcula un **confidence score**
- Registra resultados en **Google Sheets** (logging + dashboard)
- Genera reportes listos para auditoría / publicación

Todo el proceso ocurre **sin intervención humana**.

---

## 🧩 Arquitectura del Workflow

Workflow completo:

![](./assets/1.workflowTerminado.jpg)

Ejecución exitosa:

![](./assets/7.flujoExitoso.jpg)

---

## ⚙️ Funcionalidades Implementadas

- ✅ API-First document intake (Webhook)
- ✅ OCR document processing
- ✅ AI structured extraction (Gemini)
- ✅ Confidence scoring
- ✅ Duplicate detection (hashing)
- ✅ Database persistence (Supabase)
- ✅ Real-time logging (Google Sheets)
- ✅ Automated reporting
- ✅ Fully automated workflow

---

## 🛠️ Tech Stack

- **n8n** — Orquestación de workflows / integración
- **Gemini 2.5 Flash** — Extracción y estructuración inteligente
- **Supabase** — Persistencia y trazabilidad (DB)
- **Google Sheets** — Logging + dashboard en tiempo real
- **JavaScript** — Lógica de negocio (normalización, hash, scoring)

---

## 🔌 Ingesta vía Webhook (Testing)

El sistema expone un endpoint para recibir documentos desde cualquier sistema externo.

Ejemplo de test en Postman:

![](./assets/4.testPostman.jpg)

**Respuesta esperada:** `Workflow was started`  
Esto confirma que la ingesta dispara el pipeline.

---

## 🗄️ Persistencia en Base de Datos (Supabase)

Cada documento procesado se almacena con:

- `document_hash` (hash único)
- `file_name`
- `extracted_data` (JSON estructurado)
- `confidence_score`
- `status`
- `created_at`

Vista de tabla en Supabase:

![](./assets/2.bdSupabase.jpg)

Esto permite:

- Trazabilidad completa
- Auditoría
- Evitar duplicados

---

## 📊 Logging y Dashboard en Tiempo Real (Google Sheets)

Cada ejecución registra un log estructurado con, por ejemplo:

- `ocrText`
- `extractedData` (JSON)
- `confidence_score`
- `timestamp / created_at`
- `status`

Ejemplo de registros:

![](./assets/3.registroProcesamiento.jpg)

---

## 🎯 Confidence Scoring Automático

El pipeline calcula un puntaje de confianza considerando:

- Completitud de campos esperados
- Validación / consistencia del output de IA
- Señales de “missing fields” o incertidumbre

Ejemplo (confidence score visible en el dashboard):

![](./assets/5.puntuacionConfianza.jpg)

Esto permite:

- Detectar documentos confiables
- Marcar casos que requieren revisión manual (si se desea agregar esa regla)

---

## 📣 Generación Automática de Reportes

El sistema genera contenido listo para auditoría o publicación (ej: formato de post):

![](./assets/6.reporte.jpg)

---

## 🧠 Arquitectura Técnica (Resumen)

Pipeline:

**Webhook**  
→ Normalization  
→ Hashing  
→ Supabase Persistence  
→ OCR  
→ Gemini AI Processing  
→ Confidence Scoring  
→ Google Sheets Logging  
→ Reporting

---

## 📈 Resultados

- ⚡ Procesamiento automático en segundos
- 🎯 Extracción estructurada confiable
- 📊 Monitoreo en tiempo real
- 🔒 Eliminación de duplicados
- 🤖 Flujo 100% automatizado

---

## 🧑‍💻 Mi Rol

- Diseño de arquitectura backend completa
- Implementación del workflow en n8n
- Integración con Gemini AI
- Desarrollo de lógica en JavaScript
- Integración con Supabase
- Implementación de confidence scoring
- Implementación de logging y dashboards
- Testing end-to-end
- Documentación técnica

---

## 💼 Casos de Uso

Este sistema puede aplicarse a:

- Procesamiento de facturas
- Automatización contable
- Document intake empresarial
- Automatización administrativa
- Integraciones con sistemas ERP
- Flujos de RPA y backoffice

---

## Author

Maria Fernanda Moreno  
Automation Developer | AI Automation | n8n  

> Showcase de proyectos: https://showcase-de-automatizaciones-y-webs.vercel.app/
---
