
#  KuCode Scanner de Vulnerabilidades Web

Durante mi práctica profesional en la Universidad de Chile, desarrollé KuCode, un escáner de vulnerabilidades web automatizado. Para validar su funcionamiento y precisión, realicé auditorías controladas en plataformas reales de la institución, contando siempre con la autorización explícita del equipo de infraestructura.
A diferencia de las soluciones convencionales basadas en una única herramienta, este proyecto integra y orquesta múltiples utilidades de seguridad dentro de un entorno optimizado en Kali Linux. A partir de una sola URL, el escáner es capaz de identificar fallos críticos que podrían exponer el código fuente o comprometer la integridad del sitio web.

---

##  Características Principales

* Detección automática de CMS y tecnologías web (WordPress, Joomla, Laravel, entre otros).
* Ejecución automatizada de hasta 8 fases de análisis.
* Generación de un puntaje global de riesgo en una escala de 0 a 100.
* Creación de reportes en PDF y HTML con hallazgos clasificados por severidad.
* Correlación de vulnerabilidades con OWASP Top 10 y OWASP ASVS.
* Análisis simultáneo de múltiples URLs.
* Consulta automática de bases de datos de vulnerabilidades y exploits conocidos.

---

##  Fases de Análisis

| Fase             | Descripción                                                                                                              |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Reconocimiento   | Fingerprinting, identificación de tecnologías y descubrimiento de subdominios.                                           |
| Cabeceras HTTP   | Evaluación de políticas y cabeceras de seguridad, incluyendo HSTS, CSP y cookies.                                        |
| Scanning         | Ejecución de herramientas como Nmap, WPScan, Nikto y Nuclei.                                                             |
| Fuzzing          | Descubrimiento de recursos ocultos mediante ffuf y *wordlists* adaptativas según la tecnología detectada.                |
| Explotación      | Validación de vulnerabilidades mediante SQLMap, Commix y pruebas controladas de fuerza bruta con Hydra.                  |
| Auditoría        | Detección de secretos expuestos, repositorios públicos, archivos sensibles y configuraciones inseguras.                  |
| Inteligencia CVE | Consulta de NVD y ExploitDB para enriquecer los hallazgos con información sobre CVEs y exploits conocidos.               |
| Reporte          | Generación de reportes interactivos en PDF y HTML con puntaje de riesgo, clasificación y recomendaciones de mitigación. |



##  Salidas Generadas

* Reporte HTML interactivo.
* Documento PDF.
* Clasificación de hallazgos por severidad.
* Puntaje global de riesgo.
* Mapeo de vulnerabilidades a OWASP Top 10 y OWASP ASVS.
* Recomendaciones de mitigación.


##  Requisitos

* Kali Linux (contenedor Docker o instalación nativa)
* Docker y Docker Compose
* Python 3.11 o superior

## Importante
Aviso de Responsabilidad: Este proyecto fue desarrollado exclusivamente para realizar auditorías profesionales. Su uso está estrictamente limitado a sistemas sobre los cuales se posea una autorización previa y por escrito de los propietarios.
