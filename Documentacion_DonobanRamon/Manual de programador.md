# Manual del Programador - Traductor de Texto a Braille

Este manual proporciona una visión general de las clases y métodos utilizados en el proyecto de Traductor de Texto a Braille.

## TranslationController

El `TranslationController` es responsable de manejar las solicitudes de traducción entre texto y braille.

### Métodos

#### translateToBraille(Request $request)

Este método recibe una solicitud HTTP POST con un texto en español y devuelve la traducción a braille.

- **Entrada:** Texto en español.
- **Salida:** Texto traducido a braille.

#### translateToEspanol(Request $request)

Este método recibe una solicitud HTTP POST con un texto en braille y devuelve la traducción a español.

- **Entrada:** Texto en braille.
- **Salida:** Texto traducido a español.

#### convertToBraille($text)

Este método convierte un texto en español a braille.

- **Entrada:** Texto en español.
- **Salida:** Texto en braille.

#### convertToText($braille)

Este método convierte un texto en braille a español.

- **Entrada:** Texto en braille.
- **Salida:** Texto en español.

## Translation

La clase `Translation` representa un modelo para las traducciones entre texto y braille.

### Métodos

#### setTable($table)

Este método establece la tabla de la base de datos a utilizar para las traducciones.

- **Entrada:** Nombre de la tabla.
- **Salida:** Instancia de la clase `Translation`.

## Migración y Semillas

La migración `translations` crea la tabla para las traducciones entre texto y braille, y la migración `translationsBrailleEsp` crea la tabla para las traducciones entre braille y español. Las semillas `TranslationsTableSeeder` llenan las tablas con datos de ejemplo.

## Rutas

Las rutas `/translate-to-braille` y `/translate-to-espanol` están asociadas a los métodos `translateToBraille` y `translateToEspanol` del `TranslationController`, respectivamente.
