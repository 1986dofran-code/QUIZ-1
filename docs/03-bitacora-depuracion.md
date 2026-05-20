# 03 - Bitacora de depuracion

Completa esta tabla durante el desarrollo. Debes registrar minimo 8 hallazgos.

| No. | Error encontrado | Tipo de error | Archivo y linea aproximada | Como lo detecte | Solucion aplicada | Prueba realizada | Resultado |
|---:|---|---|---|---|---|---|---|
| 1 | Faltaba cerrar el parentesis en `if (nombre.length < 3)` | Sintaxis | `js/app.js`, validacion de nombre | La consola detenia la lectura del archivo JavaScript | Agregue el parentesis de cierre antes de la llave | Ejecute `node --check js/app.js` y recargue la pagina | El archivo ya se puede interpretar |
| 2 | El evento submit ejecutaba `validarRegistro()` inmediatamente | Evento | `js/app.js`, conexion del formulario | Al cargar la pagina se llamaba la funcion sin enviar el formulario | Cambie a `form.addEventListener("submit", validarRegistro)` | Recargue y probe enviar el formulario | La funcion se ejecuta solo al enviar |
| 3 | Faltaba `evento.preventDefault()` | Flujo de formulario | `js/app.js`, inicio de `validarRegistro` | El formulario podia recargar la pagina | Agregue `evento.preventDefault()` | Envie datos validos e invalidos | La pagina no se recarga y muestra mensajes |
| 4 | El id `email` no existia en el HTML | Referencia DOM | `js/app.js`, lectura del correo | En `index.html` el campo se llama `correo` | Cambie `getElementById("email")` por `getElementById("correo")` | Envie un registro con correo valido | El correo se lee correctamente |
| 5 | Los ids `btnEjemplo` y `panelMensaje` no coincidian con el HTML | Referencia DOM | `js/app.js`, constantes iniciales | Compare los ids del HTML con los del JS | Use `btnEjemplos` y `panelMensajes` | Presione el boton de casos y mostre mensajes | Los elementos responden |
| 6 | Edad, nota y asistencia se estaban leyendo como texto | Tipo de dato | `js/app.js`, captura de datos | Revise que `.value` devuelve cadenas | Use `Number()` y valide campos vacios | Probe numeros validos, vacios y fuera de rango | Las comparaciones funcionan correctamente |
| 7 | La validacion de edad estaba invertida | Logica | `js/app.js`, condicion de edad | Un estudiante de 15 anos era rechazado | Cambie la condicion a edad vacia, no numerica o menor que 12 | Probe edad 10 y edad 15 | 10 se rechaza y 15 pasa |
| 8 | La validacion de nota usaba `&&` en vez de operador OR | Logica | `js/app.js`, condicion de nota | Una nota no puede ser menor que 0 y mayor que 5 al mismo tiempo | Cambie la condicion para rechazar notas menores que 0 o mayores que 5, y agregue validacion de vacio | Probe nota 6, -1 y 4.2 | 6 y -1 se rechazan, 4.2 pasa |
| 9 | Se usaba asignacion `estado = "No aprobado"` en vez de comparacion | Logica | `js/app.js`, `obtenerRecomendacion` | Todos los registros terminaban con recomendacion de no aprobado | Cambie a `estado === "No aprobado"` | Cargue casos de prueba | Cada estado mantiene su recomendacion correcta |
| 10 | El ciclo de la tabla usaba `i <= registros.length` | Logica / ciclo | `js/app.js`, `renderizarTabla` | La ultima vuelta intentaba leer un registro inexistente | Cambie a `i < registros.length` | Cargue tres casos de prueba | La tabla muestra tres filas sin error |
| 11 | `panelResultado` no existia y `classlist` estaba mal escrito | Referencia DOM | `js/app.js`, `mostrarMensaje` | La consola indicaba variables o propiedades no definidas | Use `panelMensajes.textContent` y `panelMensajes.classList` | Force mensajes de error y exito | Los mensajes se muestran con estilo |
| 12 | Los casos de prueba se agregaban sin estado ni recomendacion | Logica | `js/app.js`, `cargarCasosPrueba` | La tabla esperaba `estado` y `recomendacion` | Calcule estado y recomendacion antes de insertar cada caso | Presione "Cargar casos de prueba" | La tabla y el resumen se actualizan |

## Preguntas de cierre

1. Cual fue el error mas dificil de encontrar y por que?

Respuesta:

El mas dificil fue el de `estado = "No aprobado"`, porque no rompe el programa. El sistema seguia funcionando, pero la recomendacion quedaba mal para registros que si estaban aprobados o en plan de mejora.

2. Que herramienta te ayudo mas: consola, `console.log()`, lectura del codigo o pruebas manuales?

Respuesta:

La consola y la lectura del codigo fueron las herramientas principales. La consola ayudo con errores de sintaxis y referencias, y las pruebas manuales ayudaron a encontrar errores logicos.

3. Que aprendiste sobre control de flujos?

Respuesta:

Aprendi que el orden y las condiciones de `if`, `else if`, `switch` y `for` afectan directamente el resultado. Una condicion invertida o un operador incorrecto puede hacer que el programa funcione, pero entregue una respuesta equivocada.

4. Que buena practica aplicarias en tus proximos proyectos?

Respuesta:

Aplicaria la practica de corregir un error a la vez, probar despues de cada cambio y documentar que se corrigio. Tambien revisaria que los ids del HTML coincidan con los usados en JavaScript.
