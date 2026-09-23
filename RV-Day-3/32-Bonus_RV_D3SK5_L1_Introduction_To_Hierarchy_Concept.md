# 32-Bonus_RV_D3SK5_L1_Introduction_To_Hierarchy_Concept

The lecture explains:

- replicated hierarchy
- hierarchical scopes
- lexical re-entrance
- hierarchical references
---

# Behavioral Hierarchy

Behavioral hierarchy means logic replicated behaviorally rather than manually instantiating modules repeatedly.

---

# Conway’s Game of Life

The simulation contains a grid of cells where each cell is either alive or dead.

## Cell Neighborhood Logic

The next-state behavior depends on neighboring cells. The decision is all based on the nine cells in the cell's immediate neighborhood.
Meaning - 3×3 neighborhood considered.

## Counting Alive Neighbors

The hardware first computes number of alive neighbors, including the cell itself total count includes:

- center cell
- surrounding neighbors

## Replicated Hierarchy

We create a replicated context for defining the logic of each cell.

---
## Hierarchical Signal Navigation

Signals may be accessed:

- upward
- downward
- sideways

through hierarchy tree.

---

# Hardware Perspective

Hierarchy allows scalable hardware replication. Without hierarchy large repeated structures become impossible to manage manually.

---

# Key Learning Outcome

After this lecture, the learner understands:

- behavioral hierarchy
- replicated logic
- lexical re-entrance

