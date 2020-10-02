# TP0
Paso 1:
Error del SERCOM: 

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

Paso 2:
Error del SERCOM:

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

Verificando el codigo...

Done processing /task/student//source_unsafe/paso2_wordscounter.c
Done processing /task/student//source_unsafe/paso2_main.c
Done processing /task/student//source_unsafe/paso2_wordscounter.h

Paso 3:
Error del SERCOM:

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

PAso 4:
Error del SERCOM:


Desempaquetando y compilando el codigo...

Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso4_main.c
  inflating: source_unsafe/paso4_wordscounter.c
  inflating: source_unsafe/paso4_wordscounter.h
Compilando el codigo...
  CC  paso4_wordscounter.o
  CC  paso4_main.o
  LD  tp

real    0m0.587s
user    0m0.209s
sys     0m0.128s

Verificando el codigo...

Done processing /task/student//source_unsafe/paso4_main.c
Done processing /task/student//source_unsafe/paso4_wordscounter.h
Done processing /task/student//source_unsafe/paso4_wordscounter.c

Desempaquetando los casos publicos...
Executando los casos publicos (sin valgrind)...

[=>] Executando el caso '/task/student//cases/archivo_invalido' (sin valgrind)...
[=>] Command line: ./tp invalid_file

real    0m0.005s
user    0m0.001s
sys     0m0.002s

[=>] Executando el caso '/task/student//cases/entrada_estandar' (sin valgrind)...
[=>] Command line: ./tp

real    0m0.003s
user    0m0.003s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/lenguage_c' (sin valgrind)...
[=>] Command line: ./tp input_c.txt

real    0m0.003s
user    0m0.002s
sys     0m0.001s

[=>] Executando el caso '/task/student//cases/nombre_largo' (sin valgrind)...
[=>] Command line: ./tp input_extremely_long_filename.txt
/task/student//test_single_program.sh: line 61:    31 Aborted                 timeout --kill-after $kill_timeout $timeout $cmd > __stdout__ 2> __stderr__ < __stdin__

real    0m0.283s
user    0m0.003s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/tda' (sin valgrind)...
[=>] Command line: ./tp input_tda.txt

real    0m0.003s
user    0m0.002s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/una_palabra' (sin valgrind)...
[=>] Command line: ./tp input_single_word.txt

real    0m0.003s
user    0m0.002s
sys     0m0.001s

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
1c1
< 134
---
> 0


[=>] Comparando nombre_largo/__stdout__...
0a1
> 2


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

real    0m1.342s
user    0m1.058s
sys     0m0.138s

Valgrind no encontro errores.
[=>] Executando el caso '/task/student//cases/entrada_estandar' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp

real    0m1.171s
user    0m0.959s
sys     0m0.121s

==00:00:00:00.000 23== Memcheck, a memory error detector
==00:00:00:00.000 23== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==00:00:00:00.000 23== Using Valgrind-3.15.0 and LibVEX; rerun with -h for copyright info
==00:00:00:00.000 23== Command: ./tp
==00:00:00:00.000 23== Parent PID: 22
==00:00:00:00.000 23==
==00:00:00:01.133 23==
==00:00:00:01.133 23== FILE DESCRIPTORS: 4 open at exit.
==00:00:00:01.133 23== Open file descriptor 3: /task/student/cases/entrada_estandar/__valgrind__
==00:00:00:01.133 23==    <inherited from parent>
==00:00:00:01.133 23==
==00:00:00:01.133 23== Open file descriptor 2: /task/student/cases/entrada_estandar/__stderr__
==00:00:00:01.133 23==    <inherited from parent>
==00:00:00:01.133 23==
==00:00:00:01.133 23== Open file descriptor 1: /task/student/cases/entrada_estandar/__stdout__
==00:00:00:01.133 23==    <inherited from parent>
==00:00:00:01.133 23==
==00:00:00:01.133 23== Open file descriptor 0: /task/student/cases/entrada_estandar/__stdin__
==00:00:00:01.133 23==    <inherited from parent>
==00:00:00:01.133 23==
==00:00:00:01.133 23==
==00:00:00:01.133 23== HEAP SUMMARY:
==00:00:00:01.133 23==     in use at exit: 3,402 bytes in 486 blocks
==00:00:00:01.133 23==   total heap usage: 488 allocs, 2 frees, 11,594 bytes allocated
==00:00:00:01.133 23==
==00:00:00:01.134 23== 3,402 bytes in 486 blocks are definitely lost in loss record 1 of 1
==00:00:00:01.134 23==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.134 23==    by 0x109301: wordscounter_next_state (paso4_wordscounter.c:35)
==00:00:00:01.134 23==    by 0x1093B5: wordscounter_process (paso4_wordscounter.c:30)
==00:00:00:01.134 23==    by 0x109197: main (paso4_main.c:24)
==00:00:00:01.134 23==
==00:00:00:01.134 23== LEAK SUMMARY:
==00:00:00:01.134 23==    definitely lost: 3,402 bytes in 486 blocks
==00:00:00:01.134 23==    indirectly lost: 0 bytes in 0 blocks
==00:00:00:01.134 23==      possibly lost: 0 bytes in 0 blocks
==00:00:00:01.134 23==    still reachable: 0 bytes in 0 blocks
==00:00:00:01.134 23==         suppressed: 0 bytes in 0 blocks
==00:00:00:01.134 23==
==00:00:00:01.134 23== For lists of detected and suppressed errors, rerun with: -s
==00:00:00:01.134 23== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)

