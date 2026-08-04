# expos_html
## tema ,HTML media

# HTML Media Elements

Los elementos multimedia de HTML permiten la integración nativa de contenido de audio y vídeo en documentos web, eliminando la necesidad histórica de complementos externos como Flash o ActiveX. Estos elementos proporcionan una forma estandarizada de presentar flujos de datos multimedia a los usuarios.

## Introducción a las etiquetas multimedia

El estándar HTML5 introdujo dos elementos principales para manejar medios:

*   **`<video>`**: Utilizado para reproducir clips de vídeo, películas o archivos de audio con subtítulos vinculados. Este elemento incluye un área de reproducción para contenido visual.
*   **`<audio>`**: Diseñado específicamente para reproducir archivos de sonido o flujos de audio. A diferencia del elemento de vídeo, no posee un área de visualización nativa para imágenes o subtítulos.

Ambos elementos actúan como contenedores de contenido incrustado y permiten la inclusión de texto alternativo dentro de sus etiquetas de apertura y cierre, el cual solo se mostrará si el navegador no admite el elemento multimedia correspondiente.

## Atributos principales de configuración

Los elementos multimedia comparten un conjunto de atributos comunes que definen su comportamiento y apariencia:

| Atributo | Descripción |
| :--- | :--- |
| **`src`** | Indica la dirección URL del recurso multimedia que se va a mostrar o reproducir. |
| **`controls`** | Atributo booleano que indica al navegador que debe mostrar su propia interfaz de controles (reproducción, pausa, volumen, etc.). |
| **`autoplay`** | Indica que el recurso debe comenzar a reproducirse automáticamente tan pronto como sea posible. Los navegadores modernos suelen requerir que el medio esté silenciado para permitir esto. |
| **`loop`** | Atributo booleano que, si está presente, hace que el recurso vuelva a empezar desde el principio al llegar al final. |
| **`muted`** | Define que el estado inicial del audio debe estar silenciado. |
| **`poster`** | (Solo en `<video>`) Especifica la URL de una imagen que se muestra mientras el vídeo se descarga o hasta que el usuario pulsa el botón de reproducción. |

## El objeto JavaScript `HTMLMediaElement`

Desde la perspectiva del DOM (Document Object Model), tanto los elementos de vídeo como de audio heredan de la interfaz **`HTMLMediaElement`**. Esta interfaz proporciona métodos, propiedades y eventos comunes para manipular el contenido multimedia mediante scripts.

### Eventos clave de reproducción
El ciclo de vida de un elemento multimedia está acompañado de diversos eventos que notifican cambios en su estado:

*   **`play`**: Se dispara cuando el elemento ya no está en pausa, ya sea por una llamada al método `.play()` o por el atributo `autoplay`.
*   **`pause`**: Se activa cuando la reproducción se detiene, estableciendo la propiedad `paused` a `true`.
*   **`ended`**: Ocurre cuando la reproducción ha llegado al final del recurso multimedia.

## Buenas prácticas: Usabilidad y Accesibilidad

Para garantizar una experiencia de usuario óptima y accesible, se recomiendan las siguientes estrategias:

### Gestión de formatos y compatibilidad
Dado que no todos los navegadores admiten los mismos códecs, es una buena práctica utilizar el elemento **`<source>`** dentro de `<video>` o `<audio>`. Esto permite especificar múltiples archivos alternativos; el navegador elegirá el primer formato que reconozca (por ejemplo, MP4, WebM u Ogg para vídeo).

### Accesibilidad con `<track>`
El elemento **`<track>`** permite especificar pistas de texto externas sincronizadas en el tiempo, fundamentales para la accesibilidad. Se utiliza para incluir:
*   **Subtítulos (`subtitles`)**: Traducciones del diálogo para usuarios que no entienden el idioma.
*   **Subtítulos para sordos (`captions`)**: Transcripción de diálogos y efectos de sonido relevantes para personas con discapacidad auditiva.
*   **Descripciones (`descriptions`)**: Descripciones textuales del contenido visual para síntesis de voz, orientadas a usuarios ciegos.

### Rendimiento y visualización
Es recomendable definir siempre los atributos **`width`** y **`height`** en los elementos de vídeo. Si no se especifican, el navegador no conocerá las dimensiones hasta que comience la carga, lo que puede provocar parpadeos o cambios bruscos en el diseño de la página mientras el vídeo se descarga. En dispositivos móviles o con recursos limitados, se aconseja liberar los recursos estableciendo el atributo `src` como una cadena vacía una vez finalizado el uso del medio.