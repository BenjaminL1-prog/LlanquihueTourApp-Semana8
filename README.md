# LlanquihueTourApp

## 1. Descripción del sistema

LlanquihueTourApp es una aplicación desarrollada en Java que permite gestionar información relacionada con la agencia ficticia **Llanquihue Tour**, ubicada en la Región de Los Lagos, Chile.

El proyecto fue evolucionando durante las distintas actividades de la asignatura, incorporando la administración de tours turísticos, servicios turísticos y nuevas entidades de la agencia, como guías turísticos, vehículos y colaboradores externos.

En esta versión se aplican conceptos de Programación Orientada a Objetos (POO), como interfaces, herencia, polimorfismo, colecciones genéricas, validación mediante `instanceof` e interfaz gráfica desarrollada con `JOptionPane`.

---

## 2. Funcionalidades principales

- Lectura de datos desde archivo de texto.
- Gestión de tours turísticos.
- Gestión de servicios turísticos.
- Registro de guías turísticos.
- Registro de vehículos.
- Registro de colaboradores externos.
- Almacenamiento de entidades mediante colecciones dinámicas (`ArrayList`).
- Visualización de información desde una interfaz gráfica.
- Implementación de interfaces para definir comportamientos comunes.
- Aplicación de herencia entre clases.
- Aplicación de polimorfismo mediante sobrescritura de métodos.
- Identificación de objetos utilizando el operador `instanceof`.

---

## 3. Estructura del proyecto

El sistema se encuentra organizado en los siguientes paquetes:

### model

Contiene las clases principales del dominio del problema:

- Tour
- Proveedor
- ServicioTuristico
- RutaGastronomica
- PaseoLacustre
- ExcursionCultural
- Registrable (interfaz)
- Persona (superclase)
- RecursoAgencia (superclase)
- GuiaTuristico
- ColaboradorExterno
- Vehiculo

### data

Contiene la lógica de acceso y gestión de datos:

- GestorDatos
- GestorServicios
- GestorEntidades

### ui

Contiene las clases relacionadas con la interfaz del sistema:

- Main
- InterfazAgencia

---

## 4. Relación entre clases

El proyecto incorpora distintos conceptos de Programación Orientada a Objetos.

La clase **Tour** mantiene una relación de composición con la clase **Proveedor**, ya que cada tour posee internamente un proveedor asociado.

Además, existe una jerarquía de herencia donde **ServicioTuristico** actúa como superclase de **RutaGastronomica**, **PaseoLacustre** y **ExcursionCultural**, permitiendo aplicar polimorfismo mediante la sobrescritura del método `mostrarInformacion()`.

Para esta versión del proyecto se incorporó una nueva jerarquía de clases. **Persona** funciona como superclase de **GuiaTuristico** y **ColaboradorExterno**, mientras que **RecursoAgencia** actúa como superclase de **Vehiculo**.

Asimismo, las entidades **GuiaTuristico**, **ColaboradorExterno** y **Vehiculo** implementan la interfaz **Registrable**, permitiendo almacenarlas dentro de una colección genérica (`ArrayList<Registrable>`).

Durante el recorrido de la colección se utiliza el operador `instanceof` para identificar el tipo específico de cada objeto y ejecutar la lógica correspondiente.

---

## 5. Ejecución del sistema

Para ejecutar el proyecto:

1. Abrir el proyecto en IntelliJ IDEA o Visual Studio Code con soporte para Java.
2. Verificar que el archivo de datos se encuentre en la ruta `resources/tours.txt`.
3. Ejecutar la clase **Main** ubicada en el paquete **ui**.
4. Utilizar el menú de la interfaz gráfica desarrollado con `JOptionPane`.
5. Registrar guías turísticos, vehículos o colaboradores externos.
6. Visualizar el resumen de las entidades registradas.

---

## 6. Tecnologías utilizadas

- Lenguaje de programación: Java
- Paradigma: Programación Orientada a Objetos (POO)
- Manejo de archivos: BufferedReader / FileReader
- Interfaz gráfica: JOptionPane (Swing)
- Estructuras de datos: ArrayList y List

### Conceptos aplicados

- Composición
- Interfaces
- Herencia
- Polimorfismo
- instanceof
- Colecciones genéricas

Entorno de desarrollo:

- IntelliJ IDEA

---

## 7. Autor

**Benjamín Lizama Osorio**

Proyecto académico desarrollado como parte del curso **Desarrollo Orientado a Objetos I**.
