# Proyecto de Control Administrativo y Reportes de una Pesquera

**Caso práctico ficticio | Rawson, Chubut | Octubre de 2026**

## 1. Objetivo

Desarrollar un caso práctico que simule tareas administrativas habituales de una empresa pesquera, con foco en la recepción y validación de información, el control de desembarques, la conciliación documental y la elaboración de reportes.

El proyecto busca demostrar el uso de Excel para:

- Registrar desembarques, guías de transporte y lotes de producción.
- Relacionar datos mediante identificadores y tablas maestras.
- Detectar datos incompletos, duplicados, inconsistencias y valores fuera de rango.
- Comparar los kilos declarados en desembarques con los consignados en guías.
- Preparar indicadores mensuales y un dashboard para facilitar el seguimiento.
- Documentar incidencias y dejar trazabilidad de las correcciones.

## 2. Contexto ficticio

Se simula un mes de trabajo administrativo en una empresa pesquera inventada, ubicada en Rawson, provincia del Chubut. El período analizado es octubre de 2026.

El escenario contempla operaciones vinculadas principalmente con langostino y, en menor proporción, merluza común y otras especies. Se utilizan barcos, plantas, especies, guías y lotes identificados mediante códigos ficticios.

El conjunto de práctica incluye registros correctos y errores intencionales. Estos últimos permiten demostrar cómo se identifican, clasifican y documentan problemas de calidad de datos antes de utilizar la información en reportes.

## 3. Herramientas utilizadas

- **Microsoft Excel:** organización de datos, tablas, fórmulas, filtros, validaciones, formato condicional, indicadores y gráficos.
- **Fórmulas de Excel:** búsquedas y cruces de información, cálculos de diferencias y controles de consistencia. Se utilizan funciones como `BUSCARV`, `CONTAR.SI`, `SI`, `SUMAR.SI.CONJUNTO` y otras funciones de apoyo.
- **CSV:** formato de intercambio para las tablas de datos y para facilitar su reutilización.
- **SQL básico (como extensión del ejercicio):** el modelo de datos puede trasladarse a tablas relacionales para practicar consultas, uniones y agregaciones. El entregable principal de este repositorio es el libro de Excel; no se presupone una base de datos productiva.
- **Git y GitHub:** versionado y publicación del proyecto como portfolio.

> Las fórmulas del libro están escritas con nombres de funciones en español y separadores habituales de una configuración regional en español. Según la configuración de Excel, puede ser necesario adaptar nombres de funciones o separadores.

## 4. Estructura del repositorio

La siguiente es una estructura sugerida para publicar el proyecto. Los nombres pueden ajustarse a los archivos que finalmente se incorporen al repositorio.

```text
proyecto-pesquera-rawson/
├── README.md
├── datos/
│   ├── desembarques_diarios.csv
│   ├── guias_transporte.csv
│   ├── lotes_produccion.csv
│   └── maestros/
│       ├── maestro_barcos.csv
│       ├── maestro_especies.csv
│       └── maestro_plantas.csv
├── excel/
│   └── Proyecto_Administrativo_Pesquera_Rawson_Octubre_2026_dashboard_validaciones.xlsx
├── documentacion/
│   ├── estructura_y_diccionario_de_datos.md
│   └── supuestos_y_criterios_de_control.md
└── capturas/
    ├── dashboard.png
    └── validaciones_errores.png
```

**Nota:** esta estructura describe cómo organizar el repositorio en GitHub. Si algún CSV, captura o documento todavía no está incluido, debe agregarse antes de publicar o quitarse temporalmente del árbol para que coincida con el contenido real.

## 5. Cómo reproducir el Excel paso a paso

