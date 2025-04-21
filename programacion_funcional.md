# 🧠 Programación Funcional en Java

La **programación funcional** es un paradigma que trata la computación como la evaluación de funciones matemáticas, evitando cambiar el estado y los datos mutables. A partir de Java 8, este estilo se volvió más accesible gracias a las expresiones lambda, streams y referencias a métodos.

---

## 🌱 Características clave

- **Funciones como ciudadanos de primera clase**
- **Inmutabilidad**
- **Funciones puras**
- **Uso de expresiones lambda**
- **Composición de funciones**
- **Referencia a Metodos**
- **Streams**


---
| Concepto                  | Descripción                                                                 | Ejemplo en Java                                                                 |
|---------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| **Funciones de primera clase** | Las funciones pueden ser asignadas a variables, pasadas como argumentos o retornadas. | `Predicate<String> p = s -> s.isEmpty();`                                       |
| **Inmutabilidad**         | Los datos no se modifican, se crean nuevas instancias.                      | `List<String> lista = List.of("A", "B"); // no modificable`                     |
| **Funciones puras**       | Siempre devuelven el mismo resultado para los mismos parámetros, sin efectos secundarios. | `int sumar(int a, int b) { return a + b; }`                                     |
| **Expresiones lambda**    | Forma concisa de escribir funciones anónimas.                               | `(x, y) -> x + y`                                                               |
| **Composición de funciones** | Unir funciones simples para formar lógicas más complejas.               | `f.andThen(g)` o `f.compose(g)`                                                |
| **Referencias a métodos** | Acceder a métodos existentes de forma funcional.                            | `String::toUpperCase`                                                           |
| **Streams**               | Procesar colecciones de manera funcional y declarativa.                     | `list.stream().filter(x -> x > 5).map(x -> x*2).collect(Collectors.toList());`  |



## 🔹 Expresiones Lambda

Las **expresiones lambda** son una característica de Java introducida en Java 8 que permiten escribir funciones anónimas (sin nombre) de manera más concisa y legible. Son especialmente útiles en programación funcional y cuando trabajamos con APIs como Streams, Collections y funciones de orden superior.

```java
// Sintaxis: (parámetros) -> expresión
List<String> nombres = Arrays.asList("Ana", "Luis", "Carlos");
nombres.forEach(nombre -> System.out.println(nombre));
```

