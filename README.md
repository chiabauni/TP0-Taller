# Taller de Programación I - TP0
## Chiara Bauni 102981
## https://github.com/chiabauni/TP0

### Paso 0: Entorno de Trabajo

a)Primero compilo y ejecuto una aplicación simple ISO C que imprima por pantalla el mensaje“Hola Mundo” y finalice retornando 0 (cero). A continuación se encuntra la ejecución de dicha aplicación con y sin Valgrind:
![paso0](https://github.com/chiabauni/TP0/blob/main/paso0.png)

b)¿Para qué sirve Valgrind?¿Cuáles son sus opciones más comunes? 
Valgrind nos permite usar distintas herramientas a la hora de revisar el uso de memoria de nuestro código. Una de las herramienta es hacer chequeos de memoria en el programa y nos avisa si hay o no pérdida de memoria y por ende si estamos liberando la memoria dinámica utilizada correctamente. Tambien nos permite saber si estamos haciendo un correcto uso de la memoria a nuestra disposición.**Chequear respuestaaa**

c)¿Qué respresenta el sizeof()?¿Cuál sería el valor de salida de sizeof(char) y sizeof(int)? El sizeof() respresenta la cantidad de bytes que ocupa el tipo de dato que se encuntra entre parentesis. El valor de salida de sizeof() varia segun el compilador y la plataforma que estemos utilizando. EN nuestro caso utilizando gcc obtenemos que sizeof(char)=1 y sizeof(int)=4.

