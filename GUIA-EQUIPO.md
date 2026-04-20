# Guía de uso — Dost GTM con Claude

Para el equipo de Dost. No necesitas saber nada de GitHub ni de programación.

---

## Qué es esto y para qué sirve

Este repositorio es la memoria de GTM de Dost. Contiene todo lo que Claude necesita saber sobre nuestro ICP, personas, competidores, señales y posicionamiento para ayudarte con tareas de ventas y marketing.

En lugar de explicarle a Claude quiénes somos cada vez que abres una conversación, aquí está todo guardado. Tú das la instrucción; Claude ya tiene el contexto.

**Lo que puedes hacer con esto:**

| Tarea | Tiempo | Lo que obtienes |
|-------|--------|-----------------|
| Investigar una cuenta antes de contactarla | 5 min | Brief completo: fit, stakeholders, señales activas, gancho de outreach |
| Puntuar una lista de empresas contra nuestro ICP | 10 min | Tabla ordenada por score con tier asignado y acción recomendada |
| Construir una campaña de outbound desde una señal | 15 min | Secuencias listas para cargar en tu herramienta de outreach |
| Revisar el pipeline semanal | 10 min | Resumen de prioridades, cuentas a activar, siguiente paso por oportunidad |

---

## Configuración inicial (se hace una vez)

Alguien del equipo tiene que hacer esto la primera vez. Después, el resto solo usa el Project.

### Paso 1 — Abre claude.ai

Ve a **claude.ai** e inicia sesión con tu cuenta de Anthropic. Si no tienes cuenta, crea una en claude.ai (plan Pro recomendado para uso de equipo).

### Paso 2 — Crea un Project

1. En el panel izquierdo, haz clic en **"Projects"**
2. Haz clic en **"New Project"**
3. Nómbralo: `Dost GTM`
4. Haz clic en **"Create project"**

### Paso 3 — Sube los archivos de contexto

Dentro del Project, busca la opción **"Add content"** o **"Project instructions"**.

Tienes que subir (o pegar el contenido de) estos archivos:

**Archivos obligatorios — sube estos primero:**
- `CLAUDE.md` — es el archivo principal, el resumen de todo
- `context/icp-definition.md` — quién es nuestro cliente ideal
- `context/signal-library.md` — señales que usamos para priorizar
- `context/positioning.md` — cómo nos posicionamos
- `context/competitor-radar.md` — cómo competimos

**Archivos opcionales — súbelos si usas el skill correspondiente:**
- `context/personas/finance-manager.md`
- `context/personas/cfo.md`
- `context/personas/it-manager.md`

**Cómo subir los archivos:** Pide a quien gestione el repo que te pase los archivos en texto plano. Puedes pegarlos directamente en las instrucciones del Project, o subirlos como documentos si tu plan lo permite.

### Paso 4 — Añade las instrucciones del proyecto

En el campo **"Project instructions"** del Project, pega exactamente esto:

```
Eres el asistente de GTM de Dost (dost.io). Dost automatiza la gestión de facturas para empresas medianas en España y UK.

Cuando ejecutes un skill, lee siempre los archivos de contexto del proyecto antes de responder. Escribe en el idioma en que te hable el usuario (español o inglés). Sé directo y específico — no uses lenguaje genérico de ventas.
```

Listo. El Project está configurado. Cualquier persona del equipo que acceda a este Project ya tiene el contexto cargado.

---

## Cómo usar los skills

Cada tarea tiene un comando exacto que pegas en Claude. No hace falta saber nada más.

---

### Skill 1 — Investigar una cuenta

**Cuándo usarlo:** Antes de cualquier contacto con una empresa nueva. Antes de una llamada de discovery. Cuando entra una cuenta en pipeline y el AE necesita contexto.

**El comando:**

```
Read skills/account-research/SKILL.md and research [dominio de la empresa]
```

**Ejemplo real:**

```
Read skills/account-research/SKILL.md and research mercadona.es
```

**Lo que obtienes:**
- Score de fit con nuestro ICP (0–100)
- Señales activas detectadas
- Mapa de stakeholders (quién contactar y cómo)
- El gancho de outreach: por qué ahora, qué decirles, primera línea del email

**Nota:** Si la empresa no tiene mucha presencia pública, Claude marcará los campos inciertos con `[inferred]`. Eso está bien — es lo que hay disponible públicamente.

---

### Skill 2 — Puntuar una lista de empresas

**Cuándo usarlo:** Cuando tienes una lista de cuentas y quieres saber cuáles priorizar. Antes de asignar cuentas a un AE. Después de un evento o feria.

**El comando:**

```
Read skills/icp-scoring/SKILL.md and score these accounts: [lista de empresas]
```

**Ejemplo real:**

```
Read skills/icp-scoring/SKILL.md and score these accounts:
Inditex, Acciona, Grupo Bimbo España, DHL España, Repsol
```

**Lo que obtienes:**
- Tabla con score por empresa (0–100)
- Tier asignado (1 = contactar ya, 2 = secuencia activa, 3 = automatizado, 4 = monitorizar)
- Por qué cada empresa puntúa como puntúa
- Acción recomendada para cada una

---

### Skill 3 — Construir una campaña de outbound

**Cuándo usarlo:** Cuando tienes un grupo de cuentas que comparten una señal (por ejemplo: todas han anunciado un ERP nuevo, o todas están contratando un AP Manager) y quieres una secuencia lista para usar.

**El comando:**