[=>] Executando el caso '/task/student//cases/lenguage_c' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_c.txt

real    0m1.152s
user    0m1.000s
sys     0m0.083s

==00:00:00:00.000 35== Memcheck, a memory error detector
==00:00:00:00.000 35== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==00:00:00:00.000 35== Using Valgrind-3.15.0 and LibVEX; rerun with -h for copyright info
==00:00:00:00.000 35== Command: ./tp input_c.txt
==00:00:00:00.000 35== Parent PID: 34
==00:00:00:00.000 35==
==00:00:00:01.116 35==
==00:00:00:01.116 35== FILE DESCRIPTORS: 5 open at exit.
==00:00:00:01.116 35== Open file descriptor 4: input_c.txt
==00:00:00:01.116 35==    at 0x495FEAB: open (open64.c:48)
==00:00:00:01.116 35==    by 0x48E2195: _IO_file_open (fileops.c:189)
==00:00:00:01.116 35==    by 0x48E2459: _IO_file_fopen@@GLIBC_2.2.5 (fileops.c:281)
==00:00:00:01.116 35==    by 0x48D4B0D: __fopen_internal (iofopen.c:75)
==00:00:00:01.116 35==    by 0x48D4B0D: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.116 35==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.116 35==
==00:00:00:01.116 35== Open file descriptor 3: /task/student/cases/lenguage_c/__valgrind__
==00:00:00:01.116 35==    <inherited from parent>
==00:00:00:01.116 35==
==00:00:00:01.116 35== Open file descriptor 2: /task/student/cases/lenguage_c/__stderr__
==00:00:00:01.116 35==    <inherited from parent>
==00:00:00:01.116 35==
==00:00:00:01.116 35== Open file descriptor 1: /task/student/cases/lenguage_c/__stdout__
==00:00:00:01.116 35==    <inherited from parent>
==00:00:00:01.116 35==
==00:00:00:01.116 35== Open file descriptor 0: /task/student/cases/lenguage_c/__stdin__
==00:00:00:01.116 35==    <inherited from parent>
==00:00:00:01.116 35==
==00:00:00:01.116 35==
==00:00:00:01.116 35== HEAP SUMMARY:
==00:00:00:01.116 35==     in use at exit: 3,874 bytes in 487 blocks
==00:00:00:01.116 35==   total heap usage: 489 allocs, 2 frees, 12,066 bytes allocated
==00:00:00:01.116 35==
==00:00:00:01.117 35== 472 bytes in 1 blocks are still reachable in loss record 1 of 2
==00:00:00:01.117 35==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.117 35==    by 0x48D4AAD: __fopen_internal (iofopen.c:65)
==00:00:00:01.117 35==    by 0x48D4AAD: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.117 35==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.117 35==
==00:00:00:01.117 35== 3,402 bytes in 486 blocks are definitely lost in loss record 2 of 2
==00:00:00:01.117 35==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.117 35==    by 0x109301: wordscounter_next_state (paso4_wordscounter.c:35)
==00:00:00:01.117 35==    by 0x1093B5: wordscounter_process (paso4_wordscounter.c:30)
==00:00:00:01.117 35==    by 0x109197: main (paso4_main.c:24)
==00:00:00:01.117 35==
==00:00:00:01.117 35== LEAK SUMMARY:
==00:00:00:01.117 35==    definitely lost: 3,402 bytes in 486 blocks
==00:00:00:01.117 35==    indirectly lost: 0 bytes in 0 blocks
==00:00:00:01.117 35==      possibly lost: 0 bytes in 0 blocks
==00:00:00:01.117 35==    still reachable: 472 bytes in 1 blocks
==00:00:00:01.117 35==         suppressed: 0 bytes in 0 blocks
==00:00:00:01.117 35==
==00:00:00:01.117 35== For lists of detected and suppressed errors, rerun with: -s
==00:00:00:01.117 35== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)

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

