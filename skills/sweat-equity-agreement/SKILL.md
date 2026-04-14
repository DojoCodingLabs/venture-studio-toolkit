---
name: sweat-equity-agreement
version: 1.0.0
description: >
  Generates a sweat equity agreement between co-founders, early employees,
  advisors, or service providers who contribute work in exchange for equity
  instead of cash. Covers vesting schedule, cliff, hours-to-equity formula,
  83(b) election (for US entities), and dilution considerations.
  Use when the user asks "sweat equity", "equity for work", "vesting schedule",
  "cliff", "co-founder equity", "advisor equity", "FAST agreement",
  "83(b) election", "acuerdo de equity por trabajo", "/sweat-equity-agreement".
  Extends FAST Agreement template from business-model-toolkit.
---

# Sweat Equity Agreement

Genera un acuerdo de **sweat equity** (equity obtenido a cambio de trabajo en lugar
de dinero) estructurado. Cubre founders, early employees, advisors, y service
providers.

## Regla de idioma

Español. Términos legales en "español (English)" primera vez.

## Directorio de salida

```
./portfolio/{venture-name}/equity/
├── sweat-equity-{recipient-name}.md     # Acuerdo por recipient
├── vesting-schedule-{recipient-name}.md # Cronograma detallado de vesting
└── cap-table-projection.md              # Impacto en cap table (si aplica)
```

## Aviso legal

**Esta skill NO es asesoría legal**. Genera un draft estructurado que debe revisarse
con abogado corporativo antes de firmarse. Sweat equity mal estructurado puede:

- Crear implicaciones fiscales inesperadas (ej. ingreso imputado al recipient al vestear)
- Generar disputas si no hay cliff + clawback bien definido
- Invalidar la ventaja de QSBS si no se hace 83(b) election dentro de 30 días

---

## Fundamentos

### Sweat equity vs. cash equity

- **Cash equity**: alguien pone dinero, recibe shares (ej. VC invierte $1M por 10%)
- **Sweat equity**: alguien pone trabajo, recibe shares (ej. co-founder sin salario por 12 meses por 25%)

### Quién recibe sweat equity

- **Co-founders**: 80+ horas/semana por salario mínimo o $0, recibe large equity stake
- **Early employees**: acepta 20-40% below-market salary + equity package
- **Advisors**: expertise + network a cambio de 0.1-1% equity (FAST agreement)
- **Service providers**: devs, designers, lawyers reducen fees 25-50% por equity
- **Family/friends con skills**: contribución profesional informal

### Valuation formula básica

```
Sweat Equity Value = Hours Worked × Hourly Rate
Shares Received = (Sweat Equity Value) / (Current Company Valuation per share)
```

Ejemplo:
- Developer charge $150/hr market rate
- Acepta $50/hr cash + $100/hr en equity
- Trabaja 200 horas = $20,000 en equity
- Si company valuation es $2M @ 1M shares totales → $2/share
- Recibe 10,000 shares (1%)

---

## Componentes esenciales del acuerdo

### 1. Vesting schedule

**Estándar de la industria**: 4-year vesting con 1-year cliff

- **Year 1 (cliff)**: 0 shares hasta los 12 meses. Al día 366, **25% vestea de golpe**
- **Year 2-4**: el restante 75% vestea mensualmente (2.08% por mes)

**Alternativas**:

- **3-year vesting + 6-month cliff**: para compromisos más cortos
- **Milestone-based**: vesting tied a deliverables específicos (común para advisors)
- **Immediate (no vesting)**: rare — a veces para advisors con contribución one-shot
- **Custom**: cases especiales (ej. "25% immediate + 75% over 3 years" para co-founders con contribución pre-formation reconocida)

### 2. Cliff

El **cliff** protege a la startup contra alguien que se vaya en los primeros meses
y se lleve shares "inmerecidas". Si la persona sale antes del cliff (12 meses usual),
recibe **0 shares**.

### 3. Acceleration clauses (opcional, para co-founders)

- **Single trigger**: al vender la company, todo el vesting pendiente se acelera
- **Double trigger**: vesting acelera solo si (a) se vende la company Y (b) la persona es despedida post-acquisition
- **Most common for founders**: double trigger (balance entre proteger founder y mantener retention post-acquisition)

### 4. 83(b) election (solo US entities)

**CRÍTICO para US LLCs/Corps**:

- Al recibir shares sujetas a vesting, **sin 83(b) election** pagás impuestos sobre el valor cuando cada tranche vestea (potentially huge si la startup crece rápido)
- **Con 83(b) election** dentro de 30 días de la grant, pagás impuestos solo sobre el valor hoy (low valuation = low tax)
- **Failure to file**: irreversible. Perdés el beneficio fiscal para siempre.

