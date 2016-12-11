Ver e interpretar notación de permisos
--------------------------------------
Es posible ver los permisos de varios archivos en un directorio
usando `ls -l`. También es posible ver los permisos para el directorio
en cuestión: `ls -ld`.

El identificador de permisos puede lucir así: `drwxrwxrwx`. La `d`
indica que el permiso pertenece a un directorio. Si dijera `l` (L)
entonces se trata de un enlace simbólico. En caso de que el identificador
pertenezca a un archivo, ese bit en cuestión es `-` para cualquier
archivo regular.

En estos identificadores se componen de varias letras que representan
la presencia de un bit. En caso de que estos bits estén desactivados,
entonces se sustituyen por `-`:

  * `r` para permisos de lectura.
  * `w` para permisos de escritura.
  * `x` para permisos de ejecución.

Estas caracteres se repiten en la cadena de permisos, pues se dividen en
tres grupos:

  * Primer grupo: permisos para dueño del archivo.
  * Segundo grupo: permisos para el grupo asignado al archivo.
  * Tercer grupo: permisos para el resto de los usuarios.

Por ejemplo: Para ver los permisos de los archivos `foo` y `baz`,
se puede usar el comando `ls` de la siguiente manera: `ls -ld foo baz`

Cambiar permisos con chmod
--------------------------
El formato para cambiar los permisos con `chmod` es
`chmod <permisos> archivos`.

Los permisos con formatos numéricos se componen usando un dígito para
cada grupo y sumando los valores asignados a cada tipo de permiso:

  * Para lectura (**r**) es 4.
  * Para escritura (**w**) es 2.
  * Para ejecución (**x**) es 1.

Algunos ejemplos:

  * `rwx` (4 + 2 + 1) = 7, todos los permisos para cierto grupo.
  * `rw-` (4 + 2) = 6
  * `r-x` (4 + 1) = 5
  * `r--` (4) = 4
  * `-wx` (2 + 1) = 3

Se usa un número compuesto de dígitos formados de la forma anteriormente
ilustrada. Por ejemplo, para dar permisos de lectura y ejecución al
archivo `foo` a todos los usuarios:

```
chmod 555 foo
```

Es posible usar también el formato `<grupo o usuario>[+/-]<permisos>`, que
es la forma más clara, directa y concisa de cambiar permisos.

En lugar de usar los números compuestos para crear permisos, se
usan instrucciones.

Es posible cambiar permisos para el usuario que posee el archivo (`u`),
el grupo asignado (`g`), los demás usuarios (`o`) o todos los usuarios
(`a`).

Se usa el signo `+` para añadir permisos, o el `-` para quitarlos.

Por ejemplo:

  * `chmod a-w file` quita los permisos de escritura (sobre el archivo)
    a todos los usuarios.
  * `chmod u+x file` otorga los permisos de ejecución al usuario dueño.
  * `chmod ug-wx file` quita los permisos de escritura y ejecución a
    al usuario dueño y al grupo asociado al archivo.
  * `chmod uo+rw file` otorga permisos de escritura y lectura al usuario
    dueño y a los demás usuarios.

Es posible también aplicar los permisos recursivamente añadiendo el
parámetro `-R` al comando de cambiar permisos.

Cambiar dueño del archivo usando chown
--------------------------------------
Es necesario tener permisos de administrador (root) para cambiar
el dueño de un archivo.

Por ejemplo, para cambiar el dueño del archivo `foo` a `jane`:
`chwon jane /tmp/foo`.

Si se desea demás cambiar el grupo también al grupo de `jane`:
`chwon jane:jane /tmp/foo`.
