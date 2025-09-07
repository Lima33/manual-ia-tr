# 🎯 Módulo: Prompting Avanzado - Más allá de la pregunta simple

**Ruta:** Nivel Intermedio
**Objetivo:** Aprender técnicas de prompting como "Cluster de Expertos" para obtener respuestas más profundas y analizar datos cualitativos como encuestas CSAT y NPS.

---

## ⚡ El Superpoder: De preguntar a dirigir a un equipo de expertos

Un prompt básico es una pregunta. Un prompt avanzado es una instrucción a un equipo de especialistas virtuales. Al darle a la IA un rol, un contexto y un formato de salida, la calidad de la respuesta se multiplica por diez.

> **Técnica Clave: El "Cluster de Expertos"**
> En lugar de pedir una sola cosa, le pides a la IA que actúe como varios expertos a la vez para analizar un problema desde diferentes ángulos.

---

### 案例 Caso de Éxito TR: Analizando el feedback de clientes de "La Ley Next"

Tenemos 50 respuestas de una encuesta NPS. Muchas son genéricas ("Buen servicio", "Podría mejorar"). ¿Cómo extraemos valor real de ahí?

**Prompt Básico:** "Resume este feedback de clientes." -> **Resultado:** Un resumen vago.

**Prompt Avanzado (Cluster de Expertos):**
Actúa como un cluster de tres expertos:
Analista de Datos Cualitativos: Lee todos los comentarios de la encuesta NPS sobre "La Ley Next" e identifica los 3 temas positivos y los 3 negativos más recurrentes.
Estratega de Customer Success: Basado en el análisis anterior, sugiere una acción concreta para reforzar los puntos positivos y una para mitigar los negativos.
Redactor de Comunicaciones: Escribe un email interno breve para el equipo de producto, resumiendo los hallazgos y las acciones sugeridas.
El output debe estar en formato Markdown, con una sección clara para cada experto.
Aquí están los comentarios:
[Pegar aquí los comentarios de la encuesta]

---

## 🔧 Zona de Práctica Segura: Tu Equipo de Expertos

Usa la plantilla de abajo para analizar cualquier tipo de feedback.

<div style="border: 1px solid #ccc; border-radius: 8px; padding: 16px; background-color: #f6f8fa;">
  <p><strong>Copia y adapta este prompt:</strong></p>
  <textarea id="prompt-area" style="width: 98%; min-height: 200px; border: 1px solid #ddd; border-radius: 4px; padding: 10px; font-family: monospace; font-size: 14px; resize: vertical;">
Actúa como un cluster de expertos para analizar el siguiente feedback de clientes sobre nuestro producto [NOMBRE DEL PRODUCTO]:

1.  **Analista de Sentimiento:** Clasifica cada comentario como positivo, negativo o neutro.
2.  **Identificador de Patrones:** Agrupa los comentarios por temas comunes (ej: usabilidad, soporte, precio, funcionalidad X).
3.  **Priorizador de Acciones:** Basado en los patrones, ¿cuál es el tema MÁS URGENTE que el equipo de producto debería abordar? Justifica por qué.

Formatea la salida en 3 secciones claras.

Feedback a analizar:
"[Pega aquí el feedback del cliente, siempre anonimizado]"
  </textarea>
  <br>
  <button onclick="copiarPrompt()" style="margin-top: 10px; padding: 8px 16px; border: none; background-color: #0366d6; color: white; border-radius: 6px; cursor: pointer;">
    📋 Copiar Prompt
  </button>
  <span id="copy-feedback" style="margin-left: 10px; color: green; font-weight: bold;"></span>
</div>

<script>
function copiarPrompt() {
  const textArea = document.getElementById('prompt-area');
  textArea.select();
  document.execCommand('copy');
  const feedback = document.getElementById('copy-feedback');
  feedback.innerText = '¡Copiado!';
  setTimeout(() => { feedback.innerText = ''; }, 2000);
}
</script>

---

[⬅️ Volver al Índice Principal](../index.md) | [Siguiente Módulo: Análisis de Datos Táctico ➡️](./02-analisis-de-datos.md)