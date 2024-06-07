### Ambiente de Desarrollo

Dado que nuestro proyecto esta elaborado en PHP, se usa el entorno de desarrollo de Laragon. Aquí se detalla cómo configurar el entorno de desarrollo:

#### Requisitos Previos

1. **Laragon**: Descargar e instalar desde [laragon.org](https://laragon.org/).
2. **Composer**: Descargar e instalar desde [getcomposer.org](https://getcomposer.org/).
3. **PHP**: Versión mínima recomendada es PHP 7.4.

#### Pasos de Instalación

1. **Clonar el repositorio**:
   Clonar el repositorio en la carpeta www de Laragon, por defecto Laragon se instala en la siguiente ruta

    ```sh
    C:\laragon\www
    ```
    Una vez enterado de la ruta de laragon, ejecutamos la siguiente linea de comando.

    ```sh
    git clone https://github.com/usuario/TraductorBrailleATexto.git C:\laragon\www
    ```

## Pasos en Laragon

Los siguientes pasos realizarlos en la terminal de Laragon.

![Screenshot 2024-06-06 215351](https://github.com/DonobanR/TraductorBrailleATexto/assets/135273301/8a881960-5548-4535-a737-37949c6ffc17)

3. **Instalar las dependencias de PHP**:

    ```sh
    composer install
    ```

4. **Instalar las dependencias de Node.js**:

    ```sh
    npm install
    ```

5. **Crear y configurar el archivo `.env`**:

    ```sh
    cp .env.example .env
    ```

    Editar el archivo `.env` con la configuración de la base de datos y otras variables de entorno necesarias.

6. **Generar la clave de la aplicación**:

    ```sh
    php artisan key:generate
    ```

7. **Ejecutar las migraciones de la base de datos**:

    ```sh
    php artisan migrate
    ```

8. **Iniciar el servidor de desarrollo**:

    ```sh
    php artisan serve
    npm run dev
    ```

#### Configuración en Visual Studio Code

1. **Instalar las extensiones recomendadas**:
    - PHP Intelephense
    - Vue Language Features (Volar)
    - ESLint
    - Prettier

2. **Configurar los depuradores**:
    - Configurar el depurador para PHP.
    - Configurar el depurador para JavaScript/Node.js.
