# User Stories — Rendimiento de Pescado

> Generado por `/discovery:generate-mvp discoveries/rendimientopescado`  
> Alcance: núcleo de valor (cadena recepción → rendimiento en producción).  
> Fuente de evidencia: `interviews/recepcion.md`, `interviews/jefe-produccion.md`, `interviews/bodega-producto-terminado.md`

---

## Historias del MVP (cadena de rendimiento)

- **[US-01]** Como operador de recepción de materia prima, quiero registrar digitalmente el peso de cada caja al descargar el camión para eliminar la planilla de papel y evitar pérdida o deterioro de los datos.
  - Criterios de aceptación:
    - Dado un camión en descarga, cuando ingreso el peso de una caja en el sistema, entonces el registro queda guardado con fecha, turno y número de caja sin depender de papel.
    - Dado que el entorno es húmedo y frío, cuando uso la pantalla de recepción, entonces puedo completar el registro con interfaz legible y usable en planta pesquera.
  - Fuente: `recepcion.md` · Requisito: R-01, R-12

- **[US-02]** Como operador de recepción de materia prima, quiero ver el total de kilos ingresados por día y por turno al cerrar la recepción para dejar de entregar estimados al jefe de producción.
  - Criterios de aceptación:
    - Dado que he registrado todas las cajas de una recepción, cuando consulto el resumen del turno, entonces veo el total exacto en kilogramos, no un aproximado.
    - Dado un día con varias recepciones, cuando consulto el acumulado del día, entonces veo la suma de kilos de todas las recepciones registradas.
  - Fuente: `recepcion.md` · Requisito: R-02

- **[US-03]** Como operador de recepción de materia prima, quiero registrar la diferencia entre el peso declarado por el proveedor y el peso medido internamente en cada recepción para poder demostrar discrepancias con datos, no con suposiciones.
  - Criterios de aceptación:
    - Dado una recepción con peso declarado por el proveedor, cuando ingreso el total medido internamente, entonces el sistema calcula y muestra la diferencia en kilogramos.
    - Dado una recepción con diferencia registrada, cuando consulto el historial, entonces puedo recuperar el detalle por proveedor y fecha.
  - Fuente: `recepcion.md` · Requisito: R-03

- **[US-04]** Como jefe de producción, quiero consultar el rendimiento del turno (kilos de lomo limpio / kilos de materia prima) en tiempo real para tomar decisiones antes del cierre de turno.
  - Criterios de aceptación:
    - Dado kilos de materia prima registrados en recepción y kilos de lomo reportados en línea, cuando consulto el panel de rendimiento, entonces veo el ratio actualizado en menos de 60 segundos desde el último registro.
    - Dado un turno en curso, cuando abro el panel, entonces todos los pesos se muestran únicamente en kilogramos, sin mezcla de unidades.
  - Fuente: `jefe-produccion.md` · Requisito: R-04, R-10, R-11

- **[US-05]** Como jefe de producción, quiero recibir una alerta cuando el rendimiento cae por debajo de un umbral configurable para corregir calidad de pescado, línea o corte antes de que sea tarde.
  - Criterios de aceptación:
    - Dado un umbral de rendimiento configurado, cuando el ratio acumulado del turno cae por debajo de ese umbral, entonces recibo una notificación visible sin esperar al cierre de turno.
    - Dado que recibo la alerta, cuando reviso el panel, entonces veo el rendimiento acumulado y la hora del último registro que disparó la caída.
  - Fuente: `jefe-produccion.md` · Requisito: R-05

- **[US-06]** Como jefe de producción, quiero generar un reporte de rendimiento por turno con kilos de materia prima, kilos procesados y kilos de lomo obtenidos para presentar cifras exactas a gerencia.
  - Criterios de aceptación:
    - Dado un turno cerrado con registros completos, cuando genero el reporte, entonces incluye kilos ingresados, kilos de lomo y rendimiento porcentual en una sola vista.
    - Dado el reporte generado, cuando lo exporto, entonces los datos provienen de los registros digitales del turno, no de estimados manuales.
  - Fuente: `jefe-produccion.md` · Requisito: R-09

---

## Historias fuera del MVP (evidenciadas, pendientes de fase 2)

Estas historias están respaldadas por entrevistas pero no entran en el MVP inicial porque atacan el dolor de bodega de producto terminado, un flujo distinto al núcleo de rendimiento.

- **[US-07]** Como responsable de bodega de producto terminado, quiero registrar cada pallet con presentación, peso y fecha de producción para identificar stock sin revisar físicamente la cámara. *(bodega-producto-terminado.md · R-06)*

- **[US-08]** Como responsable de bodega de producto terminado, quiero un inventario actualizado con cada entrada y salida para no comprometer stock que ya salió. *(bodega-producto-terminado.md · R-07)*

- **[US-09]** Como responsable de bodega de producto terminado, quiero que producción me avise cuando genera pallets listos para ingresar y poder planificar espacio y carga de trabajo. *(bodega-producto-terminado.md · R-08)*
