# 🛡️ Implementación de Laboratorio XDR/SIEM con Wazuh

## 📝 Descripción del Proyecto
Este proyecto documenta el despliegue de un entorno de monitorización de seguridad y detección de amenazas (XDR/SIEM) utilizando Wazuh. El objetivo es centralizar la recolección de eventos, auditar la seguridad y monitorizar la integridad de diferentes endpoints (físicos y virtuales) en una red local.

## 🏗️ Topología y Arquitectura
El entorno de laboratorio está compuesto por un nodo central (Servidor) y múltiples agentes distribuidos:

* **Wazuh Server (XDR/SIEM):** Desplegado como Máquina Virtual (VirtualBox/VMware) sobre el host principal.
* **Agente 1 (Entorno Virtual):** Máquina virtual de prueba para simulación de ataques y evaluación de vulnerabilidades.
* **Agente 2 (Entorno Físico):** Laptop física conectada a la red local, utilizada para monitorizar métricas de salud del sistema, inestabilidad de hardware y eventos de seguridad en un escenario de uso real.

## 🛠️ Tecnologías y Herramientas
* **SIEM/XDR:** Wazuh (Open Source)
* **Virtualización:** VirtualBox
* **Sistemas Operativos (Agentes):** Windows 11, Ubuntu Server, CentOS

## 🚀 Proceso de Despliegue

### 1. Preparación del Servidor
* Configuración de la red virtual (Adaptador Puente / NAT).
* Importación del instalador del sistema operativo Ubuntu Server.
* Asignación de recursos (vCPU y RAM).

### 2. Despliegue de Agentes
* Instalación del agente de Wazuh en el entorno virtual (Agente 1).
* Instalación y vinculación del agente en el equipo físico (Agente 2).
* Verificación de conectividad en el Dashboard.

## 🔍 Pruebas de Concepto (Casos de Uso)
*(En esta sección se documentarán con capturas de pantalla los eventos detectados).*

1. **Monitorización de Integridad:** Detección de cambios no autorizados en archivos del sistema.
2. **Alertas de Autenticación:** Registro de múltiples intentos fallidos de inicio de sesión.
3. **Auditoría de Hardware/Sistema:** Captura de eventos críticos del sistema operativo en el Agente 2 (ej. reinicios inesperados, errores de almacenamiento).

## 💡 Lecciones Aprendidas y Conclusión
*(Espacio para redactar los retos técnicos enfrentados durante la configuración, como la gestión de reglas de firewall locales o la interpretación de los logs recolectados, y cómo se resolvieron).*
