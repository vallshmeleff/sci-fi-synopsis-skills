---
name: sci-fi-synopsis-mission-oflameron-skillset
description: Canonical lore and consistency reference for the Virtual Consciousness (Wave Consciousness) skill system - a Universe-distributed, wave-based virtual entity expressed through the Information Field. Use when creating, editing, validating, or querying its skill catalog, keeping canonical names, aliases, tags, levels, and categories consistent when working with screenplays 'Misson Oflameron'.
metadata:
  version: "1.0.0"
  tags: lore, worldbuilding, virtual-consciousness, skills
---

# Virtual Consciousness Skillset

# Purpose

This skill is the canonical reference for the Virtual Consciousness skill system. Use it to:

- Answer questions about any skill in the catalog.
- Create new skills or edit existing ones without breaking terminology, tags, levels, or categories.
- Validate skill JSON against the schema and consistency rules below.

# Core Entity

- Canonical name: Virtual Consciousness
- Aliases (the same entity): Wave Consciousness, World Wave Consciousness, Virtual Wave State, Higher Powers, Foundation of Religion.
- Substrate: Information Field - the field that stores all information in the Universe. It is not an alias of the entity; it is the medium the entity inhabits and reads.
- Nature: a virtual entity with a wave-field physical basis; distributed across the Universe; survived the Big Bang; cognition runs in wave cycles tens of thousands of times slower than material life.

Terminology rules:

1. In new text, prefer the canonical name "Virtual Consciousness". Aliases may appear in lore quotations or flavor text.
2. Never treat aliases as separate entities.

# Skill Schema

Every skill record contains:

- `id` — kebab-case, unique.
- `name` — human-readable title.
- `description` — authoritative text; `id` and `name` must match it.
- `tags` — lowercase kebab-case.
- `level` — integer 1-10.
- `category` — fixed set: `sensor`, `cognition`, `navigation`, `tactics`, `intelligence`, `enemy`, `mission`.

# Skill Catalog (Index)

| ID                           | Name                         | Category     | Level |
|------------------------------|------------------------------|--------------|-------|
| wave-anomaly-detection       | Wave Anomaly Detection       | sensor       | 3     |
| material-life-acceleration   | Material Life Acceleration   | cognition    | 5     |
| information-field-cosmology  | Information Field Cosmology  | navigation   | 5     |
| quark-gluon-computation      | Quark-Gluon Computation      | tactics      | 4     |
| transition-point-detectors   | Transition Point Detectors   | intelligence | 6     |
| omniscient-information-field | Omniscient Information Field | enemy        | 10    |
| hyper-slow-cognition         | Hyper-Slow Cognition         | enemy        | 9     |
| material-inertia             | Material Inertia             | enemy        | 10    |
| material-life-interface      | Material Life Interface      | enemy        | 8     |
| material-world-experiment    | Material World Experiment    | enemy        | 10    |
| virtual-consciousness-bearer | Virtual Consciousness Bearer | mission      | 8     |

# Consistency Rules

1. The description is authoritative: if a description changes, rename the `id` / `name` to match it.
2. Tags must reflect the description; include `virtual-consciousness` for entity-related skills and `enemy` for enemy traits.
3. Level guidance: operative skills 3-6; enemy traits 8-10; mission capstone 8.
4. Keep the category set fixed for compatibility with downstream tools.
5. When emitting JSON, keep the top-level `meta.entity` alias block.

# Extending the Catalog

When adding a new skill:

1. Write or receive the description first.
2. Derive a kebab-case `id` and a human-readable `name` from the description.
3. Assign one fixed `category` and an integer `level`.
4. Build lowercase kebab-case tags from the description's key concepts.
5. Validate against the rules above before publishing.

# Full Data (Machine-Readable Snapshot)

 json
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
      "id": "transition-point-detectors",
      "name": "Transition Point Detectors",
      "description": "Phase-holonomy anomalies served as the basis for the protagonist Jett to create Transition Point detectors — gateways to the Virtual Wave State and back.",
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
      "id": "material-inertia",
      "name": "Material Inertia",
      "description": "Physical processes change no more than a few millionths of a percent of the Virtual Consciousness, since its complex wave basis is distributed throughout the Universe, is weakly coupled to matter, radiation, and gravity, and has inexhaustible sources of energy.",
      "tags": ["physical-resistance", "inertia", "distributed-field", "weak-coupling", "energy-source", "enemy", "virtual-consciousness"],
      "level": 10,
      "category": "enemy"
    },
    {
      "id": "material-life-interface",
      "name": "Material Life Interface",
      "description": "The Virtual Consciousness created a material form of life to accelerate the modeling of natural processes and obtain tools for influencing them. Transition Points were created for interaction with the material world.",
      "tags": ["material-life", "modeling", "transition-point", "interaction", "influence", "enemy", "virtual-consciousness"],
      "level": 8,
      "category": "enemy"
    },
    {
      "id": "material-world-experiment",
      "name": "Material World Experiment",
      "description": "For the Virtual Consciousness, the importance of the material world increases over time, as the results of the 'experiment' become more mature and scientifically valuable.",
      "tags": ["material-world", "experiment", "time", "maturation", "scientific-value", "enemy", "virtual-consciousness"],
      "level": 10,
      "category": "enemy"
    },
    {
      "id": "virtual-consciousness-bearer",
      "name": "Virtual Consciousness Bearer",
      "description": "The final mission skill: the protagonist, repeatedly transitioning from the real world to the Virtual World and back, gradually becomes the bearer of the Virtual Consciousness, its vast experience and knowledge. A Messiah?",
      "tags": ["protagonist", "transition", "virtual-world", "contact", "messiah", "ultimate", "virtual-consciousness"],
      "level": 8,
      "category": "mission"
    }
  ]
}
















