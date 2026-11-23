# STANZAS Y CONFIGURACIÓN DEMO EZPROXY (NOTA TÉCNICA 2)

> **SIMULACIÓN ACADÉMICA.** El oferente debe presentar las stanzas o medios para configurar un DEMO mediante el EZproxy de la Universidad, con el fin de realizar pruebas de uso, funcionamiento, contenido y acceso. Ajustar hosts/dominios a los reales del servicio.

---

## 1. DESCRIPCIÓN

Se entregan a continuación las **stanzas de configuración** para el servidor **EZproxy** de la Universidad de Cundinamarca, que permiten el acceso remoto autenticado a los recursos ofertados, así como los datos para habilitar un **ambiente DEMO** de pruebas.

## 2. DATOS PARA EL DEMO

| Parámetro | Valor (DEMO) |
|-----------|--------------|
| URL de acceso DEMO | https://demo.[proveedor].com/ucundinamarca |
| Usuario de prueba | demo_ucundinamarca |
| Contraseña de prueba | [se entrega por canal seguro] |
| Vigencia del DEMO | [30] días desde la activación |
| Método de autenticación | IP institucional + Proxy (EZproxy) |
| Soporte durante DEMO | soporte@[proveedor].com / +57 3XX XXX XXXX |

## 3. STANZAS EZPROXY

```
# =========================================================
# Stanza: Base de datos de disertaciones y tesis (PQDT-like)
# =========================================================
Title ProQuest Dissertations & Theses Global
URL https://www.proquest.com
HJ proquest.com
HJ search.proquest.com
DJ proquest.com
Find <body
Replace <body onload="..."

# =========================================================
# Stanza: Academic Video Online (AVON-like)
# =========================================================
Title Academic Video Online
URL https://video.alexanderstreet.com
HJ alexanderstreet.com
HJ video.alexanderstreet.com
DJ alexanderstreet.com

# =========================================================
# Stanza: Academic Complete (eBooks)
# =========================================================
Title Ebook Central / Academic Complete
URL https://ebookcentral.proquest.com
HJ ebookcentral.proquest.com
DJ proquest.com

# =========================================================
# Stanza: RefWorks (gestor de referencias)
# =========================================================
Title RefWorks
URL https://refworks.proquest.com
HJ refworks.proquest.com
DJ proquest.com
HTTPHeader -request -process Referer
```

## 4. CONFIGURACIÓN DE RANGOS IP (ejemplo)

```
# Rangos IP de la Universidad de Cundinamarca (ejemplo – reemplazar por los reales)
# Sede Fusagasugá
IncludeIP  xxx.xxx.0.0-xxx.xxx.255.255
# Seccionales y extensiones
IncludeIP  xxx.xxx.1.0-xxx.xxx.1.255
```

## 5. INSTRUCCIONES DE PRUEBA

1. Cargar las stanzas en el archivo `config.txt` del servidor EZproxy institucional.
2. Reiniciar el servicio EZproxy.
3. Acceder a la URL de DEMO desde la red institucional o mediante proxy.
4. Autenticarse con las credenciales de prueba suministradas.
5. Verificar: acceso al contenido, descarga, búsqueda, exportación de referencias y reproducción de video.

> **Nota:** Las stanzas aquí incluidas son ilustrativas para la simulación. En un caso real se deben entregar las stanzas oficiales del proveedor y validar con el administrador de EZproxy de la Universidad.

<br>

___________________________________
**SOFÍA MARÍN FRANCO**
Representante Legal — SMF & NRO Soluciones de Información Académica S.A.S.
