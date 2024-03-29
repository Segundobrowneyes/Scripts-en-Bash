# Bash scripting
Bash es un lenguaje de scripting que se utiliza en sistemas Unix y Linux para automatizar tareas y realizar operaciones en el sistema operativo. La lógica detrás de los scripts de bash se basa en las siguientes etapas:

Shebang: la primera línea de un script de bash es el "shebang", que indica al sistema operativo que se debe ejecutar el script con el intérprete de bash. El shebang es #!/bin/bash.

Variables: en los scripts de bash, es posible definir y usar variables. Las variables se pueden definir con el siguiente formato: nombre_variable=valor. Luego, se puede acceder al valor de la variable con el formato $nombre_variable.

Argumentos: los scripts de bash pueden recibir argumentos cuando se ejecutan. Estos argumentos se pueden acceder mediante variables especiales: $1, $2, $3, etc. También se puede acceder a todos los argumentos mediante la variable $@.

Comprobación de número de argumentos: es común verificar en un script de bash que se han proporcionado el número correcto de argumentos. Esto se puede hacer con una estructura de control de flujo como un if-statement. Por ejemplo:

```
if [ $# -ne 2 ]; then
    echo "Error: se requieren dos argumentos."
    exit 1
fi
```
Operadores lógicos: los scripts de bash usan operadores lógicos como && (and), || (or) y ! (not) para controlar el flujo de ejecución.

Estructuras de control de flujo: en bash, existen varias estructuras de control de flujo, como if-statements, for-loops y while-loops, que permiten realizar operaciones de manera repetitiva o solo bajo ciertas condiciones.

Comandos: por último, los scripts de bash son secuencias de comandos que se ejecutan en el terminal. Estos comandos pueden ser comandos internos de bash, como echo o cd, o pueden ser programas externos, como ls o grep.

## Exit

Exit es un comando en Bash que se utiliza para terminar la ejecución de un script o de una sesión de terminal. Cuando se ejecuta el comando exit, el script o la sesión de terminal finaliza y el sistema operativo vuelve al modo de comandos o a la sesión anterior, si es que existe.

El comando exit puede recibir un argumento opcional, que es un número entero. Este número se conoce como "código de salida" y se utiliza para indicar el estado de la salida. Por convención, un código de salida de 0 indica una salida exitosa, mientras que cualquier otro número indica un error. Por ejemplo:

```
# Ejemplo de código de salida exitoso
exit 0

# Ejemplo de código de salida con error
exit 1

```
En los scripts de Bash, es común utilizar el comando exit para indicar el final del script y para proporcionar un código de salida que indique el resultado de la ejecución del script. Por ejemplo:

```
# Script de ejemplo
if [ $# -ne 2 ]; then
    echo "Error: se requieren dos argumentos."
    exit 1
fi
echo "Los argumentos proporcionados son $1 y $2"
exit 0


```
En este ejemplo, el script verifica si se han proporcionado dos argumentos y, si no es así, muestra un mensaje de error y sale del script con un código de salida de 1. Si se proporcionan dos argumentos, el script muestra un mensaje con los argumentos y sale del script con un código de salida de 0.
