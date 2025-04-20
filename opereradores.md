<h1 style="text-align: center;" > Guia de programación en Java</h1>
<div style="text-align: center;" >
  <h2><strong>OPERADORES EN JAVA</strong></h2>
</div>

## ➕ ¿Qué son los operadores?

Los operadores son símbolos que nos permiten realizar operaciones sobre variables o valores. Pueden ser matemáticos, lógicos, de comparación, entre otros.

🧮 **Operadores Matemáticos**
Se usan para realizar cálculos básicos como suma, resta, multiplicación, etc.

<div style="text-align: center;" >
  <h4><strong>🔢 Principales operadores matemáticos</strong></h4>
</div>            


| Operador| Descripción| Ejemplo ->Resultado|
|---------|------------|------------|
|`+`|`Suma`|`5 + 3 → 8`|
|`-`|`Resta`|`5 - 3 → 2`|
|`*`|`Multiplicación`|`5 * 3 → 15`|
|`/`|`División`|`15 / 3 → 5`|
|`%`|`Módulo (resto)`|`	9 % 4 → 1`|


<div style="text-align: center;" >
  <h4><strong>🎯 Aplicación práctica operadores matemáticos</strong></h4>
</div>  

```Java
System.out.println("Suma: " + (a + b));
System.out.println("Resta: " + (a - b));
System.out.println("Multiplicación: " + (a * b));
System.out.println("División: " + (a / b));
System.out.println("Módulo: " + (a % b));
```
⚖️ **Operadores de Comparación**
Se usan para comparar dos valores. El resultado siempre será true o false.

🔍 **Operadores de comparación**

|Operador|Significado|Ejemplo (true o false)|
|--------|-----------|----------------------|
|==	|Igual a|5 == 5 → true|
|!=	|Diferente de|4 != 3 → true|
|>	|Mayor que|6 > 2 → true|
|<|Menor que|3 < 5 → true|
|>=	|Mayor o igual que|7 >= 7 → true|
|<=|Menor o igual que|2 <= 3 → true|

<div style="text-align: center;" >
  <h4><strong>✏️ Ejemplo práctico:</strong></h4>
</div>       


```Java
int x = 5;
int y = 10;

System.out.println(x == y); // false
System.out.println(x != y); // true
System.out.println(x < y);  // true
System.out.println(x >= y); // false

```
---

## 🔗 **Operadores lógicos en Java**

Los **operadores lógicos** permiten combinar múltiples expresiones booleanas y evalúan a `true` o `false` dependiendo de la lógica aplicada.

| Operador | Nombre|Descripción| Ejemplo|Resultado|
|----------|-------|-----------|--------|---------|
|`&&`| AND (Y lógico)| Verdadero si **ambas** condiciones son verdaderas| `(5 > 2) && (4 < 6)`| `true`|
|`Doble Barra vertical`| OR (O lógico) |Verdadero si **al menos una** condición es verdadera | `(3 > 5) `Operador` (10 == 10)`|`true`|
| `!` |NOT (Negación)| Invierte el valor lógico de una expresión | `!(7 > 3)`| `false`|

---

### 🧪 Ejemplos prácticos

```java
public class OperadoresLogicos {
    public static void main(String[] args) {
        boolean a = true;
        boolean b = false;

        System.out.println("a && b = " + (a && b)); // false
        System.out.println("a || b = " + (a || b)); // true
        System.out.println("!a = " + (!a));         // false
        System.out.println("!b = " + (!b));         // true

        // Combinación con expresiones
        int edad = 20;
        boolean esAdulto = (edad >= 18) && (edad < 65);
        System.out.println("¿Es adulto? " + esAdulto); // true
    }
}
```

### Operadores de Asignación


Estos operadores permiten **asignar valores** a las variables de manera eficiente. Aunque el operador de asignación básico es =, Java tiene varios operadores compuestos que facilitan la manipulación de valores.

| Operador | Descripción                      | Ejemplo   | Resultado         |
|----------|----------------------------------|-----------|-------------------|
| `=`      | Asignación simple                | `a = 5`   | Asigna 5 a `a`    |
| `+=`     | Suma y asigna                    | `a += 3`  | `a = a + 3`       |
| `-=`     | Resta y asigna                   | `a -= 2`  | `a = a - 2`       |
| `*=`     | Multiplica y asigna              | `a *= 4`  | `a = a * 4`       |
| `/=`     | Divide y asigna                  | `a /= 2`  | `a = a / 2`       |
| `%=`     | Aplica el módulo y asigna        | `a %= 3`  | `a = a % 3`       |


## ➖ **Operadores Unarios en Java**

Los operadores unarios realizan operaciones con un solo operando. Son utilizados para **modificar el valor de una variable** o para obtener el valor de una expresión.

| Operador | Descripción                      | Ejemplo   | Resultado         |
|----------|----------------------------------|-----------|-------------------|
| `+`      | Operador de signo positivo       | `+a`      | Devuelve `a` (sin cambios) |
| `-`      | Operador de signo negativo       | `-a`      | Negativo de `a`   |
| `++`     | Incremento (aumenta 1)           | `a++`     | Incrementa `a` en 1 |
| `--`     | Decremento (disminuye 1)         | `a--`     | Decrementa `a` en 1 |
| `!`      | Negación lógica                  | `!a`      | Invertir valor lógico de `a` |

```java
int a = 5;
System.out.println(++a);  // Imprime 6 (pre-incremento)
System.out.println(a--);  // Imprime 6 (post-decremento), luego a = 5
System.out.println(a);    // Imprime 5
```

### Conclusión sobre los Operadores en Java

En Java, los **operadores** son herramientas fundamentales que permiten realizar diversas operaciones con los datos en nuestros programas. Desde operaciones matemáticas básicas como la suma ➕ y la resta ➖, hasta comparaciones 🔍 y evaluaciones lógicas 🤖, los operadores permiten que nuestras aplicaciones sean dinámicas y funcionales.

Es importante comprender los distintos tipos de operadores, como los **aritméticos** 🔢, **de comparación** ⚖️, **lógicos** 🔗, **unarios** 🔄 y **de asignación** 📥, para poder utilizarlos de manera efectiva y escribir código limpio y eficiente.

Conocer cómo y cuándo utilizar cada operador nos permite optimizar nuestros programas 💻, realizar validaciones ✅, manejar flujos de control 🔄 y modificar datos de manera precisa 🧠. En resumen, los operadores son piezas clave en la programación que permiten interactuar con los valores de las variables y crear la lógica de nuestros algoritmos 🧑‍💻.
