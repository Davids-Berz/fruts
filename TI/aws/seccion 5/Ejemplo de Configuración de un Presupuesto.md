A continuación se muestra un ejemplo de configuración de un presupuesto mensual de $200 con alertas al 80% y 100% del presupuesto:

```
{
    "BudgetName": "Presupuesto Mensual de AWS",
    "BudgetLimit": {
        "Amount": 200,
        "Unit": "USD"
    },
    "CostFilters": {},
    "CostTypes": {
        "IncludeTax": true,
        "IncludeSubscription": true,
        "UseBlended": false
    },
    "TimeUnit": "MONTHLY",
    "TimePeriod": {
        "Start": "2024-07-01T00:00:00Z",
        "End": "2025-07-01T00:00:00Z"
    },
    "Subscribers": [
        {
            "SubscriptionType": "EMAIL",
            "Address": "example@example.com"
        }
    ],
    "Notification": {
        "NotificationType": "ACTUAL",
        "ComparisonOperator": "GREATER_THAN",
        "Threshold": 80,
        "ThresholdType": "PERCENTAGE",
        "NotificationState": "ALARM"
    }
}
```

### Gestión de Presupuestos

Una vez creado el presupuesto, puedes gestionarlo y ajustarlo según sea necesario:

- **Ver Reportes**: Monitorea el uso y los costos actuales en comparación con el presupuesto definido.
- **Ajustar Presupuestos**: Modifica el monto presupuestado y los umbrales de alerta según las necesidades cambiantes de tu organización.
- **Análisis de Costos**: Utiliza AWS Cost Explorer junto con AWS Budgets para analizar los patrones de gastos y optimizar el uso de los recursos.