**Proceso**:
1. Receive grant document
2. Dentro de 30 días: enviar 83(b) election form al IRS (certified mail, return receipt)
3. Dar copia al company tax records
4. Guardar receipt para life

### 5. Clawback / buyback provision

Si la persona sale **voluntariamente** (quits) o con cause (fired for fraud):
- Shares vestidas: keeps them
- Unvested shares: revierten al company

Si la persona sale **involuntariamente sin cause** (layoff):
- Shares vestidas: keeps them
- Unvested: usualmente revierten, pero algunas startups aceleran X meses

### 6. ROFR (Right of First Refusal)

Si la persona quiere vender sus shares, la company tiene derecho de comprarlas
primero antes de que vayan a un third party. Protege contra dilución no controlada.

### 7. Drag-along / tag-along

- **Drag-along**: majority shareholders pueden forzar minorities a vender en acquisition
- **Tag-along**: si majority vende, minorities pueden "tag along" y vender también
  (protege minorities contra ser dejados afuera)

---

## Comparación: Sweat Equity vs. ESOP vs. SAFE

| Instrumento | Qué es | Para quién | Dilución | Tax event |
|---|---|---|---|---|
| **Sweat Equity** | Shares directas otorgadas por trabajo | Co-founders, early team | Inmediata al grant | Al vestear (o 83(b) al grant) |
| **ESOP** (Employee Stock Option Plan) | Opciones para comprar shares futuro | Employees | Al ejercer opciones | Al ejercer |
| **RSU** (Restricted Stock Units) | Promise de shares al vestear | Employees mid-stage | Al vestear | Al vestear |
| **SAFE** (Simple Agreement for Future Equity) | Conversión a equity en próximo round | Investors early-stage | Al round siguiente | Al round (complicado) |

**Regla**: sweat equity es para **founders y very early stage**. ESOP/RSU son para
employees después de Series A.

---

## Flujo del skill

### Paso 1 — Contexto

**SE-1**: "¿Para quién es el acuerdo?
- (a) Co-founder
- (b) Early employee
- (c) Advisor (FAST agreement)
- (d) Service provider (dev, designer, lawyer, etc.)
- (e) Otro"

**SE-2**: "¿Datos del recipient?
- Nombre completo
- Email
- País/jurisdicción fiscal del recipient (crítico — tax implications varían)
- Relación con founders (familia, colega, cold contact, network intro)"

### Paso 2 — Contribución esperada

**SE-3**: "¿Qué contribución va a hacer?
- Descripción del trabajo (dev, design, marketing, business dev, advisory, etc.)
- Horas estimadas por mes
- Duración esperada (6 meses, 1 año, 2 años, indefinido)
- Hitos/milestones específicos si aplica"

**SE-4**: "¿Cuál es el market hourly rate para este trabajo? (si es advisor, cuánto cobraría consulting?)"

### Paso 3 — Compensation mix

**SE-5**: "¿Qué mix de cash/equity estás ofreciendo?
- 100% equity, $0 cash
- 50/50 (split half cash half equity)
- 25% cash, 75% equity (common para early team)
- 75% cash, 25% equity (bridge para bootstrap founders)
- Otro (especificar)"

### Paso 4 — Equity structure

**SE-6**: "¿Current company valuation?
- Estimado realista (conservador, usar lowest defensible para tax reasons)
- Shares totales outstanding
- Shares disponibles en option pool (si aplica)"

**SE-7**: "¿Qué porcentaje de equity estás ofreciendo?
- Advisor: 0.1% - 1% (estándar FAST agreement)
- Early employee key: 0.5% - 2%
- Co-founder: 10% - 49% (depending on timing y contribución)
- Service provider one-shot: 0.05% - 0.5%"

### Paso 5 — Vesting structure

**SE-8**: "¿Vesting schedule?
- 4-year / 1-year cliff (ESTÁNDAR — recomendado para co-founders y early team)
- 3-year / 6-month cliff (shorter commitment)
- Milestone-based (advisors, service providers — equity vestea al completar deliverable)
- Immediate (solo para advisors one-shot)
- Custom (especificar)"

**SE-9**: "¿Acceleration clause?
- Double trigger (acquisition + despido) — RECOMENDADO para co-founders
- Single trigger (solo acquisition) — más founder-friendly
- Sin acceleration
- Otro"

### Paso 6 — 83(b) check (si US entity)

**SE-10**: "¿La entity está incorporada en US (Delaware LLC, Delaware C-Corp, etc.)?
- Sí → el recipient DEBE filing 83(b) election dentro de 30 días del grant. Incluir recordatorio + instrucciones en el acuerdo.
- No (entity non-US) → no aplica 83(b), pero validar tax implications en jurisdicción del recipient"

