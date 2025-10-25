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
|CRUD simple|1. CRUD Docente<br>2. CRUD Materia|
|CRUD dependiente|1. CRUD Dictado depende de CRUD Docente y CRUD Materia|
|Listado<br>+<br>detalle|1. Listado de consultas filtrado por profesor, materia, fecha y rango de horario, muestra nombre completo del profesor, descripción de la materia, fecha de la consulta, hora de inicio y fin de la consulta => detalle muestra datos completos de la consulta, permite al alumno inscribirse y permite al docente modificar o eliminar la consulta<br>2. Listado de docentes filtrado por materia, muestra nombre, apellido y correo => detalle redirecciona al listado de consultas para dicho docente<br>3. Listado de materias filtrado por docente, muestra descripción => detalle redirecciona al listado de consultas para dicha materia<br>4. Listado de docentes (para administradores), muestra id, legajo, nombre, apellido y correo => CRUD Docente<br>5. Listado de materias (para administradores), muestra id y descripción => CRUD Materia |
|CUU/Epic|1. Definir un horario de consulta (docente)<br>2. Realizar inscripción a un horario de consulta (alumno)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Alumno<br>2. CRUD Docente<br>3. CRUD Materia<br>5. CRUD Dictado (depende de CRUD Docente y CRUD Materia)<br>5. CRUD Consulta (depende de CRUD Dictado)<br>6. CRUD Calificacion (depende de CRUD Consulta)|
|CUU/Epic|1. Definir un horario de consulta (docente)<br>2. Realizar inscripción a un horario de consulta (alumno)<br>3. Cancelar un horario de consulta (docente)<br>4. Eliminar inscripción a un horario de consulta (alumno)|


### Alcance Adicional Voluntario

\-
