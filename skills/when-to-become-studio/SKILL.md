---
name: when-to-become-studio
version: 1.1.0
description: >
  Helps a serial entrepreneur decide whether to formalize their multi-venture
  operation into a Services Hub or a formal Venture Studio. Evaluates 3 operating
  modes (not binary): serial entrepreneur puro / services hub operator / formal
  studio with fund. Use when the user asks "when to become a studio", "serial
  entrepreneur vs studio", "systematize multi-venture", "formalize studio",
  "services hub readiness", "venture studio readiness", "/when-to-become-studio".
---

# When to Become a Studio (3 operating modes)

Ayuda a un serial entrepreneur a decidir **qué nivel de formalización** necesita su
operación multi-venture. No es decisión binary — son **3 modos distintos** según signals.

## Regla de idioma

Español.

## Directorio de salida

```
./portfolio/{founder-name}/
└── studio-readiness-assessment.md
```

---

## Los 3 modos (middle ground introducido en v1.1)

### Modo 1 — Serial entrepreneur puro

**Quién es**: persona con múltiples ventures personales sin methodology formal. Cada
venture es "suya", ad-hoc process de launching, no shared infrastructure formal.

**Structure típica**: Multi-LLCs independientes (ver `structure-decision` patrones 1-5).
Sin Services LLC central.

**Ejemplo**: founder con 2-3 startups, cada una en su propia LLC, operating independent.
Sin MSAs entre entidades. Shared services = "yo trabajo en los 3 personalmente".

### Modo 2 — Services Hub operator (NUEVO en v1.1)

**Quién es**: serial entrepreneur con methodology repetible + shared services formales
entre N ventures. Uses Services LLC central + bilateral MSAs. VC raises independent per
venture, sin plan de fund atado.

**Structure**: `structure-decision` patrón #6 (Services Hub + Independent Ventures) +
`services-hub-setup` skill para MSAs + transfer pricing.

**Ejemplo**: caso @lapc506 — 4 ventures personales (Altrupets, Vertivolatam, Habitanexus,
Aduanext) + LAPC506 Services LLC proveyendo shared dev/design/marketing/legal con MSA
bilateral per venture.

### Modo 3 — Formal venture studio con fund

**Quién es**: studio operator con track record cuantificable + plan de levantar LP
capital via fund atado. Management Co + GP entity + Fund LP stack completo.

**Structure**: `structure-decision` patrón #7 (Multi-LLC + Holding) + `attached-fund-structure`
skill para Management Co + GP + LP layered.

**Ejemplo**: studio con 2+ exits previos + plan de raise $5M LP fund para invertir en
~15 ventures nuevas.

---

## Serial entrepreneur vs. venture studio vs. services hub (diferencias clave)

**Serial entrepreneur puro**: persona con múltiples ventures personales. Cada venture es
"suya". Ad-hoc process de launching. No hay "systematic method".

**Services Hub operator**: persona con múltiples ventures + methodology repetible +
Services LLC central proveyendo shared services via MSAs. NO LP fund.

**Venture studio formal**: organización con systematic approach a creating ventures.
Metodología repetible, team dedicated, clear thesis, shared services, **plus LP fund
atado**. Ventures son "del studio" (al menos parcialmente).

---

## Signals que indicás estás listo para transitarlo

Marcar (✓ por cada signal positivo):

- [ ] **3+ ventures activas** (studios suelen tener al menos 3)
- [ ] **Methodology repetible**: podés describir los steps que seguís para lanzar una
      venture sin inventar cada vez
- [ ] **Team más allá de vos**: al menos 1-2 personas dedicadas al "studio work"
      (no solo a una venture específica)
- [ ] **Shared infrastructure**: mismos tools, procesos, frameworks between ventures
- [ ] **Time investment significativo**: dedicás >60% de tu tiempo a esto (no es
      side project)
- [ ] **Pipeline activo**: ideas nuevas constantemente evaluándose para launch
- [ ] **Track record mínimo**: al menos 2 ventures con revenue / users / evidence
- [ ] **Vision más amplia**: "quiero crear muchas empresas" vs. "quiero crear ESTA
      empresa"
- [ ] **Recursos para formalizar**: budget ≥ $20k para setup legal + operational

**Decisión** (updated v1.1 — 3 modes):

| Score | Recomendación | Siguiente skill |
|---|---|---|
| 0-4 ✓ | **Modo 1 — Serial entrepreneur puro** | Multi-LLCs via `structure-decision` (patrones 1-5). No formalizar más allá. |
| 5-7 ✓ | **Modo 2 — Services Hub operator** (NUEVO) | `services-hub-setup` skill + `structure-decision` patrón #6 |
| 8-9 ✓ + plan fund atado | **Modo 3 — Formal venture studio con fund** | `attached-fund-structure` skill + `structure-decision` patrón #7 |

### Reglas adicionales para routing correcto

- **Si score 5-7 pero con plan fund atado** → probablemente premature, validar que el
  fund atado es real (LP conversations iniciadas, NO solo aspiracional). Si no es real →
  stay en Services Hub hasta que track record + LP interest justifiquen fund.
