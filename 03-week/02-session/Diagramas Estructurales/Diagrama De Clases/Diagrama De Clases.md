# Diagrama de Clases UML

El **Diagrama de Clases** es uno de los **diagramas estructurales** más importantes en UML.  
Su objetivo principal es **modelar la estructura estática del sistema** mostrando las **clases**, sus **atributos**, **métodos** y las **relaciones** que existen entre ellas.

Es considerado la **base de la mayoría de los modelos UML**, ya que permite representar el diseño conceptual y lógico de un sistema orientado a objetos.

---

## Principales Características
- 📌 Representa la **estructura estática** del sistema.  
- 📌 Describe **clases, atributos, métodos** y **relaciones**.  
- 📌 Permite identificar el **modelo conceptual** y el **modelo de diseño**.  
- 📌 Es el diagrama más utilizado en UML.  
- 📌 Sirve de **puente entre el análisis y la programación**.  
- 📌 Puede usarse tanto en la **fase de diseño** como en la **fase de documentación** del software.  

---

### 1. Elementos Principales

#### a) Clases
Las clases son los bloques de construcción del diagrama. Se representan con un rectángulo dividido en tres secciones:
* **Sección Superior:** El **nombre** de la clase.
* **Sección Media:** Los **atributos** o propiedades de la clase.
* **Sección Inferior:** Las **operaciones** o métodos que la clase puede realizar.

**Visibilidad de Atributos y Operaciones:**
* `+` **Público**: Accesible desde cualquier clase.
* `#` **Protegido**: Accesible por la clase y sus subclases.
* `-` **Privado**: Solo accesible dentro de la propia clase.
* `~` **Paquete**: Accesible dentro del mismo paquete.

---

# Diagrama de Clases en UML  

## 1. Elementos del Diagrama de Clases  

### a) Clases  
Las clases son los bloques de construcción principales. Representan un conjunto de objetos que comparten las mismas características, relaciones y semántica.  

Se representan con un **rectángulo dividido en tres secciones**:  

- **Sección Superior:** Nombre de la clase.  
- **Sección Media:** Atributos (propiedades o campos).  
  - Sintaxis:  
    ```
    visibilidad nombre: tipo [multiplicidad] = valor_inicial {propiedad}
    ```
- **Sección Inferior:** Operaciones (métodos o funciones).  
  - Sintaxis:  
    ```
    visibilidad nombre(lista_de_parámetros): tipo_de_retorno {propiedad}
    ```

#### Visibilidad (Modificadores de Acceso)
- `+` Público: Accesible desde cualquier lugar.  
- `#` Protegido: Accesible solo por la clase y sus subclases.  
- `-` Privado: Accesible solo por la propia clase.  
- `~` Paquete: Accesible dentro del mismo paquete.  

---

## 2. Estructura de un Diagrama de Clases  
La estructura se compone de las clases y sus relaciones.  
Un diagrama bien diseñado debe ser **legible y coherente**, mostrando cómo interactúan los diferentes componentes del sistema.  
No es solo una lista de clases, sino una **red interconectada**.  

---

## 3. Relaciones entre Clases  

### a) Asociación  
- Representa una relación estructural entre clases.  
- Se dibuja con una línea recta entre ellas.  
- Puede tener:  
  - **Nombre:** Describe la naturaleza de la relación (ej. *trabaja en*).  
  - **Roles:** Cómo cada clase participa en la relación (ej. *empleado* – *departamento*).  
  - **Multiplicidad:** Número de objetos relacionados:  
    - `1` → Uno y solo uno.  
    - `0..1` → Cero o uno.  
    - `*` → Cero o más.  
    - `1..*` → Uno o más.  
    - `n` → Exactamente *n*.  
    - `n..m` → De *n* a *m*.  

### b) Agregación  
- Relación **todo-parte** débil.  
- La parte puede existir independientemente del todo.  
- Se representa con un **rombo vacío** en el lado del *todo*.  

### c) Composición  
- Relación **todo-parte** fuerte.  
- La parte **no puede existir** sin el todo.  
- Si el todo se destruye, las partes también.  
- Se representa con un **rombo sólido**.  

### d) Herencia (Generalización/Especialización)  
- Representa una relación **“es un”**.  
- Una subclase hereda atributos y operaciones de la superclase.  
- Se representa con una **flecha triangular hueca** hacia la superclase.  

### e) Dependencia  
- Una clase depende de otra (cambios en una pueden afectar a la otra).  
- Relación débil.  
- Se representa con una **línea discontinua con flecha**.  

---

