# Proyecto con el que se sigue la teoría del módulo 2 del curso

# a. Renderizando una colección, módulos
El primer commit, llamado 'Principio', es el código con el que comienza a explicarse la teoría.
Duda: ¿por qué ReactDOM.render(<App notes={notes} />...?, es decir, ¿por qué es necesario incluir ahí la matriz notes?

La primera modificación es colocar las notas utilizando el método 'map'. Observar que todo el código JavaScript va entre llaves.
El 'key' no aparece en pantalla, se incluye para evitar la advertencia 'Each child in a list should have a unique "key" prop.' en la consola de desarrollo, vamos que es algo necesario al usar el método 'map' con una lista. React utiliza los atributos key de los objetos en una matriz para determinar cómo actualizar la vista generada por un componente cuando el componente se vuelve a renderizar.