d)¿El sizeof() de una struct de C es igual a la suma del sizeof() de cada uno sus elementos? Justifique mediante un ejemplo. No necesariamente, puede ocurrir que el sizeof() de una struct de C sea mayor a la suma del sizeof() de cada uno sus elementos. Lo podemos ver en el siguiente ejemplo:
![paso0_1](https://github.com/chiabauni/TP0/blob/main/paso0_2.png)
![paso0_2](https://github.com/chiabauni/TP0/blob/main/paso0_1.png)

Por lo que podemos concluir que el sizeof() de una struct de C es mayor o igual a la suma del sizeof() de cada uno sus elementos.

e)Investigar la existencia de los archivos estándar: STDIN, STDOUT, STDERR. Explicar brevemente su uso y cómo redirigirlos en caso de ser necesario (caracteres > y <) y comoconectar la salida estándar de un proceso a la entrada estándar de otro con un pipe (carácter|).
**Agregar esta respuesta**


### Paso 1: SERCOM - Errores de generación y normas de programación
a. A continuación mostramos los problemas de estilo detectados por el SERCOM: 
```
Verificando el codigo...

/task/student//source_unsafe/paso1_wordscounter.c:27:  Missing space before ( in while(  [whitespace/parens] [5]
/task/student//source_unsafe/paso1_wordscounter.c:41:  Mismatching spaces inside () in if  [whitespace/parens] [5]
/task/student//source_unsafe/paso1_wordscounter.c:41:  Should have zero or one spaces inside ( and ) in if  [whitespace/parens] [5]
/task/student//source_unsafe/paso1_wordscounter.c:47:  An else should appear on the same line as the preceding }  [whitespace/newline] [4]
/task/student//source_unsafe/paso1_wordscounter.c:47:  If an else has a brace on one side, it should have it on both  [readability/braces] [5]
/task/student//source_unsafe/paso1_wordscounter.c:48:  Missing space before ( in if(  [whitespace/parens] [5]
/task/student//source_unsafe/paso1_wordscounter.c:53:  Extra space before last semicolon. If this should be an empty statement, use {} instead.  [whitespace/semicolon] [5]
/task/student//source_unsafe/paso1_wordscounter.h:5:  Lines should be <= 80 characters long  [whitespace/line_length] [2]
/task/student//source_unsafe/paso1_main.c:12:  Almost always, snprintf is better than strcpy  [runtime/printf] [4]
/task/student//source_unsafe/paso1_main.c:15:  An else should appear on the same line as the preceding }  [whitespace/newline] [4]
/task/student//source_unsafe/paso1_main.c:15:  If an else has a brace on one side, it should have it on both  [readability/braces] [5]
Done processing /task/student//source_unsafe/paso1_wordscounter.c
Done processing /task/student//source_unsafe/paso1_wordscounter.h
Done processing /task/student//source_unsafe/paso1_main.c
Total errors found: 11
```
1. Problema en la linea 27 del documento paso1_wordscounter.c hace la siguiente corrección:
![1](https://github.com/chiabauni/TP0/blob/main/1.png)
2. Problema en la linea 41 del documento paso1_wordscounter.c hace la siguiente corrección:
![2](https://github.com/chiabauni/TP0/blob/main/2.png)
3. Problema en la linea 47 del documento paso1_wordscounter.c hace la siguiente corrección:
![3](https://github.com/chiabauni/TP0/blob/main/3.png)
4. Problema en la linea 48 del documento paso1_wordscounter.c hace la siguiente corrección:
![4](https://github.com/chiabauni/TP0/blob/main/4.png)
5. Problema en la linea 53 del documento paso1_wordscounter.c hace la siguiente corrección:
![5](https://github.com/chiabauni/TP0/blob/main/5.png)
6. Problema en la linea 5 del documento paso1_wordscounter.h hace la siguiente corrección:
![6](https://github.com/chiabauni/TP0/blob/main/6.png)
7. Problema en la linea 12 del documento paso1_main.c hace la siguiente corrección:
![7](https://github.com/chiabauni/TP0/blob/main/7.png)
8. Problema en la linea 15 del documento paso1_main.c hace la siguiente corrección:
![8](https://github.com/chiabauni/TP0/blob/main/8.png)

b. A continuación mostramos los errores de generación del ejecutable detectados por el SERCOM: 
```
Desempaquetando y compilando el codigo...
Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso1_main.c
  inflating: source_unsafe/paso1_wordscounter.c
  inflating: source_unsafe/paso1_wordscounter.h
Compilando el codigo...
  CC  paso1_main.o
paso1_main.c: In function ‘main’:
paso1_main.c:22:9: error: unknown type name ‘wordscounter_t’
   22 |         wordscounter_t counter;
      |         ^~~~~~~~~~~~~~
paso1_main.c:23:9: error: implicit declaration of function ‘wordscounter_create’ [-Wimplicit-function-declaration]
   23 |         wordscounter_create(&counter);
      |         ^~~~~~~~~~~~~~~~~~~
paso1_main.c:24:9: error: implicit declaration of function ‘wordscounter_process’ [-Wimplicit-function-declaration]
   24 |         wordscounter_process(&counter, input);
      |         ^~~~~~~~~~~~~~~~~~~~
paso1_main.c:25:24: error: implicit declaration of function ‘wordscounter_get_words’ [-Wimplicit-function-declaration]
   25 |         size_t words = wordscounter_get_words(&counter);
      |                        ^~~~~~~~~~~~~~~~~~~~~~
paso1_main.c:27:9: error: implicit declaration of function ‘wordscounter_destroy’ [-Wimplicit-function-declaration]
   27 |         wordscounter_destroy(&counter);
      |         ^~~~~~~~~~~~~~~~~~~~
make: *** [<builtin>: paso1_main.o] Error 1

real    0m0.046s
user    0m0.013s
sys     0m0.017s
[Error] Fallo la compilacion del codigo en 'source_unsafe.zip'. Codigo de error 2
```
El compilador tiene toda la informacion para generar codigo objeto pero no puede validarlo por que no se incluyo el archivo .h con las firmas de las funciones y declaraciones de las estructuras en el main.c. Esto provoca que el compilador no sepa que el struct wordscounter_t existe o si es un typo del programador(Error:"error: unknown type name ‘wordscounter_t’"). Tampoco sabe que las funciones wordscounter_create(), wordscounter_process(), wordscounter_get_words(), wordscounter_destroy() existen y cuantos argumentos reciben y cuales son sus tipos(Error:"implicit declaration of function ‘funcion’").
Sin la informacion brindada por el .h el compilador no puede chequear la sintaxis del codigo y por lo tanto tendremos estos errores.

c.**¿El sistema reportó algún WARNING? ¿Por qué?**

### Paso 2: SERCOM - Errores de generación 2

a. Las correcciones realizadas respecto a la versión anterior son:
* Se corrigieron todos los problemas de estilo detectados en el paso 1.
* Se incluyo el "paso2_wordscounter.h" en el main del paso 2.
* El tipo wordscounter_t paso de almacenar la cantidad de palabras procesadas de un archivo en el paso 1 a procesar cantidad de palabras dentro de un archivo en el paso 2.

b. A continuación mostramos la correcta ejecución de la verificación de estilo de programación detectados por el SERCOM:
```
Verificando el codigo...

Done processing /task/student//source_unsafe/paso2_wordscounter.c
Done processing /task/student//source_unsafe/paso2_main.c
Done processing /task/student//source_unsafe/paso2_wordscounter.h
```

c. A continuación mostramos los errores de generación del ejecutable detectados por el SERCOM: 
```
Desempaquetando y compilando el codigo...

Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso2_main.c
  inflating: source_unsafe/paso2_wordscounter.c
  inflating: source_unsafe/paso2_wordscounter.h
Compilando el codigo...
  CC  paso2_wordscounter.o
In file included from paso2_wordscounter.c:1:
paso2_wordscounter.h:7:5: error: unknown type name ‘size_t’
    7 |     size_t words;
      |     ^~~~~~
paso2_wordscounter.h:20:1: error: unknown type name ‘size_t’
   20 | size_t wordscounter_get_words(wordscounter_t *self);
      | ^~~~~~
paso2_wordscounter.h:1:1: note: ‘size_t’ is defined in header ‘<stddef.h>’; did you forget to ‘#include <stddef.h>’?
  +++ |+#include <stddef.h>
    1 | #ifndef __WORDSCOUNTER_H__
paso2_wordscounter.h:25:49: error: unknown type name ‘FILE’
   25 | void wordscounter_process(wordscounter_t *self, FILE *text_file);
      |                                                 ^~~~
paso2_wordscounter.h:1:1: note: ‘FILE’ is defined in header ‘<stdio.h>’; did you forget to ‘#include <stdio.h>’?
  +++ |+#include <stdio.h>
    1 | #ifndef __WORDSCOUNTER_H__
paso2_wordscounter.c:17:8: error: conflicting types for ‘wordscounter_get_words’
   17 | size_t wordscounter_get_words(wordscounter_t *self) {
      |        ^~~~~~~~~~~~~~~~~~~~~~
In file included from paso2_wordscounter.c:1:
paso2_wordscounter.h:20:8: note: previous declaration of ‘wordscounter_get_words’ was here
   20 | size_t wordscounter_get_words(wordscounter_t *self);
      |        ^~~~~~~~~~~~~~~~~~~~~~
paso2_wordscounter.c: In function ‘wordscounter_next_state’:
paso2_wordscounter.c:30:25: error: implicit declaration of function ‘malloc’ [-Wimplicit-function-declaration]
   30 |     char* delim_words = malloc(7 * sizeof(char));
      |                         ^~~~~~
paso2_wordscounter.c:30:25: error: incompatible implicit declaration of built-in function ‘malloc’ [-Werror]
paso2_wordscounter.c:5:1: note: include ‘<stdlib.h>’ or provide a declaration of ‘malloc’
    4 | #include <stdbool.h>
  +++ |+#include <stdlib.h>
    5 |
cc1: all warnings being treated as errors
make: *** [<builtin>: paso2_wordscounter.o] Error 1

real    0m0.232s
user    0m0.035s
sys     0m0.038s
[Error] Fallo la compilacion del codigo en 'source_unsafe.zip'. Codigo de error 2
```
El linker genera en el archivo "paso2_wordscounter.h" los errores "unknown type name ‘size_t’" ya que la definicion de "size_t" se encuentra en la biblioteca <stddef.h> y esta no fue incluida en el archivo .h; tambien genera "unknown type name ‘FILE’" ya que la definicion de "FILE" se encuentra en la biblioteca <stdio.h> y esta no fue incluida en el archivo .h. Ademas el linker genera en el archivo "paso2_wordscounter.c" los errores "implicit declaration of function ‘malloc’" y "incompatible implicit declaration of built-in function ‘malloc’" esto se debe a que la declaracion y definicion de esta funcion se encuntran en la libreria <stdlib.h> la cual no esta incluida en el archivo. Finalmente el linker genera el error "conflicting types for ‘wordscounter_get_words’" **EXPLICAR DE DONDE SALE ESTE ERROR**.


### Paso 3: SERCOM - Errores de generación 3

a. Las correcciones realizadas respecto a la versión anterior son:
* Se incluye en el archivo paso3_wordscounter.h las bibliotecas: <string.h> <stdio.h>.
* Se incluye en el archivo paso3_wordscounter.c la biblioteca: <stdlib.h>.

b. A continuación mostramos los errores de generación del ejecutable detectados por el SERCOM: 
```
Desempaquetando y compilando el codigo...

Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso3_main.c
  inflating: source_unsafe/paso3_wordscounter.c
  inflating: source_unsafe/paso3_wordscounter.h
Compilando el codigo...
  CC  paso3_wordscounter.o
  CC  paso3_main.o
  LD  tp
/usr/bin/ld: paso3_main.o: in function `main':
/task/student/source_unsafe/paso3_main.c:27: undefined reference to `wordscounter_destroy'
collect2: error: ld returned 1 exit status
make: *** [/task/student/MakefileTP0:142: tp] Error 1

real    0m0.546s
user    0m0.184s
sys     0m0.087s
[Error] Fallo la compilacion del codigo en 'source_unsafe.zip'. Codigo de error 2

Verificando el codigo...

Done processing /task/student//source_unsafe/paso3_main.c
Done processing /task/student//source_unsafe/paso3_wordscounter.c
Done processing /task/student//source_unsafe/paso3_wordscounter.h
```
El linker genera en el archivo "paso3_main.o" el error "undefined reference to 'wordscounter_destroy'" esto se debe a que la funcion 'wordscounter_destroy' esta declarada en el archivo "paso3_wordscounter.h" pero no esta definida en el archivo "paso3_wordscounter.c" lo que genera un error a la hora de linkear la firma con la definicion(ya que esta ultima no existe). 


### Paso 4: SERCOM - Memory Leaks y Buffer Overflows
a. Las correcciones realizadas respecto a la versión anterior son:
* Se agrega al archivo "paso4_wordscounter.c" del paso4 la definicion de la funcion 'wordscounter_destroy'.

b. A continuación mostramos los errores detectados por Valgrind de la prueba "TDA" detectados por el SERCOM: 
```
[=>] Executando el caso '/task/student//cases/tda' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_tda.txt

real    0m1.117s
user    0m0.944s
sys     0m0.109s

==00:00:00:00.000 59== Memcheck, a memory error detector
==00:00:00:00.000 59== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==00:00:00:00.000 59== Using Valgrind-3.15.0 and LibVEX; rerun with -h for copyright info
==00:00:00:00.000 59== Command: ./tp input_tda.txt
==00:00:00:00.000 59== Parent PID: 58
==00:00:00:00.000 59==
==00:00:00:01.079 59==
==00:00:00:01.079 59== FILE DESCRIPTORS: 5 open at exit.
==00:00:00:01.079 59== Open file descriptor 4: input_tda.txt
==00:00:00:01.079 59==    at 0x495FEAB: open (open64.c:48)
==00:00:00:01.079 59==    by 0x48E2195: _IO_file_open (fileops.c:189)
==00:00:00:01.079 59==    by 0x48E2459: _IO_file_fopen@@GLIBC_2.2.5 (fileops.c:281)
==00:00:00:01.079 59==    by 0x48D4B0D: __fopen_internal (iofopen.c:75)
==00:00:00:01.079 59==    by 0x48D4B0D: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.079 59==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.079 59==
==00:00:00:01.079 59== Open file descriptor 3: /task/student/cases/tda/__valgrind__
==00:00:00:01.079 59==    <inherited from parent>
==00:00:00:01.079 59==
==00:00:00:01.079 59== Open file descriptor 2: /task/student/cases/tda/__stderr__
==00:00:00:01.079 59==    <inherited from parent>
==00:00:00:01.079 59==
==00:00:00:01.079 59== Open file descriptor 1: /task/student/cases/tda/__stdout__
==00:00:00:01.079 59==    <inherited from parent>
==00:00:00:01.079 59==
==00:00:00:01.079 59== Open file descriptor 0: /task/student/cases/tda/__stdin__
==00:00:00:01.079 59==    <inherited from parent>
==00:00:00:01.079 59==
==00:00:00:01.079 59==
==00:00:00:01.079 59== HEAP SUMMARY:
==00:00:00:01.079 59==     in use at exit: 1,977 bytes in 216 blocks
==00:00:00:01.079 59==   total heap usage: 218 allocs, 2 frees, 10,169 bytes allocated
==00:00:00:01.079 59==
==00:00:00:01.080 59== 472 bytes in 1 blocks are still reachable in loss record 1 of 2
==00:00:00:01.080 59==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.080 59==    by 0x48D4AAD: __fopen_internal (iofopen.c:65)
==00:00:00:01.080 59==    by 0x48D4AAD: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.080 59==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.080 59==
==00:00:00:01.080 59== 1,505 bytes in 215 blocks are definitely lost in loss record 2 of 2
==00:00:00:01.080 59==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.080 59==    by 0x109301: wordscounter_next_state (paso4_wordscounter.c:35)
==00:00:00:01.080 59==    by 0x1093B5: wordscounter_process (paso4_wordscounter.c:30)
==00:00:00:01.080 59==    by 0x109197: main (paso4_main.c:24)
==00:00:00:01.080 59==
==00:00:00:01.080 59== LEAK SUMMARY:
==00:00:00:01.080 59==    definitely lost: 1,505 bytes in 215 blocks
==00:00:00:01.080 59==    indirectly lost: 0 bytes in 0 blocks
==00:00:00:01.080 59==      possibly lost: 0 bytes in 0 blocks
==00:00:00:01.080 59==    still reachable: 472 bytes in 1 blocks
==00:00:00:01.080 59==         suppressed: 0 bytes in 0 blocks
==00:00:00:01.080 59==
==00:00:00:01.080 59== For lists of detected and suppressed errors, rerun with: -s
==00:00:00:01.080 59== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)
```
En esta prueba podemos ver que hay dos errores que generan que se pierda memoria, vemos que de las 218 veces que resevamos memoria unicamente se liberó 2 veces memoria. Por un lado tenemos 472 bytes en 1 bloque que son perdida y en el Heap Summary vemos que ese error se encuentra en la linea 14 del archivo "paso4_main.c". En esta linea encontramos "input = fopen(filepath, "r");" el error surge al no incluir luego de esta linea un "fclose(input)" para cerrar el archivo y no perder memoria. Luego, tenemos que 1,505 en 215 bloques se pierden y en el Heap Summary vemos que ese error se encuentra en la linea 35 del archivo "paso4_wordscounter.c". En esta linea encontramos "char* delim_words = malloc(7 * sizeof(char));" el error surge al no liberar la memoria reservada con "free(delim_words)" al no liberar la memoria pedida por el malloc, se genera una enorme perdidad de memoria.

c. A continuación mostramos los errores detectados por Valgrind de la prueba "Long Filename" detectados por el SERCOM:

```
[=>] Executando el caso '/task/student//cases/nombre_largo' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_extremely_long_filename.txt

real    0m1.091s
user    0m0.895s
sys     0m0.133s

**00:00:00:01.033 47** *** memcpy_chk: buffer overflow detected ***: program terminated
==00:00:00:00.000 47== Memcheck, a memory error detector
==00:00:00:00.000 47== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==00:00:00:00.000 47== Using Valgrind-3.15.0 and LibVEX; rerun with -h for copyright info
==00:00:00:00.000 47== Command: ./tp input_extremely_long_filename.txt
==00:00:00:00.000 47== Parent PID: 46
==00:00:00:00.000 47==
**00:00:00:01.033 47** *** memcpy_chk: buffer overflow detected ***: program terminated
==00:00:00:01.033 47==    at 0x483E9CC: ??? (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.033 47==    by 0x4843C0A: __memcpy_chk (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.033 47==    by 0x109168: memcpy (string_fortified.h:34)
==00:00:00:01.033 47==    by 0x109168: main (paso4_main.c:13)
==00:00:00:01.056 47==
==00:00:00:01.056 47== FILE DESCRIPTORS: 4 open at exit.
==00:00:00:01.056 47== Open file descriptor 3: /task/student/cases/nombre_largo/__valgrind__
==00:00:00:01.056 47==    <inherited from parent>
==00:00:00:01.056 47==
==00:00:00:01.056 47== Open file descriptor 2: /task/student/cases/nombre_largo/__stderr__
==00:00:00:01.056 47==    <inherited from parent>
==00:00:00:01.056 47==
==00:00:00:01.056 47== Open file descriptor 1: /task/student/cases/nombre_largo/__stdout__
==00:00:00:01.056 47==    <inherited from parent>
==00:00:00:01.056 47==
==00:00:00:01.056 47== Open file descriptor 0: /task/student/cases/nombre_largo/__stdin__
==00:00:00:01.056 47==    <inherited from parent>
==00:00:00:01.056 47==
==00:00:00:01.057 47==
==00:00:00:01.057 47== HEAP SUMMARY:
==00:00:00:01.057 47==     in use at exit: 0 bytes in 0 blocks
==00:00:00:01.057 47==   total heap usage: 0 allocs, 0 frees, 0 bytes allocated
==00:00:00:01.057 47==
==00:00:00:01.057 47== All heap blocks were freed -- no leaks are possible
==00:00:00:01.057 47==
==00:00:00:01.057 47== For lists of detected and suppressed errors, rerun with: -s
==00:00:00:01.057 47== ERROR SUMMARY: 0 errors from 0 contexts (suppressed: 0 from 0)
```
En este caso vemos que no hay ninguna perdida de memoria, pero si hay un error: buffer overflow. Esto se debe a la linea 13 del archivo "paso4_main.c" donde encontramos "memcpy(filepath, argv[1], strlen(argv[1]) + 1);". La funcion memcpy sirve para copiar los bytes de la ubicación apuntada por la argv[1] directamente al bloque de memoria apuntado por filepath. El problema que puede surgir al utilizar esta funcion es que el buffer fuente puede llegar a tener un tamaño mayor que el buffer de destino y asi generar un overflow.

d.¿Podría solucionarse este error utilizando la función strncpy? ¿Qué hubiera ocurrido con la ejecución de la prueba?

e.Explicar de qué se trata un segmentation fault y un buffer overflow.



### Paso 5: SERCOM - Código de retorno y salida estándar

a. Las correcciones realizadas respecto a la versión anterior son:
* Se quita el memcpy dejando unicamente la funcion fopen.
* Se agrega la funcion fclose(dentro de un if) para abrir y cerrar correctamente los archivos.
* Se elimina el malloc para guardar memoria para un vector con los delimitadores de palabras y se remplaza por un const char* con las puntuaciones.

b. A continuación mostramos los errores detectados de la prueba "Invalid File" y "Single Word" detectados por el SERCOM: 
```
Desempaquetando los casos publicos...
Executando los casos publicos (sin valgrind)...

[=>] Executando el caso '/task/student//cases/archivo_invalido' (sin valgrind)...
[=>] Command line: ./tp invalid_file

real    0m0.006s
user    0m0.001s
sys     0m0.002s

[...]

[=>] Executando el caso '/task/student//cases/una_palabra' (sin valgrind)...
[=>] Command line: ./tp input_single_word.txt

real    0m0.002s
user    0m0.002s
sys     0m0.000s

Desempaquetando las salidas esperadas de los casos publicos...
Comparando las salidas con las salidas esperadas...

[=>] Comparando archivo_invalido/__return_code__...
1c1
< 255
---
> 1


[=>] Comparando archivo_invalido/__stdout__...
[=>] Comparando entrada_estandar/__return_code__...
[=>] Comparando entrada_estandar/__stdout__...
[=>] Comparando lenguage_c/__return_code__...
[=>] Comparando lenguage_c/__stdout__...
[=>] Comparando nombre_largo/__return_code__...
[=>] Comparando nombre_largo/__stdout__...
[=>] Comparando tda/__return_code__...
[=>] Comparando tda/__stdout__...
[=>] Comparando una_palabra/__return_code__...
[=>] Comparando una_palabra/__stdout__...
1c1
< 0
---
> 1


[Error] Se encontraron diferencias entre las salidas obtenidas y las esperadas.

Executando los casos publicos (con valgrind)...

[=>] Executando el caso '/task/student//cases/archivo_invalido' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp invalid_file

real    0m1.225s
user    0m0.954s
sys     0m0.146s

Valgrind no encontro errores.

[...]

[=>] Executando el caso '/task/student//cases/una_palabra' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_single_word.txt

real    0m1.121s
user    0m0.943s
sys     0m0.107s

Valgrind no encontro errores.

Comparando las salidas con las salidas esperadas...

[=>] Comparando archivo_invalido/__return_code__...
1c1
< 255
---
> 1


[=>] Comparando archivo_invalido/__stdout__...
[=>] Comparando entrada_estandar/__return_code__...
[=>] Comparando entrada_estandar/__stdout__...
[=>] Comparando lenguage_c/__return_code__...
[=>] Comparando lenguage_c/__stdout__...
[=>] Comparando nombre_largo/__return_code__...
[=>] Comparando nombre_largo/__stdout__...
[=>] Comparando tda/__return_code__...
[=>] Comparando tda/__stdout__...
[=>] Comparando una_palabra/__return_code__...
[=>] Comparando una_palabra/__stdout__...
1c1
< 0
---
> 1


[Error] Se encontraron diferencias entre las salidas obtenidas y las esperadas.

Finalizando...
Parece que no has superado todos los casos. Prueba tu trabajo localmente, bloque a bloque y revisa el enunciado. Ayudate de GDB y Valgrind.
```
El SERCOM nos permite identificar el error, al correr las pruebas publicas y compararlas con el resultado esperado. Vemos que para las pruebas "Invalid File" y "Single Word" los resultados obtenidos son distintos a los esperados por lo que el codigo no pasa estas pruebas. **AGREGAR ALGO MAS?**

c. A continuación vemos la ejecucción del comando **hexdump**:
![paso_5](https://github.com/chiabauni/TP0/blob/main/paso_5.png)
El ultimo caracter del archivo input_single_word.txt es **AGREGAR EXPLICACION**

d. A continuación vemos la ejecucción con **gdb**:
![gdb_1](https://github.com/chiabauni/TP0/blob/main/gdb_1.png)
![gdb_2](https://github.com/chiabauni/TP0/blob/main/gdb_2.png)
![gdb_3](https://github.com/chiabauni/TP0/blob/main/gdb_3.png)
![gdb_4](https://github.com/chiabauni/TP0/blob/main/gdb_4.png)
![gdb_5](https://github.com/chiabauni/TP0/blob/main/gdb_5.png)
![gdb_6](https://github.com/chiabauni/TP0/blob/main/gdb_6.png)

### Paso 6: SERCOM - Entrega exitosa

a. Las correcciones realizadas respecto a la versión anterior son:
* Se modifica el valor definido para el ERROR, en el paso 5 es -1 y en el paso 6 es 1.
* Se reemplaza el const char* con los delimitadores de palabras y se remplaza por la palabra DELIM_WORDS definida con las puntuaciones que delimitan las palabras.
* Se cambia la logica de la funcion "wordscounter_next_state()" permitiendo contar una palabra cunado el caracter siguiente es "\n" y **CHEQUEAR SI CAMBIA ALGO MAS**

```
38,41c37,41
<     if (c == EOF) {
<         next_state = STATE_FINISHED;
<     } else if (state == STATE_WAITING_WORD) {
<         if (strchr(delim_words, c) == NULL)
---
> 
>     if (state == STATE_WAITING_WORD) {
>         if (c == EOF) { 
>             next_state = STATE_FINISHED;
>         } else if (strchr(DELIM_WORDS, c) == NULL) {
42a43
>         }
44c45,48
<         if (strchr(delim_words, c) != NULL) {
---
>         if (c == EOF) { 
>             next_state = STATE_FINISHED;
>             self->words++;
>         } else if (strchr(DELIM_WORDS, c) != NULL) {
48a53
> 
```
b. A continuación vemos todas las entregas realizadas, tanto exitosas como fallidas:
![Submission History](https://github.com/chiabauni/TP0/blob/main/Submission History.png)

c. A continuación vemos la ejecucción de la prueba "single Word" con las distintas variables indicadas:
![paso_6](https://github.com/chiabauni/TP0/blob/main/paso_6.png)
![paso_6.1](https://github.com/chiabauni/TP0/blob/main/paso_6.1.png)
