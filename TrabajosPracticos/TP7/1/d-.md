```mermaid
stateDiagram-v2
    [*] --> Registrado
    Registrado --> Activo: Activación completada
    Activo --> Bloqueado: Intentos fallidos o suspensión
    Bloqueado --> Activo: Rehabilitación
    Activo --> Baja: Eliminación de cuenta
    Baja --> [*]

```