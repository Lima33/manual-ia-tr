# 💡 Entrenamiento: Análisis de Datos (Operations)

**Misión:** Transformar datos brutos, estructurados y no estructurados, en insights que impulsen decisiones de negocio.

---

??? tip "Entrenamiento 1: Cruzar Datos para Encontrar la Causa Raíz"

    **El Desafío:** Tenemos datos de encuestas NPS (sentimiento) y datos de uso del producto (comportamiento), pero no sabemos cómo se conectan.

    **La Técnica (Prompt para Aplicar):**
    ```text
    Actúa como un Analista de Datos de Operaciones (Data Ops). Te proporcionaré dos tipos de datos sobre un grupo de clientes.

    **Dato 1 (No Estructurado - NPS):**
    - Cliente A (NPS 5): "La herramienta es lenta para generar reportes."
    - Cliente B (NPS 9): "Me encanta la función de importación."
    - Cliente C (NPS 6): "El reporteador es muy confuso."

    **Dato 2 (Estructurado - Uso):**
    - Cliente A: Frecuencia de uso de "Reportes": 20 intentos/semana.
    - Cliente B: Frecuencia de uso de "Importación": 15/semana.
    - Cliente C: Frecuencia de uso de "Reportes": 1 intento/semana.

    Tu tarea es:
    1.  Cruzar la información.
    2.  Generar un insight accionable.
    3.  Formular una hipótesis clara.

    **Ejemplo de Salida Esperada:**
    "**Insight:** Los clientes con bajo NPS (A y C) se quejan del módulo de reportes. **Hipótesis:** El Cliente A es un 'power user' frustrado por la lentitud, mientras que el Cliente C es un usuario que ha abandonado la función por su complejidad. Debemos abordar la performance y la usabilidad del módulo de reportes."
    ```

---

??? tip "Entrenamiento 2: Curar Datos y Proponer Mejoras de Valor"

    **El Desafío:** El mercado evoluciona. Necesitamos analizar las peticiones de los clientes para guiar el futuro del producto.

    **La Técnica (Prompt para Aplicar):**
    ```text
    Actúa como un Product Manager Estratégico.

    He recopilado una lista de 50 peticiones de funcionalidades de nuestros clientes en los últimos 6 meses.

    Analiza la siguiente lista y realiza estas tareas:
    1.  **Curación de Datos:** Agrupa las peticiones en 3 a 5 categorías temáticas.
    2.  **Propuesta de Valor:** Identifica la categoría más solicitada y describe en una frase el "dolor" del cliente que hay detrás.
    3.  **Sugerencia de Roadmap:** Propón una nueva funcionalidad para el roadmap del próximo trimestre que solucione ese dolor.

    Peticiones de los Clientes:
    "[Pega aquí la lista de peticiones]"
    ```