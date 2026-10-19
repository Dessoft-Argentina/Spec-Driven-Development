# Requerimientos — <Nombre de la funcionalidad / proyecto>

> Es el documento con más impacto. Un error acá lo heredan el diseño y las tareas.
> Cada criterio de aceptación tiene que poder probarse: si no se puede verificar, todavía no es un requerimiento.
> Revisá y aprobá este archivo ANTES de escribir design.md.

## Introducción

<2 a 4 oraciones: qué es esta funcionalidad, para quién es y qué problema resuelve.
Si existe una visión general del producto, enlazala acá.>

## Glosario (opcional pero recomendado)

- **<Término>** — <definición, para que cada palabra signifique lo mismo en todo el documento>.

## Fuera de alcance

<Lista de cosas que esta spec explícitamente NO cubre. Evita que el alcance crezca sin control
y deja claras las expectativas. "En esta versión no vamos a hacer X" es una aclaración válida y valiosa.>

- ...

## Requerimientos

### R1 — <Nombre corto del requerimiento>

**Historia de usuario:** Como <rol>, quiero <capacidad>, para <beneficio>.

**Criterios de aceptación** (notación EARS):

1. CUANDO <disparador / evento>, EL SISTEMA DEBERÁ <respuesta observable>.
2. MIENTRAS <se encuentre en cierto estado>, CUANDO <disparador>, EL SISTEMA DEBERÁ <respuesta>.
3. SI <condición previa / caso de error>, ENTONCES EL SISTEMA DEBERÁ <respuesta>.
4. EL SISTEMA DEBERÁ <condición que se cumple siempre — requerimiento ubicuo>.
5. DONDE <una funcionalidad / configuración esté habilitada>, EL SISTEMA DEBERÁ <respuesta — funcionalidad opcional>.

### R2 — <Nombre corto del requerimiento>

**Historia de usuario:** Como <rol>, quiero <capacidad>, para <beneficio>.

**Criterios de aceptación:**

1. CUANDO ..., EL SISTEMA DEBERÁ ...
2. SI ..., ENTONCES EL SISTEMA DEBERÁ ...

<!--
Machete de palabras clave EARS (cada criterio tiene que tener una de estas formas):
  • Ubicuo:            EL SISTEMA DEBERÁ <respuesta>                              — siempre se cumple
  • Por evento:        CUANDO <disparador>, EL SISTEMA DEBERÁ <respuesta>         — reacción a un evento
  • Por estado:        MIENTRAS <estado>, EL SISTEMA DEBERÁ <respuesta>           — se cumple durante un estado
  • No deseado:        SI <condición>, ENTONCES EL SISTEMA DEBERÁ <respuesta>     — errores / casos borde
  • Opcional:          DONDE <funcionalidad>, EL SISTEMA DEBERÁ <respuesta>       — detrás de un flag / configuración
  • Combinado:         por ejemplo, MIENTRAS <estado>, CUANDO <disparador>, EL SISTEMA DEBERÁ <respuesta>

(En inglés: WHEN / WHILE / IF ... THEN / WHERE ... THE SYSTEM SHALL)

Un buen criterio es: observable (se puede ver que pasa), inequívoco (tiene una sola lectura)
y verificable (una prueba o un chequeo manual da aprobado/desaprobado). Evitá "rápido", "fácil",
"amigable": cuantificalos (por ejemplo, "en menos de 2 segundos", "en 3 toques o menos").
-->

## Requerimientos no funcionales (opcional)

Separalos cuando atraviesan varias funcionalidades (rendimiento, seguridad, accesibilidad, idiomas).

- **RNF1 — Rendimiento:** EL SISTEMA DEBERÁ <p. ej. mostrar el dashboard en menos de 2 s con conexión 4G>.
- **RNF2 — Seguridad:** EL SISTEMA DEBERÁ <p. ej. exigir una sesión con 2FA verificado en todas las rutas de la app>.
- **RNF3 — Accesibilidad:** EL SISTEMA DEBERÁ <p. ej. cumplir WCAG 2.1 AA en los flujos principales>.

## Preguntas abiertas

Todo lo que todavía no está decidido. Resolvelo o posponelo de forma explícita antes de aprobar este documento:
que una pregunta abierta no termine convertida, sin que nadie se dé cuenta, en una suposición del desarrollador.

- [ ] <pregunta> — responsable: <quién decide> — se necesita para: <etapa>
