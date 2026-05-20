# 04 - Cuestionario Semana 11

Responde el cuestionario en este mismo archivo. Algunas preguntas son de seleccion multiple y otras son abiertas.

## Preguntas de seleccion multiple

### 1. Que es un error de sintaxis en JavaScript?

Respuesta: A. Un error que ocurre cuando el codigo esta mal escrito.

### 2. Que herramienta del navegador permite revisar errores de JavaScript?

Respuesta: B. Consola.

### 3. Que significa que `document.getElementById("btnEnviar")` devuelva `null`?

Respuesta: B. Que no existe un elemento con ese ID o no esta disponible en ese momento.

### 4. Que hace `event.preventDefault()` en un formulario?

Respuesta: A. Evita que el formulario recargue o envie la pagina automaticamente.

### 5. Cual es una buena practica al depurar?

Respuesta: C. Corregir una cosa, probar y documentar.

### 6. Que estructura permite tomar decisiones?

Respuesta: A. `if`.

### 7. Que estructura permite recorrer varios registros?

Respuesta: A. `for`.

### 8. Que problema puede causar este codigo?

```js
let nota = document.getElementById("nota").value;
let suma = nota + 1;
```

Respuesta: A. Que `nota` se trate como texto y no como numero.

### 9. Que operador debe usarse para comparar igualdad estricta en JavaScript?

Respuesta: C. `===`

### 10. Que error hay en este fragmento?

```js
if (edad >= 18 {
  console.log("Mayor de edad");
}
```

Respuesta: A. Falta un parentesis de cierre.

## Preguntas abiertas

### 11. Explica con tus palabras que es depurar codigo.

Respuesta:

Depurar codigo es revisar un programa para encontrar errores, entender por que ocurren, corregirlos y probar que la solucion realmente funciona.

### 12. Cual es la diferencia entre un error de sintaxis y un error logico?

Respuesta:

Un error de sintaxis ocurre cuando el codigo esta escrito de una forma que JavaScript no puede leer, por ejemplo un parentesis faltante. Un error logico ocurre cuando el codigo si se ejecuta, pero el resultado no es el esperado.

### 13. Por que es importante documentar los errores encontrados?

Respuesta:

Es importante porque permite demostrar el proceso de solucion, recordar que se corrigio y explicar las pruebas realizadas. Tambien ayuda a no repetir el mismo error en otros proyectos.

### 14. Describe una prueba que realizaste para comprobar que el sistema funcionaba.

Respuesta:

Use el boton "Cargar casos de prueba" y verifique que aparecieran tres registros en la tabla: Ana como Aprobado, Luis como Plan de mejora y Sara como No aprobado. Tambien revise que el resumen mostrara total 3.

### 15. Que relacion tiene el control de flujos con la validacion de formularios?

Respuesta:

El control de flujos permite decidir que hacer con los datos del formulario. Con `if` se rechazan datos invalidos, con `else if` se clasifican resultados y con `for` se recorren registros para mostrarlos en pantalla.
