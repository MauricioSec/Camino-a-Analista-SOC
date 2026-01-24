# 🤖 Desarrollo de Herramientas de Seguridad (Bash Scripting)

**Estado:** Completado ✅
**Lenguaje:** Bash (Shell Scripting)
**Entorno:** Termux (Android Linux)

## 🎯 Objetivo
Automatizar tareas repetitivas de reconocimiento de red (Network Discovery) y análisis de logs mediante la creación de scripts personalizados. El objetivo es reducir el tiempo de detección de amenazas y la identificación de activos en la red.

## 🛠️ Herramienta Desarrollada: `Scanner Pro` (Network Sweeper)

Se desarrolló un script modular capaz de realizar barridos de ping (Ping Sweeps) dinámicos. A diferencia de un comando estático, esta herramienta acepta argumentos del usuario para definir el segmento de red y el rango de búsqueda en tiempo de ejecución.

### 💻 Código Fuente (Logic Flow)

El script implementa estructuras de control fundamentales:
* **Validación de Argumentos (`if -z`):** Programación defensiva para asegurar que el usuario ingrese los datos necesarios.
* **Bucles (`for`):** Iteración automatizada sobre rangos de direcciones IP generados con `seq`.
* **Redirección de I/O:** Manejo de salidas estándar (`stdout`) y errores (`/dev/null`) para limpiar la interfaz visual.

```bash
#!/bin/bash
# Fragmento de la lógica principal
for i in $(seq $INICIO $FIN); do
    IP="$RED.$i"
    if ping -c 1 -W 1 $IP > /dev/null; then
        echo "[+] 📡 VIVO: $IP"
    fi
done
