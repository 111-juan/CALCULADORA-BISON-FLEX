
#  Calculadora avanzada con Flex & Bison – Ejercicio 1

Este proyecto implementa una calculadora avanzada con soporte para:
- Variables y asignaciones.
- Comparaciones.
- Estructuras de control (`if`, `while`).
- Funciones definidas por el usuario.
- Funciones internas (`sqrt`, `log`, `exp`, `print`).
- Evaluación de expresiones matemáticas.
- Construcción y evaluación de un Árbol de Sintaxis Abstracta (AST).

## 📌 Objetivo del ejercicio 1

> Modificar la sintaxis de la calculadora para que las estructuras de control sean más intuitivas.  
> En vez de depender de múltiples `;` para cerrar bloques, se agregaron palabras clave de cierre:
- `fi` para cerrar `if`
- `done` para cerrar `while`

Esto mejora la legibilidad y flexibilidad de las listas de sentencias.

---

## 🗂 Estructura de archivos

| Archivo        | Descripción                                                                 |
|----------------|------------------------------------------------------------------------------|
| `fb3-2.h`      | Definiciones de estructuras y funciones para el AST y la tabla de símbolos. |
| `fb3-2func.c`  | Implementación de funciones internas (`sqrt`, `log`, etc.).                  |
| `calc.l`       | Analizador léxico con Flex. Reconoce tokens y palabras clave.               |
| `calc.y`       | Analizador sintáctico con Bison. Define la gramática del lenguaje.          |
| `main.c`       | Función principal que ejecuta el parser.                                    |

---

## ⚙️ Requisitos

- Linux con compilador `gcc`
- `flex` y `bison` instalados

Instálalos (si no los tienes) con:

```bash
sudo apt update
sudo apt install flex bison gcc
