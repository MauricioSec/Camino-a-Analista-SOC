# 📚 Fundamentos de Redes y Modelo OSI (Capas 1 y 2)

**Fuente Original:** Conceptos de redes de computadoras (MSc. Ing. Angel Caffa - UdelaR)
**Fecha de Estudio:** 11 de Enero, 2026
**Categoría:** Networking / Teoría Fundamental

---

## 1. Contexto y Fundamentos Informáticos
Para comprender las redes, primero se debe nivelar el conocimiento sobre la arquitectura base de la computadora, definida por el esquema clásico: **Entrada - Proceso - Salida**.

### Arquitectura de Hardware
* **Periféricos:** De entrada (teclado, mouse), salida (monitores) y procesamiento (CPU).
* **Jerarquía de Memoria:**
    * **RAM:** Volátil y de trabajo. (Crítica en análisis forense por contener datos en vivo).
    * **ROM:** De arranque y permanente.
    * **Almacenamiento Secundario:** Persistente (Discos duros, cintas, medios ópticos).

### Software
* Se diferencia entre **Sistema Operativo** y **Aplicación**.
* La seguridad del sistema depende de su arquitectura: si es **mono/multiusuario** y **mono/multitarea**.

---

## 2. Redes de Computadoras: Definición y Evolución
Se define una red como un conjunto de computadoras autónomas interconectadas para compartir recursos.

* **Cambio de Paradigma:** Se pasó del modelo centralizado (Mainframes) a la computación en red distribuida, ganando flexibilidad, escalabilidad y tolerancia a fallos.
* **Modelo Cliente/Servidor:** Arquitectura predominante donde:
    * **Servidor:** Gestiona lógica y datos pesados.
    * **Cliente:** Gestiona la interfaz.
    * *Beneficio:* Optimiza el tráfico de red y el procesamiento local.
* **Teoría de Grafos:** Se usa para modelar redes matemáticamente (Vértices = Hosts, Aristas = Conexiones).

---

## 3. Modelos de Referencia (OSI y TCP/IP)
Para estandarizar la comunicación global, se utilizan modelos de abstracción por capas.

### Modelo OSI (Open Systems Interconnection)
Es la columna vertebral teórica. Divide la comunicación en 7 capas:
1.  **Física**
2.  **Enlace**
3.  **Red**
4.  **Transporte**
5.  **Sesión**
6.  **Presentación**
7.  **Aplicación**

> **Encapsulamiento:** Proceso donde los datos bajan por la pila agregando cabezales (encapsulado) y suben en el destino quitándolos (desencapsulado).

---

## 4. Análisis de Capas Inferiores (Capa 1 y 2)

### Capa 1: Física (Transmisión de Bits)
Su objetivo es transmitir "bits brutos" a través de un medio físico.

* **Medios de Transmisión:**
    * **Guiados:** Par trenzado (UTP/STP), Coaxial y Fibra Óptica (inmune a interferencias electromagnéticas).
    * **No Guiados:** Radiofrecuencia, microondas y satélites.
* **Conceptos Clave:**
    * **Ancho de banda:** Velocidad máxima teórica (Teoremas de Nyquist y Shannon).
    * **Módem:** Modulación/Demodulación para usar líneas analógicas.
    * **Multiplexión:** Compartir un canal (por tiempo o frecuencia).

### Capa 2: Enlace de Datos (Estructuración)
Transforma la transmisión de bits "crudos" en una línea libre de errores para la capa superior.

* **Tramas (Frames):** Unidad de datos de esta capa.
* **Subcapas:**
    * **MAC (Media Access Control):** Gestiona el acceso al medio físico (Direccionamiento Físico).
    * **LLC (Logical Link Control):** Control de flujo y errores.
* **Integridad de Datos:**
    * **Distancia de Hamming:** Teoría para detección y corrección de errores.
    * **Métodos:** Paridad, CRC (Comprobación de Redundancia Cíclica).

---

## 🏁 Síntesis
El documento establece que la red física (cables, fibra) y la lógica de enlace (tramas, corrección de errores) son la base sobre la cual se construye toda la comunicación digital moderna. Sin una Capa 1 y 2 robustas, el enrutamiento y las aplicaciones no pueden existir.

---

## 🛡️ Nota del Analista (Aplicación SOC)
* **Capa 1 en Ciberseguridad:** La seguridad física es el primer control. Si un atacante tiene acceso físico al cable o al switch, puede realizar un "Tap" o desconectar servicios (Denegación de Servicio física).
* **Capa 2 en Ciberseguridad:** Aquí ocurren ataques de red local como el **ARP Spoofing** o **MAC Flooding**. Comprender la subcapa MAC es vital para investigar incidentes dentro de la LAN.
* **Memoria RAM:** Entender su volatilidad es fundamental para la respuesta a incidentes; si se apaga un equipo comprometido, se pierde la evidencia en la memoria (claves de cifrado, procesos maliciosos).
