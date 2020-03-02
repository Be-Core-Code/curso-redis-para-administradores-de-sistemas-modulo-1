### Instalación

La manera recomendada de desplegar Redis en producción es en Linux.

#### Instalación

En este curso nos centraremos en Linux por lo que sólo hablaremos de la instalación en otros sistemas operativos
a título informativo.

^^^^^^

### Instalación: Linux

Dos métodos:

* Usando los paquetes creados para cada distributión
* A partir del código fuente 

notes:

Todas las distribuciones de Linux mayoritarias disponen de paquetes para Redis
con actualizaciones bastante frecuentes y en sincronía con el código fuente.


^^^^^^

#### Instalación: Linux

* Utilizaremos los paquetes distribuidos por Alpine Linux. El uso de paquetes tiene las siguientes ventajas:
  * Cofiguración de usuarios y permisos adecuados tras la instalación
  * Integración con el sistema de arranque
  * Integración con sistemas de logs, rotación de logs, etc

^^^^^^

#### Instalación: Linux

* En el [siguiente enlace](https://redis.io/topics/quickstart) disponéis de indicaciones
  completas para hacer la instalación a partir del código fuente

^^^^^^

#### Instalación: Linux

En Alpine Linux instalamos redis a través del gestor de paquetes `apk`:

```bash
> apk add redis
```

^^^^^^

### Instalación: Windows

Si necesitamos desplegar Redis en windows, tenemos que ser conscientes de las 
[limitaciones que Redis tiene en este Sistema Operativo:](https://redislabs.com/ebook/appendix-a/a-3-installing-on-windows/a-3-1-drawbacks-of-redis-on-windows/)

Windows no implementa `fork` y redis depende de esta llamada para persistir los datos de manera asíncrona son bloquear
el hilo principal de ejecución. 

^^^^^^

#### Instalación: Memurai

Port de Redis con soporte nativo para Windows.

[https://www.memurai.com/](https://www.memurai.com/)

**Esta es la opción recomendada para desplegar en producción.** 


^^^^^^

#### Instalación: Windows 10 con WSL

* Levantas redis dentro de la distribución de Linux que hayas instalado dentro de 
  Windows ([Más información](https://redislabs.com/blog/redis-on-windows-10/))


^^^^^^

#### Instalación: Binarios para Windows

En [este enlace](https://github.com/dmajkic/redis/downloads) disponéis de binarios compilados para Windows hasta la 
versión 2.4.5. **Si necesitáis versiones más modernas tendréis que [compilarla vosotros](https://github.com/microsoftarchive/redis)**

^^^^^^

#### Instalación: Docker

Otra opción es desplegar Redis como un contenedor docker en windows.

^^^^^^

### Instalación: OS-X

* Lo más cómodo es a través de `brew`

```bash 
> brew install redis
```

* La otra opción es [compilando el código fuente](https://redislabs.com/ebook/appendix-a/a-2-installing-on-os-x/).

^^^^^^

### 💻️ Ejercicion: Instalación

Instala Redis en tu máquina con Alpine Linux.
