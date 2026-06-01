# KuCode-portfolio
Scanner de vulnerabilidades web


Scanner de vulnerabilidades web que realicé durante mi práctica laboral en la Universidad de Chile, donde lo probé en sitios reales de la universidad con autorización del equipo de infraestructura.

No es un wrapper de una sola herramienta. Orquesta varias herramientas dentro de un contenedor Kali Linux. Le pasás una URL, detecta el CMS, elige las wordlists, corre las fases en orden y te genera un reporte en Word y HTML con los hallazgos clasificados por severidad.

¿Qué hace?

Detecta automáticamente el CMS (WordPress, Joomla, Laravel, etc.)
Corre hasta 10 fases de análisis en orden
Genera un score de riesgo global de 0 a 100
Produce un reporte Word y HTML con hallazgos clasificados por severidad
Mapea los resultados contra OWASP Top 10 y ASVS
Soporta múltiples URLs en paralelo
Envía notificaciones por Slack, Discord o email al terminar
Fases de análisis

Fase	Descripción
Reconocimiento	Fingerprinting, subdominios, tecnologías
Cabeceras HTTP	HSTS, CSP, cookies, headers de seguridad
Scanning	Nmap, WPScan, Nikto, Nuclei
Fuzzing	ffuf con wordlists adaptativas al CMS
Explotación	SQLMap, Commix, fuerza bruta con Hydra
Auditoría	TruffleHog, archivos expuestos, .git público
Inteligencia CVE	Consulta NVD API y ExploitDB por cada CVE encontrado
Reporte	Word + HTML interactivo con score y recomendaciones
Requisitos

Docker
curl
jq
Instalación

cd KuCode
chmod +x kucode.sh
./kucode.sh --build
Uso

# Escaneo básico
./kucode.sh https://ejemplo.com

# Escaneo completo
./kucode.sh https://ejemplo.com --full

# Varios sitios en paralelo
./kucode.sh site1.com site2.com site3.com --full -p 2

# Solo reconocimiento
./kucode.sh https://ejemplo.com --only-recon
Herramientas

Nmap · WPScan · ffuf · SQLMap · Commix · Nuclei · OWASP ZAP · Hydra · tshark · TruffleHog · Subfinder · Katana · Nikto · Wafw00f · SSLScan

## Aviso legal

Este proyecto fue desarrollado para uso profesional. Queda estrictamente prohibido utilizarlo en sistemas sin autorización explícita del propietario. Cualquier uso no autorizado es responsabilidad exclusiva de quien lo ejecute.
