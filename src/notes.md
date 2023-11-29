
# Ownership

## Intro

- Mecanismo que le permite a Rust ser memory safe sin necesidad de tener GC

## A grounded conceptual

- Esto es basado en un articulo de Will Chrichton.
- La idea principal es que para enseñar Rust necesitamos no solo mostrar como funciona ownership sino también por qué funciona

## Que es safety

### Programa safe

- Primero mostrar un programa safe.
- Tenemos una idea intuitiva de como va a ejecutar el programa.
- De forma concreta, el programa compila a assembly

### Programa unsafe

- Un programa medio artificial.
- Supongamos que lo podemos compilar.
- El programa correría de todas formas.
- Comprararlo con lenguaje dinámico.
- Afortunadamente no compila.
- UB es especialmente complicada cuando lidiamos con memoria y punteros.

## Stack

- Para entender los problemas con memory safety, necesitamos entender como rust maneja la memoria.
- Al leer una variable el valor se copia
- Copiar puede ser caro

## Heap

- Box se usa para poner cosas en el heap
- Variable guarda un puntero a la memoria
- Cuando la copiamos no se copia todo el contenido sino que solo el puntero
- Rust no deja liberar la memoria manualmente

## Box deallocation

- Si hay una Box guardada en una variable, al liberar el stack frame se libera la memoria
- Esto puede causar problemas si se copia la box
- Introducir ownership.
  - Solo hay un dueño
  - La propiedad se transfiere
  - Solo se libera la memoria cuando el stack frame de la variable que es dueña de la memoria se libera.

## Colecciones

- Continuando con la idea
- Las colecciones como vec, string, o hashmap son como las boxes y tambien representan ownership.
- Cuando uno las mueve se mueve su ownership
- Al hacer push se move la memoria

## Move

- Ups, que pasa si usamos la variable
- Contrastar con C++ move semantics
- En rust no compila
- una solución es clonar

## Summary

- leer de la slide
- pausa para preguntas

## Borrowing Motivation

- go through program -> compile and
- some solution -> return ownership back -> yikes

## References

- la solucion de rust a estos problemas son referencias

## Dereference

- explicar cada paso

## Vec

- mostrar que tiene capacidad

## Aliasing

-
