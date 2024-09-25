Juan Joya
Juan Gallardo
Jefferson Gutierrez

Descripción General
Este programa es una calculadora simple que utiliza Bison y Flex para analizar y evaluar expresiones matemáticas. Es capaz de realizar operaciones aritméticas básicas como suma, resta, multiplicación y división. Además, maneja errores comunes como la división por cero y expresiones inválidas. 

Requisitos Previos
Antes de ejecutar este programa, debes tener instalados Bison y Flex en tu sistema.

Paso a Paso para Ejecutar el Programa

1. Creación de los Archivos:
   - Crea un archivo llamado calc.y y pega el contenido de la sección correspondiente en este archivo.
   - Crea un archivo llamado calc.l y pega el contenido de la sección correspondiente en este archivo.

2. Generación de Código C:
   - En la terminal, navega al directorio donde guardaste los archivos y ejecuta los siguientes comandos:
   
     bison -d calc.y -b calc
     o
     bison -d calc_INVERSA.y -b calc
     o
     bison -d calc_PARENTESIS.y -b calc
     
     flex calc.l
     gcc calc.tab.c lex.yy.c -o calculadora -lm
     
   - Estos comandos generarán los archivos calc.tab.h, calculadora.tab.c, y lex.yy.c, y luego compilarán todo para crear un ejecutable llamado calculadora.

3. Ejecución del Programa:
   - Para iniciar la calculadora, ejecuta el siguiente comando en la terminal:
     ./calculadora
   - La calculadora estará lista para recibir expresiones matemáticas.

4. Uso del Programa:
   - Escribe cualquier expresión matemática (como 3 + 4 * 2) y presiona Enter. El resultado se mostrará inmediatamente.
   - Para terminar el programa, simplemente presiona Ctrl + C.

Ejemplos de Salida

- Entrada:
  3 + 4 * 2
  Salida:
  Resultado: 11

- Entrada:
  (1 + 2) * (3 + 4)
  Salida:
  Resultado: 21
