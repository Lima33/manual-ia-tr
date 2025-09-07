# 📂 Módulo: Gestión de Archivos Múltiples

**Ruta:** Nivel Intermedio
**Objetivo:** Aprender a usar la IA para "conversar" con documentos (PDFs, transcripciones) y sintetizar información clave de manuales de producto.

---

## ⚡ El Superpoder: Tener un experto que ha leído toda la documentación por ti

Nadie tiene tiempo de leerse un manual de 200 páginas para responder una pregunta. Con la IA, puedes "alimentarla" con el manual y luego hacerle preguntas directas en lenguaje natural.

**Nota:** Esta funcionalidad suele requerir herramientas de IA que permitan la carga de archivos (como ChatGPT Plus, Copilot Pro, Claude, etc.).

---

### 案例 Caso de Éxito TR: Respondiendo a una pregunta compleja sobre "Sistema de Información Legal (SIL)"

Un cliente pregunta: "¿Cuál es el procedimiento exacto para archivar jurisprudencia de la Corte Suprema en SIL y etiquetarla para que mi equipo la encuentre en menos de 10 segundos?". Esta información está en la página 147 del manual de usuario.

**Proceso:**
1.  **Cargar el Documento:** Sube el PDF del manual de usuario de SIL a la herramienta de IA.
2.  **Hacer la Pregunta:** Usa un prompt que haga referencia al documento.

**Prompt de Consulta de Documentos:**He subido el manual de usuario del "Sistema de Información Legal (SIL)".
Actúa como un formador experto en este producto.
Basándote EXCLUSIVAMENTE en el contenido del manual, responde a la siguiente pregunta del cliente de la forma más clara y concisa posible. Formatea la respuesta como una lista de pasos numerados.
Pregunta del cliente:
"¿Cuál es el procedimiento exacto para archivar jurisprudencia de la Corte Suprema en SIL y etiquetarla para que mi equipo la encuentre en menos de 10 segundos?"
**Resultado:** La IA extrae la información precisa de la página 147 y la presenta como una guía paso a paso, ahorrando al colaborador el tiempo de búsqueda y lectura.

---

## 🔧 Zona de Práctica Segura: Conversa con tus documentos

<div style="border: 1px solid #ccc; border-radius: 8px; padding: 16px; background-color: #f6f8fa;">
  <p><strong>Copia y adapta este prompt (para usar después de subir un archivo):</strong></p>
  <textarea id="prompt-area" style="width: 98%; min-height: 120px; border: 1px solid #ddd; border-radius: 4px; padding: 10px; font-family: monospace; font-size: 14px; resize: vertical;">
Basándome en el documento que he subido ([NOMBRE O TIPO DE DOCUMENTO]):

1.  **Resume el propósito principal del documento en 3 puntos clave.**
2.  **Extrae toda la información relevante sobre el siguiente tema: [TEMA ESPECFÍCO QUE BUSCAS].**
3.  **¿Hay alguna advertencia o paso crítico mencionado en el documento sobre este tema?**
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

[⬅️ Volver al Índice Principal](../index.md) | [¡Felicidades! Has completado la Ruta Intermedia ➡️](../index.md)