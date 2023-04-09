# Manual de instalación de "dex"

## Descripción

"Dex" es un script en bash que permite listar los contenedores Docker en estado "running", ordenados numéricamente y etiquetados con un número para su fácil selección.

## Requerimientos

- Un sistema operativo basado en Unix (como Linux o macOS).
- Docker instalado y en funcionamiento.
- Permisos de superusuario (root) para instalar el script.

## Procedimiento de instalación

1. Abre una terminal y ejecuta el siguiente comando para descargar el script:

    ```bash
    curl -o dex https://raw.githubusercontent.com/SoportePhonix/dex/main/dex
    ```

<br>

2. Mueve el archivo "dex" al directorio "/usr/local/bin/" con el siguiente comando:

    ```bash
    sudo mv dex /usr/local/bin/
    ```  
   
    Este comando mueve el archivo "dex" al directorio "/usr/local/bin/", que es un directorio estándar en el PATH de Linux donde se encuentran los comandos ejecutables.

<br>

3. Haz que el archivo "dex" sea ejecutable con el siguiente comando:

    ```bash
    sudo chmod +x /usr/local/bin/dex
    ```

    Este comando agrega permisos de ejecución al archivo "dex", lo que permite que se ejecute como un comando.

<br>

4. Verifica que el archivo "dex" esté en el PATH de tu sistema ejecutando el siguiente comando:

    ```bash
    echo $PATH
    ```

    Si "/usr/local/bin/" no está incluido en la salida, debes agregarlo al archivo "/etc/environment" o "/etc/profile". Puedes hacerlo ejecutando el siguiente comando:

    ```bash
    sudo nano /etc/environment
    ```

    Agrega la siguiente línea al final del archivo:

    ```
    PATH="/usr/local/bin:$PATH"
    ```

    Guarda los cambios presionando "Ctrl + O" seguido de "Enter" y luego cierra el editor de texto presionando "Ctrl + X".

    Luego, reinicia la terminal o carga el archivo "/etc/environment" con el siguiente comando:

    ```bash
    source /etc/environment
    ```

<br>

5. Para utilizar el comando "dex", abre una terminal y escribe el siguiente comando:

    ```bash
    dex
    ```

    Este comando lista los contenedores Docker en estado "running", ordenados numéricamente y etiquetados con un número para su fácil selección. Luego, el script te pedirá que elijas el contenedor al que deseas ingresar escribiendo el número correspondiente.

    **Nota:** Asegúrate de tener Docker en funcionamiento antes de ejecutar el comando "dex".

### ¡Listo! Ahora puedes utilizar el comando "dex" para listar y seleccionar contenedores Docker en tu sistema.
