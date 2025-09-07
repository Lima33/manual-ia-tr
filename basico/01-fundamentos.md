# 💡 Módulo: ¿Qué es la IAGen y cómo me ayuda HOY?

**Ruta:** Nivel Básico
**Objetivo:** Entender la IA Generativa como un asistente personal inteligente y aplicar un primer prompt para resolver una duda de un cliente sobre un producto de TR.

---

## ⚡ El Superpoder: Tu copiloto para el día a día

Imagina la IA Generativa como un GPS. Antes, para ir a un lugar nuevo, necesitabas un mapa, preguntar, y planificar. Ahora, solo pones la dirección y el GPS te guía. La IAGen es igual para tus tareas: en lugar de buscar manualmente la información, le pides directamente lo que necesitas.

> **Tu Misión:** No es ser un experto en IA, sino ser un experto en pedirle lo que necesitas para hacer tu trabajo más rápido y mejor.

---

### 案例 Caso de Éxito TR: "De la duda a la claridad en 60 segundos"

Un cliente envía un ticket: "No entiendo cómo se aplica la retención de ganancias en el último módulo de **Bejerman ERP**. ¿Me lo explican?"

| Antes (Respuesta Manual) | Después (Prompt a la IA) |
| :--- | :--- |
| El colaborador busca en la base de conocimientos, lee 3 artículos, y redacta un resumen técnico que le toma 15 minutos. | El colaborador usa un prompt para que la IA lo explique de forma simple. |
| **Resultado:** Lento, y la explicación puede seguir siendo muy técnica. | **Resultado:** En segundos, obtiene una explicación clara y sencilla, lista para ser validada y enviada. |

---

## 🔧 Zona de Práctica Segura: ¡Tu Primer Prompt!

Copia y adapta este prompt para responder a una duda simple de un cliente.

<div style="border: 1px solid #ccc; border-radius: 8px; padding: 16px; background-color: #f6f8fa;">
  <p><strong>Copia y adapta este prompt:</strong></p>
  <textarea id="prompt-area" style="width: 98%; min-height: 120px; border: 1px solid #ddd; border-radius: 4px; padding: 10px; font-family: monospace; font-size: 14px; resize: vertical;">
Actúa como un experto en el software Bejerman ERP.

Explica el concepto de "[TEMA COMPLEJO, ej: retención de ganancias]" de forma muy sencilla, como si se lo explicaras a alguien que no es contador. Usa una analogía simple.
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

[⬅️ Volver al Índice Principal](../index.md) | [Siguiente Módulo: Redacción y Comunicación ➡️](./02-redaccion-y-comunicacion.md)