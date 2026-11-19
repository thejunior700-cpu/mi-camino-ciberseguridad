# Python – input, int y mi primera calculadora

**Fecha:** 18 de noviembre de 2026
**Recurso:** Intérprete de Python (python3)

## input() — pedir datos
Seguí practicando con `input()`, que hace que el programa te pida un
dato. Siempre lo guarda como texto.

Primero lo usé para que me preguntara mi nombre:

    nombre = input("Como te llamas? ")
    print("Hola, " + nombre)

Escribí mi nombre y el programa me saludó.

## El error de texto vs número
Después probé pedir un número y sumarle 10:

    numero = input("Escribe un numero: ")
    print(numero + 10)

Escribí 5, pero Python lo tomó como **texto** (porque todo lo que
viene de `input` es texto). Al intentar sumarle 10 (un número), me
saltó este error:

    TypeError: can only concatenate str (not "int") to str

Eso significa: "solo puedo unir texto con texto, no puedo sumar
texto con un número".

## int() — arreglar el error
Para arreglarlo usé `int()`, que convierte el texto en número entero:

    numero = int(input("Escribe un numero: "))
    print(numero + 10)

Con eso Python ya tomó el 5 como número de verdad, y la suma
funcionó (dio 15).

## Mi calculadora
Después hice una calculadora que hace operaciones con dos números.
Usé `int()` para que los tomara como números:

    a = int(input("Primer numero: "))
    b = int(input("Segundo numero: "))
    print("Suma:", a + b)
    print("Resta:", a - b)
    print("Multiplicacion:", a * b)
    print("Division:", a / b)

Puse 7 y 11, e hice que sumara, restara, multiplicara y dividiera.

## Lo que aprendí
- `input()` siempre guarda lo que escribís como texto.
- Para hacer cuentas hay que convertir con `int()` (entero) o
  `float()` (decimales).
- Operadores: `+` suma, `-` resta, `*` multiplicación, `/` división
  (siempre da decimal).
- Leer el error (TypeError) me ayudó a entender qué estaba mal y
  arreglarlo.

## Glosario
- *input()* = pedir un dato al usuario (lo guarda como texto)
- *int()* = convertir a número entero
- *float()* = convertir a número con decimales
- *TypeError* = error de tipo (ej. mezclar texto y número)
