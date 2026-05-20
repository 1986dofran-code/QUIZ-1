# 05 - Mapa conceptual / Notes

## Tema central

**Errores frecuentes en JavaScript, depuracion sistematica y control de flujos**

## 1. Errores frecuentes en JavaScript

- Error de sintaxis:
  - Definicion: ocurre cuando el codigo esta escrito de forma incorrecta y JavaScript no puede interpretarlo.
  - Ejemplo: `if (nombre.length < 3 {`.
  - Como se corrige: revisando parentesis, llaves, comas, comillas y mensajes de consola.

- Error de referencia:
  - Definicion: ocurre cuando se llama una variable, funcion o elemento del DOM que no existe.
  - Ejemplo: `document.getElementById("email")` cuando el HTML usa `id="correo"`.
  - Como se corrige: comparando nombres, ids y variables usadas en HTML y JavaScript.

- Error de tipo:
  - Definicion: ocurre cuando un dato se usa como un tipo diferente al esperado.
  - Ejemplo: leer una nota con `.value` y tratarla como numero sin convertirla.
  - Como se corrige: usando conversiones como `Number()` y validando valores vacios.

- Error logico:
  - Definicion: ocurre cuando el programa se ejecuta, pero la respuesta es incorrecta.
  - Ejemplo: usar `edad >= 12` para mostrar error de edad minima.
  - Como se corrige: probando casos reales y revisando si la condicion expresa la regla correcta.

- Error en eventos:
  - Definicion: ocurre cuando una funcion se conecta mal a una accion del usuario.
  - Ejemplo: `addEventListener("submit", validarRegistro())`.
  - Como se corrige: pasando la referencia de la funcion, por ejemplo `validarRegistro`, sin parentesis.

## 2. Depuracion sistematica

- Reproducir error: repetir la accion que falla para observar el comportamiento.
- Leer consola: revisar el primer error mostrado por el navegador.
- Usar `console.log()`: imprimir valores cuando el resultado no es claro.
- Corregir una cosa a la vez: hacer cambios pequenos para saber que arreglo cada problema.
- Probar de nuevo: recargar la pagina y repetir el caso.
- Documentar: anotar error, causa, solucion y prueba realizada.

## 3. Control de flujos

- `if`: evalua una condicion y ejecuta codigo si es verdadera.
- `else`: ejecuta una alternativa cuando el `if` no se cumple.
- `else if`: permite revisar varias condiciones en orden.
- `switch`: permite elegir una accion segun un valor especifico.
- `for`: recorre una lista o arreglo con un contador.
- `while`: repite instrucciones mientras una condicion sea verdadera.

## 4. Buenas practicas

- Nombres claros: usar variables e ids faciles de entender.
- Conversion de tipos: convertir entradas numericas antes de compararlas.
- Validacion de entradas: verificar campos vacios, rangos y formatos.
- Comparaciones correctas: usar `===` para igualdad estricta y evitar asignaciones por error.
- Pruebas con datos validos e invalidos: confirmar que el sistema acepta y rechaza correctamente.
- Bitacora de depuracion: registrar el proceso para explicar como se resolvio el problema.

## Version final del mapa

Mapa textual completado en este archivo. Resume los conceptos principales de la semana y se relaciona con las correcciones realizadas en `js/app.js`.
                                   ┌──────────────────────────────┐
                                   │        JAVASCRIPT            │
                                   │ Errores y Depuración         │
                                   └─────────────┬────────────────┘
                                                 │
         ┌───────────────────────────────────────┼───────────────────────────────────────┐
         │                                       │                                       │
         ▼                                       ▼                                       ▼

┌──────────────────────┐             ┌──────────────────────┐             ┌──────────────────────┐
│ ERRORES FRECUENTES   │             │ DEPURACIÓN           │             │ CONTROL DE FLUJOS    │
└─────────┬────────────┘             └─────────┬────────────┘             └─────────┬────────────┘
          │                                    │                                    │
          │                                    │                                    │

 ┌────────┼────────┐                 ┌─────────┼──────────┐            ┌────────────┼─────────────┐
 │        │        │                 │         │          │            │            │             │
 ▼        ▼        ▼                 ▼         ▼          ▼            ▼            ▼             ▼

Error   Error    Error          Reproducir   Leer      Usar        if           else         else if
de      de       de             error        consola   console.log()
sintaxis referencia tipo

 │        │        │                 │         │          │
 ▼        ▼        ▼                 ▼         ▼          ▼

Código   Variable Datos        Repetir     Revisar   Mostrar
mal      o id     usados       acción      primer    valores
escrito  no       con tipo     que falla   error     en consola
         existe   incorrecto

 │
 ▼

Error lógico
y eventos

 │
 ▼

Resultados incorrectos
o funciones mal conectadas


────────────────────────────────────────────────────────────────────────────

                     ┌────────────────────────────┐
                     │     BUENAS PRÁCTICAS      │
                     └────────────┬──────────────┘
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼

 Nombres claros         Conversión de tipos       Validación de entradas

        │                         │                         │
        ▼                         ▼                         ▼

 Variables fáciles       Number() y parseFloat()   Revisar campos vacíos,
 de entender             para datos numéricos      rangos y formatos


        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼

 Comparaciones          Pruebas con datos          Bitácora de
 correctas              válidos e inválidos        depuración

        │                         │                         │
        ▼                         ▼                         ▼

 Usar ===               Confirmar funcionamiento    Registrar:
 y evitar errores       correcto del sistema        error, causa,
                                                     solución y prueba