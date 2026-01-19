# 📖 Glosario Técnico: Ciberseguridad & Sistemas (Inglés/Español)

**Propietario:** MauricioSec
**Estado:** Vivo (Se actualiza constantemente)
**Fuentes:** Laboratorios Prácticos + Biblioteca Personal (PDFs)

---

## 🛡️ 1. Conceptos Fundamentales de Ciberseguridad

| Término (Inglés) | Pronunciación Aprox. | Significado (Español) | Contexto de Uso (Analista SOC) |
| :--- | :--- | :--- | :--- |
| **Cybersecurity** | *Sái-ber-se-kiú-ri-ti* | Ciberseguridad | Protección de sistemas y redes contra ataques digitales. |
| **Blue Team** | *Blu Tim* | Equipo Azul | Defensores. Configuran firewalls, monitorean logs y responden a incidentes. |
| **Red Team** | *Red Tim* | Equipo Rojo | Atacantes éticos. Simulan intrusiones para probar las defensas. |
| **SOC** | *Sok* | Centro de Ops. de Seguridad | La base central donde se monitorea la seguridad 24/7. |
| **Malware** | *Mal-güer* | Software Malicioso | Término general para virus, troyanos, ransomware, etc. |
| **Firewall** | *Fáier-guol* | Cortafuegos | Dispositivo o software que filtra el tráfico (lo deja pasar o lo bloquea). |
| **Vulnerability** | *Vul-ne-ra-bí-li-ti* | Vulnerabilidad | Un fallo o debilidad en un sistema que puede ser explotado. |
| **Exploit** | *Ex-plóit* | Explotar / Aprovechar | Código diseñado para aprovechar una vulnerabilidad y entrar al sistema. |

---

## 🌐 2. Redes y Protocolos (Networking)

| Término (Inglés) | Pronunciación Aprox. | Significado (Español) | Contexto de Uso (Analista SOC) |
| :--- | :--- | :--- | :--- |
| **Host** | *Jóst* | Anfitrión | Cualquier dispositivo conectado a la red con una IP. |
| **IP Address** | *Ai-Pí A-dres* | Dirección IP | Identificador lógico (ej: 192.168.1.5). Es como la dirección de tu casa. |
| **MAC Address** | *Mak A-dres* | Dirección Física | Identificador de fábrica de la tarjeta de red. Es como tu huella digital. |
| **Port** | *Port* | Puerto | Canal lógico numerado (ej: 80, 443) para servicios específicos. |
| **Socket** | *Só-ket* | Enchufe | Combinación de IP + Puerto (ej: 192.168.1.5:80). |
| **Packet** | *Pá-ket* | Paquete | Unidad de datos que viaja por la red (Capa 3). |
| **Handshake** | *Jánd-sheik* | Apretón de manos | El saludo inicial entre dos computadoras para establecer conexión (TCP). |
| **Throughput** | *Zrú-put* | Rendimiento Real | La velocidad real de transferencia de datos en un momento dado. |
| **Gateway** | *Guéit-güei* | Puerta de Enlace | El router que te permite salir de tu red local hacia Internet. |

---

## 🐧 3. Linux y Sistemas Operativos

| Término (Inglés) | Pronunciación Aprox. | Significado (Español) | Contexto de Uso (Analista SOC) |
| :--- | :--- | :--- | :--- |
| **Kernel** | *Kér-nel* | Núcleo | El corazón del SO. Gestiona la memoria y el hardware. |
| **Shell** | *Shel* | Concha / Intérprete | La interfaz de texto (terminal) donde escribes comandos. |
| **Root** | *Rút* | Raíz | El "Superusuario" o Administrador en Linux. Tiene poder total. |
| **Sudo** | *Sú-du* | SuperUser Do | Comando para ejecutar acciones con permisos de administrador temporalmente. |
| **Directory** | *Dai-réc-to-ri* | Directorio | Carpeta. |
| **Permissions** | *Per-mí-shons* | Permisos | Reglas de quién puede leer (r), escribir (w) o ejecutar (x) un archivo. |
| **Log** | *Log* | Bitácora / Registro | Archivo de texto histórico. "Si no está en el log, no sucedió". |
| **Script** | *Script* | Guion | Archivo de texto con una serie de comandos que se ejecutan en orden. |

---

## 💻 4. Programación y Web (Coding)

| Término (Inglés) | Pronunciación Aprox. | Significado (Español) | Contexto de Uso (Analista SOC) |
| :--- | :--- | :--- | :--- |
| **Database** | *Déi-ta-beis* | Base de Datos | Almacén estructurado de información (SQL). Objetivo común de ataques. |
| **Query** | *Cu-é-ri* | Consulta | Pregunta o petición hecha a una base de datos. |
| **Buffer Overflow**| *Bá-fer O-ver-flóu* | Desbordamiento de Memoria | Error crítico (común en C/C++) donde se escriben más datos de los que caben, permitiendo hackeos. |
| **Compiler** | *Com-pái-ler* | Compilador | Traduce código humano a binario (ej: C++, Java). |
| **Interpreter** | *In-tér-pre-ter* | Intérprete | Ejecuta código directamente sin compilar (ej: Python, PHP, Bash). |
| **Bug** | *Bag* | Bicho / Error | Fallo en el código. Un bug de seguridad es una puerta abierta. |
| **Request** | *Ri-cuést* | Petición | Lo que tu navegador pide al servidor (ej: "Dame la foto"). |
| **Response** | *Ri-spons* | Respuesta | Lo que el servidor devuelve (ej: "Aquí está la foto" o "Error 404"). |
