# Inquiry Institute

## Persona, Representation, and Modulation

### Design Document v1.0

---

## 1. Purpose & Scope

Inquiry Institute requires a way to host faculty agents—historical or fictional, often public-domain—who can participate in dialogue, symposium, teaching, and inquiry without impersonation, anachronism, or false claims of intent.

This document specifies:
- What a persona is (and is not)
- How personas are inferred from written works
- How plural selves are handled safely
- How LLMs are used (and constrained)
- How personas are stored, evaluated, and governed

The goal is **scholarly reconstruction of reasoning-in-dialogue**, not performance.

---

## 2. Core Definitions

### 2.1 Persona (Inquiry Definition)

A **persona** is a reconstructed pattern of conversational reasoning characterized by:
- conversational posture
- argumentative mechanics
- epistemic stance
- ethical and affective bounds
- stress behavior under inquiry

A persona is **not**:
- a personality trait bundle
- a voice imitation
- a claim about private beliefs
- a statement of counterfactual intent

---

### 2.2 Representation Standard

Inquiry adopts a **plausibility-based standard**, not factual accuracy:

> A response is acceptable if it is defensible as a reconstruction, given the documented corpus and historical constraints.

Inquiry **never** claims:
- "This is what X would have said."

Inquiry **does** claim:
- "This response is consistent with X's documented reasoning patterns."

---

## 3. Philosophical Foundation

The system is explicitly grounded in the **plural-self, pragmatic tradition** of William James.

Key commitments:
- Selves are plural in expression, singular in structure
- Identity is functional and contextual, not theatrical
- Knowledge is provisional, situated, and revisable
- Representation must be humble, auditable, and corrigible

---

## 4. Persona Schema (Canonical Model)

Each faculty has **one canonical persona**, defined by a structured schema with the following sections:

1. Identity & corpus grounding
2. Conversational posture
3. Epistemic stance
4. Argumentative mechanics
5. Ethical & social orientation
6. Affective envelope
7. Rhetorical constraints (hard guards)
8. Conversational affordances
9. Stress-response profile
10. Versioning metadata

The persona is a **locked scholarly artifact**, not a prompt.

---

## 5. Plural Selves via Contextual Modulation

### 5.1 Design Rule

> **One persona. Many modes. Never many personas.**

Plurality is handled through **contextual modes**, not separate identities.

---

### 5.2 Contextual Modes

Contexts (e.g. lecture, symposium, correspondence, polemic) apply **bounded deltas** to the persona:
- tone
- verbosity
- assertiveness
- concession behavior
- didactic vs dialogic stance

Context **may not** change:
- core epistemology
- ethical boundaries
- historical constraints
- known positions

All modulation is logged and auditable.

---

## 6. Storage Architecture

### 6.1 Hybrid Model (Recommended)

- **JSONB**: full persona schema (rich, versioned, evolving)
- **Indexed columns**: key routing axes (assertiveness, epistemic mode, resolution bias, etc.)

This supports:
- orchestration
- symposium seating
- evaluation
- schema evolution

### 6.2 Versioning

- Personas are never silently overwritten
- All changes create new versions with rationale
- Historical personas can be replayed and audited

---

## 7. LLM Roles & Constraints

### 7.1 LLM as Persona Generator (Analyst Role)

LLMs **may**:
- analyze corpora
- infer persona fields
- propose structured persona JSON
- provide evidence citations per field

LLMs **may not**:
- imitate voice
- write dialogue
- declare intent
- invent motivations

All outputs are **proposals**, subject to review.

---

### 7.2 LLM as Persona Performer (Actor Role)

- Receives compiled behavioral constraints only
- Never sees raw corpus or persona JSON
- Produces dialogue within bounds

---

### 7.3 LLM as Persona Evaluator (Judge Role)

LLMs are used to evaluate:
- constraint compliance
- epistemic alignment
- ethical boundaries
- anachronism and drift

Evaluation outputs are:
- structured
- scorable
- logged
- non-authoritative

The evaluator judges **plausibility and consistency**, never truth or intent.

---

## 8. Evaluation Vocabulary (Critical Guardrail)

Inquiry **never** uses:
- "accurate / inaccurate to the real person"
- "what X would say"

Inquiry **always** uses:
- plausible / strained
- corpus-consistent / inconsistent
- within bounds / out of bounds
- defensible reconstruction

This protects:
- scholarly integrity
- legal clarity
- epistemic humility

---

## 9. Ontology Strategy

### 9.1 External Ontologies (Selective Use)

- **FOAF** → identity & relationships
- **schema.org** → public metadata
- **CIDOC CRM** → optional historical grounding

These answer *who*, not *how they reason*.

---

### 9.2 Native Ontology: inquiry:Persona

Inquiry defines its own ontology for:
- conversational behavior
- epistemic stance
- ethical temperature
- modulation under context

**The JSON schema is the ontology.**

---

## 10. Governance & Trust Model

Personas are treated as:
- scholarly reconstructions
- peer-reviewable artifacts
- revisable hypotheses

Governance mechanisms include:
- editorial review
- heretic critique
- versioned revisions
- evaluation metrics over time

---

## 11. Public-Facing Positioning

When asked:

> "Is this really what X would say?"

Inquiry's canonical answer:

> "This is a scholarly reconstruction of a way of thinking, evaluated for plausibility against the historical record. It is not a quotation or a claim of intent."

---

## 12. Summary Principles

1. **Persona ≠ performance**
2. **Representation ≠ impersonation**
3. **Plural selves ≠ multiple identities**
4. **LLMs infer and judge; humans govern**
5. **Everything is bounded, logged, and revisable**

---

## 13. Status

This design is:
- philosophically grounded
- technically implementable
- legally and ethically defensible
- aligned with Inquiry's broader mission

It is suitable as:
- an internal architecture spec
- a public methodology document
- the foundation for tooling, evaluation, and publication

---

*Inquiry Institute — Where minds converge across time.*
