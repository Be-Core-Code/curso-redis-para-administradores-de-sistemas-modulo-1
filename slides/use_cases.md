### Casos de uso

Redis empezó siendo una base de datos en memoria... pero ahora se está convirtiendo en algo bastante más potente.

^^^^^^

#### Casos de uso

* [RedisTimeSeries](https://oss.redislabs.com/redistimeseries/): estructura de datos para almacenar series temporales
* [RedisGears](https://oss.redislabs.com/redisgears/overview.html): permite construir un `operations pipe (OPP)`. 
  Básicamente se define una operación que se ejecuta para cada clave en la que el resultado de la clave anterior se pasa
  como argumento a la operación con la clave siguiente
* [RedisStreams](https://redis.io/topics/streams-intro) estructura de datos a la que sólo se le pueden añadir 
  datos (_append only_)

^^^^^^
  
#### Casos de uso

Todos estos módulos y mejoras de Redis se han combinado en una plataforma orientada a IoT 
([RedisEdge](https://redislabs.com/redis-enterprise/redis-edge/)) que podéis ver en acción en [este
enlace](https://redislabs.com/blog/my-other-stack-is-redisedge/).

^^^^^^

#### Casos de uso

Estos ejemplos y casos de uso nos dan una idea de hasta dónde podemos llegar con Redis y hacia dónde está evolucionando.

^^^^^^

#### Casos de uso

Aparte de estos casos (un poco "extremos") podemos destacar los siguientes usos más habituales de Redis:

* [Cache](https://redislabs.com/redis-enterprise/use-cases/caching/)
* [Gestión de sesiones](https://redislabs.com/redis-enterprise/use-cases/session-management/)
* [Creación de paneles de control](https://redislabs.com/redis-enterprise/use-cases/leaderboards/)
* [Message Broker](https://redislabs.com/redis-enterprise/use-cases/messaging/)
* [Fast Data Ingest](https://redislabs.com/redis-enterprise/use-cases/fast-data-ingest/)



