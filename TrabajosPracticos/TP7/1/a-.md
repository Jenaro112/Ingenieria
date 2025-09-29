```mermaid
%%{init: {'theme': 'default'}}%%
usecaseDiagram
    actor Cliente

    rectangle SistemaDeGestionDeTickets {
        usecase (Registrar nuevo cliente)
        usecase (Iniciar sesión)
        usecase (Cambiar contraseña)
        usecase (Actualizar datos de cliente)
        usecase (Abrir nuevo ticket)
        usecase (Actualizar ticket)
        usecase (Consultar tickets existentes)
        usecase (Borrar ticket)
    }

    Cliente --> (Registrar nuevo cliente)
    Cliente --> (Iniciar sesión)
    Cliente --> (Cambiar contraseña)
    Cliente --> (Actualizar datos de cliente)
    Cliente --> (Abrir nuevo ticket)
    Cliente --> (Actualizar ticket)
    Cliente --> (Consultar tickets existentes)
    Cliente --> (Borrar ticket)

    (Registrar nuevo cliente) .> (Iniciar sesión) : <<extend>>
    (Iniciar sesión) .> (Abrir nuevo ticket) : <<include>>
    (Iniciar sesión) .> (Actualizar ticket) : <<include>>
    (Iniciar sesión) .> (Consultar tickets existentes) : <<include>>
    (Iniciar sesión) .> (Borrar ticket) : <<include>>
```