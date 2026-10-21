# Code Review Checklist

This checklist corresponds directly to the 4 core steps defined in [SKILL.md](file:///Users/vikramshinde/Learning/GMS%20AI/tryout/.agents/skills/code-review/SKILL.md).

---

## 1. Correctness
*Verify that the code satisfies specifications and behaves as intended.*

- [ ] **Functional Requirements**: Does the code fulfill the requested behavior and acceptance criteria?
- [ ] **Logic & Calculations**: Are equations, formulas, state updates, and branching conditions mathematically and logically correct?
- [ ] **Type & Data Integrity**: Are types, schema contracts, and API return values handled accurately without unintentional coercions?
- [ ] **Control Flow**: Are all conditional paths, loops, and async sequences properly awaited, branched, and resolved?
- [ ] **File / Format Validity**: Are source files free of unintended syntax artifacts, markdown fences, or copy-paste errors?

---

## 2. Edge Cases
*Ensure error conditions and boundaries are handled robustly.*

- [ ] **Null / Undefined / Empty Values**: Are optional references, empty strings, and empty collections gracefully handled?
- [ ] **Boundary Conditions**: Are bounds handled correctly (0, negative numbers, maximum values, off-by-one indices)?
- [ ] **User & Device Inputs**: Are all user input vectors accounted for (e.g., clicks, taps, drag/touch events, keyboard navigation)?
- [ ] **System & Network Failures**: Are network errors, audio device suspension, missing permissions, or rejected promises caught and communicated?
- [ ] **Saturation & Overflow**: Are resource limits, audio volume stacking, or numeric overflow guarded against clipping or crashes?

---

## 3. Style
*Follow project naming and architectural patterns.*

- [ ] **Naming Conventions**: Are functions, variables, and components descriptive and aligned with project conventions?
- [ ] **Separation of Concerns**: Is markup, styling, business logic, and presentation appropriately decoupled?
- [ ] **Modularity & Simplicity**: Are functions concise and focused on a single responsibility? Avoid deeply nested logic.
- [ ] **No Magic Values**: Are hardcoded strings, frequencies, coordinates, and thresholds extracted into named constants or configs?
- [ ] **Clean Syntax**: Is the code free of dead code, commented-out debugging statements, and redundant boilerplate?

---

## 4. Performance
*Identify potential bottlenecks or inefficiencies.*

- [ ] **DOM & Rendering Efficiency**: Avoid forced synchronous layout thrashing (e.g. repeated `offsetWidth` reads) and unnecessary re-renders.
- [ ] **Memory Management**: Are off-screen elements, caches, and event listeners cleaned up or bounded to prevent unbounded growth?
- [ ] **Algorithmic Complexity**: Are iterations and data searches optimized (e.g., using Sets/Maps instead of nested array scans)?
- [ ] **Resource Lifecycle**: Are audio nodes, timers, file streams, and network connections deterministically stopped and disconnected?
- [ ] **Asset Size & Startup**: Is initial page load and initialization lightweight and non-blocking?
