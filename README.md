# Cross-Cultural-AI-negotiator-main-

# What is My Nego Agent

An AI advisor that helps commercial managers prepare cross-cultural negotiations. It runs on Claude Projects and draws on a structured knowledge base of negotiation methodology and cross-cultural theory.

> Group project developed for a university course on cross-cultural negotiation (May–July 2026).

## What it does

Given a negotiation scenario, the agent returns advice grounded in its knowledge base and makes its reasoning explicit:

- names the cultural dimensions it relies on (Hofstede, Meyer) and Trompenaars' procedural role
- structures preparation with negotiation frameworks such as BATNA and ZOPA
- defers stakeholder mapping when the information provided is insufficient, instead of guessing
- runs a pre-output self-check and flags low-confidence answers for regions with thin source coverage

## How it is built

The project is organised around a strict separation between knowledge and behaviour:

| Component | Role |
| --- | --- |
| **Knowledge Base (KB)** | Domain knowledge: negotiation methodology and cross-cultural frameworks, with regional profiles. A markdown document of about 43,000 lines. |
| **System Instructions (SI)** | Behaviour: how the agent reasons, what every answer must contain, and when it must defer. |
| **PRD** | Product requirements, kept aligned with the SI. |

Rule of the project: domain knowledge lives in the KB, behavioural instructions live in the SI.

## Knowledge base coverage

- **Negotiation methodology:** Fisher & Ury, Voss, Wheeler, Lewicki, Salacuse
- **Cross-cultural frameworks:** Hofstede, Trompenaars, Meyer, Hall, Gesteland
- **Regional profiles:** East Asia, Western Europe, Gulf and Arab contexts, and others

## Evaluation

The system was evaluated on four checks, repeated across document iterations: completeness, consistency, specificity, and KB/SI separation. 

## Known limitations

- Source coverage is thinner for the Maghreb and for Latin America. The Maghreb is not treated as equivalent to a generic Arab-world profile, and the SI instructs the agent to flag low confidence for these regions.
- Like any LLM-based tool, the agent can hallucinate on peripheral geographies. It is decision support for preparation, not a substitute for local expertise.

## Repository structure

```
.
├── README.md
├── knowledge-base/
├── system-instructions/
├── prd/
└── evaluation/
```

## Disclaimer

Academic project. The frameworks and theories referenced belong to their respective authors.
