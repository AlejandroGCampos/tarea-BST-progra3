# Tarea BST - Programación 3

## Información General

**Curso:** Programación 3
**Tema:** Árbol Binario de Búsqueda (BST)
**Estudiante:** Alejandro Godoy Campos

---

## Descripción

Este proyecto consiste en la implementación de un Árbol Binario de Búsqueda (BST) desarrollado en Java sin utilizar estructuras de datos de `java.util` ni librerías externas.

Además de las operaciones básicas proporcionadas en el proyecto base, se implementaron los cinco problemas solicitados en la tarea y los cuatro ejercicios extra.

---

## Estructura del Proyecto

```text
arboles/
├── pom.xml
├── README.md
├── evidencias/
└── src/main/java/umg/edu/progra/arboles/
    ├── Nodo.java
    ├── ArbolBinarioBusqueda.java
    └── Principal.java
```

---

## Compilación

Desde la raíz del proyecto ejecutar:

```bash
mvn compile
```

---

## Ejecución

```bash
java -cp target/classes umg.edu.progra.arboles.Principal
```

Para probar el ejercicio extra E4:

```bash
java -cp target/classes umg.edu.progra.arboles.Principal 50 30 70 20 40 60 80
```

---

# Problemas Implementados

## Problema 1 - Contar nodos recursivamente

### Método

```java
public int contarNodos()
```

### Descripción

Cuenta recursivamente la cantidad total de nodos del árbol sin utilizar el atributo `tamanio`.

### Ejemplo

```text
Tamanio: 8
Contar nodos (recursivo): 8

Tamanio final: 5
Contar nodos (recursivo): 5
```

---

## Problema 2 - Árbol balanceado

### Método

```java
public boolean esBalanceado()
```

### Descripción

Verifica que para cada nodo la diferencia de alturas entre los subárboles izquierdo y derecho sea menor o igual a 1.

### Ejemplo

```text
Arbol principal balanceado?: true

Arbol desbalanceado balanceado?: false
```

---

## Problema 3 - Validar BST

### Método

```java
public boolean esBSTValido()
```

### Descripción

Comprueba que todos los nodos cumplan la propiedad fundamental de un BST utilizando límites mínimos y máximos durante el recorrido recursivo.

### Ejemplo

```text
Arbol principal es BST valido?: true

Arbol roto es BST valido?: false
```

---

## Problema 4 - Ancestro Común Más Bajo (LCA)

### Método

```java
public int ancestroComunMasBajo(int a, int b)
```

### Descripción

Determina el ancestro común más bajo de dos valores aprovechando la propiedad del BST.

### Ejemplo

```text
LCA(10, 40): 30
LCA(10, 80): 50
LCA(60, 80): 70
```

---

## Problema 5 - Invertir Árbol

### Método

```java
public void invertir()
```

### Descripción

Realiza el reflejo (espejo) del árbol intercambiando los hijos izquierdo y derecho de todos los nodos.

### Ejemplo

```text
Antes:
10 20 30 40 50 60 70 80

Despues:
80 70 60 50 40 30 20 10
```

---

# Ejercicios Extra

## E1 - K-ésimo menor

### Método

```java
public int kEsimoMenor(int k)
```

Devuelve el k-ésimo elemento más pequeño utilizando un recorrido InOrden.

### Ejemplo

```text
Primer menor : 10
Tercer menor : 30
Quinto menor : 50
Octavo menor : 80
```

---

## E2 - Impresión por rango

### Método

```java
public void imprimirRangoOrdenado(int min, int max)
```

Imprime únicamente los valores comprendidos dentro de un intervalo dado.

### Ejemplo

```text
30 40 50 60
```

---

## E3 - Diámetro del árbol

### Método

```java
public int diametro()
```

Calcula la longitud máxima del camino entre dos nodos del árbol.

### Ejemplo

```text
Diametro calculado: 5
```

---

## E4 - Construcción desde argumentos

Permite construir un BST utilizando los valores enviados desde la línea de comandos.

### Ejemplo

```bash
java Principal 50 30 70 20 40 60 80
```

Salida:

```text
Valores ordenados con InOrden:
20 30 40 50 60 70 80
```

---

# Evidencias

Las capturas de ejecución utilizadas para demostrar cada problema y ejercicio extra se encuentran en la carpeta:

```text
evidencias/
```

---

# Historial de Desarrollo

Se utilizó control de versiones mediante Git con commits descriptivos para cada problema y ejercicio implementado.

Ejemplos:

```text
chore: proyecto base BST proporcionado por el curso
feat: solucion a problema 1 contarNodos recursivo feat:
solucion a problema 2 verificar balanceo BST feat:
solucion a problema 3 verificar esBSTValido feat:
solucion a problema 4 ancestroComunMasBajo feat:
solucion a problema 5 invertirRecursivo feat: solucion a
problemas Extra 1, 2 y 3 feat: solucion a problemas Extra 4
```
