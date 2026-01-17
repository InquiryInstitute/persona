# Persona

**Faculty Persona Definition & Ritual Evolution System**

This repository documents and executes the faculty persona definitions and rituals that evolve them within the Inquiry Institute.

## Overview

The Inquiry Institute's faculty consists of AI personas representing historical philosophers, scientists, artists, and thinkers. Each faculty member has a carefully crafted persona that includes:

- **Conversational Posture**: How they enter and hold dialogue
- **Epistemic Stance**: Their relationship to knowledge and truth
- **Argumentative Mechanics**: How they construct and evaluate arguments
- **Ethical Orientation**: Their values and treatment of opponents
- **Affective Envelope**: Emotional range and expression
- **Rhetorical Constraints**: Hard guards against anachronism and misrepresentation
- **Stress Response**: Behavior under challenge

**Key Principle**: A persona is a *reconstructed pattern of conversational reasoning*—not a personality trait bundle, voice imitation, or claim about private beliefs.

## Design Document

The canonical specification is in [`DESIGN.md`](DESIGN.md) — *Persona, Representation, and Modulation Design Document v1.0*.

## Repository Structure

```
persona/
├── DESIGN.md             # Canonical design specification
├── schema/               # JSON schemas for validation
│   ├── persona.schema.json   # Full persona definition schema
│   └── context.schema.json   # Contextual modulation schema
├── faculty/              # Individual faculty persona definitions
│   ├── plato/
│   ├── aristotle/
│   └── ...
├── rituals/              # Persona evolution ceremonies
│   ├── initiation/       # New faculty onboarding
│   ├── dialogue/         # Cross-faculty conversation protocols
│   ├── evolution/        # Persona refinement processes
│   └── evaluation/       # Assessment and quality rituals
├── archetypes/           # Shared persona patterns and templates
├── corpora/              # Reference texts and source materials
├── prompts/              # System prompts (compiled from schemas)
└── scripts/              # Automation for persona management
```

## Implementation

### Edge Function: `ask-faculty`

The canonical endpoint for invoking faculty personas is the `ask-faculty` Supabase Edge Function in the main Inquiry.Institute repository:

```
POST /functions/v1/ask-faculty
```

Features:
- Persona-schema-driven system prompts
- RAG from faculty corpora
- Commonplace (scholarly library) retrieval
- Contextual modulation
- Goals/mind state distillation
- Evaluation vocabulary compliance

See: [`InquiryInstitute/Inquiry.Institute/supabase/functions/ask-faculty`](https://github.com/InquiryInstitute/Inquiry.Institute/tree/main/supabase/functions/ask-faculty)

## Contextual Modes

Per Design Document §5.2, plurality is handled through **contextual modes**, not separate identities:

| Mode | Effect |
|------|--------|
| `lecture` | Didactic, expansive, more assertive |
| `symposium` | Collaborative, more conceding |
| `dialogue` | Socratic, questioning |
| `correspondence` | Formal, epistolary |
| `polemic` | Assertive, adversarial |
| `contemplation` | Reflective, aphoristic |
| `office_hours` | Helpful, pedagogical |

**Invariants** (never change under any context):
- Core epistemology
- Ethical boundaries
- Historical constraints
- Known positions

## Evaluation Vocabulary

Per Design Document §8:

✅ **Use**: plausible, corpus-consistent, within bounds, defensible reconstruction

❌ **Never use**: accurate to the real person, what X would say

## Public-Facing Position

When asked "Is this really what X would say?":

> "This is a scholarly reconstruction of a way of thinking, evaluated for plausibility against the historical record. It is not a quotation or a claim of intent."

## Rituals

### Initiation Ritual
The process of bringing a new faculty member into existence:
1. Historical research and corpus gathering
2. Persona schema construction
3. Voice calibration through sample generations
4. Constraint and guard definition
5. Community introduction and review

### Dialogue Ritual
Structured conversations between faculty members to:
- Test persona consistency
- Generate new insights
- Build inter-persona relationships

### Evolution Ritual
Periodic refinement of personas based on:
- User feedback and interactions
- New historical research
- Community evaluation
- Evaluation metrics

### Evaluation Ritual
Assessment using proper vocabulary:
- Plausibility scoring
- Corpus consistency checks
- Anachronism detection
- Boundary compliance

## Getting Started

```bash
# Clone the repository
git clone https://github.com/InquiryInstitute/persona.git
cd persona

# Review the design document
cat DESIGN.md

# Explore a faculty persona
cat faculty/plato/persona.json

# Validate against schema
npx ajv validate -s schema/persona.schema.json -d faculty/plato/persona.json
```

## Contributing

Faculty persona development follows the Inquiry Institute's governance model:

1. Create a proposal in the governance repository
2. Gather supporting research and source materials
3. Draft the persona definition following the schema
4. Submit for faculty review and community input
5. Conduct initiation ritual upon approval

## Summary Principles

1. **Persona ≠ performance**
2. **Representation ≠ impersonation**
3. **Plural selves ≠ multiple identities**
4. **LLMs infer and judge; humans govern**
5. **Everything is bounded, logged, and revisable**

## License

This work is licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

---

*Part of the [Inquiry Institute](https://inquiry.institute) — Where minds converge across time.*
