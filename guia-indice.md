# Explicación detallada del índice del TFM

# Capítulo 1. Introducción

## 1.1 Contexto y motivación

En este apartado se presenta el problema que da origen al TFM y la importancia del ámbito tratado. Debe justificarse por qué resulta relevante desarrollar un laboratorio Red Team orientado a la simulación de ataques en entornos empresariales. También se contextualiza el uso de vulnerabilidades OWASP, Active Directory y técnicas de pivoting dentro del panorama actual de la ciberseguridad.

## 1.2 Objetivos del trabajo

### 1.2.1 Objetivo general

Define la finalidad principal del proyecto. En este caso, el objetivo general consiste en diseñar e implementar un laboratorio de ciberseguridad reproducible que permita simular ataques reales en una infraestructura corporativa segmentada.

### 1.2.2 Objetivos específicos

Describe las metas concretas necesarias para alcanzar el objetivo principal. Por ejemplo:

* Implementar un servidor web vulnerable.
* Desplegar un entorno Active Directory.
* Configurar segmentación de red.
* Simular técnicas de movimiento lateral.
* Automatizar el despliegue del laboratorio.
* Documentar escenarios de explotación.

## 1.3 Alcance y limitaciones

Explica qué cubre el proyecto y qué queda fuera de su alcance. Aquí se indica que el laboratorio tiene un propósito académico y formativo, que las vulnerabilidades son intencionadas y que el entorno está diseñado para funcionar de forma aislada y controlada.

## 1.4 Organización de la memoria

Resume brevemente la estructura del documento y explica el contenido de cada capítulo para facilitar la navegación y comprensión de la memoria.

---

# Capítulo 2. Gestión y metodología del proyecto

## 2.1 Metodología de desarrollo

Describe el enfoque utilizado durante el desarrollo del proyecto. En este caso puede justificarse una metodología incremental o iterativa, donde el laboratorio se construye progresivamente añadiendo nuevos componentes, vulnerabilidades y escenarios ofensivos.

## 2.2 Planificación del proyecto

Incluye la planificación temporal del TFM:

* Fases de desarrollo.
* Cronograma.
* Hitos importantes.
* Organización de tareas.

Puede complementarse con diagramas de Gantt.

## 2.3 Recursos utilizados

### 2.3.1 Hardware

Describe el equipamiento utilizado:

* Equipo anfitrión.
* Recursos asignados a las máquinas virtuales.
* Memoria RAM.
* CPU.
* Almacenamiento.

### 2.3.2 Software

Incluye todas las herramientas y tecnologías empleadas:

* VMware Workstation.
* Kali Linux.
* Ubuntu Server.
* Windows Server 2012.
* Windows 7.
* Docker.
* Apache.
* MySQL.
* Metasploit.
* Burp Suite.
* Ligolo-ng, etc.

## 2.4 Coste del proyecto (opcional)

Permite estimar el coste económico del proyecto:

* Hardware utilizado.
* Licencias.
* Tiempo de desarrollo.
* Recursos empleados.

---

# Capítulo 3. Análisis del entorno y requisitos

## 3.1 Requisitos funcionales

Define las funcionalidades que debe cumplir el laboratorio:

* Despliegue reproducible.
* Acceso a servicios vulnerables.
* Simulación de ataques.
* Segmentación de red.
* Entorno Active Directory operativo.

## 3.2 Requisitos no funcionales

Describe características de calidad del sistema:

* Estabilidad.
* Modularidad.
* Reproducibilidad.
* Facilidad de despliegue.
* Aislamiento del entorno.

## 3.3 Análisis de amenazas y superficie de ataque

Analiza las posibles vías de ataque presentes en el laboratorio:

* Servicios expuestos.
* Vulnerabilidades web.
* Credenciales débiles.
* Servicios internos.
* Movimiento lateral.
* Enumeración de red.

Aquí se justifica el diseño ofensivo del escenario.

## 3.4 Justificación del uso de OWASP y MITRE ATT&CK

Explica por qué se utilizan estos marcos de referencia:

* OWASP Top 10 para vulnerabilidades web.
* MITRE ATT&CK para modelar tácticas y técnicas ofensivas.

Esto aporta base metodológica y académica al TFM.

---

# Capítulo 4. Diseño del laboratorio

## 4.1 Arquitectura general

Presenta la visión global del laboratorio y cómo se relacionan sus componentes.

### 4.1.1 Arquitectura física

Describe la infraestructura virtual:

* Máquinas virtuales.
* Recursos hardware.
* Redes VMware.
* Adaptadores NAT e internos.

### 4.1.2 Arquitectura lógica

Explica la organización funcional del laboratorio:

* DMZ.
* Red interna.
* Active Directory.
* Segmentación de servicios.

### 4.1.3 Segmentación de red

Describe la separación entre redes:

* NAT.
* VMnet10.
* Subredes internas.
* Acceso restringido.
* Pivoting entre segmentos.

### 4.1.4 Diagrama completo de infraestructura

