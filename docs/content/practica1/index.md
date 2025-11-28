+++
date = '2025-11-27T17:15:05-08:00'
draft = false
title = 'Práctica 1: Elementos básicos de los lenguajes de programación'
+++

# **Practica 1:** Elementos básicos de los lenguajes de programación

## Elementos basicos

**Nombres:**\
Los nombres son identificadores que se usan para variables, funciones, y tipos de datos.
- **Variables:** static_var, bss_var, bookCount, choice.
- **Funciones:** addBook, displayBooksRecursive, freeLibrary.
- **Estructuras de datos:** book_t, member_t, genre_t, MemoryRecord.

**Marcos de activacion:**\
Un marco de activación es una estructura en la pila (stack) que se crea al llamar a una función. Almacena las variables locales y los parámetros.
- En la llamada a addBook(&library, &bookCount), se crea un nuevo marco para addBook. Este marco contiene copias de los punteros a library y bookCount, así como un puntero local new_book.

**Bloques de alcance:**\
El alcance define la región del código donde un nombre es válido.
- **Alcance global:** Variables como static_var y heap_allocations se declaran fuera de cualquier función y pueden ser accedidas desde cualquier parte del programa.
- **Alcance local:** La variable new_book en la función addBook solo es accesible dentro de esa función.

**Administracion de memoria:**\
El prograna utiliza varios segmentos de memoria:
- **Stack:** Las variables locales en main, como choice y bookCount, se asignan en la pila. Su administración es automática.
- **Heap:** Se utiliza memoria dinámica con malloc en addBook y addMember para los nodos de las listas enlazadas. Se libera explícitamente con free en freeLibrary y freeMembers para evitar fugas de memoria.
- **Segmento de datos estatico:** static_var es un ejemplo de una variable con vida útil estática.
- **Segmentos BSS:** bss_var es una variable global no inicializada, por lo que reside en este segmento.

**Expresiones:**\
Una expresión es una combinación de operadores, variables y valores que se evalúa a un solo valor.
- sizeof(book_t) calcula el tamaño de la estructura book_t.
- current->id == bookID es una expresión booleana utilizada en una condición.
- (*count)++ incrementa el valor de la variable a la que apunta count.

**Comando:**\
Un comando es una instrucción que le indica a la computadora que realice una acción.
- printf("Ingresa ID del libro: "); imprime un mensaje en la consola.

- scanf("%d", &new_book->id); lee la entrada del usuario.

- return 0; sale de la función main.

- free(current); libera memoria.

**Control de secuencia:**\
Esto se refiere al orden en que se ejecutan los comandos.
- **Seleccion:** La sentencia switch (choice) en main dirige el flujo del programa a diferentes bloques de código.
- **Iteracion:** El bucle do-while en main repite el menú hasta que el usuario elige salir. Los bucles while y for se utilizan para recorrer las listas enlazadas y los arreglos.
- **Recursion:** La función displayBooksRecursive se llama a sí misma para recorrer recursivamente la lista de libros.

**Subprogramas:**\
Los subprogramas son funciones que realizan tareas específicas, lo que promueve la reutilización del código.
- **Funciones:** addBook, issueBook, freeLibrary, saveLibraryToFile, etc., son todas funciones.
- **Parametros:** addBook toma un puntero a un puntero (book_t **library) y un puntero a un entero (int* count) para modificar las variables originales.
- **Valor de entorno:** findBookById devuelve un puntero a una estructura book_t o NULL si no la encuentra.

**Tipos de datos:**\
El programa utiliza varios tipos de datos para representar diferentes tipos de información.
- **Tipos primitivos:** int para IDs, char para arreglos de caracteres, y size_t para tamaños de memoria.
- **Tipos definidos por el usuario:** 

1. enum: La enumeración genre_t define un conjunto de constantes para los géneros de libros.

2. struct: Las estructuras book_t y member_t agrupan datos relacionados.