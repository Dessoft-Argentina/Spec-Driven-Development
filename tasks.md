# Tareas — <Nombre de la funcionalidad / proyecto>

> El plan de ejecución. Si los requerimientos y el diseño están bien hechos, las tareas salen casi solas.
> Reglas prácticas:
>   • Cada tarea es lo bastante chica para terminarla y verificarla en una sola sesión.
>   • Cada tarea indica los IDs de requerimientos que cumple (trazabilidad en los dos sentidos).
>   • Cada tarea tiene un chequeo concreto de aprobado/desaprobado: "se ve bien" no es un chequeo.
>   • Ordená por dependencias y anotá qué bloquea a qué.
>   • Las tareas son solo pasos de desarrollo/implementación (no "pasar a producción" ni "mandarle un mail al cliente").

## Referencias

- Estado: `[ ]` pendiente · `[~]` en curso · `[x]` terminada · `[!]` bloqueada
- Cada tarea indica los requerimientos que cumple: _(R1, R2)_

## Tareas

- [ ] **1. <Tarea base: preparar el terreno sobre el que se apoyan las demás>**
  - <subpaso: lo concreto que hay que hacer>
  - <subpaso>
  - **Cumple:** R1
  - **Depende de:** —
  - **Terminada cuando:** <chequeo específico y verificable: una prueba que pasa, la salida de un comando, un comportamiento observable>

- [ ] **2. <Siguiente tarea>**
  - <subpaso>
  - **Cumple:** R1, R2
  - **Depende de:** 1
  - **Terminada cuando:** <chequeo>

- [ ] **3. <Una tarea que se divide en trabajo en paralelo>**
  - [ ] 3.1 <subtarea que se puede hacer de forma independiente>
    - **Cumple:** R2
    - **Terminada cuando:** <chequeo>
  - [ ] 3.2 <subtarea sin superposición con la 3.1, se puede hacer en paralelo sin riesgo>
    - **Cumple:** R3
    - **Terminada cuando:** <chequeo>
  - **Depende de:** 2

- [ ] **4. <Tarea de integración / conexión entre partes>**
  - **Cumple:** R2, R3
  - **Depende de:** 3
  - **Terminada cuando:** <chequeo de punta a punta de todo lo construido hasta acá>

- [ ] **5. <Tarea de verificación: pruebas / QA de esta etapa>**
  - Escribir y ejecutar pruebas que cubran los criterios de aceptación de R1 a R3
  - **Cumple:** R1, R2, R3 (verificación)
  - **Depende de:** 4
  - **Terminada cuando:** <todas las pruebas en verde; cada criterio de requirements.md está probado>

## Control de cobertura (opcional pero valioso)

Una tabla rápida que demuestra que cada requerimiento tiene al menos una tarea. Los huecos saltan a la vista.

| Requerimiento | Cubierto por la(s) tarea(s) |
|---------------|-----------------------------|
| R1            | 1, 2, 5                     |
| R2            | 2, 3.1, 4, 5                |
| R3            | 3.2, 4, 5                   |
