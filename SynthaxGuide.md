# LogicSlayer: The Definitive Syntax Guide

This guide provides the core building blocks for "vanquishng" complex processes using Mermaid logic. 

---

## 1. The Core Declaration
Every file must begin with a type and direction. LogicSlayer is optimized for **horizontal** layouts to fit slide formats.

| Code | Result | Use Case |
| :--- | :--- | :--- |
| `graph LR` | Left to Right | **Slide format (Recommended)** |
| `graph TD` | Top Down | Detailed technical documentation |

---

## 2. Node Geometry (Shapes)
The brackets you use around a label define its visual meaning on the slide.

| Syntax | Visual Shape | Operational Meaning |
| :--- | :--- | :--- |
| `A[Process]` | **Square** | A standard action or task. |
| `B{Decision}` | **Diamond** | A split in logic (Yes/No, If/Then). |
| `C(Start)` | **Rounded** | Entry or Exit points of a process. |
| `D((Goal))` | **Circle** | Milestones or final business objectives. |
| `E[[Sub]]` | **Double Border** | A separate process defined elsewhere. |

---

## 3. Connecting the Logic (Edges)
Arrows define the flow of authority or information.

* **Standard Arrow:** `A --> B`
* **Text on Arrow:** `A -- Approved --> B`
* **Dashed (Optional):** `A -.-> B`
* **Thick (Priority):** `A ==> B`

---

## 4. Visual Styling (Slayer Themes)
You can highlight specific nodes by applying manual styles at the end of your logic.

* **Highlight a Node:** `style NodeID fill:#ff3f34,color:#fff,stroke:#333`
* **Dashed Border:** `style NodeID stroke-dasharray: 5 5`

---

## 5. Appendix: Glossary of Visual Symbols
*For non-technical stakeholders reviewing LogicSlayer exports.*

| Symbol | Syntax | Meaning in the Workflow |
| :--- | :---: | :--- |
| **Terminator** | `(Text)` | Identifies where a process begins or where the user exits. |
| **Process** | `[Text]` | A discrete task, work item, or calculation. |
| **Decision** | `{Text}` | A fork in the road. Stakeholders should check the labeled arrows (Yes/No) here. |
| **Milestone** | `((Text))` | Represents a critical achievement, goal, or interface point. |
| **Subroutine** | `[[Text]]` | Indicates a complex secondary process that happens "behind the scenes." |
| **Database** | `[(Text)]` | A point where information is stored or retrieved from a system. |
| **Directed Flow** | `-->` | The absolute path of authority; where the work moves next. |
| **Dotted Flow** | `-.->` | Non-blocking or informational flow (e.g., an automated notification). |

---

## 6. Slayer Best Practices
1.  **Unique IDs:** Always use short, unique IDs (like `A`, `B`, `Step1`) and put the readable text in the brackets `[Text]`.
2.  **Logic-First:** Don't worry about where the boxes sit. Mermaid handles the layout automatically.
3.  **Label Decisions:** Always label the arrows coming out of a diamond `{}`.
4.  **Export Often:** Use the **Unified Export** in LogicSlayer to keep your `.mmd` source file alongside your `.svg` visual.

---
**LogicSlayer v1.1** | *Complexity is the enemy. Logic is the weapon.*