real    0m1.112s
user    0m0.942s
sys     0m0.103s

==00:00:00:00.000 71== Memcheck, a memory error detector
==00:00:00:00.000 71== Copyright (C) 2002-2017, and GNU GPL'd, by Julian Seward et al.
==00:00:00:00.000 71== Using Valgrind-3.15.0 and LibVEX; rerun with -h for copyright info
==00:00:00:00.000 71== Command: ./tp input_single_word.txt
==00:00:00:00.000 71== Parent PID: 70
==00:00:00:00.000 71==
==00:00:00:01.076 71==
==00:00:00:01.076 71== FILE DESCRIPTORS: 5 open at exit.
==00:00:00:01.076 71== Open file descriptor 4: input_single_word.txt
==00:00:00:01.076 71==    at 0x495FEAB: open (open64.c:48)
==00:00:00:01.076 71==    by 0x48E2195: _IO_file_open (fileops.c:189)
==00:00:00:01.076 71==    by 0x48E2459: _IO_file_fopen@@GLIBC_2.2.5 (fileops.c:281)
==00:00:00:01.076 71==    by 0x48D4B0D: __fopen_internal (iofopen.c:75)
==00:00:00:01.076 71==    by 0x48D4B0D: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.076 71==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.077 71==
==00:00:00:01.077 71== Open file descriptor 3: /task/student/cases/una_palabra/__valgrind__
==00:00:00:01.077 71==    <inherited from parent>
==00:00:00:01.077 71==
==00:00:00:01.077 71== Open file descriptor 2: /task/student/cases/una_palabra/__stderr__
==00:00:00:01.077 71==    <inherited from parent>
==00:00:00:01.077 71==
==00:00:00:01.077 71== Open file descriptor 1: /task/student/cases/una_palabra/__stdout__
==00:00:00:01.077 71==    <inherited from parent>
==00:00:00:01.077 71==
==00:00:00:01.077 71== Open file descriptor 0: /task/student/cases/una_palabra/__stdin__
==00:00:00:01.077 71==    <inherited from parent>
==00:00:00:01.077 71==
==00:00:00:01.077 71==
==00:00:00:01.077 71== HEAP SUMMARY:
==00:00:00:01.077 71==     in use at exit: 507 bytes in 6 blocks
==00:00:00:01.077 71==   total heap usage: 8 allocs, 2 frees, 8,699 bytes allocated
==00:00:00:01.077 71==
==00:00:00:01.077 71== 35 bytes in 5 blocks are definitely lost in loss record 1 of 2
==00:00:00:01.077 71==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.077 71==    by 0x109301: wordscounter_next_state (paso4_wordscounter.c:35)
==00:00:00:01.077 71==    by 0x1093B5: wordscounter_process (paso4_wordscounter.c:30)
==00:00:00:01.077 71==    by 0x109197: main (paso4_main.c:24)
==00:00:00:01.077 71==
==00:00:00:01.077 71== 472 bytes in 1 blocks are still reachable in loss record 2 of 2
==00:00:00:01.077 71==    at 0x483B7F3: malloc (in /usr/lib/x86_64-linux-gnu/valgrind/vgpreload_memcheck-amd64-linux.so)
==00:00:00:01.077 71==    by 0x48D4AAD: __fopen_internal (iofopen.c:65)
==00:00:00:01.077 71==    by 0x48D4AAD: fopen@@GLIBC_2.2.5 (iofopen.c:86)
==00:00:00:01.077 71==    by 0x109177: main (paso4_main.c:14)
==00:00:00:01.077 71==
==00:00:00:01.077 71== LEAK SUMMARY:
==00:00:00:01.077 71==    definitely lost: 35 bytes in 5 blocks
==00:00:00:01.077 71==    indirectly lost: 0 bytes in 0 blocks
==00:00:00:01.077 71==      possibly lost: 0 bytes in 0 blocks
==00:00:00:01.077 71==    still reachable: 472 bytes in 1 blocks
==00:00:00:01.077 71==         suppressed: 0 bytes in 0 blocks
==00:00:00:01.077 71==
==00:00:00:01.077 71== For lists of detected and suppressed errors, rerun with: -s
==00:00:00:01.077 71== ERROR SUMMARY: 1 errors from 1 contexts (suppressed: 0 from 0)

