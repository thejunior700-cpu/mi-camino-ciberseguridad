# Python – Primeros pasos (print, variables, operaciones)

**Fecha:** 16 de noviembre de 2026
**Recurso:** Intérprete de Python (Python 3.9.6)

---

## Qué es Python y por qué lo aprendo
Python es un lenguaje de programación muy usado en ciberseguridad para
automatizar tareas: revisar logs, procesar datos, escribir scripts que
prueban cosas. No hace falta ser experto, pero lo básico da mucha
ventaja a un analista.

## El intérprete interactivo
Escribiendo `python3` en la terminal entro al intérprete: un modo
donde escribo código y veo el resultado al instante. El prompt cambia
a `>>>`. Para salir: `exit()` o Ctrl+D.

---

## Lo que aprendí

### print() — mostrar en pantalla
Muestra lo que le paso entre paréntesis.

    print("Hola, estoy aprendiendo Python")

### Variables — cajitas con nombre
Una variable guarda un valor con un nombre para reutilizarlo.

    usuario = "admin"
    print(usuario)        # muestra: admin

### Concatenar textos con +
El signo `+` une (concatena) textos.

    print("Usuario conectado: " + usuario)
    # muestra: Usuario conectado: admin

### Operaciones con números
Con números SIN comillas, Python hace la cuenta.

    print(5 + 3)     # 8
    print(10 * 2)    # 20

---

## Concepto clave: texto vs. número
- **Con comillas** → es texto (string). Ej: `"5"` es el carácter cinco.
- **Sin comillas** → es número. Ej: `5` es el valor cinco.

Por eso `"5" + "3"` daría `"53"` (une textos), pero `5 + 3` da `8`
(suma números). Confundir estos dos es un error muy común al empezar.

## Glosario
- *print* = mostrar en pantalla
- *variable* = un nombre que guarda un valor
- *string* = texto (va entre comillas)
- *concatenar* = unir textos con +
- *intérprete interactivo* = modo donde escribo código y veo el
  resultado al instante (prompt `>>>`)
