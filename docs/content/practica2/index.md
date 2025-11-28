+++
date = '2025-11-27T17:15:17-08:00'
draft = false
title = 'Practica2: Programación Orientada a Objetos'
+++

# **Práctica 2:** Programación Orientada a Objetos

## **1. Explicación de Conceptos de POO**

La Programación Orientada a Objetos es un paradigma que organiza el software en torno a **objetos**, los cuales combinan datos (atributos) y comportamiento (métodos). A continuación, se explican sus pilares fundamentales.

---

## **Clase y Objeto**

Una **clase** es una plantilla o plano para crear objetos. Define los atributos y métodos que los objetos tendrán.  
Un **objeto** es una instancia de una clase; ocupa memoria y puede usar los métodos definidos en su clase.

**Ejemplo:**  
La clase *Libro* define cómo será cualquier libro en el sistema.  
Un objeto como `libro_don_quijote` es una instancia concreta de esa clase con sus propios datos.

---

## **Herencia**

La **herencia** permite que una clase hija obtenga atributos y métodos de una clase base. Esto promueve la reutilización del código.

**Ejemplo:**  
Las clases *Libro* y *Revista* pueden heredar de *ItemBiblioteca*, que contiene atributos como `item_id`, `titulo`, y métodos como `prestar()`.

---

## **Encapsulamiento**

El encapsulamiento agrupa los datos y los métodos dentro de un mismo objeto, restringiendo el acceso directo a los datos internos.

En Python se hace por convención usando `_atributo` como "protegido".

**Ejemplo:**  
En la clase *Biblioteca*, las listas `_items` y `_usuarios` están encapsuladas.  
No se modifican directamente, sino mediante métodos como `agregar_item()` o `prestar_item()`.

---

## **Abstracción**

La abstracción oculta los detalles internos y ofrece solo lo esencial para el usuario.

Una clase abstracta es una clase que no se puede instanciar y sirve como modelo.

**Ejemplo:**  
El usuario solo necesita llamar `mi_biblioteca.prestar_item()`, sin conocer cómo se busca el usuario, el libro o cómo se actualiza el registro.  
La clase *ItemBiblioteca* es abstracta porque no tiene sentido instanciar un “ítem genérico”.

---

## **Polimorfismo**

El polimorfismo permite que distintos objetos respondan al mismo método de forma diferente.

**Ejemplo:**  
Las clases *Libro* y *Revista* tienen el método `mostrar_detalles()`.  
Si recorremos una lista con libros y revistas, al llamar `item.mostrar_detalles()` cada uno ejecuta su propia versión.

---

## **Comparación: Versión en C vs. Versión en Python (POO)**

| **Aspecto** | **En C (estructuras)** | **En Python (POO)** |
|-------------|-------------------------|----------------------|
| Representación | `struct` solo guarda datos | `class` combina datos y métodos |
| Memoria | `malloc` y `free` (manual) | Automática con garbage collector |
| Persistencia | Archivos con `fopen`, `fscanf` | JSON o CSV con `json`, `csv` |
| Abstracción | Funciones sueltas | Métodos en clases |
| Herencia / Polimorfismo | No existe | Clases hijas heredan métodos |
| Encapsulamiento | No hay | Atributos privados `_atributo`, `@property` |
| Interacción | `printf/scanf` | `print/input`, más seguro |

---

## **Conclusiones**

1. La migración de C a Python con POO facilita el diseño, ya que las clases agrupan datos y comportamiento.
2. Python reduce la complejidad al no requerir manejo manual de memoria.
3. La herencia y el polimorfismo permiten extender el sistema sin duplicar código.
4. El encapsulamiento mejora la seguridad y consistencia de los datos.
5. En general, POO ofrece un sistema más claro, mantenible y escalable que la versión en C.

