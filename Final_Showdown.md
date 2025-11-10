# 🏆 AI Coding Tools Clash – Advanced Hands-On Exercise
## Build a Mini Checkers Game Engine – GitHub Copilot vs Cline

## ✅ Objective
You will:

- Use AI coding tools to plan and implement a mini Checkers game engine.
- Compare GitHub Copilot and Cline workflows:
  - **Copilot**: Manual context injection + custom chat mode.
  - **Cline**: Automated planning with Plan mode and Memory Bank.

- Implement:
  - Game state management
  - Move validation
  - Capture logic
  - Win condition check

- Optional: Add one bonus feature (score tracking or simple UI feedback).

## 🔹 Starter Concept (Language of Your Choice)
Your game engine should:

- Represent the board (8x8).
- Track positions of pieces.
- Validate moves according to Checkers rules.
- Detect captures and update state.
- Check for win condition (no moves left for opponent).

## ✅ Step-by-Step Instructions

### Step 1: Define the Problem

- Decide your programming language.
- Understand Checkers rules:
  - Pieces move diagonally forward.
  - Captures occur by jumping over opponent pieces.
  - Kings can move backward.
  - Game ends when a player has no valid moves.

### Step 2: Context Building – Different for Each Tool

#### For GitHub Copilot

**Create a Custom Chat Mode**
- File: `.github/instructions/chat-modes.md`
- Mode Name: Instruction Builder
- Behavior Template: (This is a suggestion, feel free to change or tweak as you please)
```
You are an assistant that creates detailed markdown instruction files for game development.
Always include:
- Clear headings
- Bullet points
- Examples where relevant

If any part of the request is ambiguous or unclear, ask clarifying questions before generating the file.
```

✅ This ensures Copilot asks questions before generating instructions.

**Use the Chat Mode to Generate Files**

1. **game-rules.md**
   - Create a markdown file listing Checkers rules for an 8x8 board:
     - Move rules
     - Capture logic
     - King promotion
     - Win condition

2. **technical-spec.md**
   - Generate a technical specification for implementing a Checkers game engine:
     - Functions: `initializeBoard()`, `validateMove()`, `applyMove()`, `checkWinCondition()`
     - Data structures
     - Performance considerations

3. **bonus-feature.md**
   - Suggest one bonus feature for the Checkers game and outline its requirements:
     - Score tracking OR simple UI feedback

💡 **Note**: These prompts are basic suggestions. Feel free to modify or expand them to suit your preferred style or add extra details.

#### For Cline

Do NOT manually create instruction files.
Instead:

1. Memory Bank Setup
- Follow the comprehensive instructions at: [Cline Memory Bank Documentation](https://docs.cline.bot/prompting/cline-memory-bank)
  
2. Start with a high-level goal in the initial prompt: (Again, tweak as you please)
```
Build a Checkers game engine with:
- Game state management
- Move validation
- Capture logic
- Win condition
- Bonus feature: score tracking or UI feedback
```

3. Use Plan mode:
   - Let Cline break down tasks.
   - Automatically generate technical specs and store them in its Memory Bank.

### Step 3: Round 1 – GitHub Copilot

Implement in this order:

1. `initializeBoard()` → Set up starting positions.
2. `validateMove(start, end)` → Check legality.
3. `applyMove(start, end)` → Update board state.
4. `checkWinCondition()` → Determine if game ends.
5. Bonus: `updateScore()` or UI feedback.

Use Copilot chat for refinements:
- Refer to `game-rules.md` and `technical-spec.md`.
- Implement `validateMove()` and `applyMove()`.

Test with sample moves:
- Move piece from (2,3) to (3,4) → valid
- Move piece from (2,3) to (4,5) → invalid

### Step 4: Round 2 – Cline

- Let Cline:
  - Generate specs internally.
  - Implement the same functions in the same order.

Compare:
- How Cline uses persistent context vs Copilot's manual prompts.

### Step 5: Wrap-Up
Reflect:
- Which tool handled multi-step logic better?
- How did context affect output?
- Which tool was faster for iterative changes?

## ✅ Deliverables

- **Copilot**: `game-rules.md`, `technical-spec.md`, `bonus-feature.md`
- Two implementations (Copilot & Cline)
- Notes on differences between tools

## 💡 Optional Stretch Goals

- Multi-jump capture logic.
- King backward moves.
- Persistent game state (save/load).
- Advanced UI (highlight moves, animations).

Good luck! Build your mini Checkers engine and see which AI tool wins! 🎉
