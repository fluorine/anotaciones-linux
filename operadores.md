Operadores para patrones
========================
 - El signo `?` representa cualquier caracter individual.
 - El signo `*` representa cualquier secuencia de caracteres.
 - `[...]` representa cualquier letra que este dentro de
   los corchetes.

Ejemplos
--------
 - `[abc]*` representa cualquier palabra que comience con *a*, *b* o *c*
 - `a??a` representa cualquier palabra de cuatro letras que comience
   y termine con *a*.
 - `[aeiou]*[x-z]` representa cualquier palabra que comience con cualquier
   vocal y termine con *x*, *y* o *z*.

Operadores de redirección
=========================
 - `a < b` redirige el contenido del archivo **b** al comando **a**.
   Este es un comportamiento común en los comandos que usualmente
   no necesita del operador de manera explícita
 - `a > b` redirige la salida estándar de **a** al archivo **b**.
   Si este no existe, se crea; si ya existe, se sobreescribe.
 - `a >> b` similar al anterior, pero si el archivo existe, se anexa
   al final del archivo **b**.
 - `a 2> b` redirige la salida de error al archivo **b**.
 - `a &> b` redirige tanta la salida estándar como la de error
   al archivo **b**.
 - `a < b > c` generaliza dos operadores: **b** es entrada y **c**
   es el archivo de salida.

Operador de expansión
=====================
 `{}` permite expandir series de caracteres separadas por coma
 para generalizarlas en varios comandos. Es posible usar también
 secuencias como *{1..7}* o *{a..c}*.

Ejemplos
--------
 - `touch memo{1, 2, 3}` crea los archivos *memo1, memo2* y *memo3*.
 - `rm -f {Joseph,Tar}-{1,2}` borra los archivos *Joseph-1, Joseph-2,
   Tar-1* y *Tar-2*.
