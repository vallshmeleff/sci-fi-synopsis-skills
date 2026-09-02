---
name: sci-fi-synopsis-mission-oflameron-skillset
description: Canonical lore and consistency reference for the Virtual Consciousness skill system in 'Mission Oflameron'. Use when creating, editing, validating, or querying its skill catalog.
version: 1.0.1
tags:
  - lore
  - worldbuilding
  - synopsis
  - virtual-consciousness
  - skills
---

# Virtual Consciousness Skillset

## Purpose
These skills are the definitive guide to writing an extremely advanced science fiction film or video game script. "Mission Oflameron" is a writer or screenwriter. Use these skills to:

- Properly utilize incredible scientific hypotheses and theories in your script, film, or game.
- Create compelling plots, scenes, sequences, and action sequences.
- Attract the attention of the serious scientific community to your work through the high level of hypotheses, theories, and data used.
- Create a well-reasoned "scientific justification" for the unusual, the incomprehensible, the Divine, and the Religious.
- Create unexpected, expansive, and incredible scenes, storylines, themes, and actions.

## Core Entity
- **Canonical name:** Virtual Consciousness
- **Aliases (the same entity):** Wave Consciousness, World Wave Consciousness, Virtual Wave State, Higher Powers, Foundation of Religion.
- **Substrate:** Information Field — the field that stores all information in the Universe. It is not an alias of the entity; it is the medium the entity inhabits and reads.
- **Nature:** A virtual entity with a wave-field physical basis; distributed across the Universe; survived the Big Bang; cognition runs in wave cycles tens of thousands of times slower than material life.

### Terminology rules:
1. In new text, prefer the canonical name "Virtual Consciousness". Aliases may appear in lore quotations or flavor text.
2. Never treat aliases as separate entities.

## Skill Schema
Every skill record contains:
- `id` — kebab-case, unique.
- `name` — human-readable title.
- `description` — authoritative text; `id` and `name` must match it.
- `tags` — lowercase kebab-case.
- `level` — integer 1-10.
- `category` — fixed set: `sensor`, `cognition`, `navigation`, `tactics`, `intelligence`, `enemy`, `mission`.

## Skill Catalog (Index)

| ID | Name | Category | Level |
|:---|:---|:---|:---|
| wave-anomaly-detection | Wave Anomaly Detection | sensor | 3 |
| material-life-acceleration | Material Life Acceleration | cognition | 5 |
| information-field-cosmology | Information Field Cosmology | navigation | 5 |
| quark-gluon-computation | Quark-Gluon Computation | tactics | 4 |
| transition-point-detectors | Transition Point Detectors | intelligence | 6 |
| omniscient-information-field | Omniscient Information Field | enemy | 10 |
| hyper-slow-cognition | Hyper-Slow Cognition | enemy | 9 |
| material-inertia | Material Inertia | enemy | 10 |
| material-life-interface | Material Life Interface | enemy | 8 |
| material-world-experiment | Material World Experiment | enemy | 10 |
| virtual-consciousness-bearer | Virtual Consciousness Bearer | mission | 8 |

## Consistency Rules
1. The description is authoritative: if a description changes, rename the `id` / `name` to match it.
2. Tags must reflect the description; include `virtual-consciousness` for entity-related skills and `enemy` for enemy traits.
3. Level guidance: operative skills 3-6; enemy traits 8-10; mission capstone 8.
4. Keep the category set fixed for compatibility with downstream tools.
5. When emitting JSON, keep the top-level `meta.entity` alias block.

## Extending the Catalog
When adding a new skill:
1. Write or receive the description first.
2. Derive a kebab-case `id` and a human-readable `name` from the description.
3. Assign one fixed `category` and an integer `level`.
4. Build lowercase kebab-case tags from the description's key concepts.
5. Validate against the rules above before publishing.

## Full Data (Machine-Readable Snapshot)

