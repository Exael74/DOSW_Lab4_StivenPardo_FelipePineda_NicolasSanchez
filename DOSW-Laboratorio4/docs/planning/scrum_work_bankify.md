# Planeación de Trabajo - Proyecto Bankify


## 1. Épica
| Campo | Descripción |
| :--- | :--- |
| **ID** | EP-01 |
| **Título** | Gestión Integral de Cuentas Bancarias y Operaciones Básicas |
| **Descripción** | Bankify requiere un sistema centralizado que permita registrar cuentas con validaciones de 10 dígitos, consultar saldos y realizar depósitos vía PSE para validar su modelo de negocio. |
| **Stakeholder** | Gerente de Operaciones de Bankify |

## 2. Historias de Usuario (HUs)
*Nota: Según las instrucciones de la Parte 2, la estimación se deja vacía en este paso.*

| ID | Título | Descripción (Como... quiero... para...) | Prioridad | Estimación |
| :--- | :--- | :--- | :--- | :--- |
| **HU-01** | Registro de Cuenta | Como **Asesor**, quiero **registrar una cuenta nueva** para **vincular clientes al sistema**. | **Alto** | |
| **HU-02** | Consulta de Saldo | Como **Cliente**, quiero **consultar mi saldo** para **conocer mi estado financiero actual**. | **Medio** | |
| **HU-03** | Depósito PSE | Como **Usuario**, quiero **realizar un depósito vía PSE** para **recargar fondos de forma segura**. | **Alto** | |
| **HU-04** | Inactivar Cuenta | Como **Cliente**, quiero **inactivar mi cuenta** para **dejar de usar los servicios temporalmente**. | **Bajo** | |

## 3. Tareas Técnicas
*Se han identificado al menos 3 tareas por cada historia de usuario.*

### HU-01: Registro de Cuenta
* **Tarea 1:** Diseñar el formulario de captura de datos de cuenta.
* **Tarea 2:** Implementar lógica de validación (10 dígitos y código de banco 01/02).
* **Tarea 3:** Crear el endpoint (API) para persistir la cuenta en la base de datos.

### HU-02: Consulta de Saldo
* **Tarea 1:** Diseñar la interfaz de visualización de saldo disponible.
* **Tarea 2:** Implementar el servicio de consulta que recupere el balance desde la DB.
* **Tarea 3:** Aplicar validación de seguridad para asegurar que el cliente solo vea su propia información.

### HU-03: Depósito PSE
* **Tarea 1:** Configurar la integración técnica con el simulador de pasarela PSE.
* **Tarea 2:** Implementar validación de montos (solo valores positivos).
* **Tarea 3:** Desarrollar la lógica de actualización automática del saldo tras la confirmación del pago.

### HU-04: Inactivar Cuenta
* **Tarea 1:** Añadir la opción "Inactivar cuenta" en el panel de configuración del perfil.
* **Tarea 2:** Crear el proceso de actualización de estado en la base de datos.
* **Tarea 3:** Implementar bloqueos en los servicios de depósito para cuentas en estado inactivo.

## 4. Justificación de Prioridades
* **Alta (HU-01, HU-03):** El registro es la base funcional del sistema y el depósito PSE representa la entrada de capital, ambos críticos para el negocio.
* **Media (HU-02):** Es fundamental para la experiencia del usuario, pero depende de la existencia de cuentas y saldos previos.
* **Baja (HU-04):** Es una funcionalidad importante de gestión, pero no impide la operación principal del banco en su fase inicial (MVP).