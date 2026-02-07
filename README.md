# Project Minerva

A collection of utilities for The Campaign Trail browser game. Each utility has a code 1 and code 2 so that they can be seen in action. All relevant code is at the end of the code 2 file, with comments

---
## Crediting
If you end up using any of these utilities, drop a link to the repo in the Code 2 of your mod.

## Utilities

- [State Visit Flavor](#-state-visit-flavor)
- [Dynamic Candidate Names](#-dynamic-candidate-names)
- [1 Election, 1 Candidate RCV](#-rcv)

### `State Visit Flavor`
**Only compatible with CTS for now**
**Description:**  
When you confirm the visit to a state, you will get another pop-up with flavor text about the visit. Clicking the "Continue" button in that pop-up will lead you back to the questions.

**Provided Example:**
Visiting Vermont will trigger the visit summary screen.

### `Dynamic Candidate Names`
**Only compatible with CTS for now**
**Description:**  
In the map during the campaign, during the vote count and after it, as well as in the ending tables (both global and per-state) the displayed name of the candidates will be dynamic based on different circumstances, while not modifying the name of the candidate object.

**Provided Example:**

In all states bar CA, the displayed names of Trump and Hillary will depend on who's winning (or won, after the vote count) the state.

In California the displayed names are always the same.

During the vote count, the names displayed will depend on who's ahead in electoral votes at that moment. The candidates here will always be sorted from most to least EVs.

The global table names will depend on who won the election. 

Each state's table names will depend on who won the state.

### `RCV`
**1 candidate and 1 election RCV (compatible with both CTS and NCT)**
**Description:**  
Implementation of RCV to simulate an election in which a single candidate is chosen (e.g Democratic Party NYC mayoral primaries). First choice votes are the base game voting percentages, second choice and beyond are simulated through transferability matrixes in each state. 

A transferability matrix shows what percentage of voters that choose (candidate represented in the row) would instead vote for (candidate represented in the column) if their original pick was eliminated. 

Includes functions to represent co-endorsements, one-way endorsements, candidates dropping out, someone from outside endorsing and simply changing the support of a column from one or more rows in the matrixes; as well as changing how the final table looks. 

Includes the possibility of using batch elimination in the vote count.

**Provided Example:**
The mod is a little showcase of each function. Double click on a state to get it's transferability matrix.