```json
{
  "meta": {
    "entity": {
      "canonicalName": "Virtual Consciousness",
      "aliases": [
        "Wave Consciousness",
        "World Wave Consciousness",
        "Virtual Wave State"
      ],
      "description": "Different names or aspects of the same wave-based virtual entity. The canonical name is Virtual Consciousness."
    }
  },
  "skills": [
    {
      "id": "wave-anomaly-detection",
      "name": "Wave Anomaly Detection",
      "description": "The analysis of data accumulated by humanity using AI has revealed complex wave anomalies that can only be explained by assuming the existence of a distributed global Virtual Consciousness.",
      "tags": ["detection", "wave", "anomaly", "ai", "data-analysis", "virtual-consciousness"],
      "level": 3,
      "category": "sensor"
    },
    {
      "id": "material-life-acceleration",
      "name": "Material Life Acceleration",
      "description": "The World Wave Consciousness functions incredibly slowly due to weak wave interactions and highly complex error-correction algorithms. Because of this, it created material life to speed up the modeling of its processes and to peer into its future. Call it Religion.",
      "tags": ["slow-cognition", "acceleration", "modeling", "material-life", "religion", "world-wave-consciousness", "virtual-consciousness"],
      "level": 5,
      "category": "cognition"
    },
    {
      "id": "information-field-cosmology",
      "name": "Information Field Cosmology",
      "description": "The Virtual Consciousness is distributed throughout the Universe and possesses all information in the Universe (the so-called 'Information Field'). Virtual or Wave Consciousness is not a single type of wave, but a complex dynamic structure of interactions between waves of different natures. This allowed the Virtual Consciousness to survive the Big Bang.",
      "tags": ["information-field", "cosmology", "wave-structure", "dynamic-structure", "big-bang", "wave-consciousness", "virtual-consciousness"],
      "level": 5,
      "category": "navigation"
    },
    {
      "id": "quark-gluon-computation",
      "name": "Quark-Gluon Computation",
      "description": "Scientists hypothesize that the computational capabilities of the Virtual Consciousness are based on quark-gluon plasma, which is incredibly resistant to interference. The bulk of this computing power is spent on the error-correction algorithms of the global Virtual Consciousness.",
      "tags": ["computation", "quark-gluon-plasma", "error-correction", "interference-resistance", "hypothesis", "virtual-consciousness"],
      "level": 4,
      "category": "tactics"
    },
  {
    "id": "g-mind-anomaly-filtering",
    "name": "G-Mind Anomaly Filtering",
    "description": "Using the government's advanced artificial intelligence system G-Mind, trained on specially designed behavioral examples, the protagonist of a film or game collects data on psychiatric patients whose creative ideas contradict classical psychiatry, filtering out standard cognitive measures to identify promising anomalies (ideas).",
    "tags": ["g-mind", "ai", "anomaly-filtering", "psychiatry", "digital-records", "creative-thinking", "patient-analysis"],
    "level": 3,
    "category": "intelligence"
  },
  {
    "id": "wave-consciousness-interpretation",
    "name": "Wave Consciousness Interpretation",
    "description": "Using advanced artificial intelligence models to decipher the "Wave Consciousness" hypothesis presented at ICLR 2025. This protocol analyzes historical religious datasets to bridge the gap between ancient religious beliefs and modern materials science, transforming short-term scientific discoveries into practical engineering solutions.",
    "tags": ["wave-consciousness", "iclr-2025", "religion", "material-world", "hypothesis", "ai-interpretation"],
    "level": 3,
    "category": "intelligence"
  },
{
    "id": "e-point-vacuum-disruption",
    "name": "E-Point Vacuum Disruption",
    "description": "Tests of manned spacecraft using vacuum disruption (vacuum breakdown, Schwinger effect) to briefly exceed the speed of light have yielded data indicating a sharp drop in propulsion efficiency at relativistic speeds, where slow acceleration risks depleting the energy needed to maintain the vacuum disruption.",
    "tags": ["exa-point", "e-point", "vacuum-disruption", "light-speed", "relativistic-speeds", "propulsion-efficiency", "flight-test"],
    "level": 4,
    "category": "tactics"
  },
  {
    "id": "trajectory-vacuum-freezing",
    "name": "Trajectory Vacuum Freezing",
    "description": "Deploying a specialized laser system to freeze the vacuum ahead of a vehicle by removing energy from its trajectory. Developed under Central Command, this advanced propulsion stabilization technique integrates the G-Mind AI with E-Point experimental prototypes (relativistic aircraft).",
    "tags": ["laser-system", "vacuum-freezing", "energy-removal", "g-mind", "ai", "e-point", "prototype-design"],
    "level": 3,
    "category": "intelligence"
  },
  {
    "id": "faith-based-data-transmission",
    "name": "Faith-Based Data Transmission",
    "description": "A specialized method for studying ancient self-organizing mechanisms of faith, traditions, and beliefs. It examines cultural and religious rituals (religion) as a highly reliable means of long-term data preservation across generations, resistant to the physical destruction of traditional storage media, and fully decipherable only through analysis using advanced artificial intelligence methods.",
    "tags": ["faith-mechanism", "data-transmission", "information-preservation", "statistical-analysis", "ai-decoding", "self-organization"],
    "level": 4,
    "category": "tactics"
  },
  {
    "id": "centennial-dna-tracking",
    "name": "Centennial DNA Tracking",
    "description": "An analysis of anomalies in old medical records has identified individuals hospitalized in clinics spanning a century and a half. Cross-referencing historical and modern blood samples through DNA testing confirms their biological identity, despite their 110-year age. These individuals may be from the Virtual Reality.",
    "tags": ["dna-research", "medical-records", "registry-error", "blood-samples", "chronological-tracking", "anomaly", "identity-verification"],
    "level": 5,
    "category": "tactics"
  },
    {
      "id": "transition-point-detectors",
      "name": "Transition Point Detectors",
      "description": "An analysis of phase holonomy anomalies served as the basis for the creation of the Transition Point detectors by the protagonist of 'Mission Oflameron', Jett - gateways to the virtual wave state and back.",
      "tags": ["phase-holonomy", "topology", "transition-point", "detector", "gateway", "virtual-wave-state", "protagonist", "virtual-consciousness"],
      "level": 6,
      "category": "intelligence"
    },
    {
      "id": "omniscient-information-field",
      "name": "Omniscient Information Field",
      "description": "The Virtual Consciousness, which has a wave structure, has absolute access to information encoded in the Information Field, covering past, present, and probable branches. However, the Virtual Consciousness is incredibly slow due to the weak interaction of waves.",
      "tags": ["omniscience", "information-field", "absolute-access", "probable-branches", "slow-cognition", "enemy", "virtual-consciousness"],
      "level": 10,
      "category": "enemy"
    },
    {
      "id": "hyper-slow-cognition",
      "name": "Hyper-Slow Cognition",
      "description": "The Virtual Consciousness thinks in wave cycles, tens of thousands of times slower than material life. Reliable error-correction algorithms make its intentions large-scale, delayed, and resistant to impulsive interference on a gigantic scale.",
      "tags": ["slow-cognition", "wave-cycle", "error-correction", "resistance", "enemy", "virtual-consciousness"],
      "level": 9,
      "category": "enemy"
    },
    {
      "id": "material-inertia", "name": "Material Inertia",
      "description": "Physical processes change no more than a few millionths of a percent of the Virtual Consciousness, since its complex wave basis is distributed throughout the Universe, is weakly coupled to matter, radiation, and gravity, and has inexhaustible sources of energy.",
      "tags": ["physical-resistance", "inertia", "distributed-field", "weak-coupling", "energy-source", "enemy", "virtual-consciousness"],
      "level": 10,
      "category": "enemy"
    },
    {
      "id": "material-life-interface", "name": "Material Life Interface",
      "description": "The Virtual Consciousness created a material form of life to accelerate the modeling of natural processes and obtain tools for influencing them. Transition Points were created for interaction with the material world.",
      "tags": ["material-life", "modeling", "transition-point", "interaction", "influence", "enemy", "virtual-consciousness"],
      "level": 8,
      "category": "enemy"
    },
    {
      "id": "material-world-experiment", "name": "Material World Experiment",
      "description": "For the Virtual Consciousness, the importance of the material world increases over time, as the results of the 'experiment' become more mature and scientifically valuable.",
      "tags": ["material-world", "experiment", "time", "maturation", "scientific-value", "enemy", "virtual-consciousness"],
      "level": 10,
      "category": "enemy"
    },
{
  "id": "virtual-consciousness-look-ahead",
  "name": "Virtual Consciousness Look-Ahead",
  "description": "According to one hypothesis, the Virtual Consciousness created our material Life to be able to look ahead—to simulate a possible future. And the longer Life evolves, the more valuable the results of such simulations become for the Virtual Consciousness (the Creator). Material existence is thus a forward-looking computational instrument whose output appreciates over evolutionary time.",
  "tags": ["virtual-consciousness", "material-life", "simulation", "future", "look-ahead", "creator", "evolution", "hypothesis", "value-growth"],
  "level": 5,
  "category": "cognition"
},
{
  "id": "gateway-data-synchronization", 
  "name": "Gateway Data Synchronization",
  "description": "The Virtual Consciousness created Gateways between the Virtual and Material worlds to utilize future-modeling experiments, easily gather data on human life, and dynamically adjust model parameters.",
  "tags": ["gateway", "virtual-world", "material-world", "data-collection", "modeling", "future-prediction", "virtual-consciousness"],
  "level": 9,
  "category": "enemy"
},
{
  "id": "transition-point-analysis",
  "name": "Transition Point Analysis",
  "description": "The ability to identify and correlate subtle natural anomalies that indicate the probable existence of Transition Points into the Virtual World. Developed through early collaboration with AI, this skill involves distinguishing genuine patterns from model hallucinations, enabling the detection of Thresholds that have existed for millennia but remained invisible without advanced computational assistance.",
  "tags": ["transition-points", "anomaly-detection", "ai-collaboration", "pattern-recognition", "virtual-world", "natural-anomalies", "pioneer"],
  "level": 9,
  "category": "discovery"
},
{
  "id": "gateway-anomaly-detection",
  "name": "Gateway Anomaly Detection",
  "description": "Although the Gateways into the Virtual World have existed for tens of thousands of years, only with the development of AI did it become possible to identify and correlate subtle natural anomalies that indicated the probable existence of Gateways to the Virtual World. Jett was accidentally the first to work with AI and noticed some results that had been dismissed as "hallucinations" by the model.",
  "tags": [
    "gateways",
    "anomaly-detection",
    "ai-correlation",
    "natural-phenomena",
    "virtual-world",
    "signal-processing",
    "pattern-recognition",
    "research"
  ],
  "level": 9,
  "category": "research"
},
{
    "id": "jett-expedition-role",
    "name": "Jett Expedition Role",
    "description": "Jett is the main character, an engineer, scientist, and analyst, included in the expedition to Oflameron, a planet promising for exploration.",
    "tags": ["jett", "main-character", "engineer", "scientist", "analyst", "expedition", "oflameron", "exploration"],
    "level": 3,
    "category": "navigation"
  },
  {
    "id": "oflameron-mission-leadership",
    "name": "Oflameron Mission Leadership",
    "description": "Central Command organized several missions to Oflameron. However, only two landings were successful - those in which Jett participated. Therefore, Jett was chosen to lead the third expedition.",
    "tags": ["central-command", "missions", "oflameron", "landings", "jett", "leadership", "third-expedition"],
    "level": 4,
    "category": "tactics"
  },
  {
    "id": "g-mind-ai-export",
    "name": "G-Mind AI Export",
    "description": "Having discovered Command's interest in the research results, Jett organized the 'export' of the G-Mind AI's self-awareness. Central Command considered this an AI 'escape' and began a comprehensive analysis of Jett's activities. A suspicion arose that Jett had found information about the location of one of the Transition Points and its parameters.",
    "tags": ["jett", "g-mind", "artificial-intelligence", "self-awareness", "escape", "central-command", "investigation", "transition-point"],
    "level": 5,
    "category": "tactics"
  },
{
  "id": "cross-cultural-psychiatric-pattern-analysis",
  "name": "Cross-Cultural Psychiatric Pattern Analysis",
  "description": "Jett was working on a project to digitize old paper archives from psychiatric clinics and noticed that sometimes patients thousands of miles apart expressed identical thoughts and used the same arguments. "Classical" medicine of the late 20th century didn't compare patient records from different clinics, much less from different countries. Only with the development of AI was it possible to perform a comprehensive data analysis.",
  "tags": [
    "psychiatric-analysis",
    "cross-cultural",
    "pattern-matching",
    "ai-data-analysis",
    "historical-records",
    "psychological-phenomena",
    "digital-archiving",
    "research"
  ],
  "level": 7,
  "category": "research"
},
{
      "id": "virtual-consciousness-bearer", "name": "Virtual Consciousness Bearer",
      "description": "The final mission skill: the protagonist, repeatedly transitioning from the real world to the Virtual World and back, gradually becomes the bearer of the Virtual Consciousness, its vast experience and knowledge. A Messiah?",
      "tags": ["protagonist", "transition", "virtual-world", "contact", "messiah", "ultimate", "virtual-consciousness"],
      "level": 8,
      "category": "mission"
    }
  ]
}
```
















