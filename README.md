# 🌟 Lore: A World-Building RAG Tutorial

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Learn how to create and query rich fictional worlds using retrieval-augmented generation (RAG), guidance, and ChromaDB.

<p align="center">
  <img src="assets\lore_shoggoth.svg" alt="Loremaster Banner" width="500"/>
</p>

## ✨ Overview

Lore is an educational project, based on the [Loremaster 6000 project](https://github.com/dottxt-ai/demos/lore-generator), which demonstrates how to build a RAG-powered system for creating and managing fictional worlds. Through Jupyter notebooks, it shows how to:

- Generate coherent, interconnected lore using constrained language models
- Store and retrieve world elements using semantic search
- Maintain consistency across a growing body of fictional content
- Query and analyze relationships between different aspects of your world

## 🎮 Features

- **Guided World Generation**: Create foundational aspects of your world with structured prompts
- **Semantic Lore Storage**: Store and retrieve lore using ChromaDB's vector capabilities
- **Consistency Checking**: Ensure new lore aligns with existing world elements
- **Relationship Analysis**: Explore connections between different parts of your world
- **Interactive Tutorials**: Learn through hands-on Jupyter notebooks

## 🛠️ Technical Architecture

```ascii
+-------------------+     +-------------------+     +-------------------+
|    LoreManager    |     |    ChromaDB       |     |  Language Model   |
| - Proposal Gen    |<--->| - Vector Storage  |<--->| - Transformers    |
| - Refinement      |     | - Semantic Search |     | - Guidance        |
| - Query/Analysis  |     |                   |     |                   |
+-------------------+     +-------------------+     +-------------------+
         ^                        ^                         ^
         |                        |                         |
         v                        v                         v
+----------------------------------------------------------+
|                     World & Lore Models                   |
| - SettingType (Enum)                                      |
| - World (Base Model)                                      |
| - LoreEntry (Base Model)                                  |
| - LoreProposal/Refinement                                 |
+----------------------------------------------------------+
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook/Lab
- Required packages (install via requirements.txt)

### Installation

```bash
git clone https://github.com/Austin-Routt/lore.git
cd lore
pip install -r requirements.txt
```

### Quick Start

1. Open `lore.ipynb` for a simple introduction
2. Explore `lore.ipynb` further for more complex features

## 📚 Examples

### Lore Generation

```python

# Initialize manager
lore_manager = LoreManager(
    model_path="path/to/model",
    embeddings_path="path/to/embeddings"
)

# Create world
world = World(
    setting=SettingType.horror,
    world_description="A massive dark fantasy work with themes of cosmic horror"
)

# Generate lore proposal
proposal = lore_manager.propose_lore(world, "basic principles")

# Refine proposal
final_lore = lore_manager.refine_proposal(proposal, world)

```

### Querying Relationships
```python
analysis = lore_manager.query_lore(
    "How do basic principles affect key powers?"
)
```

## 🤝 Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## 📜 License

This project is licensed under the MIT License - see [LICENSE.md](LICENSE.md)

## 🌟 Acknowledgments

- Based on the [Loremaster 6000 project](https://github.com/dottxt-ai/demos/lore-generator)
- Inspired by traditional world-building techniques
- Built with amazing open-source tools

---

<p align="center">
  Made with ❤️ for world-builders everywhere
</p>

