```mermaid
sequenceDiagram
    participant Cliente
    participant ControladorCliente
    participant ClienteDAO
    participant TicketDAO

    Cliente->>ControladorCliente: Solicitar ingreso
    ControladorCliente->>ClienteDAO: Validar datos
    ClienteDAO-->>ControladorCliente: Datos validados
    ControladorCliente->>TicketDAO: Crear ticket inicial
    TicketDAO-->>ControladorCliente: Ticket creado
    ControladorCliente-->>Cliente: Confirmar ingreso

```