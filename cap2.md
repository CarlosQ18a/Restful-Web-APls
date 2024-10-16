```
{
  "collection": {
    "version": "1.0",
    "href": "http://www.youpyetwepostit.com/api/47210977342911065",
    "items": [
      {
        "href": "http://www.youpyetwepostit.com/api/messages/47210977342911065",
        "data": [
          { "name": "date_posted", "value": "2014-04-20T20:15:32.858Z" },
          { "name": "text", "value": "Squid!" }
        ],
        "links": []
      }
    ]
  }
}
```
Este microblog individual se representa como un documento completo en formato application/vnd.collection+json. Es una colección con una lista de items que solo contiene un elemento. La plantilla completa también era un documento válido en formato application/vnd.collection+json, aunque no utilizaba la propiedad collection en absoluto.

Esta es una conveniencia de la estructura de Collection+JSON. Casi todo en el documento es opcional. Esto significa que no es necesario escribir analizadores adicionales para manejar diferentes tipos de documentos. Collection+JSON usa el mismo formato JSON para representar listas de elementos, plantillas individuales completadas y resultados de búsqueda.

# Liberado por Restricciones

Una lección contraintuitiva del diseño RESTful es que las restricciones pueden ser liberadoras. La restricción de seguridad del método GET de HTTP es algo bueno. Gracias a la restricción de seguridad, sabes que si no sabes qué hacer con una URL, siempre puedes hacer un GET y revisar la representación. Incluso si eso no ayuda, nada terrible sucederá solo porque realizaste una solicitud GET. Eso es liberador, y solo es posible debido a un servicio muy seguro en el lado del servidor.

Si el servidor te envía un documento de texto que dice "9", no tienes manera de saber si se supone que es un número o la palabra "9". Pero si obtienes un documento JSON que dice "9", sabes que es un número. El estándar JSON define el significado del contenido, y eso hace posible que el cliente y el servidor tengan una conversación significativa.

Durante los últimos años, cientos de compañías han pasado por esta línea de pensamiento:

- Necesitamos una API.
- Usaremos JSON como el formato del documento.

_________________________________________________________________________

Liberados de la limitaciones | 25
