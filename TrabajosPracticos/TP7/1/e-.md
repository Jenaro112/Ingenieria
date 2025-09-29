```mermaid
stateDiagram-v2
    [*] --> Abierto
    Abierto --> En_Proceso: Asignado a técnico
    En_Proceso --> Resuelto: Solución implementada
    Resuelto --> Cerrado: Cliente confirma solución
    Cerrado --> [*]

```