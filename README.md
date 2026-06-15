# FECYT-I+P: 
## "Efectividad de la asistencia prestada a los pacientes con cáncer de mama y cáncer colorrectal en el SNS: utilización de técnicas de minería de procesos para informar políticas para su mejora"

Referencia del proyecto: **FCT-25-22533**

Entidad coordinadora: **[Instituto Aragonés de Ciencias de la Salud (IACS)](https://www.iacs.es/)**

IP: **Enrique Bernal-Delgado** ORCID:[0000-0002-0961-3298](https://orcid.org/0000-0002-0961-3298)

## Descripción del Proyecto
Este proyecto de investigación tiene como objetivo principal evaluar el acceso efectivo a la atención sanitaria de los pacientes con cáncer de mama y cáncer colorrectal en el Sistema Nacional de Salud (SNS). Ante la preocupación por los tiempos de espera y su posible impacto negativo en los resultados de salud, esta iniciativa propone analizar el proceso asistencial completo, desde el diagnóstico hasta el alta.
El proyecto es impulsado por el Grupo de Ciencia de Datos para la Investigación en Servicios y Políticas Sanitarias del IACS, en colaboración con el Ministerio de Sanidad y diversas Comunidades Autónomas (como Aragón, Navarra e Islas Baleares).

### Objetivos:
1. Descubrir empíricamente la variedad de trayectorias asistenciales seguidas por pacientes con sospecha de cáncer de mama y colon.
2. Estimar las diferencias entre el proceso asistencial teórico (basado en guías y manuales) y el proceso asistencial real.
3. Predecir el impacto de estas diferencias en los resultados sanitarios en los pacientes (e.g., supervivencia o estadio en el momento del tratamiento).
4. Identificar proveedores asistenciales con mejor desempeño en términos de tiempos de espera y resultados.
5. Transferir el conocimiento adquirido a las autoridades sanitarias para la mejora de las políticas mediante diálogos informados y cuadros de mando.

## Metodología 
El análisis se basa en técnicas de Minería de Procesos (Process Mining) para derivar modelos de procesos directamente a partir de marcas de tiempo en los sistemas de información.

## Enfoque Federado y Privacidad
Al basarse en datos sanitarios -de vida real- mantenidos en múltiples jurisdicciones, el estudio adopta una naturaleza observacional y federada.
Para garantizar la privacidad y cumplir con consideraciones éticas estrictas, los datos sensibles y seudonimizados nunca abandonan su lugar de origen. Se utiliza una topología master-to-worker (M2W):
- Nodo Coordinador (IACS): Diseña el Modelo Común de Datos (CDM), desarrolla el código de análisis y empaqueta la infraestructura en contenedores seguros (Docker).
- Nodos Participantes (CCAA): Realizan la extracción y transformación de sus datos locales, despliegan los contenedores on-premise para ejecutar el análisis, y devuelven únicamente resultados agregados al nodo coordinador.
Utilizando como soporte las herramientas desarrolladas por el Grupo de Investigación: [Common Data Model Builder (cdmb)](https://github.com/cienciadedatosysalud/cdmb-web) y [ASPIRE](https://github.com/cienciadedatosysalud/aspire).

Puede consultarse más información sobre su funcionamiento y sobre el proceso de desarrollo de un estudio federado consultando el [manual de ASPIRE](https://github.com/cienciadedatosysalud/manual_aspire)

