# Python – Condicionales (if, elif, else)

**Fecha:** 24 de noviembre de 2026
**Recurso:** Intérprete de Python (python3)

## Qué aprendí
Hoy avanzamos para que un programa empiece a **tomar decisiones**.
Antes, la calculadora solo me daba un resultado; ahora el programa
decide qué hacer según los datos que le dé.

(Nota: `if`, `elif` y `else` no son comandos, son **instrucciones**
o palabras clave de Python.)

## if / else
Hacen que el programa tome decisiones. Si se cumple una condición,
hace una cosa; si no, hace otra.

## elif (else if)
Para un caso del medio: cuando no es ni lo primero ni lo último.

## Operadores de comparación
- `==` → igual a (con DOS iguales)
- `!=` → distinto (signo de exclamación + igual)
- `<` menor, `>` mayor, `<=` menor o igual, `>=` mayor o igual

### El detalle del igual
- `=` (uno solo) → asigna una variable
- `==` (dos) → compara

Confundirlos es un error típico.

## La sangría (indentación)
Lo que va dentro del `if` va con espacios adelante (Tab). Si NO los
pongo, salta un error (`IndentationError`).

## El ejemplo que hice
Un mini-detector de intentos de login fallidos:

    intentos = int(input("Cuantos intentos de login fallidos? "))
    if intentos == 0:
        print("Todo normal")
    elif intentos < 5:
        print("Vigilar la cuenta")
    else:
        print("Alerta: posible ataque de fuerza bruta")

## Glosario
- *if / else* = si / si no
- *elif* = caso del medio (si no, y además)
- *== / !=* = igual a / distinto de
- *indentación (sangría)* = espacios al inicio que marcan qué va dentro del if
- *fuerza bruta* = cuando un atacante prueba muchas contraseñas hasta acertar
