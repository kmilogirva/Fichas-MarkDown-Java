# 🧳 **Colecciones, JSON y Manejo de Datos en Java**

En Java, las **colecciones** y el manejo de **JSON** son herramientas esenciales para organizar, almacenar y procesar grandes volúmenes de datos. Además, Java ofrece diversas técnicas para gestionar datos de forma eficiente, como el uso de listas, mapas y la conversión de objetos a formatos JSON.

---

## 📚 **Colecciones en Java**

Las **colecciones** son estructuras de datos que permiten almacenar y manipular grupos de objetos de manera flexible y eficiente. Java ofrece diferentes tipos de colecciones como `List`, `Set`, `Queue`, y `Map`.

### 🔹 **Tipos de Colecciones**

| Colección | Descripción                                      | Ejemplo de uso                      |
|-----------|--------------------------------------------------|-------------------------------------|
| **List**  | Almacena elementos en un orden específico y permite duplicados. | `List<String> lista = new ArrayList<>();` |
| **Set**   | Almacena elementos sin permitir duplicados.     | `Set<String> set = new HashSet<>();` |
| **Map**   | Almacena pares clave-valor.                      | `Map<Integer, String> map = new HashMap<>();` |
| **Queue** | Almacena elementos en una cola de acceso FIFO (First In, First Out). | `Queue<Integer> queue = new LinkedList<>();` |

---

## 🔄 **Operaciones Comunes en Colecciones**

### **Añadir elementos**

```java
List<String> lista = new ArrayList<>();
lista.add("Java");
lista.add("Python");

String elemento = lista.get(0);  // Accede al primer elemento de la lista
lista.remove("Python");  // Elimina el primer elemento "Python"
boolean contiene = lista.contains("Java");  // Devuelve true si "Java" está en la lista
```

## **🌐 Manejo de JSON en Java**

El formato JSON **(JavaScript Object Notation)** es ampliamente utilizado para intercambiar datos entre sistemas. En Java, existen bibliotecas como Jackson o Gson para convertir objetos Java en formato JSON y viceversa.

### **🔹 Ejemplo con la biblioteca Gson**
```java
import com.google.gson.Gson;

public class Persona {
    String nombre;
    int edad;

    public Persona(String nombre, int edad) {
        this.nombre = nombre;
        this.edad = edad;
    }
}

public class Main {
    public static void main(String[] args) {
        Persona persona = new Persona("Juan", 25);
        Gson gson = new Gson();
        String json = gson.toJson(persona);  // Convierte el objeto Persona a JSON
        System.out.println(json);
    }
}
```

Resultado:
```java
{"nombre":"Juan","edad":25}
```

## **🌐 Manejo de JSON en Java**

El manejo de datos en Java incluye tareas como leer y escribir datos en archivos, **realizar operaciones en bases de datos** y procesar datos desde diversos formatos.

### **🔹 Leer Datos desde un Archivo**
```java
import java.io.*;

public class LeerArchivo {
    public static void main(String[] args) {
        try (BufferedReader br = new BufferedReader(new FileReader("archivo.txt"))) {
            String linea;
            while ((linea = br.readLine()) != null) {
                System.out.println(linea);  // Imprime cada línea del archivo
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
### **🔹 Escribir Datos en un Archivo**
```java
import java.io.*;

public class EscribirArchivo {
    public static void main(String[] args) {
        try (BufferedWriter bw = new BufferedWriter(new FileWriter("archivo.txt"))) {
            bw.write("Hola, este es un archivo de ejemplo.");
            bw.newLine();
            bw.write("Escribiendo más datos.");
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

## **🏗️ Manejo de Datos con Bases de Datos (JDBC)**

El acceso a bases de datos en Java se realiza a través de **JDBC (Java Database Connectivity).** JDBC permite ejecutar consultas SQL y manejar datos almacenados en bases de datos.

### **🔹 Conectar a una Base de Datos**
```java
import java.sql.*;

public class ConexionDB {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/mi_base_de_datos";
        String usuario = "root";
        String clave = "password";

        try (Connection conn = DriverManager.getConnection(url, usuario, clave)) {
            System.out.println("Conexión exitosa a la base de datos.");
        } catch (SQLException e) {
            e.printStackTrace();
        }
    }
}
```

## **🛠️ Consejos y Buenas Prácticas**

**Uso eficiente de las colecciones:** Elige la colección correcta para tu caso de uso (por ejemplo, `ArrayList` para orden, `HashSet` para evitar duplicados).

**Evita conversiones innecesarias de JSON:** Convierte objetos a JSON solo cuando sea necesario para intercambiar datos con otros sistemas.

**Manejo de excepciones:** Siempre maneja las excepciones al trabajar con archivos o bases de datos para evitar errores en tiempo de ejecución.