Incluye el diagrama completo del laboratorio mostrando:

* Kali Linux.
* Ubuntu vulnerable.
* DC01.
* DEV01.
* Conexiones y flujo de ataque.

---

## 4.2 Diseño del servidor vulnerable

### 4.2.1 Stack tecnológico

Describe las tecnologías utilizadas en el servidor:

* Apache.
* PHP.
* MySQL.
* Docker.
* Docker Compose.

### 4.2.2 Portal PYME vulnerable

Explica el desarrollo y funcionamiento de la aplicación vulnerable:

* Usuarios.
* Roles.
* Paneles.
* Gestión de tickets.
* Funcionalidades implementadas.

### 4.2.3 Vulnerabilidades implementadas

Documenta las vulnerabilidades introducidas:

* SQL Injection.
* XSS.
* Command Injection.
* Broken Access Control.
* Weak Authentication.
* File Inclusion, etc.

---

## 4.3 Diseño de la infraestructura Active Directory

### 4.3.1 DC01

Describe el controlador de dominio:

* Windows Server 2012.
* Active Directory.
* DNS.
* WinRM.
* SMB.

### 4.3.2 DEV01

Describe la estación de trabajo corporativa:

* Windows 7.
* Unión al dominio.
* Servicios activos.
* Uso como punto de pivoting.

### 4.3.3 Usuarios y políticas

Explica la configuración del dominio:

* Usuarios.
* Grupos.
* Contraseñas.
* Políticas básicas.
* Permisos.

### 4.3.4 Servicios internos

Documenta los servicios disponibles:

* SMB.
* RDP.
* WinRM.
* DNS.
* Comparticiones internas.

---

## 4.4 Diseño del escenario ofensivo

Explica la cadena de ataque diseñada:

* Reconocimiento.
* Explotación web.
* Reverse shell.
* Escalada Linux.
* Pivoting.
* Enumeración AD.
* Movimiento lateral.
* Compromiso del dominio.

---

## 4.5 Automatización y despliegue

### 4.5.1 Docker

Describe el uso de contenedores para desplegar servicios vulnerables.

### 4.5.2 Script setup_tfm_lab.sh

Explica el funcionamiento del script automatizado de instalación y configuración del laboratorio.

### 4.5.3 Reproducibilidad del laboratorio

Describe cómo se garantiza que el entorno pueda desplegarse nuevamente de forma consistente.

---

## 4.6 Repositorio y estructura del proyecto

Presenta la organización del repositorio:

* Carpetas.
* Scripts.
* Docker Compose.
* Configuraciones.
* Documentación.

---

# Capítulo 5. Validación y explotación del laboratorio

## 5.1 Metodología de pruebas

Describe cómo se realizarán las pruebas ofensivas:

* Reconocimiento.
* Enumeración.
* Explotación.
* Post-explotación.
* Validación de resultados.

---

## 5.2 Escenarios de ataque realizados

### 5.2.1 Reconocimiento inicial

Uso de herramientas de escaneo y enumeración para identificar servicios y superficie de ataque.

### 5.2.2 Explotación web

Explotación de vulnerabilidades OWASP presentes en la aplicación.

### 5.2.3 Obtención de reverse shell

Acceso remoto al servidor comprometido mediante shells reversas.

### 5.2.4 Escalada de privilegios Linux

Técnicas utilizadas para obtener privilegios elevados en Ubuntu.

### 5.2.5 Pivoting

Uso del servidor comprometido para acceder a la red interna.

### 5.2.6 Enumeración Active Directory

Obtención de información del dominio:

* Usuarios.
* Equipos.
* Servicios.
* Relaciones de confianza.

### 5.2.7 Movimiento lateral

Acceso a otros sistemas internos utilizando credenciales o servicios comprometidos.

### 5.2.8 Compromiso del dominio

Escenario final donde se demuestra el impacto de la cadena de ataque.

---

## 5.3 Validación de reproducibilidad

Comprueba que el laboratorio puede desplegarse y utilizarse de forma repetible y estable.

---

# Capítulo 6. Conclusiones y trabajo futuro

## 6.1 Conclusiones

Resume los resultados obtenidos:

* Objetivos alcanzados.
* Valor técnico del laboratorio.
* Aplicación académica y formativa.

## 6.2 Líneas futuras

Propone posibles mejoras:

* SIEM.
* EDR.
* Azure AD.
* Kubernetes.
* Blue Team.
* Nuevos escenarios ofensivos.

---

# Anexos

## Anexo I. Manual de despliegue

Guía detallada para desplegar el laboratorio desde cero.

## Anexo II. Manual de explotación

Documentación paso a paso de los escenarios ofensivos implementados.

## Anexo III. Configuración de red

Configuración técnica de redes, IPs y segmentación.

## Anexo IV. Scripts y automatizaciones

Incluye scripts desarrollados para automatizar despliegues y configuraciones.

## Anexo V. Evidencias adicionales

Capturas, logs, pruebas y material complementario utilizado durante el proyecto.
