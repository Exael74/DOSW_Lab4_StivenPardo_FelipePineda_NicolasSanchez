# Planeación del Sistema

## Desglose de trabajo: Épicas, Historias de Usuario y Tareas

La implementación de los requerimientos identificados de Bankify se desglosa de la siguiente manera:

### 1. Épica:
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-1 (EP-01) |
| **Título** | Gestión Integral de Cuentas Bancarias y Operaciones Básicas |
| **Descripción** | Bankify requiere un sistema centralizado que permita registrar cuentas con validaciones de 10 dígitos, consultar saldos y realizar depósitos vía PSE para validar su modelo de negocio. |
| **Stakeholder** | Gerente de Operaciones de Bankify |

### 2. Historias de usuario:

#### HU-01
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-2 (HU-01) |
| **Título** | Registro de Cuenta |
| **Descripción** | Como Asesor, quiero registrar una cuenta nueva para vincular clientes al sistema. |
| **Prioridad** | Alta |
| **Estimación** | 5 Puntos de historia |

#### HU-02
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-3 (HU-02) |
| **Título** | Consulta de Saldo |
| **Descripción** | Como Cliente, quiero consultar mi saldo para conocer mi estado financiero actual. |
| **Prioridad** | Media |
| **Estimación** | 3 Puntos de historia |

#### HU-03
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-4 (HU-03) |
| **Título** | Depósito PSE |
| **Descripción** | Como Usuario, quiero realizar un depósito vía PSE para recargar fondos de forma segura. |
| **Prioridad** | Alta |
| **Estimación** | 8 Puntos de historia |

#### HU-04
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-5 (HU-04) |
| **Título** | Inactivar Cuenta |
| **Descripción** | Como Cliente, quiero inactivar mi cuenta para dejar de usar los servicios temporalmente. |
| **Prioridad** | Baja |
| **Estimación** | 2 Puntos de historia |

*(Nota sobre el video de Planning Poker: El equipo hace uso del "Poder de no hacer el video" otorgado previamente durante la clase, por lo que este requisito se encuentra validado y eximido de entrega).*

### 3. Tareas:

#### Tareas HU-01
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-6 (TR-01-01) |
| **Título** | Diseño de formulario |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Diseñar el formulario de captura de datos de cuenta. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-7 (TR-01-02) |
| **Título** | Implementación de validaciones |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Implementar lógica de validación (10 dígitos y código de banco 01/02). |
| **Tareas requisito** | TR-01-01 |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-8 (TR-01-03) |
| **Título** | Endpoint de registro |
| **ID de la Historia de Uso asociada** | HU-01 |
| **Descripción** | Crear el endpoint (API) para persistir la cuenta en la base de datos. |
| **Tareas requisito** | TR-01-02 |

#### Tareas HU-02
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-9 (TR-02-01) |
| **Título** | Diseño de visualización |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Diseñar la interfaz de visualización de saldo disponible. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-10 (TR-02-02) |
| **Título** | Servicio de consulta |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Implementar el servicio de consulta que recupere el balance desde la DB. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-11 (TR-02-03) |
| **Título** | Validación de seguridad |
| **ID de la Historia de Uso asociada** | HU-02 |
| **Descripción** | Aplicar validación de seguridad para asegurar que el cliente solo vea su propia información. |
| **Tareas requisito** | TR-02-02 |

#### Tareas HU-03
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-12 (TR-03-01) |
| **Título** | Integración pasarela |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Configurar la integración técnica con el simulador de pasarela PSE. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-13 (TR-03-02) |
| **Título** | Validación de montos |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Implementar validación de montos (solo valores positivos). |
| **Tareas requisito** | TR-03-01 |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-14 (TR-03-03) |
| **Título** | Lógica de actualización |
| **ID de la Historia de Uso asociada** | HU-03 |
| **Descripción** | Desarrollar la lógica de actualización automática del saldo tras la confirmación del pago. |
| **Tareas requisito** | TR-03-02 |

#### Tareas HU-04
| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-15 (TR-04-01) |
| **Título** | Opción panel de perfil |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Añadir la opción "Inactivar cuenta" en el panel de configuración del perfil. |
| **Tareas requisito** | Ninguna |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-16 (TR-04-02) |
| **Título** | Actualización de estado DB |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Crear el proceso de actualización de estado en la base de datos. |
| **Tareas requisito** | TR-04-01 |

| Campo | Descripción |
| :--- | :--- |
| **ID** | BANK-17 (TR-04-03) |
| **Título** | Bloqueo de servicios |
| **ID de la Historia de Uso asociada** | HU-04 |
| **Descripción** | Implementar bloqueos en los servicios de depósito para cuentas en estado inactivo. |
| **Tareas requisito** | TR-04-02 |


## Justificación de Prioridades
* **Alta (HU-01, HU-03):** El registro es la base funcional del sistema y el depósito PSE representa la entrada de capital, ambos críticos para el negocio.
* **Media (HU-02):** Es fundamental para la experiencia del usuario, pero depende de la existencia de cuentas y saldos previos.
* **Baja (HU-04):** Es una funcionalidad importante de gestión, pero no impide la operación principal del banco en su fase inicial (MVP).
