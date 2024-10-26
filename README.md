Parte 1: Introducción Teórica a la Especificidad
1. ¿Qué es la especificidad?
    Explicación de cómo el navegador decide qué reglas CSS aplicar cuando hay conflictos.
    Introducción a los selectores básicos y cómo afectan la especificidad.

        Tabla de especificidad con diferentes tipos de selectores.
        
        | Selector          | Descripción                | Ejemplo                              | Especificidad |
        |-------------------|----------------------------|--------------------------------------|---------------|
        | `*`               | Universal                  | `* { }`                              | 0             |
        | `element`         | Elemento                   | `h1 { }`                             | 1             |
        | `.class`          | Clase                      | `.highlight { }`                     | 10            |
        | `#id`             | ID                         | `#main { }`                          | 100           |
        | `element.class`   | Elemento + Clase           | `p.highlight { }`                    | 11            |
        | `[attr="val"]`    | Atributo                   | `input[type="text"] { }`             | 10            |
        | `:pseudo-class`   | Pseudoclase                | `a:hover { }`                        | 10            |
        | `::pseudo-element`| Pseudoelemento             | `p::before { }`                      | 1             |
        | `#id .class`      | ID + Clase                 | `#main .highlight { }`               | 110           |
        | `!important`      | Sobrescribe especificidad  | `p { color: red !important; }`       | Anula         |



Parte 2: Ejemplos Prácticos 
1. Ejemplo básico: 
    El color del texto hola mundo sera rojo porque el selector ID tiene mayor especifidad que los otros selectores(clase y etiqueta)

2. Demostracion de !important: 
    El color del texto hola mundo sera color azul porque !important tiene prioridad, independientemente de la especifidad

Parte 3: Ejercicios Practicos
1. Ejercicio 1: Calculando la Especifidad:
    ¿Qué color tendrá el título <h1> ?
        El color del titulo <h1> sera rojo, porque el selector ID tiene mayor especifidad

2. Ejercicio 2: Resolviendo Conflictos de especifidad:
    agregamos un selector con mayor especifidad como 
        #box .text {
            color: yellow;
        }

Parte 4: Desafio Final
    Desafío: Diseñando una Página Completa con Estilos Conflictivos
        Dales a los participantes un archivo HTML con múltiples elementos y clases, y pídeles que agreguen estilos CSS para lograr un diseño específico. Deberán aplicar todo lo aprendido sobre especificidad para resolver los conflictos y obtener el resultado correcto.

Desafío CSS:
    El <h1> en el .header debe ser de color blanco.
    El texto del <p> en .content debe ser rojo.
    El texto del <footer> debe ser gris.

    .header h1{
        color: white;
    }

    .content p{
        color: red;   
    }

    #footer p{
        color: grey;
    }

