# 🤖 Sistema Backend de Procesamiento Documental con Gemini AI

Pipeline backend automatizado para la ingesta, procesamiento y análisis inteligente de documentos utilizando <b>n8n, Gemini 2.5 Flash, Supabase y Google Sheets</b>, incluyendo <b>confidence scoring</b>, persistencia estructurada y monitoreo en tiempo real.


## 🎯 Problema

- El procesamiento manual de facturas y documentos administrativos presenta múltiples limitaciones:

- Alto consumo de tiempo operativo

- Propensión a errores humanos

- Falta de trazabilidad

- Riesgo de duplicación de documentos

- Ausencia de validación automática

- Dificultad para escalar el proceso

Las organizaciones necesitan un sistema backend automatizado capaz de:

- Recibir documentos

- Procesarlos con IA

- Validarlos

- Persistirlos

- Monitorearlos en tiempo real
  

## 🚀 Solución

Se desarrolló un <b>pipeline backend API-First utilizando n8n</b> que:

• recibe documentos vía webhook<br><br>
• normaliza los datos <br><br>
• detecta duplicados mediante hashing <br><br>
• extrae texto mediante OCR <br><br>
• analiza el contenido utilizando Gemini 2.5 Flash <br><br>
• calcula un confidence score automático <br><br>
• almacena resultados estructurados en Supabase <br><br>
• genera logs y dashboards en Google Sheets <br><br>
• produce reportes automáticos <br><br>

Todo el proceso ocurre <b>sin intervención humana.</b>


## 🧠 Arquitectura del Workflow


![](./assets/1.workflowTerminado.jpg) 





## 🔌 Ingesta vía Webhook (Testing)



![](./assets/4.testPostman.jpg)



El sistema expone un endpoint para recibir documentos desde cualquier sistema externo.

Ejemplo de test utilizando Postman:

Respuesta:

``` 
Workflow was started

```` 

Esto confirma la ejecución del pipeline.




## 🗄️ Persistencia en Base de Datos (Supabase)


Cada documento procesado se almacena con:

• hash único <br><br>
• nombre <br><br>
• datos extraídos <br><br>
• confidence score <br><br>
• estado <br><br>
• timestamp <br><br>


![](./assets/2.bdSupabase.jpg) 



Esto permite:

• trazabilidad completa <br><br>
• auditoría <br><br>
• evitar duplicados <br><br>




## 📊 Logging y Dashboard en Tiempo Real


Cada ejecución genera registros estructurados en Google Sheets:

Incluye:

• OCR Text <br><br>
• Datos estructurados <br><br>
• Confidence score <br><br>
• Timestamp <br><br>
• Status <br><br>


![](./assets/3.registroProcesamiento.jpg)





## 🎯 Confidence Scoring Automático

El sistema calcula un puntaje de confianza basado en:

• completitud de datos <br><br>
• validación IA <br><br>
• consistencia <br><br>

Ejemplo:


![](./assets/5.puntuacionConfianza.jpg) 



Esto permite:

• detectar documentos confiables <br><br>
• identificar documentos que requieren revisión <br><br>



## 📢 Generación Automática de Reportes

El sistema genera contenido listo para auditoría o publicación.

Ejemplo:


![](./assets/6.reporte.jpg)





✅ Ejecución Exitosa del Pipeline

Workflow completo ejecutado correctamente:


![](./assets/7.flujoExitoso.jpg)





## 🛠️ Tech Stack
 
Orquestación:

<b>- n8n </b>

 Inteligencia Artificial:

<b>- Gemini 2.5 Flash</b>

Backend:

<b>- JavaScript</b>

Base de datos:

<b>- Supabase</b>

Dashboard:

<b>- Google Sheets</b>

Integración:

<b>- REST API</b>

<b>- Webhooks </b>




## ⚙️ Funcionalidades Implementadas


✔ API-First document intake <br><br>
✔ OCR document processing <br><br>
✔ AI structured extraction <br><br>
✔ Confidence scoring <br><br>
✔ Duplicate detection (hashing) <br><br>
✔ Database persistence <br><br>
✔ Real-time logging <br><br>
✔ Automated reporting <br><br>
✔ Fully automated workflow <br><br>




## 🧩 Arquitectura Técnica


Pipeline:

Webhook <br><br>
→ Normalization <br><br>
→ Hashing <br><br>
→ Supabase Persistence <br><br>
→ OCR <br><br>
→ Gemini AI Processing <br><br>
→ Confidence Scoring <br><br>
→ Google Sheets Logging <br><br>
→ Reporting <br><br>




## 📈 Resultados

⚡ Procesamiento automático en segundos

🎯 Extracción estructurada confiable

📊 Monitoreo en tiempo real

🔒 Eliminación de duplicados

🤖 100% automatizado




## 🧑‍💻 Mi Rol

• Diseño de arquitectura backend completa <br><br>
• Implementación workflow en n8n <br><br>
• Integración con Gemini AI <br><br>
• Desarrollo lógica en JavaScript <br><br>
• Integración Supabase <br><br> 
• Implementación confidence scoring <br><br>
• Implementación logging y dashboards <br><br>
• Testing end-to-end <br><br>
• Documentación técnica <br><br>


## 💼 Caso de Uso

Este sistema puede aplicarse a:

• procesamiento de facturas <br><br>
• automatización contable <br><br>
• document intake empresarial <br><br>
• automatización administrativa <br><br>
• sistemas ERP <br><br>
• RPA <br><br>
