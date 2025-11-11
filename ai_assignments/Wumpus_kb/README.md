# 🧠 Wumpus World – Knowledge-Based Agent

This project implements a logical inference agent for the Wumpus World — a classic AI problem from knowledge representation and reasoning.
The agent uses propositional logic (not full SAT solving, but smart inference rules) to identify safe cells, infer pits, and grab gold safely in a small 4×4 grid world.

### Overview

In this 4×4 world:

- Some cells contain Pits (fall = death).

- One cell contains a Wumpus (you die if you walk into it).

- One cell contains Gold (your goal).

The agent perceives:

- Breeze → one or more neighboring cells contain a pit.

- Stench → Wumpus is in a neighboring cell.

- Glitter → gold is in the current cell.

## Agent: Knowledge Based

| Rule                                    | Meaning                                       |
| --------------------------------------- | --------------------------------------------- |
| ¬B(x,y) ⇒ all neighbors are safe        | If no breeze → no pits nearby                 |
| B(x,y) ⇒ at least one neighbor is a pit | If breeze → one or more neighbors may be pits |
| If a cell becomes known-safe            | Remove it from all “possible pit” lists       |
| If only one possible pit remains        | Mark it as a **definite pit**                 |