Comparando las salidas con las salidas esperadas...

[=>] Comparando archivo_invalido/__return_code__...
1c1
< 255
---
> 1


[=>] Comparando archivo_invalido/__stdout__...
[=>] Comparando entrada_estandar/__return_code__...
1c1
< 42 (from valgrind)
---
> 0


[=>] Comparando entrada_estandar/__stdout__...
[=>] Comparando lenguage_c/__return_code__...
1c1
< 42 (from valgrind)
---
> 0


[=>] Comparando lenguage_c/__stdout__...
[=>] Comparando nombre_largo/__return_code__...
1c1
< 42 (from valgrind)
---
> 0


[=>] Comparando nombre_largo/__stdout__...
0a1
> 2


[=>] Comparando tda/__return_code__...
1c1
< 42 (from valgrind)
---
> 0


[=>] Comparando tda/__stdout__...
[=>] Comparando una_palabra/__return_code__...
1c1
< 42 (from valgrind)
---
> 0


[=>] Comparando una_palabra/__stdout__...
1c1
< 0
---
> 1


[Error] Se encontraron diferencias entre las salidas obtenidas y las esperadas.


Paso 5:
Error del SERCOM:

Desempaquetando y compilando el codigo...

Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso5_main.c
  inflating: source_unsafe/paso5_wordscounter.c
  inflating: source_unsafe/paso5_wordscounter.h
Compilando el codigo...
  CC  paso5_main.o
  CC  paso5_wordscounter.o
  LD  tp

real    0m0.549s
user    0m0.174s
sys     0m0.093s

Verificando el codigo...

Done processing /task/student//source_unsafe/paso5_wordscounter.h
Done processing /task/student//source_unsafe/paso5_main.c
Done processing /task/student//source_unsafe/paso5_wordscounter.c

Desempaquetando los casos publicos...
Executando los casos publicos (sin valgrind)...

[=>] Executando el caso '/task/student//cases/archivo_invalido' (sin valgrind)...
[=>] Command line: ./tp invalid_file

real    0m0.006s
user    0m0.001s
sys     0m0.002s

[=>] Executando el caso '/task/student//cases/entrada_estandar' (sin valgrind)...
[=>] Command line: ./tp

real    0m0.003s
user    0m0.003s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/lenguage_c' (sin valgrind)...
[=>] Command line: ./tp input_c.txt

real    0m0.003s
user    0m0.002s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/nombre_largo' (sin valgrind)...
[=>] Command line: ./tp input_extremely_long_filename.txt

real    0m0.003s
user    0m0.002s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/tda' (sin valgrind)...
[=>] Command line: ./tp input_tda.txt

real    0m0.003s
user    0m0.001s
sys     0m0.002s

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
[=>] Executando el caso '/task/student//cases/entrada_estandar' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp

real    0m1.177s
user    0m0.999s
sys     0m0.098s

Valgrind no encontro errores.
[=>] Executando el caso '/task/student//cases/lenguage_c' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_c.txt

