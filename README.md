# Calculadora en Bison y Flex

Este proyecto es una calculadora avanzada desarrollada en **C**, utilizando **Flex** (generador de analizadores léxicos) y **Bison** (generador de analizadores sintácticos). La calculadora permite el uso de variables, funciones, estructuras de control, operadores lógicos y más.

##  Integrantes

- Juan Balaguera  
- Nicolás Garzón  
- Juan Pablo Beltrán  

##  Archivos principales

- `fb3-2.h`: Definiciones de estructuras y funciones usadas en el AST.  
- `fb3-2.l`: Archivo léxico (Flex) que define los tokens.  
- `fb3-2.y`: Archivo sintáctico (Bison) que define la gramática y las acciones.  
- `fb3-2func.c`: Contiene funciones auxiliares necesarias para la ejecución de la calculadora.  

##  Requisitos

Asegúrate de tener instalados en Linux los siguientes paquetes:

```bash
sudo apt update
sudo apt install flex bison gcc build-essential

# Paso 1: Abre la terminal y navega al directorio del proyecto
cd CALCULADORA-BISON-FLEX

# Paso 2: Ejecuta Bison para generar los archivos del parser
bison -d fb3-2.y  # Esto genera fb3-2.tab.c y fb3-2.tab.h

# Paso 3: Ejecuta Flex para generar el analizador léxico
flex fb3-2.l      # Esto genera fb3-2.lex.c

# Paso 4: Compila todo con GCC incluyendo el archivo de funciones
gcc -o  fb3-2.tab.c fb3-2.lex.c fb3-2func.c -lm

# Paso 5: Esto creara un archivo a.out

# Paso 5: Ejecuta la calculadora
./a.out

