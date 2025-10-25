# Modelo Relacional
Las siguientes relaciones (tablas) fueron obtenidas a partir del [Modelo Entidad-Relación](/docs/Modelo_Entidad-Relacion.png) mostrado en el archivo [proposal.md](/proposal.md)

Administradores(nombre, apellido, **correo**) \
&nbsp;&nbsp;&nbsp;&nbsp;correo → CP

Alumnos(**legajoAlumno**, nombre, apellido, correo, password) \
&nbsp;&nbsp;&nbsp;&nbsp;legajoAlumno → CP

Docentes(**legajoDocente**, nombre, apellido, correo, password) \
&nbsp;&nbsp;&nbsp;&nbsp;legajoDocente → CP

Materias(**idMateria**, descripcion) \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria → CP

EstadosConsulta(**idEstado**, descripcion) \
&nbsp;&nbsp;&nbsp;&nbsp; idEstado → CP

Dictados(**idMateria**, **legajoDocente**) \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente → CP \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria → CF(Materias) NN

Consulta(**idMateria**, **legajoDocente**, **nroConsulta**, horaInicio, horaFin, estado) \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente, nroConsulta → CP \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente → CF(Dictados) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria → CF(Materias) NN \
&nbsp;&nbsp;&nbsp;&nbsp;legajoDocente → CF(Docentes) NN \
&nbsp;&nbsp;&nbsp;&nbsp;estado → CF(EstadosConsultas(idEstado)) NN

Inscripciones(**legajoAlumno**, **idMateria**, **legajoDocente**, **nroConsulta**) \
&nbsp;&nbsp;&nbsp;&nbsp;legajoAlumno, idMateria, legajoDocente, nroConsulta → CP \
&nbsp;&nbsp;&nbsp;&nbsp;legajoAlumno → CF(Alumnos) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente, nroConsulta → CF(Consulta) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente → CF(Dictados) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria → CF(Materias) NN \
&nbsp;&nbsp;&nbsp;&nbsp;legajoDocente → CF(Docentes) NN

Calificacion(**idMateria**, **legajoDocente**, **nroConsulta**, **nroCalificacion**, valor) \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente, nroConsulta, nroCalificacion → CP \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente, nroConsulta → CF(Consulta) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria, legajoDocente → CF(Dictados) NN \
&nbsp;&nbsp;&nbsp;&nbsp;idMateria → CF(Materias) NN \
&nbsp;&nbsp;&nbsp;&nbsp;legajoDocente → CF(Docentes) NN