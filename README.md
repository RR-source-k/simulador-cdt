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

## Estructura del Repositorio

* `simulador_cdt.ipynb`: Notebook ejecutable con el código fuente del simulador e interfaz Gradio.
* `README.md`: Documentación del proyecto.

## Requisitos e Instalación

### Requisitos previos

* Python 3.x
* Jupyter Notebook, JupyterLab o entorno compatible (Google Colab, VS Code).

### Instalación de dependencias

Asegúrate de instalar la librería `gradio` ejecutando en tu terminal o celda del notebook:

```bash
pip install gradio
```

## Uso

1. Abre el notebook principal:

```bash
jupyter notebook simulador_cdt.ipynb
```

*(También puedes abrirlo directamente en Google Colab o VS Code).*

2. Ejecuta la celda principal dentro del archivo `simulador_cdt.ipynb`.

3. Al ejecutarse, Gradio desplegará la interfaz gráfica (localmente o mediante un enlace público de Gradio si utilizas Colab) para interactuar con la herramienta.

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