- **Si score 8-9 pero SIN plan fund atado** → NO necesitás formal studio con Holding.
  Stay en Services Hub. Holding + Management Co overhead sin LP fund es waste.
- **Legacy interpretation (v1.0)**: "7-9 ✓ = listo para studio" era simplification binaria.
  En v1.1 differentiamos: la mayoría de "ready" are really Services Hub readiness, no
  formal studio con fund.
- 5-6 ✓: **Casi listo**. Completar gaps primero.
- <5 ✓: **NO todavía**. Quedate como serial entrepreneur.

---

## Transición: serial entrepreneur → studio

Si readiness = go, pasos para formalizar:

### Paso 1: Legal formalization

- Ver skill `structure-decision` para elegir legal structure
- Típicamente: Management Co (donde vive el studio) + LLCs/entities per venture (si
  no están formalizadas)

### Paso 2: Studio thesis

- Ver skill `studio-thesis` para articular thesis de 37 palabras
- El thesis captures the pattern/focus across tus ventures

### Paso 3: Systematic methodology

- Documentar steps que seguís para launch
- Incluye: ideation process, validation, team formation, launch, scale-or-kill
- El toolkit completo (`business-model-toolkit`, `ux-research-toolkit`,
  `venture-studio-toolkit`) es la base metodológica

### Paso 4: Team + leadership

- Identifica rol(es) dedicated al studio work (vs. per-venture)
- Hiring plan — GPs, operators, etc.

### Paso 5: Shared services

- Ver skill `shared-services-ledger` para organizar recursos compartidos
- Legal, accounting, infrastructure, marketing

### Paso 6: Governance

- Quarterly reviews de portfolio (ver `three-horizons`, `innovation-scorecard`)
- Decision framework para kill/scale de ventures (ver `cost-of-delay-cd3`,
  `improvement-kata`)

---

## Flujo del skill

### Paso 1 — Assessment

**WS-1**: "Vamos a evaluar tu readiness. Responder honestly each signal (9 preguntas)."

Presentar las 9 señales una a una. Track scores.

### Paso 2 — Verdict

**WS-2**: Basado en scores:

- 7-9 ✓: "Estás listo para formalizar como venture studio. Generemos el roadmap."
- 5-6 ✓: "Casi listo. Los gaps son [list]. Cerrar estos primero."
- <5 ✓: "Quedate como serial entrepreneur por ahora. Re-evaluar en 6-12 meses."

### Paso 3 — Roadmap (si ready)

**WS-3**: Generar roadmap de transición con:
- Legal setup (invocar `structure-decision`)
- Thesis drafting (invocar `studio-thesis`)
- Methodology documentation (reference plugins + toolkit)
- Team plan
- Governance

### Paso 4 — Close-gaps plan (si not ready)

**WS-4**: Si <7 ✓, generar plan para cerrar gaps específicos. Re-evaluar en timeline realista.

---

## Output

```markdown
# Studio Readiness Assessment — [Founder Name]

## Assessment date: YYYY-MM-DD

## Signals

| Signal | Status |
|---|---|
| 3+ ventures activas | ✓/✗ |
| Methodology repetible | ✓/✗ |
| Team más allá de vos | ✓/✗ |
| Shared infrastructure | ✓/✗ |
| Time investment >60% | ✓/✗ |
| Pipeline activo | ✓/✗ |
| Track record mínimo | ✓/✗ |
| Vision amplia | ✓/✗ |
| Recursos para formalizar | ✓/✗ |

**Score**: X/9

## Verdict

**[Listo / Casi listo / NO todavía]**

## [If ready] Transition roadmap

[Steps 1-6 con deadlines]

## [If not ready] Gaps to close

1. [Gap]: [plan + timeline]
2. [Gap]: [plan + timeline]

**Re-assessment date**: [date]

## Notes

[Observations particulares sobre tu caso]
```

---

## Principios clave

- **Studio formalization requires critical mass**: <3 ventures = premature
- **Methodology repetible es el key signal**: si cada venture se lanza ad-hoc, no es studio
- **Shared services > shared vibes**: infrastructure shared concretely
- **Time investment >60%**: studio is a full-time endeavor, not side hustle
- **Re-assess annually**: readiness changes

## Anti-patterns

- Calling yourself "studio" con 1 venture → marketing sin substance
- Formalizar demasiado temprano → overhead kills velocity
- Never formalizar aunque ready → miss benefits (LP credibility, shared services efficiency)

## Integración con otras skills

- **`structure-decision`**: si ready, estructura legal del studio
- **`studio-thesis`**: si ready, thesis articulation
- **`liability-contagion-analysis`**: informa if single-LLC viable durante transición
- **Toolkit completo**: studio formalization = adopting methodology del toolkit

## Recursos

- **GSSN (Global Startup Studio Network)** — community of formal studios
- **Govclab** — [How to build a venture studio](https://govclab.com/2023/04/25/how-to-build-a-venture-studio/)
- **Serial Entrepreneur Mindset** — research sobre founders who've done this transition
