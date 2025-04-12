# Propuesta TP DSW

## Grupo
### Integrantes
* 50306 - Bay, María Victoria
* 51367 - Gallegos, Nicolás Gabriel

### Repositorios
* [frontend app](https://github.com/NicoGabrielGallegos/DSW-FrontendApp)
* [backend app](https://github.com/NicoGabrielGallegos/DSW-BackendApp)

## Tema
### Descripción
El sistema le otorgará al usuario (alumno o docente), las herramientas necesarias para la creación e inscripción a horarios de consultas de alguna materia en particular. Además, podrá emitir listados sobre diversas estadísticas de alumnos, docentes y materias.

### Modelo Entidad-Relación
![Model de Dominio](/docs/Modelo_Entidad-Relacion.png)

## Alcance Funcional 

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Alumno<br>2. CRUD Docente|
|CRUD dependiente|1. CRUD Calificacion depende de CRUD Consulta<br>2. CRUD Dictado depende de CRUD Docente y CRUD Materia|
|Listado<br>+<br>detalle| 1. Listado de consultas por profesor y/o materia (para alumnos), muestra horario de las consulta, nombre completo del profesor y descripción de la materia => detalle CRUD Inscripción<br> 2. Listado de consultas por materia (para docentes), muestra horario de las consultas, descripción de la materia => detalle CRUD Consulta|
|CUU/Epic|1. Definir un horario de consulta (docente)<br>2. Realizar inscripción a un horario de consulta (alumno)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Alumno<br>2. CRUD Docente<br>3. CRUD Materia<br>4. CRUD Calificacion<br>5. CRUD Dictado|
|CUU/Epic|1. Definir un horario de consulta (docente)<br>2. Realizar inscripción a un horario de consulta (alumno)<br>3. Cancelar un horario de consulta (docente)<br>4. Eliminar inscripción a un horario de consulta (alumno)|


### Alcance Adicional Voluntario

\-
