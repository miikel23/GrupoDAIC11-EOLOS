# EOLOS - Grupo 11

## Descripción
El proyecto EOLOS permite monitorizar la calidad y, por consecuencia, la ventilación de espacios cerrados, registrando, a su vez, diferentes características (estáticas y dinámicas) del entorno, de manera que pueda ofrecer datos que permitan realizar un análisis exhaustivo que pueda llevar a conclusiones clave en la lucha contra la covid-19. 

En el prototipo se plantea lo siguiente:
- La medición de niveles de gas y compuestos orgánicos volátiles (COV)
- La detección de apertura o cierre de vías de ventilación (ventanas y puertas, principalmente)

Además, ofrecerá una interfaz web sencilla que permitirá a los usuarios consultar los datos recogidos por sus dispotivos de medición asi como la parametrización de los mismos (para ajustar valores como la frecuencia de medición, o los niveles de alerta), de manera que el proceso de obtención de conocimiento a partir de los mismos se agilice en la medida de lo posible. Por último, en caso de que las mediciones superen los máximos establecidos (ya sean los predeterminados o los indicados por el usuario*), se emitirá una alerta visual (led rojo) que permita avisar del peligro a los usuarios del espacio en cuestión.

## Detalles de la implementación
Se plantea hacer uso de Raspberry Pi como dispositivo de recolección de muestras (medidas), que se sincronizará periódicamente con un servidor en la nube, de forma que los datos recogidos por la Raspberry Pi puedan consultarse desde cualquier lugar y dispositivo gracias a una interfaz web. 

Para el servidor, se propone utilizar una arquitectura basada en contendores que permita alojar tres servicios distintos:
- Una base de datos InfluxDB para el almacenamiento de las muestras
- Un servidor Grafana para gestionar todo lo relacionado con las visualizaciones de datos
- Un servidor web para ofrecer a los usuarios una forma amigable de consultar sus mediciones y realizar ajustes

Para alojar dichos servicios, se hará uso de servicios en la nube a fin de mantener el proyecto lo más sencillo posible.

## Instalación para desarrolladores
En caso de querer colaborar en este proyecto, los pasos para crear un entorno de desarrollo son los siguientes:
1. Clonar el repositorio `$ git clone https://github.com/miikel23/GrupoDAIC11-EOLOS.git eolos`
2. Instalar dependencias `$ npm install`
3. Para ejecutar el proyecto `npm run start`

## Uso 
Para hacer uso del proyecto es necesario:
1. Acceder desde el navegador a la direccion ip `http://93.189.90.190` e introducir los datos de usuario.
2. Una vez dentro del sistema se puede elegir que dispositivo se desea seleccionar y acceder a los datos en tiempo real.
3. Para cerrar sesion hacer click sobre el boton `logout`

## Integrantes del grupo
- Mikel Moreno Moreno
- Pablo Villacorta Benito
