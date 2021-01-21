---
title: Estructura de datos
date: 2021-01-20T17:01:08-06:00
tags: 
- estructura de datos
- pila
- cola
- arbol
- tabla hash
- grafo
---

Las estructuras de datos son estructuras conformadas en nodo y dato enlazados de tal manera que su búsqueda, inserción o eliminación tenga la mayor eficiencia posible.

## Nodo

Un nodo es aquel que contiene el dato a almacenar y los apuntadores hacia los demás nodos que conforman las estructuras de datos.

```c
typedef struct Nodo {
    Dato dato;
    Nodo *anterior;
    Nodo *siguiente;
} Nodo;
```

## Lista

Una lista contiene nodos y los nodos contienen de 1 a 2 apuntadores hacia los siguientes o anteriores nodos. Los tipos de listas que se conocen, son:

- Lista simple: Es aquella lista en la que sus nodos únicamente tienen apuntadores al siguiente nodo, el siguiente apuntador del último nodo es nulo.

```c
typedef struct Nodo {
    Dato dato;
    Nodo *siguiente;
} Nodo;

typedef struct Lista {
    Nodo *primero;
    Nodo *ultimo;
};
```

- Lista doble: Es aquella lista en la que sus nodos tienen apuntadores al anterior y nodo siguiente, el apuntador anterior del primer nodo es nulo al igual que el nodo siguiente del último nodo.

```c
typedef struct Nodo {
    Dato dato;
    Nodo *anterior;
    Nodo *siguiente;
} Nodo;

typedef struct Lista {
    Nodo *primero;
    Nodo *ultimo;
};
```

- Lista simple circular: Es aquella lista en la que sus nodos tienen apuntadores al siguiente nodo, el último nodo apunta al primer nodo.

```c
typedef struct Nodo {
    Dato dato;
    Nodo *siguiente;
} Nodo;

typedef struct Lista {
    Nodo *primero;
    Nodo *ultimo;
};
```

- Lista doble circular: Es aquella lista en la que sus nodos tienen apuntadores al anterior y nodo siguiente, el último nodo apunta al primer nodo y el primer nodo apunta al último nodo.

```c
typedef struct Nodo {
    Dato dato;
    Nodo *anterior;
    Nodo *siguiente;
} Nodo;

typedef struct Lista {
    Nodo *primero;
    Nodo *ultimo;
};
```

## Pila

Una pila es una lista simple, en donde, la inserción y la extracción de ítems se realiza por el frente.

## Cola

Una cola es una lista simple, en donde, la inserción de ítems se realiza por la cola y la extracción por el frente.

## Árbol

El árbol es una estructura de datos en donde el padre tiene uno o varios hijos y los hijos tienen solamente un padre. Existen varios tipos de árboles, las cuales son:

- Árbol binario: Es el árbol más simple de todos en donde no importa el orden en que se inserten los ítems, los nodos de dicho árbol tienen 2 apuntadores hacia los nodos hijos.
- Árbol AVL: Al contrario del árbol binario, en este árbol sí importa el orden de inserción de los ítems, los nodos también tienen 2 apuntadores hacia los nodos hijos.
- Árbol B: Es el árbol más complejo de todos, pues cada nodo tiene un arreglo de ítems y uno de apuntadores, en donde cada ítem tiene 2 apuntadores hacia los nodos hijos.
- Árbol B*: Es el mismo árbol B, pero cada hijo se encuentra enlazado a sus primos para un recorrido más óptimo.
- Árbol Rojo-Negro: Es un árbol en donde los nodos tienen el color rojo y negro para mantener un equilibrio en el árbol.

## Grafo

Un grafo es un conjunto de nodos entrelazados entre sí, el cual, dichos enlaces tienen peso, con dicho peso, se puede determinar la ruta rápida hacia determinado nodo.

## Tabla Hash

La tabla hash es un arreglo de n ítems, las cuales, tienen un par de clave-valor.