1. **Descargar el libro de Excel** incluido en la carpeta `excel/`.
2. **Abrirlo con Microsoft Excel** y habilitar la edición si el programa lo solicita. El archivo está configurado para recalcular las fórmulas al abrirse.
3. **Consultar `Inicio_Instrucciones`** para conocer el propósito de cada hoja y el flujo de trabajo.
4. **Revisar las tablas maestras:** `Maestro_Barcos`, `Maestro_Especies` y `Maestro_Plantas`. Estas hojas contienen los identificadores utilizados para relacionar los registros.
5. **Cargar o modificar los datos de práctica** en `Desembarques_Diarios`, `Guias_Transporte` y `Lotes_Produccion`. Para conservar los controles, respetar los encabezados, los formatos y los identificadores de las tablas.
6. **Verificar las fórmulas y controles** de las hojas operativas. Se calculan datos relacionados y se señalan posibles duplicados, valores negativos, fechas fuera del período, identificadores inexistentes, campos vacíos y diferencias documentales.
7. **Revisar `Validaciones_Errores`:** analizar las incidencias detectadas y documentar cualquier corrección con fecha, responsable, valor original, valor corregido y evidencia de respaldo. No reemplazar un dato sin verificar primero el documento fuente.
8. **Consultar `Reporte_Mensual`:** revisar los indicadores y resúmenes que alimentan los gráficos.
9. **Abrir `Dashboard`:** visualizar los principales indicadores y gráficos del período. Los indicadores de desembarque validado consideran únicamente los movimientos cuyo resultado de control es `OK`.
10. **Probar el modelo:** modificar una copia del archivo con algunos registros de prueba y observar cómo cambian las validaciones, los resúmenes y el dashboard. Mantener intacta una copia original para poder volver al escenario inicial.

Si se trabaja con los CSV, se pueden importar desde Excel mediante **Datos → Desde texto/CSV**. Conviene revisar el tipo de dato de las fechas, los separadores decimales y los identificadores antes de anexar registros.

## 6. Supuestos y limitaciones

- Todos los datos, nombres, códigos, barcos, plantas, guías, lotes y movimientos son inventados para fines educativos.
- El período de análisis es octubre de 2026. Se incluyen algunas incidencias intencionales, entre ellas duplicados, kilos negativos o vacíos, identificadores inexistentes, fechas fuera del período y diferencias entre desembarque y guía.
- Los objetivos o cuotas que pudieran aparecer en los datos son referencias ficticias de planificación. No representan cupos, permisos ni cuotas oficiales.
- La diferencia entre kilos desembarcados y kilos consignados en una guía es un control documental. Por sí sola no demuestra merma industrial, pérdida física ni irregularidad.
- La diferencia entre kilos desembarcados y kilos registrados en lotes es una diferencia administrativa de conciliación. No equivale necesariamente a rendimiento o merma del proceso productivo.
- Los totales sin filtrar pueden incluir registros con errores intencionales. Para los indicadores principales del dashboard se consideran los movimientos aprobados por los controles (`OK`).
- El dashboard utiliza resúmenes calculados mediante fórmulas y gráficos vinculados a esos rangos auxiliares. No son tablas dinámicas nativas.
- El libro no está conectado a sistemas de gestión, balanzas, documentación oficial ni bases de datos reales. La carga y revisión se realizan sobre información de práctica.
- Las reglas de control son criterios demostrativos y simplificados. No constituyen una auditoría integral ni reemplazan procedimientos internos, documentación respaldatoria o normativa aplicable.
- El resultado puede variar según la versión de Excel y la configuración regional. Se recomienda abrir el archivo en Excel y comprobar que las fórmulas se hayan recalculado.

## 7. Qué demuestra el proyecto

Este ejercicio permite mostrar habilidades aplicables a puestos administrativos, de carga de datos y soporte operativo:

- Organización de información en tablas estructuradas.
- Manejo de identificadores y tablas maestras.
- Búsqueda y cruce de datos con fórmulas.
- Control de calidad de datos y detección de inconsistencias.
- Conciliación básica de información entre registros relacionados.
- Seguimiento de incidencias y trazabilidad de correcciones.
- Elaboración de indicadores, resúmenes y gráficos para reportes.
- Presentación de información de forma clara para facilitar el control y la toma de decisiones.

También sirve como base para una segunda etapa con SQL: creación de tablas, definición de claves, consultas `SELECT`, filtros `WHERE`, uniones `JOIN`, agrupaciones `GROUP BY` y controles de duplicados o registros huérfanos.

## 8. Aclaración sobre los datos

**Este proyecto es íntegramente ficticio y fue creado con fines de práctica, aprendizaje y demostración de habilidades.** No contiene información operativa, comercial ni personal de empresas pesqueras reales. Los nombres, identificadores, cantidades, fechas, objetivos y situaciones del ejemplo no deben interpretarse como datos reales ni utilizarse para tomar decisiones operativas.

---

*Proyecto de portfolio — Control administrativo, calidad de datos y reportes en Excel.*
