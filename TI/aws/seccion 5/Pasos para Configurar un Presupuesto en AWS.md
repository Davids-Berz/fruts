#### Paso 1: Acceder a la Consola de AWS Budgets

1. Inicia sesión en la [Consola de administración de AWS](https://aws.amazon.com/console/).
2. En el menú de servicios, busca y selecciona **Budgets** o **Presupuestos**.

#### Paso 2: Crear un Nuevo Presupuesto

1. En la consola de AWS Budgets, haz clic en **Create budget** (Crear presupuesto).
    
2. Selecciona el tipo de presupuesto que deseas crear. AWS Budgets ofrece varios tipos de presupuestos:
    
    - **Cost Budget**: Para controlar los costos.
    - **Usage Budget**: Para controlar el uso de servicios.
    - **Savings Plans Budget**: Para controlar los ahorros.
    - **RI Utilization Budget**: Para controlar la utilización de instancias reservadas.
    - **RI Coverage Budget**: Para controlar la cobertura de instancias reservadas.
    - **Savings Plans Utilization Budget**: Para controlar la utilización de Savings Plans.
    - **Savings Plans Coverage Budget**: Para controlar la cobertura de Savings Plans.
3. Para este ejemplo, seleccionaremos **Cost Budget**.
    

#### Paso 3: Configurar los Detalles del Presupuesto

1. **Name your budget**: Proporciona un nombre descriptivo para tu presupuesto, como "Presupuesto Mensual de AWS".
2. **Period**: Selecciona la periodicidad de tu presupuesto:
    - Monthly (Mensual)
    - Quarterly (Trimestral)
    - Annually (Anual)
3. **Start Month**: Selecciona el mes de inicio para tu presupuesto.
4. **Budgeted Amount**: Introduce la cantidad presupuestada (por ejemplo, $200).

#### Paso 4: Establecer Alertas

1. **Alerts and Notifications**:
    
    - **Set up alerts**: Puedes configurar alertas para recibir notificaciones cuando tu gasto se acerque o supere el presupuesto.
    - **Thresholds**: Define los umbrales de alerta. Por ejemplo, recibir una alerta al 80% y 100% del presupuesto.
    - **Subscribers**: Introduce las direcciones de correo electrónico de los destinatarios que recibirán las alertas.
2. **Create notification**:
    
    - Haz clic en **Create notification** para cada umbral de alerta que desees configurar.

#### Paso 5: Revisar y Crear el Presupuesto

1. **Review your budget**: Revisa los detalles de tu presupuesto y las alertas configuradas.
2. Haz clic en **Create budget** para finalizar la configuración.