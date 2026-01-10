# 🛡️ SOC Fundamentals - TryHackMe Write-up

**Fecha:** 06 de Enero, 2026
**Categoría:** Blue Team / Operaciones de Seguridad
**Plataforma:** TryHackMe

## 🎯 Objetivo del Módulo
Comprender la estructura, roles y procesos dentro de un Centro de Operaciones de Seguridad (SOC). Entender cómo fluye un incidente desde la detección hasta la respuesta.

## 🧠 Conceptos Clave Aprendidos

### 1. ¿Qué es un SOC?
Significa **Security Operations Center** (Centro de Operaciones de Seguridad).
Es una instalación dedicada donde un equipo especializado trabaja **24/7** para monitorear continuamente la red, identificar actividades sospechosas y prevenir daños.

### 2. Los Niveles de Analistas (Tiers)
* **Analista Nivel 1 (Triage):** monitoreo, filtrar falsos positivos.
* **Analista Nivel 2 (Incident Responder):** Investigación profunda.
* **Analista Nivel 3 (Threat Hunter):** Búsqueda proactiva.

### Roles de Soporte y Gestión
Además de los analistas, el SOC necesita:
* **Security Engineer (Ingeniero de Seguridad):** Se encarga de que las herramientas (SIEM, EDR) funcionen bien. Ellos configuran e implementan el software.
* **Detection Engineer (Ingeniero de Detección):** Escribe la "lógica" o reglas específicas para detectar amenazas nuevas.
* **SOC Manager:** Gestiona al equipo, los procesos y reporta directamente al CISO (Jefe de Seguridad).

### 3. Herramientas Esenciales
* **SIEM:** (Security Information and Event Management)
* **EDR:** (Endpoint Detection and Response)

### 4. Capacidades Principales del SOC
El enfoque principal se divide en dos grandes áreas:
* **Detección (Detection):** Encontrar vulnerabilidades, intrusiones o actividad no autorizada (ej: alguien intentando loguearse con una contraseña robada).
* **Respuesta (Response):** Análisis de causa raíz y minimización del impacto una vez confirmado el incidente.

### 5. Los 3 Pilares del SOC
Para que un SOC funcione, necesita el equilibrio entre:
1.  **People (Gente):** El equipo humano (analistas) disponible 24/7.
2.  **Process (Procesos):** Las reglas y procedimientos estandarizados.
3.  **Technology (Tecnología):** Las herramientas (Hardware/Software) que usan.

### 6. El Proceso de Triage (Las 5 Ws)
El trabajo principal de un Analista Tier 1 es el **Triage**: investigar una alerta para decidir si es real o falsa. Para hacerlo, debo responder las 5 preguntas clave:

1.  **What (Qué):** ¿Qué pasó? (Ej: Malware detectado, Exfiltración de datos).
2.  **When (Cuándo):** ¿A qué hora ocurrió? (Vital para correlacionar logs).
3.  **Where (Dónde):** ¿En qué máquina o carpeta? (Ej: Host "GEORGE PC").
4.  **Who (Quién):** ¿Qué usuario está involucrado? (Ej: Usuario "John").
5.  **Why (Por qué):** La causa raíz (Ej: Descargó software pirata).

### 7. Tecnología y Herramientas Principales
El "músculo" del SOC para centralizar y automatizar:

* **SIEM (Security Information and Event Management):**
    * **Función:** Recolecta registros (logs) de toda la empresa en un solo lugar.
    * **Clave:** Usa reglas de correlación para detectar cosas sospechosas. Se enfoca en **Detección y Alerta**.
* **EDR (Endpoint Detection and Response):**
    * **Función:** Es como un antivirus evolucionado. Se instala en cada dispositivo (endpoint).
    * **Clave:** Da visibilidad en tiempo real y permite **Responder** (aislar un PC, matar un proceso) automáticamente.
* **Firewall:**
    * **Función:** La barrera de la red.
    * **Clave:** Monitorea y filtra todo el tráfico que entra y sale de la organización.
  
## 🔍 Ejercicio Práctico / Reto
* **Reto:** Identificar componentes del SOC.
* **Solución/Análisis:** Se identificó que el monitoreo proactivo reduce el "Dwell Time" (tiempo de permanencia del atacante).

## 🔗 Conexión con mi Biblioteca Teórica
Este módulo se conecta directamente con el concepto de **"Defensa en Profundidad"** que tengo en mi bibliografía, ya que el SOC monitorea las distintas capas de seguridad (Física, Red, Host) para detectar intrusiones.

## 🏁 Conclusión
El SOC es el cerebro de la ciberseguridad defensiva. Mi rol como Junior será ser los "ojos" que filtran el ruido para encontrar las amenazas reales.

## 🏁 Resultado del Laboratorio Práctico
* **Actividad:** Port Scanning.
* **Origen:** Host NESSUS (10.0.0.8).
* **Destino:** 10.0.0.3.
* **Clasificación:** Falso Positivo (Actividad autorizada por el equipo de vulnerabilidades).
* **Flag obtenida:** `THM{000_INTRO_TO_SOC}`

### 💡 Lección Aprendida
Como Analista Tier 1, la comunicación interna es vital. Saber que el equipo de vulnerabilidades estaba haciendo pruebas me permitió cerrar una alerta de "Alta Severidad" como un falso positivo rápidamente, evitando pánico innecesario en la organización.
