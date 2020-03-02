### ¿Qué es Redis?

Es una base de datos en memoria que ofrece replicación, persistencia, alto rendimiendo y un modelo de datos sencillo y flexible.

Aunque Redis dispone sólo de 5 estructuras de datos, su rapidez y flexibilidad lo hacen el candidato ideal para 
resolver múltiples problemas.

notes:

Las 5 estructuras de datos que Redis pone a nuestra disposición son:

* Cadenas (`Strings`)
* Listas (`Lists`)
* Conjuntos (`Sets`)
* Diccionarios (`Hashes`)
* Conjuntos ordenados (`Sorted Sets`)

^^^^^^

#### ¿Qué es Redis?

Vamos a ver un ejemplo de uso para entender cómo funciona.

Vamos a implementar un sencillo sistema para contar cuantas veces se visita el perfil de un usuario.

 
^^^^^^

#### ¿Qué es Redis?

Para implementarlo utilizaremos un conjunto ordenado (__Sorted Set__).

```redis-cli
redis-cli > ZINCRBY visitas 1 user:1
"1"
redis-cli > ZINCRBY visitas 1 user:3
"1"
redis-cli > ZINCRBY visitas 1 user:1
"2"
```

^^^^^^

#### ¿Qué es Redis?

Ya está, no necesitamos más. No necesitamos crear tablas, ni verificar si el registro ya existe, ni nada...

...sólo conectarnos con el cliente y ejecutar el comando `ZINCRBY`.


^^^^^^

#### ¿Qué es Redis?

Sólo hemos tenido que tomar una decisión acerca del nombre que van a tener los elementos de conjunto
ordenado `visitas`, que en este caso es `user:[ID_DEL_USUARIO]`.

^^^^^^

#### ¿Qué es Redis?

¿qué otras cosas podemos hacer?

* Ver todos los usuarios que tienen visitas

```redis-cli
redis-cli > ZRANGE visitas 0 -1
1) "user:3"
2) "user:1" 
```

* Ver los usuarios con más visitas

```redis-cli
redis-cli > zrevrange visitas 0 -1 WITHSCORES
 1) "user:10"
 2) "34"
 3) "user:6"
 4) "12"
 5) "user:9"
 6) "10"
 7) "user:3"
 8) "2"
 9) "user:1"
10) "2" 
```
