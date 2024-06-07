# Manual de Instalación y Configuración para el Ambiente de Desarrollo

## GitDesk
Por comodidad, se sugiere utilizar GitDesktop en Windows. Después de instalar GitDesktop, procederemos a clonar el proyecto. Durante este proceso, en el campo "Local Path" debemos ingresar la ruta correspondiente a la carpeta www de Laragon. Por ejemplo, si Laragon está instalado en la ruta predeterminada, la ruta sería `C:\laragon\www`. Laragon es un entorno de desarrollo local que organiza los proyectos web en su carpeta www, permitiendo acceder a ellos directamente a través del servidor local que proporciona.

A continuación, procedemos a realizar la clonación del proyecto. Una vez completada esta operación, abriremos el repositorio clonado con Visual Studio Code (VS Code). Al abrir el proyecto, VS Code puede solicitar la instalación de Git Bash.

Esta herramienta es esencial por las siguientes razones:

Git Bash: Ofrece un entorno de línea de comandos basado en Unix en Windows, permitiendo utilizar comandos Git y scripts de shell de manera similar a cómo se harían en sistemas operativos basados en Unix (como Linux y macOS). Esto es particularmente útil para desarrolladores que están acostumbrados a trabajar en entornos Unix o que necesitan ejecutar scripts específicos que requieren un entorno Unix.
Por lo tanto, la instalación de esta herramienta es fundamental para asegurarse de que Visual Studio Code pueda interactuar correctamente con Git, permitiendo a los desarrolladores gestionar el código fuente de manera efectiva y aprovechar al máximo las capacidades de control de versiones que ofrece Git.

## Requisitos Previos

    PHP >= 7.4
    Composer
    Node.js y npm
    Servidor MySQL o MariaDB

## Instalación en Otra Máquina desde un Repositorio Git
1. Descargar e instalar Laragon desde [este enlace](https://laragon.org/download/index.html).
2. Clonar el repositorio en la carpeta Laragon/www. Utilice GitDesk para clonar el repositorio. En el campo "Local Path", ingrese la ruta correspondiente a la carpeta www de Laragon (por ejemplo, `C:\laragon\www`).
3. Abrir el proyecto en Visual Studio Code:
    - Una vez completada la clonación, abra el repositorio clonado con Visual Studio Code.
    - Copie el archivo `.env.example` y renómbrelo a `.env` directamente en Visual Studio Code.

**Abrir la Terminal de Laragon**\
4. Instalar dependencias php con el comando 
    ```
    composer install
    ```
5. Instalar dependencias Inertia.js con el comando 
    ```
    npm install
    ```
7. Generar la Key de la Aplicación con el comando
    ```
    php artisan key:generate
    ```
9. Migrar las Tablas en la Base de Datos con el comando 
    ```
    php artisan migrate
    ```
11. Poblar las Tablas con el comando 
    ```
    php artisan db:seed --class=TranslationsTableSeeder
    ```
13. Para que los cambios en los archivos Vue.js sean notorios usar el comando 
    ```
    npm run dev
    ```

**Adicional**
Para limpiar la Base de Datos usamos el comando 
    ```
    php artisan migrate:refresh
    ```

Con estos pasos, tendrás un entorno de desarrollo completamente configurado y listo para trabajar en tu proyecto.
