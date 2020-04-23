# Buscador de gatites - Segunda parte

A partir del código de la [clase 65](https://github.com/Ada-Online-2da-Gen/ejercicios-javascript/tree/master/codigo-clases/Clase%2065), completar las siguientes funcionalidades:

### Buscador de imágenes por raza

Cargar el select del buscador de imágenes con la lista de razas, y realizar una búsqueda de imágenes con dicha raza, actualizando los resultados. Al seleccionar una nueva raza, se tiene que volver a la página 0 (y actualizar respectivamente el indicador de la página). El select debería tener un option que permita realizar la búsqueda de imágenes normal con todas las razas.


### Lista de razas con filtros

- La sección debería cargar un listado con todas las razas
- El contenedor de resultados es el elemento con id `breed-results`
- Dentro de la misma se encuentra un template de ejemplo
- La card de cada raza debería contener una imagen de la misma y el nombre de la raza
- La lista de razas se obtiene con `https://api.thecatapi.com/v1/breeds/`
- La imagen de una raza se obtiene con `https://api.thecatapi.com/v1/images/search?breed_ids={breed-id}`
- Esa lista obtenida debería filtrarse según los filtros elegidos
- Cada checkbox tiene en como atributo `data-filter` el nombre de la propiedad del objeto raza al que refiere
- En la respuesta, llega como 1 si tiene el atributo y 0 sino. Por ejemplo, la raza Sphynx tiene "rare" con 1 (es exótica), "hairless" con 1 (no tiene pelos), "short_legs" con 0 (tiene piernas largas)
- Para saber si un checkbox está chequeado, se usa la propiedad `checked` del elemento que devuelve un booleano, p. ej.:
```js
document.querySelector('.checkbox').checked // false
```
- Al modificarse cualquier filtro, debería actualizarse la lista de resultados
- Debería mostrar la cantidad de resultados obtenidos
<br>

Refactorizar el resto de código en lo posible para reutilizar y simplificar funciones y realizar la menor cantidad de pedidos HTTP repetidos que se pueda.

