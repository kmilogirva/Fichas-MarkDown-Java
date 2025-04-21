# Guía de programación en Java

<div style="text-align: center;" >
  <h2><strong>FUNCIONES CON STRINGS EN JAVA</strong></h2>
</div>

---

## 🧠 ¿Qué es un String?

En Java, un **String** es un tipo de dato que representa una **cadena de texto**. Es un objeto que contiene una secuencia de caracteres como `"Hola Mundo"`.

Podemos realizar muchas operaciones sobre los Strings gracias a los métodos que Java proporciona.

---

## 🔧 ¿Qué se puede hacer con un String?

- 📏 Medir su longitud
- 🔠 Convertir a mayúsculas o minúsculas
- 🔍 Buscar una palabra o carácter
- ✂️ Extraer una parte
- 🔁 Reemplazar contenido
- ➕ Unir con otros Strings (concatenación)

---

## 📚 Principales métodos de la clase `String`

Primero, declaramos una variable:

```java
String mensaje = "Hola Mundo";
```
| Método                  | Descripción                                      | Ejemplo                                  | Resultado         |
|-------------------------|--------------------------------------------------|------------------------------------------|-------------------|
| `.length()`             | Devuelve la longitud del string                  | `mensaje.length()`                        | `10`               |
| `.toUpperCase()`        | Convierte a mayúsculas                          | `mensaje.length().toUpperCase()`                   | `"HOLA MUNDO"`          |
| `.toLowerCase()`        | Convierte a minúsculas                          | `mensaje.toLowerCase()`                   | `"hola mundo"`          |
| `.charAt(int index)`    | Devuelve el carácter en una posición            | `mensaje.charAt(2)`                       | `'l'`             |
| `.substring(int i, j)`  | Devuelve una subcadena                          | `mensaje.substring(0, 4)`           | `"Hola"`          |
| `.equals(String)`       | Compara si dos strings son iguales              | `"Hola".equals("hola")`                  | `false`           |
| `.equalsIgnoreCase()`   | Igual que `equals` pero ignora mayúsculas       | `"Hola".equalsIgnoreCase("hola")`        | `true`            |
| `.contains(String)`     | Verifica si contiene una subcadena              | `"Java".contains("va")`                  | `true`            |
| `.replace("a", "e")`    | Reemplaza caracteres o palabras                 | `"manzana".replace("a", "e")`            | `"menzene"`       |
| `.trim()`               | Elimina espacios al inicio y final              | `"  hola  ".trim()`                      | `"hola"`          |
| `.isEmpty()`            | Verifica si la cadena está vacía                | `"".isEmpty()`                           | `true`            |

---

## 🧪 Ejemplo práctico

```java
public class FuncionesString {
    public static void main(String[] args) {
        String texto = "  Bienvenido a Java  ";

        System.out.println("Texto original: '" + texto + "'");
        System.out.println("Longitud: " + texto.length());
        System.out.println("En mayúsculas: " + texto.toUpperCase());
        System.out.println("En minúsculas: " + texto.toLowerCase());
        System.out.println("Primera letra: " + texto.charAt(0));
        System.out.println("Subcadena: " + texto.substring(3, 12));
        System.out.println("Contiene 'Java': " + texto.contains("Java"));
        System.out.println("Texto sin espacios: '" + texto.trim() + "'");
        System.out.println("Está vacío: " + texto.isEmpty());

        String nuevoTexto = texto.replace("Java", "Python");
        System.out.println("Texto reemplazado: " + nuevoTexto);
    }
}
```


# 🖨️ ¿Qué es *Printing* en Java?

En Java, **"printing"** se refiere al proceso de **mostrar información en la consola o salida estándar**, es decir, lo que el usuario ve en pantalla mientras se ejecuta el programa.

---

## ✏️ ¿Cómo se hace?

Se utilizan los siguientes métodos:

- `System.out.print()`
- `System.out.println()`

---

## ✅ Ejemplos:

```java
System.out.println("Hola mundo");     // Imprime "Hola mundo" y salta a la siguiente línea
System.out.print("Hola");             // Imprime "Hola" sin salto de línea
System.out.println(" mundo");         // Imprime " mundo" en la misma línea
```

# 🔍 Scanner en Java

El **Scanner** en Java es una clase que permite **leer datos desde la entrada estándar**, normalmente el **teclado**. Es muy útil para programas interactivos que necesitan que el usuario ingrese información.

---

## 🧰 ¿Qué necesito para usar Scanner?

Primero, debes **importar la clase Scanner** desde la biblioteca `java.util`:

```java
import java.util.Scanner;
```

## 🧪 ¿ Cómo se utiliza?

```java
import java.util.Scanner;

public class EjemploScanner {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in); // Crear el objeto Scanner

        System.out.print("Ingresa tu nombre: ");
        String nombre = input.nextLine(); // Leer una línea de texto

        System.out.print("Ingresa tu edad: ");
        int edad = input.nextInt(); // Leer un número entero

        System.out.println("Hola " + nombre + ", tienes " + edad + " años.");
        
        input.close(); // Cerrar el Scanner al finalizar
    }
}
```

| Método         | Descripción                             | Ejemplo                             |
|----------------|-----------------------------------------|-------------------------------------|
| `nextLine()`   | Lee una línea completa de texto         | `String nombre = input.nextLine();` |
| `next()`       | Lee una sola palabra (hasta un espacio) | `String palabra = input.next();`    |
| `nextInt()`    | Lee un número entero                    | `int edad = input.nextInt();`       |
| `nextDouble()` | Lee un número decimal                   | `double altura = input.nextDouble();` |
| `nextBoolean()`| Lee un valor booleano (`true/false`)    | `boolean valor = input.nextBoolean();` |


## ⚠️ Recomendaciones
Siempre cierra el Scanner con **input.close();** al final del programa.

Ten cuidado al mezclar nextLine() con otros métodos como nextInt() o nextDouble(), ya que a veces queda un salto de línea pendiente y se necesita llamar a nextLine() adicionalmente.

## 🎯 ¿Para qué se usa?
Leer nombres, edades, valores, decisiones del usuario, etc.

Crear programas interactivos como menús, encuestas o formularios.

Capturar datos desde el teclado en tiempo de ejecución.