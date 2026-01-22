# 📱 Laboratorio de Operaciones de Campo: Auditoría de Red con Termux

**Fecha:** 22 de Enero, 2026
**Estado:** Completado ✅
**Entorno:** Android (Honor Magic 7) / Emulador de Terminal Linux (Termux)
**Herramientas:** Nmap, Netcat, SSH, cURL, Bash scripting, DNSutils.

---

## 🎯 Objetivo del Laboratorio
Demostrar la capacidad de desplegar un entorno de análisis de seguridad portátil (SOC móvil) para realizar reconocimiento de red, gestión de procesos y auditoría de servicios en una infraestructura real (Router Starlink), utilizando exclusivamente una terminal móvil basada en Linux (Termux).

---

## 🛠️ 1. Configuración del Entorno y Hardening
Se transformó un dispositivo móvil estándar en una estación de trabajo Linux operativa.

* **Gestión de Paquetes:** Configuración de repositorios (`pkg update`) y cambio de mirrors a `grimler.se` para asegurar la disponibilidad de herramientas.
* **Gestión de Permisos (Linux Filesystem):**
    * Creación de estructura de directorios segura.
    * Implementación de **Notación Octal** (`chmod 640`) para asegurar la confidencialidad de la información crítica (Dueño: Lectura/Escritura, Grupo: Lectura, Otros: Sin acceso).
* **Gestión de Almacenamiento:** Enlace simbólico entre el entorno aislado (Sandbox) de Termux y el almacenamiento interno de Android (`termux-setup-storage`).

---

## 📡 2. Análisis de Procesos y Servicios (Host Discovery)
Monitorización activa del sistema para identificar anomalías y consumo de recursos en tiempo real.

* **Identificación de Procesos:** Uso del comando `ps` y `top` para listar tareas activas.
* **Kill Chain de Procesos:** Simulación de procesos "zombies" en segundo plano (`sleep 1000 &`) y terminación manual mediante `kill -9 [PID]` para restaurar el rendimiento del sistema.

---

## 🔍 3. Reconocimiento de Red (Network Mapping)
Auditoría de caja negra contra el router perimetral de la red (Infraestructura Starlink).

### Identificación de Activos
Se identificó la topología de red local y la puerta de enlace predeterminada.
* **Comando:** `ifconfig` (adaptado por restricciones de Android 12+).
* **Validación de Conectividad:** Análisis de latencia y pérdida de paquetes mediante `ping` hacia el Gateway y DNS externos.

### Escaneo de Puertos y Servicios (Nmap)
Se ejecutó un escaneo de puertos y detección de versiones contra el Gateway (`192.168.1.1`).

**Comando ejecutado:**
```bash
nmap -sV -p- 192.168.1.1

PORT     STATE  SERVICE    VERSION
22/tcp   open   ssh        OpenSSH 7.4 (protocol 2.0)
53/tcp   closed domain
80/tcp   open   http       Golang net/http server
443/tcp  closed https
9000/tcp open   grpc       (Servicios de Telemetría Starlink)

