# 🛡️ Defensa en Profundidad (Defense in Depth)

## 📖 Definición
La **Defensa en Profundidad** es una estrategia de seguridad que emplea múltiples capas de controles de seguridad en todo un sistema informático. Su objetivo es que, si un control falla, otros estén listos para detener el ataque.

---

## 🏗️ Las Capas de la Cebolla (Security Layers)

Para que el SOC detecte una intrusión, el atacante normalmente debe intentar vulnerar estas capas:

1. **Seguridad Física:** Controles de acceso a servidores, cámaras y guardias.
2. **Perímetro (Red Externa):** Firewalls y sistemas de protección contra DDoS.
3. **Red Interna:** Segmentación de red, IDS/IPS y seguridad en el Wi-Fi.
4. **Host (Dispositivo):** Antivirus, EDR y endurecimiento del Sistema Operativo (Patching).
5. **Aplicación:** Desarrollo seguro y firewalls de aplicaciones web (WAF).
6. **Datos:** Cifrado de archivos y bases de datos (el corazón de la cebolla).

---

## 🔗 Relación con el SOC
El SOC actúa como el **sistema nervioso** que conecta estas capas:
* **Visibilidad:** El SIEM recolecta logs de cada capa para detectar anomalías.
* **Respuesta:** Si el Firewall (Capa de Red) es superado, el SOC utiliza el EDR (Capa de Host) para detener la amenaza.

> **Concepto Clave:** "La seguridad es tan fuerte como su eslabón más débil".