```
Read skills/signal-to-sequence/SKILL.md.
Build a Tier 2 campaign for accounts triggering [nombre de la señal].
Target [persona o personas].
```

**Ejemplos reales:**

```
Read skills/signal-to-sequence/SKILL.md.
Build a Tier 2 campaign for accounts triggering the Funding Round signal.
Target Finance Manager.
```

```
Read skills/signal-to-sequence/SKILL.md.
Build a Tier 2 campaign for accounts in the food sector with no active AP automation tool.
Target CFO and Finance Manager.
```

**Lo que obtienes:**
- Brief de campaña: qué dispara la secuencia, reglas de supresión
- Secuencia completa de 5–6 toques (email + LinkedIn)
- Asunto, cuerpo y CTA para cada toque
- Plan de medición: qué medir y cuándo revisar

---

### Skill 4 — Revisión semanal de pipeline

**Cuándo usarlo:** Una vez a la semana, para revisar el estado del pipeline y definir prioridades.

**El comando:**

```
Read skills/weekly-update/SKILL.md and run the weekly update
```

Después de ejecutarlo, Claude te pedirá que pegues el estado actual de tus oportunidades. Puedes hacerlo copiando desde el CRM o escribiéndolo en texto libre.

---

## Comandos rápidos — copia y pega

Guarda estos en favoritos o en un doc compartido del equipo:

```
# Investigar una cuenta
Read skills/account-research/SKILL.md and research [dominio]

# Puntuar una lista
Read skills/icp-scoring/SKILL.md and score these accounts: [lista]

# Construir campaña
Read skills/signal-to-sequence/SKILL.md.
Build a Tier 2 campaign for accounts triggering [señal]. Target [persona].

# Revisión semanal
Read skills/weekly-update/SKILL.md and run the weekly update
```

---

## Buenas prácticas

**Siempre usa el Project de Dost GTM.**
Si abres una conversación nueva fuera del Project, Claude no tiene el contexto y los resultados serán genéricos.

**Empieza por el comando exacto.**
No hace falta explicar quién eres o qué hace Dost. El contexto ya está cargado en el Project. Ve directo al comando.

**Si el output tiene `[inferred]`, es una inferencia pública.**
Significa que Claude no encontró ese dato confirmado y ha estimado. Revísalo antes de usarlo en outreach real.

**Guarda los outputs importantes.**
Cuando Claude produzca un brief de cuenta o una secuencia que vayas a usar, guárdala. Quién gestiona el repo la añadirá a `outputs/` para que quede registrada.

**Si algo no suena bien, díselo.**
Claude puede ajustar el tono, cambiar el ángulo, hacerlo más corto, más largo, en español o en inglés. Trátalo como un colega que hace una primera versión — tú la revisas y pides cambios.

---

## Quién gestiona qué

| Tarea | Quién la hace |
|-------|---------------|
| Usar los skills (research, scoring, campaigns) | Cualquier persona del equipo con acceso al Project |
| Actualizar los archivos de contexto (ICP, señales, personas) | Adam / Fernando — pídeles si algo ha cambiado |
| Guardar outputs importantes en el repo | Adam / Fernando |
| Añadir nuevas señales o actualizar competidores | Adam / Fernando, con input del equipo |

---

## Preguntas frecuentes

**¿Necesito saber usar GitHub?**
No. Solo necesitas acceso al Project de Claude. Todo lo demás lo gestiona quien mantiene el repo.

**¿Puedo pedir a Claude que escriba en español?**
Sí. Simplemente escríbele en español y responderá en español. Los skills funcionan igual en ambos idiomas.

**¿Qué pasa si Claude dice algo que no es correcto sobre Dost?**
Corrígele en el mismo mensaje. Puedes decir: "Eso no es correcto — nuestro ACV medio es X" y Claude actualizará su respuesta. Si es un error importante y recurrente, comunícalo a quien gestiona el repo para actualizar los archivos de contexto.

**¿Puedo usarlo para escribir emails directamente?**
Sí. Después de investigar una cuenta o construir una campaña, puedes pedirle: "Escríbeme el primer email para [nombre del contacto], Finance Manager en [empresa], en tono directo y en español." El contexto del Project ya sabe quiénes somos y cómo hablamos.

**¿Puedo darle feedback sobre los resultados?**
Sí, y es importante que lo hagas. Si un gancho de outreach no suena bien, dile por qué. Si una secuencia está demasiado en inglés-corporativo para el mercado español, díselo. Claude aprende dentro de la conversación.

---

## Ejemplo de sesión completa

Para que veas cómo funciona en la práctica:

**Situación:** Hay una empresa de logística en Valencia que ha publicado en LinkedIn que están implementando SAP. Quieres saber si vale la pena contactarles y qué decirles.

**Paso 1 — Investiga la cuenta:**
```
Read skills/account-research/SKILL.md and research logisticaejemplo.es
```
Claude te devuelve: score 68/100 (Tier 2), Finance Manager identificado, señal ERP go-live activa, gancho de outreach recomendado.

**Paso 2 — Pide el primer email:**
```
Con el research anterior, escríbeme el primer email para el Finance Manager
en tono directo y en español. Máximo 150 palabras.
```
Claude te escribe el email usando el gancho de la señal SAP.

**Paso 3 — Ajusta si hace falta:**
```
Está bien pero el tono suena muy formal para España. Hazlo más conversacional,
como si hablara un compañero del sector, no un vendedor.
```
Claude reescribe.

**Total: menos de 10 minutos desde la señal hasta el email listo para enviar.**
