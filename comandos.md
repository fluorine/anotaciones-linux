Comandos y atajos de teclado para consola de Linux
==================================================
Información del sistema y documentación
---------------------------------------
 - `uname` ofrece información general sobre el sistema.
   Tiene varias opciones.
 - `who` tiene información sobre los usuarios en el sistema.
 - `who am i` muestra información sobre la sesión.
 - `id` ofrece información sobre tu identidad.
 - `man [comando]` muestra un manual del comando provisto.
    También sirve para buscar información de funciones
    de la librería estándar de C.
 - `date` muestra la fecha y hora del sistema.
 - `pwd` imprime el directorio de trabajo.
 - `hostname` muestra el nombre de la máquina.
 - `type [comando]` localiza el comando provisto en el sistema.
 - `locate [comando]` localiza un comando en el sistema.
 - `history [n?]` muestra los *n* últimos comandos que
    han sido utilizados en el terminal de comandos.
 - `!!` ejecuta el comando utilizado por última vez.
 - `!?str?` ejecuta el comando que contenga *str*.
 - `alias var='str'` crea un alias *var* para un comando o
    secuencia de comandos *str*.
 - `unalias var` elimina el alias *var*.
 - `exit` sale del *shell*.
 - `help` lista y muestra los comandos integrados en el *shell*.
 - `chown` o `chmod`, ver documentación sobre
   [permisos](permisos.md).

Manejo de archivos
------------------
 - `mv <a> <b>` mueve el archivo o directorio **a**, al directorio **b**.
   El parámetro `-i` es útil para evitar sobreescribir por error.
 - `rm <a ...>` elimina el archivo indicado. El parámetro `-r` permite
   borrar recursivamente; se usa para borrar directorios llenos.
 - `rmdir <a>` elimina el directorio vacío **a**.
 - `cp <a> <b>` copia el archivo o directori **a** al directorio **b**.
   Sirve también para renombrar archivos. Al igual que en `mv` parámetro
   `-i` es útil para evitar sobreescribir por error.
 - `cd [directorio]` cambiar el directorio de trabajo.
 - `mkdir [directorio]` crea un directorio en el directorio de trabajo
    con el nombre provisto.
 - `ls [directorio?]` devuelve una lista de archivos y directorios:
    - `-a` muestra archivos ocultos (archivos de punto)
    - `-l` lista larga
 - `cat [archivo]` muestra contenido del archivo.
 - `less [archivo]` muestra el contenido de un archivo de manera
    similar a los manuales.
 - `more [archivo]` imprime el archivo provisto, aunque ofrece opciones
    que `cat` no ofrece.
 - `nano [archivo]` sirve para abrir un archivo usando el editor nano.
 - `vim [archivo]` sirve para abrir un archivo usando el editor vim.

Atajos de teclado para navegar
------------------------------
 - `Ctrl + L` limpia la pantalla.
 - `Alt + A` ir al principio de la línea.
 - `Alt + E` ir al final de la línea.
 - `Ctrl + F` mueve el cursor un caracter hacia enfrente.
 - `Ctrl + B` mueve el cursor un caracter hacia atrás.
 - `Alt + F` mueve el cursor una palabra hacia enfrente.
 - `Alt + B` mueve el cursor una palabra hacia atrás.

Atajos de teclado para editar
-----------------------------
 - `Ctrl + C` borra toda la línea.
 - `Ctrl + K` corta la línea desde el cursor hasta el final.
 - `Ctrl + U` corta la línea desde el cursor hasta el principio.
 - `Ctrl + W` corta la palabra anterior.
 - `Alt + D` corta la palabra siguiente.
 - `Ctrl + D` borrar caracter bajo el cursor.
 - `Backspace` borra caracter anterior.
 - `Ctrl + T` transpone carater actual y anterior.
 - `Alt + T` transpone palabra actual y anterior.
 - `Alt + U` cambia toda la palabra a mayúsculas.
 - `Alt + L` cambia toda la palabra a minúsculas.
 - `Alt + C` capitaliza la palabra.

Metacomandos
------------
 - ´a | b´ conecta la salida del comando *a* a la entrada
   del comando *b*.
 - ´a ; b ; c´ - Es posible ejecutar secuencias de comandos,
   si los separamos por `;`.
 - `a &` ejecuta el comando *a* en segundo plano. Si se cierra el *shell*,
   entonces el programa en segundo plano deja de ejecutarse.
 - `$[expresión aritmética]` evalúa una expresión aritmética y
   devuelve su resultado para uso en cualquier cadena de texto.
 - `$(comando)` devuelve la salida de un comando en cualquier
   cadena de texto.

Variables de shell
------------------
 - `$USER` contiene el nombre del usuario del sistema.
 - `$HOME` o `~` es el directorio de usuario.
 - `$OLDPWD` o simplemente `-` es el directorio de trabajo anterior al actual.
 - `$PWD` o `.` se actualiza para contener el directorio de trabajo.
 - `..` se refiere al directorio superior en referencia al *path*
 - `$RANDOM` tiene un valor aleatorio que va de 0 a 99999.
