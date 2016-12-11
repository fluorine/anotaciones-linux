El comando `locate <file>` permite buscar archivos en Linux.
La base de datos de este comando puede actualizarse usando
el comando `updatedb` desde el usuario _root_.

El parámetro `-i` permite ignorar mayúsculas o minúsculas.

El mejor comando para buscar en Linux es `find`. Este comando
también permite al usuario hacer acciones sobre lo que se encuentre.
Este comando permite buscan por atributos de nombre, permisos, tamaño,
tiempos de modificación, etc.

Por ejemplo, buscar por nombre: `find /etc -name passwd`. Es posible
usar `*` o `?` como comodines para hacer búsquedas más generales.
`-iname` es similar, pero permite ignorar el caso de las letras.

Es posible buscar archivos por tamaño. El parámetro `-size +10M` busca
archivos mayores de 10 Mb, mientras que `-1M` busca archivos menores a
1 Mb. Es posible buscar archivos mayores a 500 Mb y menores a 1 Gb
utilizando el parámetro `-size +500M -size -1G`.

Para buscar archivos por usuario, se usa `-user <user name>`.
Por ejemplo, para mostrar una lista de archivos y descartar los archivos
del usuario _root_, se usa `-not -user root -ls`.

Es incluso posible buscar por permisos, como sería usar `-perm 755` para
mostrar todos los archivos con permiso `rwxr-xr-x`.

El comando `grep` permite buscar dentro de archivos de texto.
Por ejemplo, para buscar la palabra _desktop_ dentro de varios
múltiples archivos en el directorio `/etc/services` se escribe:
`grep desktop /etc/services`. El parámetro `-i` sirve para ignorar
el caso del _string_. Por otro lado, `-r` permite buscar de forma
recursiva.
