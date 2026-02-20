# 🛡️ Reporte de Progreso: Formación Continua - Analista SOC

**Perfil:** MauricioSec | Analista SOC en Formación
**Objetivo del Repositorio:** Documentar la ruta de aprendizaje estructurada, laboratorios prácticos y asimilación de competencias técnicas para operaciones de ciberseguridad defensiva (Blue Team).
**Estado:** Activo / En Progreso 🔄

---

## 🎯 Resumen Ejecutivo
Este documento detalla el avance técnico y la consolidación de la "Mentalidad SOC". La formación se ha estructurado evitando saltos, comenzando desde los fundamentos absolutos de la informática y redes, hasta el análisis de evidencia digital y correlación de eventos, manteniendo siempre un enfoque operativo y agnóstico a la plataforma.

---

## 🧠 1. Mentalidad Operativa y Fundamentos (Base Técnica)
Comprender el "terreno" antes de defenderlo. No se trata de memorizar ataques, sino de entender cómo piensan los sistemas.

* **Definición del Rol:** Diferenciación clara entre Blue Team (defensa, monitorización, respuesta) y Red Team (evaluación ofensiva).
* **Tríada CIA:** Comprensión de los pilares de la seguridad (Confidencialidad, Integridad, Disponibilidad) y cómo cada ataque busca quebrar uno o más de estos principios.
* **Flujo de Trabajo SOC:** Recepción de alertas, validación de contexto, investigación de incidentes y manejo de Falsos Positivos para evitar la fatiga de alertas.

---

## 🐧 2. El Terreno: Sistemas Operativos (Linux)
El Analista SOC vive dentro de los sistemas operativos. Se ha desarrollado la capacidad de operar, administrar y auditar sistemas basados en Linux exclusivamente desde la Interfaz de Línea de Comandos (CLI).

* **Navegación y Administración:** Dominio de la jerarquía del sistema de archivos (`/etc`, `/var/log`, `/home`, `/bin`).
* **Gestión de Permisos:** Comprensión profunda de la notación octal y permisos `rwx`. Identificación de configuraciones de riesgo (ej. `chmod 777`).
* **Control de Procesos:** Monitorización del sistema (`ps`, `top`) y gestión del ciclo de vida de los procesos (`kill`).
* **Identidad y Privilegios:** Uso de los principios de menor privilegio (SUDO vs Root).

---

## 🌐 3. Visibilidad de Redes (Networking)
"Si entiendo la conversación, no necesito leer el mensaje". Dominio de cómo viajan los datos para detectar anomalías en el comportamiento de la red.

* **Modelo OSI y TCP/IP:** Comprensión del encapsulamiento (Capas 1 a 7) para entender exactamente dónde ocurre cada protocolo.
* **Comportamiento del Tráfico:** * Diferenciación de conexiones entrantes y **salientes** (Vital para detectar exfiltración de datos o balizamiento C2).
  * Reconocimiento de que el cifrado (HTTPS) oculta el contenido, pero no el comportamiento (volumen, frecuencia, destino).
* **Auditoría y Diagnóstico:** Uso de herramientas de descubrimiento y análisis (`ping`, `nmap`, escaneo de puertos, `netcat`).

---

## 🕵️‍♂️ 4. Análisis de Logs y Evidencia Digital
El corazón del SOC. Los logs son el registro estructurado de eventos objetivos; sin logs no hay investigación.

* **Filosofía del Analista:** No se lee línea por línea al azar. Se busca contexto: *¿Es normal para este sistema? ¿Es normal para este usuario/horario?*
* **Técnicas de Búsqueda Offline:** Procesamiento de grandes volúmenes de texto (syslog, auth.log) mediante herramientas de terminal.
* **Correlación Manual:** Identificación de patrones combinados. Entender que eventos aislados (un fallo de login, un comando sudo, una conexión externa) no dicen nada por sí solos, pero juntos cuentan una historia de compromiso.

---

## 🛠️ Arsenal Técnico y Laboratorios Destacados
* **Despliegue de SOC Móvil:** Transformación de un entorno Android (Termux) en una estación de trabajo Linux auditando infraestructura real.
* **Scripting Defensivo:** Desarrollo de herramientas propias en **Bash** para descubrimiento de red (optimizando la latencia con subprocesos y paralelismo).
* **Análisis Forense con CLI:** Uso de `grep`, `awk`, `sort`, `uniq` para filtrar ruido, extraer indicadores de compromiso (IPs atacantes) y contabilizar incidencias (Top Talkers).
* **Sniffing de Red:** Intercepción de paquetes con `tcpdump` para diseccionar la comunicación a nivel de capa 3 y 4.

---

## 🚀 Próximos Pasos (Hoja de Ruta)
* **Integración de Programación:** Inicio de formación formal en **Desarrollo Full Stack Python** (Beca SENCE / Talento Digital).
* **Objetivo a corto plazo:** Aplicar la lógica de programación y Python para automatizar la recolección de logs, el análisis de red y la construcción de scripts orientados a la ciberseguridad.

> *"La ciberseguridad no depende del hardware, sino de la capacidad del analista para interrogar al sistema y entender el patrón."*
