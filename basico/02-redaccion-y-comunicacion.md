# ✍️ Módulo: Redacción y Comunicación con IA

**Ruta:** Nivel Básico
**Objetivo:** Usar prompts para resumir tickets largos, redactar respuestas empáticas y ajustar el tono para diferentes perfiles de cliente de Thomson Reuters.

---

## ⚡ El Superpoder: De redactor a estratega de la comunicación

En soporte y CS, no solo respondemos preguntas, construimos relaciones. La IA nos libera del trabajo pesado de la redacción para que podamos enfocarnos en la estrategia: ¿cómo debe sentirse este cliente después de interactuar con nosotros?

---

### 案例 Caso de Éxito TR: "Antes y Después"

Imagina un ticket largo y frustrado de un cliente sobre un problema de facturación en **Legal ONE**.

| Antes (Respuesta Manual) | Después (Respuesta asistida por IA) |
| :--- | :--- |
| "Estimado cliente, hemos recibido su ticket. Revisaremos el problema de facturación que menciona y le daremos una respuesta. Saludos." | "Hola [Nombre del Cliente], entiendo tu frustración con la factura de Legal ONE, y te pido disculpas por la confusión. He revisado el ticket y ya estoy trabajando con el equipo de facturación para resolverlo. Para tu tranquilidad, te mantendré informado/a personalmente antes del final del día. Gracias por tu paciencia." |
| **Análisis:** Correcto, pero frío y genérico. No genera confianza. | **Análisis:** Empático, personalizado, establece un compromiso claro y reduce la ansiedad del cliente. |

---

## 🔧 Zona de Práctica Segura: ¡Tu Turno!

Copia y adapta este prompt maestro para gestionar cualquier comunicación.

<div style="border: 1px solid #ccc; border-radius: 8px; padding: 16px; background-color: #f6f8fa;">
  <p><strong>Copia y adapta este prompt:</strong></p>
  <textarea id="prompt-area" style="width: 98%; min-height: 150px; border: 1px solid #ddd; border-radius: 4px; padding: 10px; font-family: monospace; font-size: 14px; resize: vertical;">
Actúa como un experto en Customer Success de Thomson Reuters. He recibido el siguiente ticket de un cliente que usa nuestro producto [NOMBRE DEL PRODUCTO, ej: Legal ONE]. El cliente parece [SENTIMIENTO, ej: frustrado, confundido].

Resume el problema principal en una sola frase. Luego, redacta una respuesta empática, profesional y tranquilizadora. La respuesta debe:
1. Validar su sentimiento.
2. Confirmar que entendimos el problema.
3. Establecer un próximo paso claro y un tiempo de respuesta.

MI TICKET:
"[Pega aquí el ticket del cliente]"
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

[⬅️ Volver al Índice Principal](../index.md) | [Siguiente Módulo: Seguridad y Confianza ➡️](./03-seguridad-y-confianza.md)