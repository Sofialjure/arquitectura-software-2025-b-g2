## Parte 4 del Foro **"DIAGRAMA DE DESPLIEGUE Y DE ESTADOS"**
----------

## DIAGRAMA DE DESPLIEGUE

## ¿Qué es?

El diagrama de despliegue es un diagrama estructural de UML que muestra la arquitectura física de un sistema, es decir, cómo el software se ejecuta sobre la infraestructura de hardware.  
Representa los nodos de hardware (servidores, dispositivos, computadoras, móviles, etc.) y cómo se conectan entre sí, además de indicar qué artefactos de software se despliegan en esos nodos.

Se usa mucho en sistemas distribuidos, aplicaciones cliente-servidor y arquitecturas en red.

---

## Estructura

Un diagrama de despliegue está compuesto por:

- **Nodos (Nodes)** → Elementos físicos (servidores, PCs, móviles, routers). Se dibujan como cubos tridimensionales.
- **Artefactos (Artifacts)** → Archivos o componentes de software que se ejecutan en un nodo (se dibujan como rectángulos con la palabra clave *artifact*).
- **Asociaciones de comunicación** → Líneas que unen nodos para representar la red o los canales de comunicación.
- **Componentes / aplicaciones** → El software desplegado dentro de un artefacto.
- **Estereotipos** → Se usan para identificar tipos de nodos o artefactos, como `<<device>>`, `<<database>>`, `<<server>>`, `<<executable>>`.

# **ACTIVIDAD**
**Contexto**. Se requiere modelar el núcleo de un sistema para un aeropuerto que gestione vuelos, pasajeros, control de check-in, seguridad, asignación de puertas, embarque y seguimiento en tiempo real (estado del vuelo, ubicación del pasajero en proceso, alertas). El sistema se integra con servicios de aerolíneas (emisión/validación de boarding pass), autoridad migratoria, control de seguridad y pantallas de información en sala. Debe soportar picos de demanda, trazabilidad y auditoría, y manejar excepciones (overbooking, cambio de puerta, retrasos, no show).

**Alcance mínimo**
- **Gestión de vuelos:** programación, estado (programado, abordando, cerrado, despegado, cancelado), asignación de puerta.
- **Gestión de pasajeros:** check-in, control de documentación, validación de boarding pass, embarque.
- **Flujo operativo:** colas por prioridad (PMR, familias, business), excepciones y reubicaciones.
- **Integraciones:** aerolínea (DCS/PSS), autoridad migratoria, seguridad aeroportuaria, pantallas (FIDS).
- **Observabilidad:** registro de eventos, tiempos de proceso y alertas operativas.
-------
# SOLUCIÓN DIAGRAMA DE DESPLIEGUE
---
---












## Parte 4 del Foro **"DIAGRAMA DE DESPLIEGUE Y DE ESTADOS"**
----------

## DIAGRAMA DE ESTADOS

## ¿Qué es?

El diagrama de estados es un diagrama de comportamiento en UML que muestra los diferentes estados por los que pasa un objeto a lo largo de su ciclo de vida, así como los eventos o transiciones que provocan esos cambios.

Se utiliza principalmente para modelar objetos dinámicos, es decir, aquellos cuyo comportamiento depende de eventos externos o internos (ejemplo: un pedido, una sesión de usuario, una máquina expendedora).

---

## Estructura

Un diagrama de estados incluye:

- **Estado** → Situación o condición en la que se encuentra un objeto (se representa como un rectángulo redondeado).
- **Transición** → Flecha que conecta estados y que ocurre cuando sucede un evento.
- **Evento** → Acción que dispara una transición (ejemplo: “clic en botón”, “tiempo expirado”).
- **Acción** → Respuesta que ocurre como parte de la transición o dentro de un estado.
- **Estado inicial** → Punto de inicio del ciclo de vida (círculo sólido).
- **Estado final** → Punto donde termina el ciclo de vida del objeto (círculo con borde y un punto negro dentro).
- **Estados compuestos** → Estados que contienen subestados internos.
- **Historial** → Indica que al volver a un estado compuesto, el objeto retoma el último subestado en el que estaba.

# **ACTIVIDAD**
**Contexto**. Se requiere modelar el núcleo de un sistema para un aeropuerto que gestione vuelos, pasajeros, control de check-in, seguridad, asignación de puertas, embarque y seguimiento en tiempo real (estado del vuelo, ubicación del pasajero en proceso, alertas). El sistema se integra con servicios de aerolíneas (emisión/validación de boarding pass), autoridad migratoria, control de seguridad y pantallas de información en sala. Debe soportar picos de demanda, trazabilidad y auditoría, y manejar excepciones (overbooking, cambio de puerta, retrasos, no show).

**Alcance mínimo**
- **Gestión de vuelos:** programación, estado (programado, abordando, cerrado, despegado, cancelado), asignación de puerta.
- **Gestión de pasajeros:** check-in, control de documentación, validación de boarding pass, embarque.
- **Flujo operativo:** colas por prioridad (PMR, familias, business), excepciones y reubicaciones.
- **Integraciones:** aerolínea (DCS/PSS), autoridad migratoria, seguridad aeroportuaria, pantallas (FIDS).
- **Observabilidad:** registro de eventos, tiempos de proceso y alertas operativas.
-------
# SOLUCIÓN DIAGRAMA DE ESTADOS 
---
---