# 🚀 Space Mission Roster

A vanilla JavaScript application for managing a space mission crew — add astronauts, swap positions, filter EVA-eligible members, and organize teams into operational chunks.

---

## 📋 About

**Space Mission Roster** is a pure JavaScript project built as part of the [freeCodeCamp](https://www.freecodecamp.org/) JavaScript curriculum (v9). It demonstrates core JS concepts — arrays, objects, loops, sorting, and array manipulation — through the practical scenario of assembling a space crew.

---

## 📁 Project Structure

```
Space-Mission-Roster/
├── main.js       # All application logic
└── README.md
```

---

## 🛸 Crew Object Structure

Each astronaut is represented as an object with the following fields:

```js
const astronaut = {
  id: 1,
  name: "Andy",
  role: "Commander",
  isEVAEligible: true,
  priority: 3
};
```

| Field | Type | Description |
|---|---|---|
| `id` | `Number` | Unique identifier for the astronaut |
| `name` | `String` | Astronaut's name |
| `role` | `String` | Mission role (e.g. Commander, Pilot) |
| `isEVAEligible` | `Boolean` | Whether the astronaut can perform spacewalks |
| `priority` | `Number` | Mission priority ranking (higher = more critical) |

---

## ✨ Features & Functions

### `addCrewMember(crew, astronaut)`
Adds an astronaut to the crew array. Checks for duplicate IDs before adding — logs a warning and returns early if a duplicate is found.

```js
addCrewMember(squad, firstAstronaut);
```

---

### `swapCrewMembers(crew, fromIndex, toIndex)`
Swaps two crew members by their array indices. Validates that both indices are within bounds — logs `"Invalid crew indices"` and returns early if not. Returns a new array without mutating the original.

```js
const updatedSquad = swapCrewMembers(squad, 2, 5);
```

---

### `sortByPriorityDescending(crew)`
Sorts a crew array **in place** by `priority` in descending order using bubble sort. Higher priority astronauts appear first.

---

### `getEVAReadyCrew(crew)`
Filters the crew to only EVA-eligible astronauts (`isEVAEligible: true`), then sorts them by priority descending. Returns the filtered, sorted array.

```js
const EVAReadySquad = getEVAReadyCrew(updatedSquad);
```

---

### `chunkCrew(crew, size)`
Splits a crew array into smaller sub-arrays ("chunks") of a given size. Useful for dividing the EVA team into operational groups. Logs a warning if `size < 1`.

```js
const EVAChunks = chunkCrew(EVAReadySquad, 3);
```

---

### `printCrewSummary(crew)`
Prints all crew members' names to the console, sorted by priority descending. Does not mutate the original array.

```js
printCrewSummary(updatedSquad);
```

---

## 👨‍🚀 Full Crew Roster

| ID | Name | Role | EVA Eligible | Priority |
|---|---|---|---|---|
| 1 | Andy | Commander | ✅ | 3 |
| 2 | Bart | Pilot | ❌ | 8 |
| 3 | Caroline | Engineer | ✅ | 4 |
| 4 | Diego | Scientist | ❌ | 1 |
| 5 | Elise | Medic | ✅ | 7 |
| 6 | Felix | Navigator | ✅ | 6 |
| 7 | Gertrude | Communications | ❌ | 4 |
| 8 | Hank | Mechanic | ✅ | 2 |
| 9 | Irene | Specialist | ✅ | 5 |
| 10 | Joan | Technician | ❌ | 1 |

---

## 🚀 How to Run

No dependencies or build steps required — just plain JavaScript.

**In the terminal:**
```bash
node main.js
```

**In the browser:**
Link `main.js` to an HTML file and open the console:
```html
<script src="main.js"></script>
```

---

## 🧠 Concepts Covered

- Arrays and objects
- `for` loops and `for...of` loops
- Functions and early returns
- Array methods: `push`, `slice`, `splice`
- Bubble sort algorithm
- Array chunking / pagination logic
- Input validation and guard clauses

---

## 🎓 Built With

- **JavaScript (ES6+)** — vanilla, no frameworks or libraries
- Completed as part of the [freeCodeCamp JavaScript Algorithms and Data Structures](https://www.freecodecamp.org/learn) curriculum

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