real    0m1.094s
user    0m0.936s
sys     0m0.090s

Valgrind no encontro errores.
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

real    0m1.059s
user    0m0.881s
sys     0m0.122s

Valgrind no encontro errores.
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

real    0m1.170s
user    0m1.004s
sys     0m0.098s

Valgrind no encontro errores.
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


Paso 6:
Error del SERCOM:

Desempaquetando y compilando el codigo...

Descomprimiendo el codigo 'source_unsafe.zip'...
Archive:  source_unsafe.zip
  inflating: source_unsafe/paso6_main.c
  inflating: source_unsafe/paso6_wordscounter.c
  inflating: source_unsafe/paso6_wordscounter.h
Compilando el codigo...
  CC  paso6_wordscounter.o
  CC  paso6_main.o
  LD  tp

real    0m0.666s
user    0m0.241s
sys     0m0.156s

Verificando el codigo...

Done processing /task/student//source_unsafe/paso6_main.c
Done processing /task/student//source_unsafe/paso6_wordscounter.c
Done processing /task/student//source_unsafe/paso6_wordscounter.h

Desempaquetando los casos publicos...
Executando los casos publicos (sin valgrind)...

[=>] Executando el caso '/task/student//cases/archivo_invalido' (sin valgrind)...
[=>] Command line: ./tp invalid_file

real    0m0.006s
user    0m0.004s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/entrada_estandar' (sin valgrind)...
[=>] Command line: ./tp

real    0m0.003s
user    0m0.001s
sys     0m0.001s

[=>] Executando el caso '/task/student//cases/lenguage_c' (sin valgrind)...
[=>] Command line: ./tp input_c.txt

real    0m0.006s
user    0m0.005s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/nombre_largo' (sin valgrind)...
[=>] Command line: ./tp input_extremely_long_filename.txt

real    0m0.003s
user    0m0.003s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/tda' (sin valgrind)...
[=>] Command line: ./tp input_tda.txt

real    0m0.003s
user    0m0.003s
sys     0m0.000s

[=>] Executando el caso '/task/student//cases/una_palabra' (sin valgrind)...
[=>] Command line: ./tp input_single_word.txt

real    0m0.003s
user    0m0.002s
sys     0m0.000s

Desempaquetando las salidas esperadas de los casos publicos...
Comparando las salidas con las salidas esperadas...

[=>] Comparando archivo_invalido/__return_code__...
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
No se encontraron diferencias.

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

real    0m1.179s
user    0m0.927s
sys     0m0.140s

Valgrind no encontro errores.
[=>] Executando el caso '/task/student//cases/entrada_estandar' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp

real    0m1.118s
user    0m0.938s
sys     0m0.105s

Valgrind no encontro errores.
[=>] Executando el caso '/task/student//cases/lenguage_c' (con valgrind)...
[=>] Command line: /usr/bin/valgrind
                --tool=memcheck
                --leak-check=full --leak-resolution=med --show-reachable=yes
                --trace-children=yes
                --track-fds=yes
                --track-origins=no
                --time-stamp=yes --num-callers=20
                --error-exitcode=42
                --log-file=__valgrind__
                --suppressions=/task/student/suppressions.txt ./tp input_c.txt

real    0m1.116s
user    0m0.957s
sys     0m0.097s

Valgrind no encontro errores.
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

real    0m1.096s
user    0m0.902s
sys     0m0.122s

Valgrind no encontro errores.
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

real    0m1.163s
user    0m1.001s
sys     0m0.100s

Valgrind no encontro errores.
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

real    0m1.131s
user    0m0.938s
sys     0m0.130s

Valgrind no encontro errores.

Comparando las salidas con las salidas esperadas...

[=>] Comparando archivo_invalido/__return_code__...
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
No se encontraron diferencias.

Desempaquetando los casos privados...
Executando los casos privados (sin valgrind)...
Desempaquetando las salidas esperadas de los casos privados...
Comparando las salidas con las salidas esperadas...
Executando los casos privados (con valgrind)...
Comparando las salidas con las salidas esperadas...
Finalizando...

Excelente. Todos los casos de pruebas, publicos y privados, fueron superados con exito.


