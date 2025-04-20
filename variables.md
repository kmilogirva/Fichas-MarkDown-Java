# Guía de programación en Java

<div style="text-align: center;" >
  <h2><strong>VARIABLES EN JAVA</strong></h2>
</div>

---

## 🧠 ¿Qué es entonces una variable?

Una **variable** es como una **cajita** con un nombre, que sirve para guardar datos. Esta caja puede cambiar su contenido a lo largo del tiempo.

Imagina que tienes una caja llamada `edad` donde puedes guardar un número. Puedes abrirla, ver su contenido, cambiarlo o usarlo para hacer cálculos.

---

## 🎯 Propósito de una variable

- **Almacenar datos temporalmente en la memoria del programa.**
- **Facilitar operaciones matemáticas, lógicas o de texto.**
- **Hacer tu código más flexible y dinámico.**
- **Permitir reutilizar valores sin tener que escribirlos múltiples veces.**

---

## 💡 Características clave

- Cada variable tiene:
  - Un **nombre**.
  - Un **tipo de dato** (ej: `int`, `String`, `boolean`, etc.).
  - Un **valor** (que puede cambiar).

---

## 🧪 Ejemplos en Java

### 🔹 Declarar una variable

Una cosa es declarar una variable, otra muy diferente inicializarla. A continuación miraremos la diferencia.

#### **DECLARAR**

```java
int edad;
```

Aquí nuestra variable está declarada pero aún no tiene valor asignado.

```java
edad = 58;
```

Aquí estamos asignando un valor a la variable que ya había sido declarada. edad ahora vale 58.

```java
int edad = 5;
```
Aquí estamos declarando y asignando un valor a la variable en la misma linea.

<div style="text-align: center;" >
  <h4><strong>🔄 Tipos comunes de variables en Java</strong></h4>
</div>


| Tipo de dato | Ejemplo                 | Descripción              |
|--------------|-------------------------|--------------------------|
| `int`        | `int edad = 30;`        | Números enteros          |
| `double`     | `double pi = 3.14;`     | Números decimales        |
| `string`     | `string nombre = "Ana";`| Texto o cadenas de caracteres |
| `bool`       | `bool esEdicion = true;`| Verdadero o falso        |
| `char`       | `char letra = 'A';`     | Un solo carácter         |


<div style="text-align: center;" >
  <h4><strong>🔄 Cómo usarlo?</strong></h4>
</div>

```java
public class Estudiante {
    public static void main(String[] args) {

        String studentName = "John Doe";
        int studentID = 15;
        int studentAge = 23;

        // Al flotante se debe agregar la 'f' al final del valor decimal
        float studentFee = 75.25f;

        // Los double no necesitan la 'f'
        double studentDouble = 75.24;

        // Char se declara con comillas simples
        char studentGrade = 'B';

        // Imprimir variables
        System.out.println("Student name: " + studentName);
        System.out.println("Student ID: " + studentID);
        System.out.println("Student age: " + studentAge);
        System.out.println("Student float: " + studentFee);
        System.out.println("Student double: " + studentDouble);
        System.out.println("Student grade: " + studentGrade);
    }
}
```