## 4. Ventajas de Usar Diagramas de Clases  
- **Claridad y Comprensión:** Visualizan la estructura del sistema de manera clara.  
- **Comunicación Efectiva:** Herramienta común entre desarrolladores, analistas y clientes.  
- **Base para la Implementación:** Se pueden traducir directamente a código.  
- **Detección de Errores de Diseño:** Identificación de problemas antes de codificar.  
- **Mantenimiento y Refactorización:** Documentación útil para evolución del sistema.  

---

## 5. Desventajas de Usar Diagramas de Clases  
- **Complejidad:** Pueden volverse difíciles de leer en sistemas grandes.  
- **No Muestran Comportamiento Dinámico:** Solo la estructura estática.  
- **Curva de Aprendizaje:** Requieren conocimientos en notación UML.  
- **Sobrediseño:** Riesgo de invertir demasiado tiempo en el modelado.  

---

## 6. Conclusión  
El **diagrama de clases** es una herramienta indispensable en el desarrollo de software orientado a objetos.  
Funciona como un **plano arquitectónico** que ofrece una visión clara de la estructura, componentes y relaciones.  

Aunque no refleja el comportamiento dinámico, sus ventajas en términos de comunicación, documentación y detección de errores superan sus desventajas.  
Dominarlo es fundamental para cualquier profesional en el diseño y construcción de **sistemas de software complejos y bien estructurados**.  



# Ejemplos de Relaciones en Diagramas de Clases UML

---

## Ejemplo de Asociación

**Clases: Usuario – Compra**

| **Usuario**              |                                    | **Compra**               |
|---------------------------|------------------------------------|--------------------------|
| - id: int                 | 1..* realiza                      | - fecha: Date            |
| - nombre: str             |                                    | - total: double          |
| + iniciarSesion()         |                                    | + calcularTotal()        |
| + verHistorialCompras()   |                                    | + anadirItem()           |

👉 **Un Usuario realiza una o más Compras**

---

## Ejemplo de Agregación

**Clases: Universidad – Departamento**

| **Universidad**           |                                    | **Departamento**         |
|---------------------------|------------------------------------|--------------------------|
| - nombre: str             | <> 1..* tiene                     | - nombre: str            |
| - ubicacion: str          |                                    | - telefono: str          |
| + obtenerDepartamentos()  |                                    | + getJefeDepartamento()  |

👉 **Una Universidad tiene uno o más Departamentos. Un Departamento puede existir sin la Universidad.**

---

## Ejemplo de Composición

**Clases: Vehículo – Motor**

| **Vehículo**              |                                    | **Motor**                |
|---------------------------|------------------------------------|--------------------------|
| - marca: str              | <#> 1                              | - tipo: str              |
| - modelo: str             |                                    | - potencia: int          |
| + arrancar()              |                                    | + encender()             |

👉 **Un Vehículo tiene un Motor. Si el Vehículo se destruye, el Motor también deja de existir.**

---

## Ejemplo de Herencia

**Clases: Persona – Estudiante**

| **Persona**               |
|---------------------------|
| - nombre: str             |
| - edad: int               |
| + caminar()               |
| + hablar()                |

Hereda hacia ↓

| **Estudiante**            |
|---------------------------|
| - matricula: str          |
| - carrera: str            |
| + estudiar()              |

👉 **Un Estudiante es una Persona.**

---

## Ejemplo de Dependencia

**Clases: Reporte – BaseDeDatos**

| **Reporte**               |                                    | **BaseDeDatos**          |
|---------------------------|------------------------------------|--------------------------|
| + generarReporte()        | ---<...--- depende de             | + conectar()             |
| + imprimir()              |                                    | + desconectar()          |

👉 **La clase Reporte depende de la clase BaseDeDatos para generar un reporte.**

---------
# EJEMPLO CON CARRITO DE COMPRAS
## Código:
# Diagrama de Clases - Carrito de Compras

```plantuml
@startuml
skinparam classAttributeIconSize 0

class Usuario {
    +int idUsuario
    +string nombre
    +string email
    +string contraseña
    +registrar()
    +iniciarSesion()
    +cerrarSesion()
}

class Producto {
    +int idProducto
    +string nombre
    +double precio
    +int stock
    +actualizarStock(cantidad:int)
    +obtenerInfo():string
}

class ItemCarrito {
    +int cantidad
    +double subtotal
    +calcularSubtotal():double
}

class Carrito {
    +int idCarrito
    +Date fechaCreacion
    +double total
    +agregarProducto(p:Producto, cantidad:int)
    +eliminarProducto(p:Producto)
    +calcularTotal():double
}

class Pedido {
    +int idPedido
    +Date fecha
    +string estado
    +confirmar()
    +cancelar()
}

class Pago {
    +int idPago
    +double monto
    +string metodo
    +procesarPago():bool
    +generarRecibo():string
}

Usuario --> Carrito
Carrito *-- ItemCarrito
ItemCarrito --> Producto
Carrito --> Pedido
Pedido --> Pago
@enduml
