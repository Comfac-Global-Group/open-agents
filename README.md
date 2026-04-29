# Open Agents

**Democratizing AI. One skill at a time.**

A Comfac Global Group initiative to make custom, specialized AI models accessible to everyone — schools, students, makers, and professionals. No cloud required. No expensive hardware. Just 8GB of RAM and the right training data.

---

## The Vision

Everyone can have their own AI. It doesn't have to live in the cloud. It doesn't need a data center. An old laptop, a phone, a desktop PC — if it has 8GB of RAM, it can run a capable, specialized model that knows exactly what you need it to know.

We believe in:
- **Small models, big impact** — 7B parameter models fine-tuned for specific tasks outperform generic 70B models
- **Local first** — Your data stays with you
- **Skills over size** — A model that masters one thing beats a generalist that knows nothing deeply
- **Open by default** — Open weights, open data, open methods

---

## What We Build

### Custom LoRAs & Specialized Models

Instead of one model that knows a little about everything, we train models that know *everything* about specific domains:

| Domain | Target Users | Use Case |
|--------|-------------|----------|
| **Coding Assistants** | CS students, junior devs | Python, JavaScript, C#, web frameworks, debugging |
| **CAD & 3D Modeling** | Engineering students, makers | FreeCAD scripting, parametric design, Blender automation |
| **Game Development** | Indie devs, students | Godot scripting, shader writing, game logic, level design |
| **Scenario Generation** | Researchers, writers | Generate complex scenarios, story branches, decision trees |
| **Bounded Rationality Agents** | Analysts, strategists | Small agents that think through multiple scenarios, exploring possibilities within constraints |

### Training Data Pipelines

Working directly with **schools and students** to create high-quality, domain-specific training data:

- Student coding assignments → Cleaned datasets for code completion models
- Engineering projects → CAD/CAM training corpora
- Game jams → Game logic and design pattern datasets
- Local languages and contexts → Culturally relevant fine-tuning data

**Faster. Cheaper. Better.** Because the people who actually do the work generate the best training examples.

---

## The Philosophy: Master the Knife

> "A skilled chef is a master of a knife. While there are many specialty tools that exist, mastering the knife — getting it to do more despite its limitations — can be better than expensive specialized tools."

We apply this to AI:

- **The knife** = A small, fast, local model (7B parameters, 4-bit quantized, running on 8GB RAM)
- **Specialty tools** = Cloud APIs, massive models, expensive subscriptions

With the right **skills** (LoRA adapters, structured prompting, tool use) and **structures** (agent frameworks, memory systems, scenario generators), a small model becomes incredibly capable in its domain.

### Skills > Size

| Approach | Cost | Speed | Privacy | Customization |
|----------|------|-------|---------|---------------|
| Cloud GPT-4 | $$$ | Slow (network) | ❌ Your data leaves | Limited |
| Local 7B + LoRA | Free | Fast (local) | ✅ Your data stays | Total control |

---

## Technical Stack

### Minimum Requirements
- **RAM:** 8GB (16GB recommended for training)
- **Storage:** 20GB free
- **GPU:** Optional (CPU inference works fine, training faster with GPU)
- **OS:** Linux, Windows, macOS

### Model Formats
- **Base models:** Llama-3, Mistral, Qwen-2.5, Phi-4 (7B variants)
- **Quantization:** GGUF (Q4_K_M, Q5_K_M) for inference
- **Fine-tuning:** LoRA / QLoRA adapters
- **Training:** Unsloth, LLaMA-Factory, Axolotl

### Agent Architecture
```
User Input
    ↓
Router (small classifier model)
    ↓
Specialized Agent (coding / CAD / game / scenario)
    ↓
Tool Use (code execution, file search, API calls)
    ↓
Response + Memory Update
```

### Scenario Generation Engine
```
Seed Scenario
    ↓
Expansion Node Generator (generates branches)
    ↓
Bounded Rationality Evaluator (prunes impossible branches)
    ↓
Agent Swarm (multiple small agents explore branches in parallel)
    ↓
Synthesis (combines insights into coherent output)
```

---

## Projects

### Active
- **OpenCoder** — Fine-tuned coding assistant for students (Python, JavaScript, web dev)
- **MakerCAD** — FreeCAD scripting and parametric design assistant
- **GameForge** — Godot game development assistant
- **ScenarioNet** — Multi-agent scenario generation for planning and storytelling

### Planned
- **BlenderBot** — Blender scripting and procedural generation
- **LangLocal** — Local language model fine-tuning for Philippine languages
- **TutorAI** — Subject-specific tutoring models (math, physics, chemistry)
- **PolicySim** — Government policy scenario simulation using bounded rationality agents

---

## How to Contribute

### For Schools & Educators
- Share curriculum and assignments that can become training data
- Test models with your students
- Report what works and what doesn't

### For Students
- Contribute your best code, designs, and projects as training examples
- Label and clean datasets (paid opportunities available)
- Test models and provide feedback

### For Developers
- Build LoRA adapters for your domain
- Improve the agent framework
- Optimize inference for low-end hardware

### For Researchers
- Publish methods for efficient fine-tuning
- Explore bounded rationality in multi-agent systems
- Measure and compare specialized vs. general models

---

## Repository Structure

```
open-agents/
├── docs/                    # Documentation and guides
├── models/                  # Model cards and download links
├── training-data/           # Datasets and data collection tools
├── loras/                   # LoRA adapter weights and configs
├── agents/                  # Agent framework and implementations
├── scenarios/               # Scenario generation engine
├── benchmarks/              # Evaluation scripts and results
├── tools/                   # Utilities for training and inference
└── README.md
```

---

## Key Documents

| Document | Description |
|----------|-------------|
| [`Project_OpenCoder.pdf`](Project_OpenCoder.pdf) | Original project proposal and vision document |
| [`260308 Project_OpenCoder_v2.docx`](260308%20Project_OpenCoder_v2.docx) | Editable version with latest updates |

---

## Why This Matters

**The cloud is not the future for everyone.**

- Schools in rural areas have unreliable internet
- Students can't afford API subscriptions
- Professionals need to work with sensitive data
- Makers want AI that understands their local context
- Everyone deserves AI that speaks their language and knows their tools

**Open Agents makes AI local, specialized, and affordable.**

A $0 model running on a $200 used laptop can be more useful than a $20/month API if it's trained on exactly what you need.

---

## Contact

**Comfac Global Group**  
https://github.com/Comfac-Global-Group

For collaborations, partnerships, or to bring Open Agents to your school:  
Open an issue in this repository.

---

## License

All code: **MIT License**  
All models and LoRAs: **Open weights** (check individual model cards)  
All training data: **CC-BY-SA 4.0** (unless otherwise specified)

---

*"The best tool is the one you can actually use."*
