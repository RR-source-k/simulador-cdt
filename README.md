# Simulador y Proyector Financiero de CDT

Un simulador interactivo desarrollado en Python con Gradio para realizar proyecciones financieras de Certificados de Depósito a Término (CDT). La aplicación permite crear, editar, visualizar y exportar análisis de rentabilidad con proyección mes a mes.

## Autor

* **Estudiante:** Erick Santiago Rincón Rojas
* **Código:** 01251151002

## Características Principales

* **Cálculo Dinámico de Tasas:** La tasa mensual se calcula de acuerdo con el plazo en meses utilizando la fórmula lineal:

  `Tasa (%) = 0.001695 * plazo + 0.0983`

* **Gestión de Escenarios (CRUD):**
  * **Crear:** Agrega múltiples escenarios con diferentes montos iniciales y plazos.
  * **Editar:** Modifica monto o plazo de un escenario existente usando su ID.
  * **Eliminar:** Remueve escenarios por su ID único.

* **Proyección Mes a Mes:** Cálculo de interés compuesto proyectado periodo a periodo.

* **Exportación de Datos:**
  * Exportar resumen de escenarios a `escenarios_cdt.csv`.
  * Exportar desglose detallado mes a mes a `proyecciones_cdt.csv`.

* **Formato de Moneda:** Formateo automático a pesos colombianos (COP).

## Tecnologías Utilizadas

* **Python 3.x**
* **Gradio** (Interfaz web interactiva)
* **CSV** (Módulo estándar para manejo e impresión de archivos CSV)

## Instalación y Requisitos

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/simulador-cdt.git
   cd simulador-cdt
   ```

2. **Instalar dependencias:**
   Asegúrate de tener instalada la librería `gradio`:
   ```bash
   pip install gradio
   ```

## Uso

Ejecuta el script principal o corre la celda en Google Colab / Jupyter Notebook:

```bash
python main.py
```

Al ejecutarse, Gradio generará una interfaz web local (y una URL pública temporal si ejecutas desde Google Colab) para interactuar con la herramienta.

### Interfaz de la Aplicación

1. **Pestaña Escenarios:**
   * Ingresa monto y plazo para calcular un nuevo CDT.
   * Visualiza los escenarios creados en una tabla resumen.
   * Modifica o elimina registros usando el ID correspondiente.
   * Exporta la tabla de resumen a formato CSV.

2. **Pestaña Proyecciones:**
   * Revisa la tabla de capitalización e intereses calculados mes por mes.
   * Exporta las proyecciones detalladas a CSV.

## Licencia

Este proyecto fue desarrollado con fines académicos.
