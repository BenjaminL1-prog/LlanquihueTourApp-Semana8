# LlanquihueTourApp

## 1. Descripción del sistema

LlanquihueTourApp es una aplicación desarrollada en Java que permite gestionar información relacionada con la agencia ficticia **Llanquihue Tour**, ubicada en la Región de Los Lagos, Chile.

En esta versión del proyecto se amplía el sistema incorporando nuevas entidades de la agencia, permitiendo registrar y administrar guías turísticos, vehículos y colaboradores externos. Además, se implementan interfaces, herencia, polimorfismo, colecciones genéricas y una interfaz gráfica básica para facilitar la interacción con el usuario.

El proyecto fue desarrollado aplicando principios de Programación Orientada a Objetos (POO), modularidad, reutilización de código y buenas prácticas de programación.

---

## 2. Funcionalidades principales

* Registro de guías turísticos.
* Registro de vehículos.
* Registro de colaboradores externos.
* Almacenamiento de entidades mediante una colección genérica (`ArrayList<Registrable>`).
* Visualización de todas las entidades registradas.
* Implementación de interfaces para definir un comportamiento común.
* Aplicación de herencia entre clases.
* Uso de polimorfismo e identificación de objetos mediante `instanceof`.
* Interfaz gráfica desarrollada con `JOptionPane` para el ingreso y visualización de información.

---

## 3. Estructura del proyecto

El sistema se encuentra organizado en los siguientes paquetes:

### model

Contiene las clases principales del dominio del problema:

* Registrable (interfaz común para las entidades gestionables).
* Persona (superclase).
* RecursoAgencia (superclase).
* GuiaTuristico.
* Vehiculo.
* ColaboradorExterno.

### data

Contiene la lógica de gestión de datos:

* GestorDatos.
* GestorEntidades.

### ui

Contiene la clase principal del sistema:

* Main.

---

## 4. Relación entre clases

El sistema incorpora dos jerarquías de herencia.

La primera corresponde a la clase **Persona**, que actúa como superclase de **GuiaTuristico** y **ColaboradorExterno**, permitiendo reutilizar atributos y comportamientos comunes.

La segunda corresponde a la clase **RecursoAgencia**, utilizada como superclase de **Vehiculo**, representando los recursos físicos administrados por la agencia.

Además, todas las entidades implementan la interfaz **Registrable**, la cual define el método `mostrarResumen()`. Esto permite almacenar objetos de distintos tipos dentro de una misma colección (`ArrayList<Registrable>`) y aplicar polimorfismo al recorrerla.

Durante el recorrido de la colección se utiliza el operador `instanceof` para identificar el tipo específico de cada objeto y ejecutar la lógica correspondiente.

---

## 5. Ejecución del sistema

Para ejecutar el proyecto:

1. Abrir el proyecto en IntelliJ IDEA o Visual Studio Code con soporte para Java.
2. Ejecutar la clase **Main** ubicada en el paquete **ui**.
3. Utilizar el menú mostrado mediante `JOptionPane`.
4. Registrar guías turísticos, vehículos o colaboradores externos.
5. Visualizar el resumen de todas las entidades registradas.

---

## 6. Tecnologías utilizadas

* Lenguaje de programación: Java
* Paradigma: Programación Orientada a Objetos (POO)
* Interfaz gráfica: JOptionPane (Swing)
* Estructuras de datos: ArrayList
* Conceptos aplicados:

  * Interfaces
  * Herencia
  * Polimorfismo
  * instanceof
  * Colecciones genéricas
* Entorno de desarrollo: IntelliJ IDEA

---

## 7. Autor

**Benjamín Lizama Osorio**

Proyecto académico desarrollado como parte del curso **Desarrollo Orientado a Objetos I**.
