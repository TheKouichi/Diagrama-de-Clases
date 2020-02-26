Empresa - Empleado - Cliente
===

``` mermaid

classDiagram
    Persona <|-- Empleado
    Persona <|-- Cliente
    Empleado <|-- Directivo
    Empleado "0..*" -- "0..*" Directivo : subordinados
    Empresa "1..*" o-- "0..*" Cliente : clientes
    Empresa "1" *-- "1..*" Empleado : empleados

    class Empleado{
        -sueldo_bruto : String
        +mostrar() void
        +calcular_salario_neto() void
    }

    class Persona{
        -nombre : String
        -edad : String
        +mostrar() void
    }

    class Cliente{
        -telefono : INTEGER
        +mostrar() void
    }

    class Directivo{
        -categoria: String
        +mostrar() void
    }

    class Empresa{
        -nombre : String
    }