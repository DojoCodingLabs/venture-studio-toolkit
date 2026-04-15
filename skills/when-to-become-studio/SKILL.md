---
name: when-to-become-studio
version: 1.0.0
description: >
  Helps a serial entrepreneur decide whether to formalize their multi-venture
  operation into a venture studio. Brief edge-case skill for founder-mode
  transitions. Use when the user asks "when to become a studio", "serial
  entrepreneur vs studio", "systematize multi-venture", "formalize studio",
  "venture studio readiness", "/when-to-become-studio".
---

# When to Become a Studio

Ayuda a un serial entrepreneur a decidir si **formalizar su operación multi-venture
como venture studio** vs. seguir operando como founder con múltiples proyectos.

## Regla de idioma

Español.

## Directorio de salida

```
./portfolio/{founder-name}/
└── studio-readiness-assessment.md
```

---

## Serial entrepreneur vs. venture studio (diferencia clave)

**Serial entrepreneur**: persona con múltiples ventures personales. Cada venture es
"suya". Ad-hoc process de launching. No hay "systematic method".

**Venture studio**: organización con systematic approach a creating ventures.
Metodología repetible, team dedicated, clear thesis, shared services. Ventures son
"del studio" (al menos parcialmente).

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

**Decisión**:
- 7-9 ✓: **Listo para studio**. Formalizar.
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
