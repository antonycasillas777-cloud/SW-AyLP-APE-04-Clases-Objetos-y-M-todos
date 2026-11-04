# SW-AyLP-APE-04: Clases, Objetos y Métodos

Guía práctica APE 04 de la asignatura **Algoritmos y Lógica de Programación**, desarrollada en **Java** con el IDE **NetBeans**.

| | |
|---|---|
| **Estudiante** | Casillas Ochoa Antony Sebastián |
| **Nivel y paralelo** | Primero - B |
| **Docente** | Ing. José Caiza |
| **Unidad de organización curricular** | Básica |
| **Institución** | Universidad Técnica de Ambato (UTA) |

---

## Objetivo general

Desarrollar programas utilizando clases, objetos y métodos, lo cual permite disminuir errores y reutilizar el código.

## Objetivos específicos

1. Definir clases con sus atributos y constructores para modelar entidades del problema.
2. Implementar métodos que realicen operaciones y cálculos sobre los datos de los objetos.
3. Relacionar varias clases entre sí mediante la creación e interacción de objetos en Java.

---

## Estructura del repositorio

```
SW-AyLP-APE-04-Clases-Objetos-y-M-todos/
├── Ejercicio 1/                      # Autor y Libro
├── Ejercicio 2/                      # Rectángulo
├── Ejercicio 3/                      # Producto y Venta
├── Ejercicio 4/                      # Cuenta
├── Ejercicio 5/                      # Usuario, Libro y Préstamo
├── Infografia_General_APE4_Java.pdf  # Resumen visual de la práctica
└── README.md
```

## Ejercicios

| N.º | Clases | Clase principal | Qué se practica |
|:---:|---|---|---|
| 1 | `Autor`, `Libro` | `MainEj1` | Atributos, constructores y relación entre objetos (un libro tiene un autor). Método `mostrarInformacion()`. |
| 2 | `Rectangulo` | `MainEj2` | Métodos que calculan a partir de los atributos del objeto. |
| 3 | `Producto`, `Venta` | `MainEj3` | Colaboración entre clases para registrar una venta. |
| 4 | `Cuenta` | `MainEj4` | Métodos que modifican el estado del objeto (saldo). |
| 5 | `Usuario`, `Libro`, `Prestamo` | `MainEj5` | Sistema de préstamos que integra varias clases. |

---

## Cómo ejecutar

**Requisitos:** JDK 8 o superior. NetBeans es opcional.

**Con NetBeans**
1. Clona el repositorio o descárgalo como ZIP.
2. Abre la carpeta del ejercicio como proyecto (`File > Open Project`).
3. Ejecuta la clase principal (`MainEjN`) con `Run File` (Shift + F6).

**Con la terminal**
```bash
git clone https://github.com/antonycasillas777-cloud/SW-AyLP-APE-04-Clases-Objetos-y-M-todos.git
cd "SW-AyLP-APE-04-Clases-Objetos-y-M-todos/Ejercicio 1"
javac *.java
java MainEj1
```
Cambia `Ejercicio 1` y `MainEj1` por el ejercicio que quieras probar.

---

## Ejemplo de código (Ejercicio 1)

```java
class Autor {
    String nombre;
    String nacionalidad;

    Autor(String nombre, String nacionalidad) {
        this.nombre = nombre;
        this.nacionalidad = nacionalidad;
    }
}

class Libro {
    String titulo;
    int anio;
    Autor autor;

    Libro(String titulo, int anio, Autor autor) {
        this.titulo = titulo;
        this.anio = anio;
        this.autor = autor;
    }

    void mostrarInformacion() {
        System.out.println("Titulo: " + titulo);
        System.out.println("Año: " + anio);
        System.out.println("Autor: " + autor.nombre);
    }
}
```

---

## Conclusiones

- Las clases y los objetos permiten organizar el código en partes independientes que representan elementos reales.
- Los métodos y constructores evitan repetir instrucciones, lo que reutiliza el código y disminuye los errores.
- Relacionar objetos de distintas clases permite resolver problemas más completos.

## Recomendaciones

- Analizar el problema antes de programar e identificar sus clases, atributos y métodos.
- Usar nombres claros y comentar el código.
- Probar cada clase con distintos datos y practicar con encapsulamiento (`private`, getters y setters).

---

## Referencias

- Deitel, P., & Deitel, H. (2018). *Java: How to program, early objects* (11.ª ed.). Pearson.
- Schildt, H. (2022). *Java: A beginner's guide* (9.ª ed.). McGraw-Hill Education.
- Oracle. (s. f.). *Lesson: Classes and objects*. The Java™ Tutorials. https://docs.oracle.com/javase/tutorial/java/javaOO/index.html
