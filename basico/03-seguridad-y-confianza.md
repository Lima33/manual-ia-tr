# 🛡️ Módulo: Seguridad y Confianza

**Ruta:** Nivel Básico
**Objetivo:** Conocer las reglas de oro sobre qué información de clientes NUNCA se debe compartir con modelos de IA públicos para proteger la privacidad y cumplir con las normativas.

---

## ⚡ El Superpoder: Ser un guardián de los datos del cliente

La confianza es nuestro activo más valioso. Usar la IA de forma segura no es una opción, es una obligación. Tu rol es aprovechar el poder de la IA sin exponer jamás la información sensible de nuestros clientes.

> **Regla de Oro:** Trata a la IA pública como si fuera una postal. Nunca escribas en ella algo que no querrías que todo el mundo leyera.

---

### 案例 Escenario de Riesgo TR: ¿Qué NUNCA debes pegar en un prompt?

Imagina que estás trabajando con un cliente que usa **HighQ**, una plataforma donde se maneja información legal extremadamente sensible.

**Ejemplo de DATOS PROHIBIDOS para IA públicas:**
*   **Información de Identificación Personal (PII):** Nombres completos, DNI, CUIT, direcciones, teléfonos, correos electrónicos.
*   **Información Financiera:** Números de tarjetas de crédito, datos bancarios, detalles de facturación.
*   **Información Confidencial del Negocio:** Estrategias legales, detalles de casos, nombres de partes en un litigio, contraseñas, nombres de usuario.
*   **Contenido de los Productos:** Cualquier dato que el cliente haya cargado dentro de su instancia de HighQ, ONVIO o Legal ONE.

**¿Cómo hacerlo bien?** **ANONIMIZA** la información.

| Mal (Inseguro) | Bien (Seguro y Anonimizado) |
| :--- | :--- |
| "El cliente Juan Pérez (CUIT 20-12345678-9) de la empresa ACME S.A. no puede acceder a su cuenta de HighQ. Su usuario es jperez@acme.com." | "Un cliente de una empresa legal no puede acceder a su cuenta de [Producto]. El error que le aparece es [código de error]. ¿Cuáles son los 3 pasos más comunes para solucionar este problema de acceso?" |

---

## ✅ Checklist de Seguridad Pre-Prompt

Antes de presionar `Enter` en cualquier IA, revisa mentalmente:

- [ ] ¿He eliminado TODOS los nombres de personas, empresas o cualquier identificador único?
- [ ] ¿He reemplazado la descripción específica del problema por una descripción genérica del MISMO TIPO de problema?
- [ ] ¿El prompt se enfoca en el "cómo" resolver el problema, no en el "quién" tiene el problema?
- [ ] Si tengo dudas, ¿es mejor NO usar la IA y consultar a mi supervisor o la documentación interna? (La respuesta siempre es SÍ).

---

[⬅️ Volver al Índice Principal](../index.md) | [¡Felicidades! Has completado la Ruta Básica ➡️](../index.md)