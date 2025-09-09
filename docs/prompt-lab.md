# 🔬 Laboratorio de Ingeniería de Prompts

### _Construye, analiza y perfecciona tus prompts en tiempo real._

---

Bienvenido a tu entorno de práctica interactivo. Usa las plantillas como punto de partida, edita el texto y observa cómo el **Analizador de Calidad** te da feedback instantáneo sobre la estructura de tu prompt.

<div class="prompt-lab-grid">
  <div class="prompt-editor">
    <h3><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M20.7 7c-.3.4-.7.8-1.1 1.1L18.8 9l-1-1-1-1 .8-.8c.3-.4.7-.7 1.1-1.1.2-.2.5-.2.7 0l1.4 1.4c.2.2.2.5 0 .7m-2.1-2.1L13 10.5V13h2.5l5.6-5.6-2.5-2.5m-7.6 8.9L3 20v-2.5l7.5-7.5 2.5 2.5L11 13.8zM3 16l-2 5 5-2 1-1-2.5-2.5-1.5 1.5z"/></svg></span> Tu Lienzo de Trabajo</h3>
    <div class="prompt-templates">
      <button class="md-button" onclick="applyTemplate('redaccion')">✍️ Plantilla de Redacción</button>
      <button class="md-button" onclick="applyTemplate('analisis')">📊 Plantilla de Análisis</button>
      <button class="md-button" onclick="applyTemplate('ideas')">💡 Plantilla de Ideas</button>
      <button class="md-button md-button--quiet" onclick="applyTemplate('clear')">Limpiar</button>
    </div>
    <textarea id="prompt-input" placeholder="Escribe tu prompt aquí o elige una plantilla para empezar..."></textarea>
  </div>
  <div class="quality-analyzer">
    <h3><span class="twemoji"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M12 2C6.5 2 2 6.5 2 12s4.5 10 10 10 10-4.5 10-10S17.5 2 12 2m-2 15-4-4 1.4-1.4 2.6 2.6 6.6-6.6L18 7l-8 8z"/></svg></span> Analizador de Calidad</h3>
    <div class="quality-score" id="prompt-score">0/10</div>
    <div class="progress-bar-container"><div class="progress-bar" id="progress-bar"></div></div>
    <ul class="checklist" style="list-style-type: none; padding-left: 0;">
      <li id="check-role" class="checklist-item">❌ **Rol:** ¿Le has dado un rol a la IA? (ej. "Actúa como...")</li>
      <li id="check-context" class="checklist-item">❌ **Contexto:** ¿Has explicado el escenario? (ej. "Tengo un cliente...")</li>
      <li id="check-task" class="checklist-item">❌ **Tarea:** ¿La instrucción principal es clara? (ej. "Redacta", "Analiza")</li>
      <li id="check-format" class="checklist-item">❌ **Formato:** ¿Has especificado cómo quieres la salida? (ej. "en una tabla", "3 puntos")</li>
      <li id="check-length" class="checklist-item">❌ **Longitud:** ¿El prompt tiene al menos 20 palabras?</li>
    </ul>
    <p><small>Nota: Esta es una puntuación estructural, no semántica. ¡Un buen prompt siempre requiere pensamiento crítico!</small></p>
  </div>
</div>

<script>
  const templates = {
    redaccion: `Actúa como un experto en Customer Success.

Tu tarea es redactar un email para un cliente que está experimentando [PROBLEMA].

El email debe ser [TONO: empático, formal, etc.] y debe incluir los siguientes puntos:
1.  Reconocimiento del problema.
2.  Un paso de acción inmediato.
3.  Un tiempo estimado para la solución.`,
    analisis: `Actúa como un analista de datos de CX.

Analiza el siguiente feedback de clientes y presenta tus hallazgos.

Feedback:
"[Pega aquí el feedback]"

El formato de tu respuesta debe ser una tabla con tres columnas: "Tema Principal", "Sentimiento (Positivo/Negativo)" y "Sugerencia Accionable".`,
    ideas: `Actúa como un equipo de innovación.

Nuestro objetivo es mejorar [ÁREA O PROCESO].

Genera una lista de 5 ideas creativas para lograr este objetivo. Piensa sin restricciones.`,
    clear: ''
  };

  const promptInput = document.getElementById('prompt-input');
  const scoreEl = document.getElementById('prompt-score');
  const progressBarEl = document.getElementById('progress-bar');

  const checks = {
    role: document.getElementById('check-role'),
    context: document.getElementById('check-context'),
    task: document.getElementById('check-task'),
    format: document.getElementById('check-format'),
    length: document.getElementById('check-length')
  };

  function applyTemplate(type) {
    promptInput.value = templates[type];
    analyzePrompt(); // Analiza inmediatamente después de aplicar la plantilla
  }

  function analyzePrompt() {
    const text = promptInput.value.toLowerCase();
    let score = 0;

    // 1. Check for Role (2 pts)
    if (/act(ú|u)a como|eres un|imagina que eres/i.test(text)) {
      score += 2;
      checks.role.classList.add('checked');
    } else {
      checks.role.classList.remove('checked');
    }

    // 2. Check for Context (2 pts)
    if (/cliente|ticket|encuesta|proyecto|problema|situaci(ó|o)n/i.test(text)) {
      score += 2;
      checks.context.classList.add('checked');
    } else {
      checks.context.classList.remove('checked');
    }

    // 3. Check for Task (2 pts)
    if (/redacta|analiza|genera|crea|resume|lista|identifica/i.test(text)) {
      score += 2;
      checks.task.classList.add('checked');
    } else {
      checks.task.classList.remove('checked');
    }
    
    // 4. Check for Format (2 pts)
    if (/tabla|lista|puntos|formato|columnas|secci(ó|o)n/i.test(text)) {
      score += 2;
      checks.format.classList.add('checked');
    } else {
      checks.format.classList.remove('checked');
    }

    // 5. Check for Length (2 pts)
    if (text.split(' ').length >= 20) {
      score += 2;
      checks.length.classList.add('checked');
    } else {
      checks.length.classList.remove('checked');
    }

    scoreEl.innerText = `${score}/10`;
    progressBarEl.style.width = `${score * 10}%`;
  }

  promptInput.addEventListener('input', analyzePrompt);
  
  // Initial analysis on page load
  analyzePrompt();
</script>