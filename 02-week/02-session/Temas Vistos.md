## Software MONOLÍTICA (Arquitectura)
--------
 Un software monolítico es un tipo de arquitectura en la que todas las funciones y componentes de una aplicación están integrados en un solo bloque de código que se ejecuta como una única unidad.
----
#### Para entenderlo un poco mejor podemos explicarlo con un ejemplo común
 Imaginemos un pastel entero. Para comerlo, tenemos que cortarlo, pero todo está hecho en la misma bandeja y mezclado: bizcocho, relleno, crema.

 En un software monolítico, la lógica de negocio, la interfaz de usuario, el acceso a datos y otros módulos están juntos en un único proyecto y se despliegan (instalan) todos al mismo tiempo.

----------
### Características
**Un solo ejecutable o paquete:** todo el código está unido.

**Despliegue conjunto:** si cambias una parte, debes volver a desplegar todo.

**Acoplamiento alto:** los módulos dependen mucho entre sí.

**Escalabilidad vertical:** si necesita más rendimiento, debes aumentar la capacidad del mismo servidor (más RAM, CPU).

### Ventajas
**Simplicidad inicial:** fácil de desarrollar y poner en marcha al inicio.

**Menos configuración:** un solo entorno y despliegue.

**Buen rendimiento:** no requiere comunicación entre servicios vía red.

### Desventajas
**Difícil de escalar horizontalmente** (varias máquinas trabajando en paralelo).

**Poca flexibilidad para cambios:** modificar un módulo puede afectar todo el sistema.

Despliegue lento cuando crece.

**Riesgo alto:** si una parte falla, puede caer todo.

-----------------
## Actividad En Clase 
### (Apuntes del profesor)
-> package => (más común [frontend, backend], doc{architecture, backlog, manual, other}, data-base{script, backup, MR, other}, other)
        -> capas {se puede?}
        -> mvc {se puede?}
        -> hexaganonal {se puede?}
        -> cliente/servidor
### Actividad
- ahí se pueden aplicar capas, MVC, hexagonal y cliente/servidor para un software monolítico? o qué arquitecturas sí sirven?.
