# 🧭 Control de Flujo en Java


El **control de flujo** en Java permite dirigir el orden en que se ejecutan las instrucciones dentro de un programa. Esto es útil para tomar decisiones, repetir tareas o reaccionar a diferentes condiciones.

---

## 🛣️ Estructuras de control principales

### 🔹 1. Condicional `if`, `else if`, `else`

```java
int edad = 18;

if (edad >= 18) {
    System.out.println("Eres mayor de edad.");
} else {
    System.out.println("Eres menor de edad.");
}
```
##  Explicación IF 🧠

La estructura condicional de `if` ,`else if`, `else` nos permite evaluar diferentes caminos o posible vertientes en la ejecución de un programa, resulta demasiado útil para tomar decisiones referentes a un caso u otro.

### 🔹 2. Condicional `switch`

```java
int dia = 2;

switch (dia) {
    case 1:
        System.out.println("Lunes");
        break;
    case 2:
        System.out.println("Martes");
        break;
    default:
        System.out.println("Otro día");
}

```

##  Explicación switch 🧠

La estructura condicional de `switch` al igual que la anterior nos permite mostrar o realizar determinada lógica si una condición especifica se cumple u no...
esta condicional resulta útil para aquellos momentos en que el usuario debe ingresa un valor y de acuerdo al valor agregado se toman unas u otras decisiones.

## 🛣️ Bucles, ciclos o loopers

### 🔸 1. Bucle `for`
```java
for (int i = 0; i < 5; i++) {
    System.out.println("Repetición " + i);
}

```
##  Explicación for 🧠

El bucle `for` nos permite realizar o ejecutar determinado número de repeticiones hasta que se alcanza el limite fijado para que dicha lógica se ejecute.

### 🔸 2. Bucle `while`
```java
int i = 0;
while (i < 5) {
    System.out.println("Valor de i: " + i);
    i++;
}
```
##  Explicación while 🧠

El bucle `while` que literalmente en la lengua española significa `mientras` es útil al momento de realizar repeticiones mientras cierta condición definida con anterioridad se cumpla,si dicha condición no se cumple `nunca se ejecutará.`

### 🔸 2. Bucle `do-while`
```java
int i = 0;
do {
    System.out.println("Este código se ejecuta al menos una vez");
    i++;
} while (i < 3);
```

##  Explicación do-while 🧠

El bucle `do-while` es muy similar al `while` con una diferencia de que la primera ejecución del programa se realiza siempre; es decir, en el ciclo `while`
la condición debe cumplirse para que el programa sea ejecutado de forma inicial en el ciclo `do-while` primero se ejecuta y luego se valida si la condición establecida se cumple o se sigue cumpliendo.