### Paso 7 — Generate agreement

Generar `./portfolio/{venture}/equity/sweat-equity-{recipient}.md`:

```markdown
# Sweat Equity Agreement — [Recipient Name]

**Effective Date**: YYYY-MM-DD
**Company**: [Entity legal name]
**Company Jurisdiction**: [Delaware LLC / etc.]
**Recipient**: [Name], [Email]
**Recipient Tax Residency**: [Country]

---

## 1. Scope of contribution

[Detalle del trabajo esperado, horas/mes, duración]

## 2. Compensation

- **Cash**: $X/mes (si aplica)
- **Equity**: X% de Company fully diluted (X shares de un total de Y)
- **Valuation base**: $X (usando valuation date)

## 3. Vesting schedule

- **Total shares granted**: X
- **Vesting period**: X años
- **Cliff**: X meses (durante cliff, 0 shares vestean)
- **Post-cliff**: vesting mensual / trimestral / por milestones
- **Table**: ver `vesting-schedule-{recipient}.md`

## 4. 83(b) election (if US entity)

**⚠️ CRITICAL**: El recipient DEBE file 83(b) election con IRS dentro de 30 días
del grant date ([YYYY-MM-DD]) para elegir pagar impuestos sobre valor actual
en lugar de value al momento de cada vesting.

**Instrucciones**:
1. Download Form 83(b) election letter (template standard)
2. Fill with: name, SSN/EIN, Company info, grant date, number of shares, FMV per share at grant
3. Send via **certified mail** (USPS, con return receipt) al IRS office donde file personal taxes
4. Copia al company (agregar al cap table records)
5. Guardar receipt del certified mail para tax records

**Deadline**: [grant date + 30 días]

## 5. Acceleration

[Double trigger / single trigger / none]

## 6. Clawback / buyback

- Voluntary departure: keeps vested shares, unvested revert to Company
- For cause termination: keeps vested shares, unvested revert
- Without cause termination: [keeps vested + X months acceleration / all vested]

## 7. ROFR

Company has Right of First Refusal on any sale of shares by Recipient. Recipient
must offer shares to Company first at same terms offered by third party.

## 8. Drag-along / Tag-along

[Standard drag/tag provisions]

## 9. Confidentiality

Recipient acknowledges confidential nature of Company information. Standard NDA terms.

## 10. IP Assignment

All IP created during contribution period relating to Company business is assigned
to Company (standard IP assignment provisions).

## 11. Dispute resolution

[Jurisdiction + arbitration clause]

---

**Signatures**:

- Recipient: _______________ Date: _______
- Company (authorized signatory): _______________ Date: _______
```

---

## Principios clave

- **Siempre cliff**: sin cliff, cualquiera puede agarrar shares y desaparecer
- **83(b) no es opcional en US**: filing tardío es irreversible, pérdida significativa
- **Valuation conservador**: low valuation at grant = low tax liability
- **IP assignment explícito**: si no se asigna IP, la persona puede reclamar ownership
- **Escrito, no verbal**: sweat equity informal termina en litigation
- **Revisión con abogado**: este skill genera draft — NO reemplaza abogado

## Anti-patterns

- **Grant sin vesting** ("ya te lo doy, es tuyo") → founder regret guaranteed
- **Missing 83(b)** → tax nightmare al crecer
- **Mix de roles** (co-founder también es advisor también es vendor) → confusión legal
- **Over-granting early** → dilución irreversible de cap table
- **Verbal agreement** → imposible enforcear, garantiza drama

## Integración con otras skills

- **`structure-decision`**: la entity matters — sweat equity works differently en LLC vs. Corp vs. offshore
- **`cap-table-per-venture`** (futuro skill): actualiza cap table con cada sweat equity grant
- **FAST Agreement** (business-model-toolkit, Fase 17): template específico para advisors — se extiende aquí
- **`structure-evolution-roadmap`**: si planeás flip to Corp, re-evaluar sweat equity grants pre-flip

## Recursos

- **Cake Equity** — [Sweat equity guide](https://www.cakeequity.com/guides/sweat-equity) + platform para cap table management
- **Orchestra** — [Sweat equity for startups](https://www.orchestra.io/blog/what-is-sweat-equity-and-how-can-it-benefit-startups-and-employees)
- **ClearTax** — [ESOP vs Sweat Equity comparison](https://cleartax.in/s/esop-vs-sweat-equity-shares)
- **Founder Institute FAST Agreement** — template público para advisor equity
- **83(b) Election Form** — [IRS template + instructions](https://www.irs.gov/)
- **Carta** / **Pulley** — platforms para cap table management con vesting tracking automático
