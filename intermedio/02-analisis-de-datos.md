# 📊 Módulo: Análisis de Datos Táctico

**Ruta:** Nivel Intermedio
**Objetivo:** Utilizar la IA para analizar lotes de tickets de soporte e identificar problemas recurrentes en productos específicos de TR.

---

## ⚡ El Superpoder: Convertir el ruido de los tickets en una señal clara

Cada ticket de soporte es un dato. Cien tickets son ruido. Pero analizados en conjunto, son una señal clara que nos dice dónde le duele al cliente. La IA es tu herramienta para encontrar esa señal en minutos.

---

### 案例 Caso de Éxito TR: ¿Por qué aumentaron los tickets de ONVIO este mes?

El equipo de soporte nota un aumento de tickets para **ONVIO**, pero no está claro el motivo.

**Acción:** Se exportan los asuntos de los últimos 100 tickets de ONVIO y se pegan en un prompt.

**Prompt Maestro de Análisis de Lotes:**Actúa como un analista de soporte Nivel 3 para Thomson Reuters, especializado en el producto ONVIO.
He extraído los asuntos de los últimos 100 tickets de soporte. Tu tarea es analizarlos y encontrar patrones.
Clusterización: Agrupa los tickets en 3 a 5 categorías temáticas (ej: "Problemas de Login", "Error de Sincronización", "Dudas de Facturación").
Cuantificación: Indica cuántos tickets corresponden a cada categoría.
Identificación de Causa Raíz: Basado en las categorías, ¿cuál es la causa raíz más probable del aumento de tickets? Formula una hipótesis.
Aquí están los datos:
[Pegar aquí la lista de asuntos de los tickets, uno por línea]
**Resultado:** La IA identifica que el 45% de los tickets mencionan "error al importar AFIP", señalando un problema específico con una integración, no con el producto en general.

---

## 🔧 Zona de Práctica Segura: Analiza tus propios datos

<div style="border: 1px solid #ccc; border-radius: 8px; padding: 16px; background-color: #f6f8fa;">
  <p><strong>Copia y adapta este prompt:</strong></p>
  <textarea id="prompt-area" style="width: 98%; min-height: 150px; border: 1px solid #ddd; border-radius: 4px; padding: 10px; font-family: monospace; font-size: 14px; resize: vertical;">
Actúa como un analista de datos de CX para Thomson Reuters.

Analiza el siguiente lote de datos [TIPO DE DATOS, ej: asuntos de tickets, comentarios de encuesta] sobre el producto [NOMBRE DEL PRODUCTO].

1.  **Identifica los 3 temas más mencionados.**
2.  **Extrae 1 o 2 ejemplos textuales representativos de cada tema.**
3.  **Sugiere a qué departamento interno (Soporte, Producto, Ventas) le interesaría más conocer cada uno de estos temas.**

Datos para analizar:
"[Pega aquí tus datos anonimizados]"
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

[⬅️ Volver al Índice Principal](../index.md) | [Siguiente Módulo: Gestión de Archivos ➡️](./03-gestion-de-archivos.md)