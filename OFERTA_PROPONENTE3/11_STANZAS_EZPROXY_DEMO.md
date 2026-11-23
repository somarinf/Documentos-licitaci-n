# STANZAS / CONFIGURACIÓN DEMO EZPROXY

**Nota Técnica 2 — Configuración DEMO EZproxy**

**Empresa proponente:** SMF & NRO Soluciones de Información Académica S.A.S.  
**Servicio:** Base de datos en línea ProQuest  
**Universidad:** Universidad de Cundinamarca

## Propósito

La siguiente configuración permite habilitar el acceso remoto seguro a los recursos de ProQuest mediante EZproxy, permitiendo que los usuarios autorizados de la Universidad accedan desde fuera de la red institucional.

## Configuración DEMO

```ezproxy
Title ProQuest
URL https://www.proquest.com
Host www.proquest.com
Host search.proquest.com
Host gateway.proquest.com
Host ezproxy.simulacion.edu.co

Allow REMOTE_ADDR
Deny *
```

## Parámetros de acceso

| Parámetro | Valor |
|---|---|
| Dominio institucional | @unicundinamarca.edu.co |
| Método de autenticación | EZproxy / Shibboleth según disponibilidad |
| Acceso remoto | Habilitado |
| Acceso simultáneo | Según licenciamiento ProQuest |
| Recurso habilitado | ProQuest |
| Vigencia | Un (1) año |

## Consideraciones técnicas

- La configuración deberá ajustarse al dominio y a la infraestructura real de la Universidad.
- Se realizarán pruebas de acceso desde la red institucional y desde conexiones externas.
- Se entregará documentación de configuración y soporte.
- La configuración demo cumple los requisitos técnicos solicitados en la Nota Técnica 2.

Cali, 23 de noviembre de 2026.

**Sofía Marín Franco**  
Representante Legal  
SMF & NRO Soluciones de Información Académica S.A.S.