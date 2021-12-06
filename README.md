# Proyecto con el que se sigue la teoría del módulo 2 del curso

# a. Renderizando una colección, módulos
El primer commit, llamado 'Principio', es el código con el que comienza a explicarse la teoría.
Duda: ¿por qué ReactDOM.render(<App notes={notes} />...?, es decir, ¿por qué es necesario incluir ahí la matriz notes?

La primera modificación es colocar las notas utilizando el método 'map'. Observar que todo el código JavaScript va entre llaves.
El 'key' no aparece en pantalla, se incluye para evitar la advertencia 'Each child in a list should have a unique "key" prop.' en la consola de desarrollo, vamos que es algo necesario al usar el método 'map' con una lista. React utiliza los atributos key de los objetos en una matriz para determinar cómo actualizar la vista generada por un componente cuando el componente se vuelve a renderizar.

Lo siguiente es quitar el props de App por desestructuración (así se llama). Ponemos directamente el dato que necesitamos.
También sacamos cada nota a partir de un nuevo componente llamado 'Note'. He utilizado la notación simplificada, sin return, para definir este componente.
También exportaremos el componente creado, como un nuevo módulo que se colocará en una carpeta llamada 'components'
App también es un componente que se importará como módulo aunque, en este caso particular, se coloca en 'src'.

# b. Formularios
Se va a incluir un formulario para que un usuario pueda agregar notas. Para ello se utiliza un hook de estado que se inicializa con la matriz de notas inicial y se actualiza con las notas agregadas por el usuario. Todo esto se hace en el componente App. He tenido que incluir los props como argumento de App porque si no la aplicación se rompe.
También es necesario incluir un formulario con un controlador de eventos para reaccionar a la escritura de una nueva nota.
Después, hay que incluir los instrumentos para controlar la escritura en el elemento input del formulario. Esto se hace con un nuevo hook de estado y un nuevo controlador de eventos.

Lo siguiente será dar una funcionalidad que nos permita ver solo las notas importantes. Para ello, añadiremos otro hook de estado que haga el seguimiento de las notas según su importancia. También habrá que incluir un componente que controle qué notas son las que se muestran. Finalmente, se incluye un botón para alternar entre mostrar todas las notas o solo las importantes.

