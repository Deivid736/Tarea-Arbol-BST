# Análisis y Desarrollo de un Árbol Binario de Búsqueda

## Resumen

Como parte de esta actividad se desarrolló una estructura de datos tipo Árbol Binario de Búsqueda (BST). La implementación fue realizada completamente en Java, incorporando algoritmos recursivos para resolver diferentes operaciones y desafíos relacionados con la organización de nodos.

El programa permite administrar elementos numéricos dentro de una estructura jerárquica, facilitando consultas, recorridos y transformaciones sobre el árbol.

---

# Preparación del entorno

Para ejecutar el proyecto se requiere:

- Java 17
- Apache Maven
- Eclipse (opcional)

Compilación:

```bash
mvn clean compile
```

Ejecución:

```bash
mvn exec:java -Dexec.mainClass="umg.edu.progra.arboles.Principal"
```

---

# Desarrollo realizado

## 1. Cálculo de la cantidad de nodos

### Objetivo

Determinar cuántos elementos existen dentro del árbol sin depender de variables auxiliares que almacenen el tamaño.

### Estrategia utilizada

Se aplicó un recorrido recursivo donde cada llamada contabiliza:

- El nodo actual.
- El subárbol izquierdo.
- El subárbol derecho.

### Evidencia

```text
Total de nodos detectados: 8
```

---

## 2. Evaluación del equilibrio estructural

### Objetivo

Verificar si la estructura mantiene una distribución razonable entre sus ramas.

### Estrategia utilizada

Se comparó la altura de ambos subárboles en cada nodo y se validó que la diferencia no excediera una unidad.

### Evidencia

```text
Resultado de balanceo: true
```

```text
Resultado de balanceo: false
```

---

## 3. Comprobación de integridad del BST

### Objetivo

Confirmar que todos los nodos cumplen las reglas fundamentales de un Árbol Binario de Búsqueda.

### Estrategia utilizada

Durante el recorrido se verificó que los valores menores permanecieran a la izquierda y los mayores a la derecha.

### Evidencia

```text
Verificación satisfactoria: true
```

```text
Verificación satisfactoria: false
```

---

## 4. Localización del ancestro compartido más cercano

### Objetivo

Encontrar el punto de convergencia más próximo entre dos nodos del árbol.

### Casos evaluados

```text
Nodo A: 10
Nodo B: 40
Ancestro encontrado: 30
```

```text
Nodo A: 10
Nodo B: 80
Ancestro encontrado: 50
```

---

## 5. Transformación espejo

### Objetivo

Generar una versión reflejada del árbol original.

### Procedimiento

Se intercambiaron los enlaces izquierdo y derecho de cada nodo mediante recursividad.

### Evidencia

Configuración original:

```text
10 20 30 40 50 60 70 80
```

Configuración invertida:

```text
80 70 60 50 40 30 20 10
```

---

# Funcionalidades adicionales

## A. Consulta por posición ordenada

### Función

Permite recuperar el elemento que ocupa una posición específica dentro del orden natural del árbol.

### Ejemplo

```text
Posición solicitada: 5
Valor obtenido: 50
```

---

## B. Filtrado por intervalo

### Función

Recupera únicamente los valores comprendidos dentro de un rango determinado.

### Ejemplo

```text
Intervalo: [20,60]
Salida: 20 30 40 50 60
```

---

## C. Longitud máxima de recorrido

### Función

Determina el recorrido más extenso posible entre dos nodos del árbol.

### Resultado

```text
Longitud máxima: 5
```

---

## D. Generación dinámica mediante parámetros

### Función

Construye automáticamente un árbol utilizando los valores proporcionados al iniciar el programa.

### Ejemplo de ejecución

```text
15 8 22 4 10 18 30
```

### Resultado observado

```text
4 8 10 15 18 22 30
```

---

# Reflexión final

La implementación permitió comprender con mayor profundidad el comportamiento interno de los árboles binarios de búsqueda y la importancia de la recursividad para resolver problemas relacionados con estructuras jerárquicas.

Además, se reforzaron habilidades relacionadas con depuración, validación de algoritmos, control de versiones mediante Git y organización incremental del desarrollo utilizando commits sucesivos.
