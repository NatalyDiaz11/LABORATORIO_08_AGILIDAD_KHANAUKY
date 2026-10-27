# Flujo real aplicado en Khanauky

## Caso seleccionado

Para demostrar la aplicación del enfoque ágil en Khanauky se tomó como ejemplo la funcionalidad:

**Generar alerta de stock mínimo.**

Esta funcionalidad forma parte del control de inventario y busca informar a Almacén cuando la cantidad disponible de un producto queda por debajo del stock mínimo definido.

## Flujo aplicado

### 1. Product Backlog

La funcionalidad se registra como una necesidad del sistema dentro del conjunto de actividades pendientes.

Elemento del backlog:

- Generar alerta de stock mínimo.

### 2. Selección para el trabajo

La funcionalidad se prioriza porque está relacionada con el control de existencias y permite detectar posibles faltantes de productos.

La actividad pasa del backlog general al trabajo del Sprint.

### 3. En proceso

Durante el desarrollo se revisan los elementos relacionados con la funcionalidad:

- Requisito REQ-003.
- Caso de uso CU-002: Atender pedido.
- Clase CLS-Stock.
- Pruebas relacionadas con el control de stock.

Se define que el sistema debe verificar el stock disponible de cada producto y generar una alerta informativa cuando la cantidad quede por debajo del mínimo definido.

### 4. Validación

Para comprobar el comportamiento se consideran las siguientes pruebas:

- PRU-003a: stock por encima o igual al mínimo definido.
- PRU-003b: stock por debajo del mínimo definido.
- PRU-003c: producto sin stock mínimo configurado.

PRU-003c verifica que, cuando un producto no tiene un stock mínimo configurado, el sistema informe esta condición, permita continuar con la atención del pedido y no genere la alerta.

### 5. En revisión

Una vez realizados los cambios, la funcionalidad pasa al estado En revisión.

En esta etapa se verifica la coherencia entre el requisito, el caso de uso, la clase y las pruebas.

También se revisa que la alerta no impida continuar con la atención del pedido, ya que su propósito es informar a Almacén.

### 6. Correcciones

Si durante la revisión se detectan observaciones, estas se corrigen antes de considerar la funcionalidad terminada.

Entre las mejoras identificadas se encuentran:

- Validar el stock mínimo por cada producto.
- Diferenciar la validación del stock de la generación de la alerta.
- Considerar productos que no tienen stock mínimo configurado.

### 7. Terminado

Cuando la funcionalidad cumple con lo definido y las observaciones han sido atendidas, la tarea puede pasar al estado Terminado.

El flujo utilizado queda representado de la siguiente manera:

Product Backlog → Pendiente → En proceso → En revisión → Terminado

## Aplicación en el tablero Kanban

En GitHub Projects se utiliza el tablero Kanban del proyecto Khanauky con cuatro estados:

- Pendiente.
- En proceso.
- En revisión.
- Terminado.

La funcionalidad "Generar alerta de stock mínimo" se encuentra actualmente en En revisión, representando una actividad que ya fue desarrollada pero que todavía requiere validación antes de pasar a Terminado.

## Conclusión

El flujo aplicado permite visualizar el avance de una funcionalidad desde su identificación hasta su finalización. Este enfoque facilita controlar el trabajo, detectar observaciones y realizar ajustes antes de considerar una tarea completada.
