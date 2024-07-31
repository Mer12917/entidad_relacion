# Diagrama Entidad-Relación

```mermaid
erDiagram
    ENCUESTA {
        int Id PK
        varchar Enunciado_pregunta
        varchar Tipo_pregunta
        varchar Opciones
        int fk_encuestado FK
    }
    ENCUESTADO {
        int Id PK
        varchar Nombres
        varchar Apellidos
        varchar Correo
        int Edad
        char Sexo
        int Teléfono
        varchar Ciudad
        varchar Municipio
        varchar Departamento
    }
    ENCUESTA ||--o{ ENCUESTADO : contiene
