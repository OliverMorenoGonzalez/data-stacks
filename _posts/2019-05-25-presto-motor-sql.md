# Un único SQL para gobernarlos a todos

Aqui hablaremos sobre PrestoSQL.
Este tutorial de introducción será bastante amigable, describiendo sin entrar en demasiados tecnicismos, luego habrá una versión extendida.

Presto es un Motor de SQL de código abierto, se usa para ejecutar consultas de análisis sobre distintas fuentes de datos cubriendo un amplio rango de volumen desde gigabytes hasta petabytes.

Presto fue diseñado para manejar "data warehousing" y analítica: análisis de datos agregando grandes cantidades de datos y produciendo reportes. Estas tipos de flujos de trabajo son a menudo clasificados como "Online Analitycal Processing" (OLAP).
Presto no fue diseñado para manejar Online Transaction Processing (OLTP).

(Algunos términos no los traduciré debido a su ambigüedad y a que os resultara mas facil buscarlos luego para entenderlos mejor)

Personalmente me centrare en la imagen de docker oficial de PrestoSQL.

## Ventajas principales:

1) SQL sobre cualquier fuente de datos mediante el uso de conectores disponibles y/o la creación de ellos. No hay más necesidad de usar implementaciones de SQL específicas para cada tecnología. "Un único SQL para gobernarlos a todos".

2) Separación del almacenamiento y el cálculo. Esto permite Escalar segun las necesidades analíticas, ahorrando costes.

3) Despliegues donde quieras: en la nube, en local, y en entornos virtualizados.

4) SQL extendido, con más tipos de operaciones y creado con el rendimiento en mente, (tratamiento de petabytes con baja latencia).

5) Fácil de instalar y depurar.

6) Alta seguridad y posibilidad de configurarla.

# Arquitectura PrestoSQL.

En Presto Motor SQL tienes un coordinador (el cerebro) y múltiples trabajadores/actuadores para procesar consultas.

El coordinador acepta sentencias de SQL provenientes del cliente y parsea, planea y agenda como las sentencias de SQL serán procesadas cuando ese proceso termina los trabajadores/actuadores entran en acción.

Los trabajadores/actuadores leen los datos de fuentes de datos y las combinan en un único proceso que es devuelto al cliente.

Apache Presto tiene una api de metadatos (es uno de los componentes del coordinador) cuya función es entender las relaciones de tus fuentes de datos (como están los datos almacenados) y los traduce para usar los datos, tras esto el resto de la ejecución es agnóstica a tu fuente de datos.

## Más ventajas de PrestoSQL.

1) Dirigido por la comunidad, es de código abierto.

2) Gran comunidad, es usado por muchas y grandes compañías, por tanto hay expertos y usuarios a los que puedes contactar, en varios casos las compañías han aportado al proyecto nuevas funcionalidades mejorándolo.

3) Sin ataduras a un proveedor especifico.

4) Alto rendimiento ANSI SQL Motor.

Proximo tutorial: Puesta en marcha y practica.
