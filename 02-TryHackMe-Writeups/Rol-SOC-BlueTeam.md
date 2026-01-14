# 🛡️ El Rol del SOC en el Blue Team

**Fecha:** 14 de Enero, 2026
**Módulo:** The Role of the SOC in the Blue Team
**Plataforma:** TryHackMe

---

## 1. La Jerarquía de Seguridad (Chain of Command)
La seguridad no es solo técnica, es un objetivo de negocio. La estructura típica en grandes empresas es:

1.  **CEO (Director Ejecutivo):** Se enfoca en los objetivos globales y comerciales.
2.  **CISO (Chief Information Security Officer):** Es el puente entre el negocio y la tecnología. Traduce los riesgos técnicos (ej: vulnerabilidades) a riesgos de negocio (ej: pérdida de dinero).
3.  **Departamentos de Seguridad:** Equipos especializados que reportan al CISO.

> **Nota:** Las prioridades cambian según la industria. Un hospital prioriza la seguridad del paciente, mientras que una fábrica prioriza que la línea de producción no se detenga (Disponibilidad).

---

## 2. Los Departamentos de Seguridad
En empresas maduras, el CISO supervisa tres áreas principales:

### 🔴 Red Team (Seguridad Ofensiva)
* **Rol:** Simulan ser atacantes reales.
* **Quiénes son:** Pentesters, Hackers Éticos.
* **Objetivo:** Encontrar fallos de seguridad atacando los sistemas antes que los criminales reales.

### 🔵 Blue Team (Seguridad Defensiva)
* **Rol:** Defensores activos de la organización.
* **Quiénes son:** **Analistas SOC**, Ingenieros de Seguridad, Incident Responders.
* **Objetivo:** Detectar intrusiones, bloquear ataques y responder a incidentes en tiempo real.
* *¡Aquí es donde pertenezco como Analista SOC!*

### 📜 GRC (Gobierno, Riesgo y Cumplimiento)
* **Rol:** La parte "legal" y normativa.
* **Quiénes son:** Auditores, Analistas de Riesgo.
* **Objetivo:** Asegurar que la empresa cumpla con las leyes (como PCI-DSS para tarjetas de crédito o GDPR para privacidad) y tenga políticas claras.

---

## 🧠 Conclusión Personal
El SOC no trabaja aislado. Somos parte del **Blue Team**, protegiendo la infraestructura contra los hallazgos que el **Red Team** descubre y siguiendo las reglas que el equipo de **GRC** establece.

---

## 3. Sub-departamentos del Blue Team
Dentro del equipo defensivo, hay especializaciones clave:

### 🏢 SOC (Security Operations Center)
* **Función:** Es la "Primera Línea de Defensa".
* **Actividad:** Monitoreo continuo 24/7, manejo de alertas y triage inicial.
* **Quiénes:** Analistas L1 (Triage), L2 (Investigación), Ingenieros y Managers.

### 🚒 CIRT (Cyber Incident Response Team)
* **Función:** Son los "Bomberos" de la ciberseguridad.
* **Actividad:** Se activan cuando un incidente es **urgente** o se sale de control del SOC. Manejan brechas críticas.
* **Habilidad Clave:** Profundo conocimiento de amenazas sin depender solo de alertas automáticas.

### 🕵️‍♂️ Roles Especializados
* **Digital Forensics:** Analizan discos y memoria para encontrar evidencias ocultas post-incidente.
* **Threat Intelligence:** Espían a los atacantes para predecir sus movimientos.

* ---

## 4. Tipos de Entornos de Trabajo: Interno vs. MSSP
Al buscar trabajo, es crucial entender los dos entornos principales donde opera un analista:

### 🏦 SOC Interno (Internal SOC)
* **Definición:** Trabajas directamente para la empresa (ej: Un Banco) protegiendo solo su infraestructura.
* **Ritmo:** Generalmente más tranquilo, turnos estables.
* **Profundidad:** Usas pocas herramientas, pero debes dominarlas a la perfección.
* **Exposición:** Ves menos incidentes, pero los investigas a fondo.

### 🚀 MSSP (Managed Security Service Provider)
* **Definición:** Trabajas para una empresa de seguridad que protege a *muchos* clientes externos a la vez.
* **Ritmo:** Alta presión, colas de alertas constantes.
* **Amplitud:** Tienes que adaptarte a docenas de herramientas diferentes de cada cliente.
* **Exposición:** Aprendizaje acelerado (“Trial by fire”) debido al alto volumen y variedad de ataques semanales.

> **Plan de Carrera:** El paso natural después de dominar el rol de **Analista L1** es ascender a **Analista L2** (Investigación profunda), aunque también se puede derivar hacia Ingeniería de Detección o Respuesta a Incidentes (CIRT).
>
> ---

## 🎮 Desafío Práctico: Simulador "TrySecureMe"
Como ejercicio final, asumí el rol de CISO para gestionar 7 incidentes simultáneos, asignando los recursos correctos según la gravedad y naturaleza del evento.

### 📋 Resolución de Incidentes
1.  **Triage de Alerta Firewall:** Asignado a **SOC L1 Analyst** (Filtrado inicial).
2.  **Análisis de Malware/Phishing:** Asignado a **SOC L2 Analyst** (Investigación profunda).
3.  **Fallo Técnico del SIEM:** Asignado a **SOC Engineer** (Mantenimiento de herramientas).
4.  **Ataque de Ransomware (Crítico):** Asignado a **CIRT Lead** (Respuesta a incidentes de alta gravedad).
5.  **Test de Nueva App Web:** Asignado a **Penetration Tester** (Seguridad Ofensiva preventiva).
6.  **Auditoría de Tarjetas (PCI DSS):** Asignado a **GRC Auditor** (Cumplimiento normativo).
7.  **Investigación de Grupo Criminal (FIN7):** Asignado a **Threat Researcher** (Inteligencia de Amenazas).

**🏆 Flag Obtenida:** `THM{trysecureme_is_secured!}`
