# Reconstructing Bridgewater

Reconstructing Bridgewater is a Python-based, narrative-driven educational game that simulates the software engineering requirements elicitation and stakeholder interview process through interactive gameplay.

Players explore a hurricane-damaged town and gather requirements by interviewing multiple community stakeholders, evaluating conflicting information, and making prioritization decisions. These choices directly affect the difficulty and outcome of a Tetris-style reconstruction phase, modeling how early design decisions influence downstream implementation.

🎮 **Play the game:** https://segvcs.itch.io/hurricane-recovery

---

## Core Features

- **Stakeholder Interview System** – Limited question budget simulating real-world constraints  
- **Decision-Based Prioritization** – Make trade-off decisions with consequences  
- **Credibility & Conflict Analysis** – Evaluate stakeholder reliability and conflicting information  
- **Tetris-Based Implementation** – Simulate resource allocation through gameplay  
- **Dynamic Difficulty** – Game challenge scales based on decision quality  
- **Performance Feedback** – Reflection phase analyzing outcomes and decisions  

---

## What You'll Learn

This game teaches real software engineering concepts:
- Requirements gathering limitations and trade-offs
- Stakeholder management and communication
- Prioritization under constraints
- How early decisions impact implementation complexity
- Technical debt and risk assessment

---

## Tech Stack

### Programming Language & Framework
- **Python 3** – Core application logic  
- **Pygame** – Rendering, event handling, UI, and game loop management  

### Software Architecture

- **Scene-Based Architecture**
  - Modular, independent game phases:
    - Act 1: Storyline & World Building
    - Act 2: Stakeholder Interviews
    - Act 3: Decision & Prioritization
    - Tetris Reconstruction Phase
    - Final Summary & Feedback

- **Centralized State Management**
  - `GameState` object maintains:
    - Player progress and session data
    - Interview selections and question tracking
    - Scores, outcomes, and game metrics

- **Scene Manager**
  - Orchestrates scene transitions
  - Persists game state across phases
  - Controls flow of the SDLC simulation

### Gameplay Systems

- **Dialog & Interview Engine**
  - Predefined stakeholder questions and responses
  - Trust and relevance scoring
  - Enforced question budget to simulate resource constraints

- **Decision Engine**
  - Multiple-choice requirement prioritization
  - Converts stakeholder input into infrastructure decisions
  - Tracks decision consistency and credibility

- **Tetris-Based Simulation**
  - Grid-based resource placement and block stacking
  - Dynamic difficulty scaling based on decision quality
  - Real-time performance metrics

### Data Management

- **JSON Storage**
  - Avatar profiles and stakeholder data
  - Dialogue and narrative content
  - Game configuration and state serialization

### Packaging & Deployment

- **PyInstaller**
  - Generates standalone Windows executables
  - `.spec` configuration for reproducible builds

---

## Getting Started

### Requirements
- Python 3.7+
- Pygame

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/reconstructing-bridgewater.git
cd reconstructing-bridgewater

# Install dependencies
pip install pygame

# Run the game
python main.py
```

### Building an Executable

```bash
pip install pyinstaller
pyinstaller main.spec
```

The `.exe` will be generated in the `dist/` folder.

---

## Project Structure

```
reconstructing-bridgewater/
├── main.py                      # Game entry point & scene manager
├── scenes/                      # Game phase implementations
│   ├── act1_storyline.py       # Opening narrative
│   ├── act2_characters.py      # Stakeholder introduction
│   ├── act3_multipleChoice.py  # Decision phase
│   ├── avatar_profile.py       # Interview system
│   ├── final_scene.py          # Feedback & summary
│   ├── game_purpose.py         # Tutorial/context
│   ├── avatars/                # Character graphics
│   ├── backgrounds/            # Scene backgrounds
│   └── avatars_data.json       # Stakeholder profiles & dialogue
├── TetrisGame/                 # Tetris mini-game
│   ├── tetris_game.py         # Game implementation
│   ├── requirements.txt        # Pygame dependency
│   └── img/                    # Game assets
└── build/                      # PyInstaller build artifacts
```

---

## How It Works

1. **Storyline Phase** – Set the context and meet stakeholders
2. **Interview Phase** – Ask questions with a limited budget, build understanding
3. **Decision Phase** – Prioritize conflicting requirements and make trade-offs
4. **Reconstruction Phase** – Play Tetris where difficulty reflects decision quality
5. **Feedback Phase** – Review outcomes and learn from your choices

---

## Contributing

Contributions welcome! Feel free to fork, improve, and submit pull requests.

---

## License

[Add your license here, e.g., MIT, GPL-3.0]

---

## Acknowledgments

This project combines game development, software architecture, and educational simulation to teach real-world software engineering concepts through interactive storytelling and gameplay.
