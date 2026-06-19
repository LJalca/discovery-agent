# Requisitos Candidatos — Rendimiento de Pescado

> Generado por `/discovery:analyze discoveries/rendimientopescado`  
> Fuente de evidencia: `interviews/recepcion.md`, `interviews/jefe-produccion.md`, `interviews/bodega-producto-terminado.md`

---

## Requisitos funcionales

- **[R-01]** Registrar digitalmente el peso de cada caja o lote al momento de la descarga en recepción, sin depender de planilla de papel.
  - Tipo: funcional
  - Origen: `recepcion.md` · Operador de Recepción

- **[R-02]** Calcular y mostrar automáticamente el total de kilos ingresados por día y por turno en recepción de materia prima.
  - Tipo: funcional
  - Origen: `recepcion.md` · Operador de Recepción

- **[R-03]** Registrar la diferencia entre el peso declarado por el proveedor y el peso medido internamente en cada recepción.
  - Tipo: funcional
  - Origen: `recepcion.md` · Operador de Recepción

- **[R-04]** Calcular y mostrar el rendimiento del proceso (kilos de lomo limpio / kilos de materia prima) en tiempo real durante el turno.
  - Tipo: funcional
  - Origen: `jefe-produccion.md` · Jefe de Producción

- **[R-05]** Notificar al Jefe de Producción cuando el rendimiento cae por debajo de un umbral configurable, sin esperar al cierre de turno.
  - Tipo: funcional
  - Origen: `jefe-produccion.md` · Jefe de Producción

- **[R-06]** Registrar el ingreso de cada pallet a bodega de producto terminado con su identificación: presentación, peso, fecha de producción.
  - Tipo: funcional
  - Origen: `bodega-producto-terminado.md` · Responsable de Bodega PT

- **[R-07]** Mantener un inventario de stock en tiempo real en bodega de producto terminado, actualizado con cada entrada y salida.
  - Tipo: funcional
  - Origen: `bodega-producto-terminado.md` · Responsable de Bodega PT

- **[R-08]** Notificar a bodega de producto terminado cuando producción genera nuevos pallets listos para ingresar.
  - Tipo: funcional
  - Origen: `bodega-producto-terminado.md` · Responsable de Bodega PT

- **[R-09]** Generar un reporte de rendimiento por turno que consolide kilos de materia prima ingresados, kilos procesados y kilos de lomo obtenidos, para presentar a gerencia.
  - Tipo: funcional
  - Origen: `jefe-produccion.md` · Jefe de Producción / Stakeholder: Gerencia

---

## Requisitos no funcionales

- **[R-10]** Todos los registros de peso deben usar kilogramos como unidad única; el sistema no debe aceptar entradas en unidades distintas.
  - Tipo: no funcional
  - Origen: `jefe-produccion.md` · Supervisores de turno (inconsistencia kilos vs. libras)

- **[R-11]** Los datos ingresados en recepción y en línea de producción deben estar disponibles para consulta en menos de 60 segundos desde el registro.
  - Tipo: no funcional
  - Origen: `jefe-produccion.md` · Jefe de Producción (retraso de horas actualmente)

- **[R-12]** El sistema debe funcionar en condiciones de frío y humedad propias de una planta pesquera (pantalla legible, interfaz resistente a guantes o entorno húmedo).
  - Tipo: no funcional
  - Origen: `recepcion.md` · Operador de Recepción (papeles se mojan)

---

## Resumen de trazabilidad

| ID   | Persona/Stakeholder origen          | Entrevista fuente                  |
|------|-------------------------------------|------------------------------------|
| R-01 | Operador de Recepción               | recepcion.md                       |
| R-02 | Operador de Recepción               | recepcion.md                       |
| R-03 | Operador de Recepción               | recepcion.md                       |
| R-04 | Jefe de Producción                  | jefe-produccion.md                 |
| R-05 | Jefe de Producción                  | jefe-produccion.md                 |
| R-06 | Resp. Bodega PT                     | bodega-producto-terminado.md       |
| R-07 | Resp. Bodega PT                     | bodega-producto-terminado.md       |
| R-08 | Resp. Bodega PT                     | bodega-producto-terminado.md       |
| R-09 | Jefe de Producción / Gerencia       | jefe-produccion.md                 |
| R-10 | Supervisores de turno               | jefe-produccion.md                 |
| R-11 | Jefe de Producción                  | jefe-produccion.md                 |
| R-12 | Operador de Recepción               | recepcion.md                       |
