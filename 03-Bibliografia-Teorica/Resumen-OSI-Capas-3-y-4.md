# 📡 Resumen: Capas de Red y Transporte (Modelo OSI)

**Fuentes:** Protocolos_del_modelo_OSI.pdf, Seguridad_por_niveles.pdf
**Fecha de Estudio:** 15 de Enero, 2026
**Tema:** Fundamentos de Comunicación

---

## 1. El Modelo OSI
Es una "pila teórica" que estandariza la comunicación. Permite que diferentes sistemas (Linux, Windows, Mac) hablen entre sí dividiendo el problema en capas.

## 2. El Proceso de Encapsulamiento
Para que los datos viajen, deben ser "empaquetados" capa por capa, similar a una carta dentro de un sobre (IP), dentro de una caja (Ethernet).
* **Capa 7 (Aplicación):** Datos puros (ej: HTTP).
* **Capa 4 (Transporte):** Se añade control de flujo y fiabilidad (ej: Cabecera **TCP**).
* **Capa 3 (Red):** Se añade direccionamiento lógico para enrutamiento (ej: Cabecera **IP**).
* **Capa 2 (Enlace):** Se añade direccionamiento físico local (ej: Trama **Ethernet**).

> **Nota del Analista:** Entender esto es vital porque las herramientas de seguridad operan en capas específicas. Un Firewall filtra IPs (Capa 3) y Puertos (Capa 4), mientras que un Switch gestiona MACs (Capa 2).

## 3. Protocolos Clave
* **TCP/IP:** La suite de protocolos que gobierna Internet.
* **RIP (Routing Information Protocol):** Protocolo utilizado por los routers para determinar el mejor camino para los datos.
* **ARP (Address Resolution Protocol):** Traduce una IP (Lógica) a una MAC (Física).
    * **Riesgo:** El *ARP Poisoning* engaña a los dispositivos para redirigir el tráfico hacia un atacante (Man-in-the-Middle).

---

## 🔍 Conclusión
La comunicación es un proceso ordenado de encapsulamiento. Un ataque puede dirigirse a diferentes niveles:
* **Capa 2:** ARP Spoofing.
* **Capa 3:** Ping Flood (DoS).
* **Capa 4:** Escaneo de Puertos (Port Scanning).
