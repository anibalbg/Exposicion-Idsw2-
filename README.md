# Exposicion-Idsw2

## Primera Reunión
En primer lugar vamos a analizar el diagrama proporcionado y proceder con la identificación de errores. El diagrama cuenta con errores como duplicaciones de entidades, entidades innecesarias...
![](/Documentos/modeloDoinio.svg)

Una vez ya hecho el diagrama de forma correcta, procedemos a añadir una clase abstracta llamada Persona de la que heredan Asistente, DirectorFestival y Jurado, esta clase contiene atributos comunes como el nombre o email.

Además de la clase abtracta, he añadido diferentes tipos de relaciones entre clases, como la herencia entre la clase abstracta Persona y las clases a las que hereda, composición entre Festival y programa y programa y sesión, ya que si un festival se elimina, sus programas también, también he añadido agregación entre sesión y pelicula ya que una sesión proyecta películas, pero las películas pueden existir de forma independiente y finalmente he utilizado asociaciones entre las demás clases, con esto ya tendríamos un buen diseño. 

![](/Documentos/Diseño.svg)

## Segunda Reunión

En la segunda reunión continuamos con el diseño modular, donde aplicamos los principios del diseño modular.

He definido diferentes modulos que agrupan clases relacionadas, las entidades de gestión en Gestión del Festival, las de evaluaciones en Evaluación... De esta forma conseguimos una clara separación de responsabilidades.

![](/Documentos/DiseñoModular.svg)


## Tercera Reunión

En esta tercera sesión he aplicado los principios SOLID, empezando por el principio de responsabilidad única en cada clase, por ejemplo, jurado, ya que su función es solo evaluar películas. Otro principio usado sería el OCP, utilizando interfaces como IPersona e IDirector, ya que permite extender funcionalidades sin modificar codigo, por ejemplo, podríamos añadir juradoInternacional sin cambiar jurado, estas interfaces también aplican al principio de sustitución de Liskov, donde directorFestival implementa IDirector o las clases DirectorFestival, Asistente y Jurado pueden sustituir a Persona sin romper su comportamiento. Finalmente, el ultimo principio utilizado es el de Inversión de dependecias, ya que Festival depende de IDirector (clase abstracta), no de DirectorFestival (implementación).


![](/Documentos/DIseñoOrientadoObjetos.svg)







