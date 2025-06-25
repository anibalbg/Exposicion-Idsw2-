
# 🎬 Exposición - IDSW2

## 🟢 Primera Reunión

En primer lugar, analizamos el diagrama proporcionado y procedimos a la **identificación de errores**. El diagrama inicial presentaba problemas como:

- **Duplicación de entidades**
- **Entidades innecesarias**
- **Relaciones inconsistentes**

📌 *Diagrama corregido del modelo de dominio:*

![Modelo del dominio](/Documentos/modeloDoinio.svg)

---

Una vez corregido, se incorporó una **clase abstracta `Persona`** de la cual heredan:

- `Asistente`
- `DirectorFestival`
- `Jurado`

Esta clase agrupa atributos comunes como el `nombre` o el `email`.

También se añadieron diferentes tipos de relaciones:

- **Herencia** entre `Persona` y sus subclases.
- **Composición** entre `Festival → Programa` y `Programa → Sesión`, ya que si un festival se elimina, sus elementos también.
- **Agregación** entre `Sesión → Película`, dado que una película puede existir sin sesión.
- **Asociaciones** entre las demás clases.

📌 *Diagrama orientado a objetos corregido:*

![Diseño](/Documentos/Diseño.svg)

---

## 🟡 Segunda Reunión

Durante esta reunión se abordó el **diseño modular** aplicando los principios de **separación de responsabilidades**.

Se organizaron las clases en módulos coherentes:

- **Gestión del Festival**: entidades administrativas
- **Evaluación**: entidades relacionadas con el jurado y premios
- **Proyecciones**: películas y sesiones
- **Participación**: asistentes

Además, se refinaron los **atributos de cada clase** para adaptarlos mejor a su función.

📌 *Diagrama de diseño modular:*

![Diseño Modular](/Documentos/DiseñoModular.svg)

---

## 🔵 Tercera Reunión

En esta fase se aplicaron los **principios SOLID** al diseño:

- **SRP (Responsabilidad Única)**: Cada clase tiene una única función (por ejemplo, `Jurado` solo evalúa películas).
- **OCP (Open/Closed Principle)**: Se introdujeron interfaces como `IPersona` e `IDirector` para permitir extender sin modificar.
- **LSP (Sustitución de Liskov)**: `DirectorFestival`, `Asistente` y `Jurado` pueden sustituir a `Persona` sin afectar la lógica.
- **DIP (Inversión de Dependencias)**: `Festival` depende de la abstracción `IDirector`, no de una implementación concreta como `DirectorFestival`.

📌 *Diagrama orientado a objetos con SOLID:*

![Diseño Orientado a Objetos](/Documentos/DIseñoOrientadoObjetos.svg)
