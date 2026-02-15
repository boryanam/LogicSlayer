# Product Requirements Document: LogicSlayer 1.1

**Product Vision:** Complexity is the enemy. Logic is the weapon.  
**Status:** Approved / Ready for Release  
**Document Version:** 1.1.0  
**Date:** February 14, 2026

---

## 1. Executive Summary
**LogicSlayer** is a high-performance, browser-based utility designed to bridge the gap between complex mental logic and professional visual communication. By utilizing a **code-first approach**, it allows users to "vanquish" the manual friction of traditional drag-and-drop tools, producing slide-optimized directed flowcharts and strategic diagrams ready for executive presentations and technical version control.

---

## 2. Target Audience
* **Product Managers:** Mapping user journeys, feature discovery, and roadmaps.
* **Operations Professionals:** Managing high-density operational workflows, SOPs, and resource distribution (Sankey).
* **System Architects:** Documenting technical infrastructure and data flows.
* **Developers:** Maintaining logic-based documentation as code within Git repositories.

---

## 3. Problem Statement
Current flowcharting solutions suffer from three primary "Complexity Monsters":
1.  **Manual Toil:** Drag-and-drop interfaces make layout consistency difficult and updates time-consuming.
2.  **Cognitive Noise:** Real-time rendering tools distract users with syntax error flags during active brainstorming.
3.  **Asset Fragmentation:** Visual exports (images) quickly become disconnected from their source logic, making long-term iteration impossible.

---

## 4. Functional Requirements

| ID | Feature | Description | Priority |
| :--- | :--- | :--- | :--- |
| **FR-1** | **The Slayer Forge** | A manual "Forge Flow" button that renders Mermaid code only on command. | P0 |
| **FR-2** | **Slide-Ready Mode** | Default horizontal (`LR`) orientation for standard 16:9 formats. | P0 |
| **FR-3** | **Unified Export** | Single-click action to export both a `.svg` visual and a `.mmd` source file with identical naming. | P0 |
| **FR-4** | **6-Tool Snippet Library** | Templates for: Linear Process, Decision Path, User Journey, Mindmap, Roadmap (Gantt), and Sankey. | P0 |
| **FR-5** | **Dynamic Naming** | Input field to define filenames across all export types. | P1 |
| **FR-6** | **Outcome Styling** | Snippets include syntax examples for coloring nodes (e.g., green for Success, red for Fail). | P1 |



---

## 5. User Stories
* **As a PM**, I want to use a **Mindmap** for discovery and a **Roadmap** for planning within the same tool to keep my project logic unified.
* **As an Operations Manager**, I want to use **Sankey diagrams** to visualize budget or resource distribution across departments.
* **As a Stakeholder**, I want to see colored outcomes in a **Decision Path** so I can instantly identify high-risk vs. success branches.

---

## 6. Technical Specifications
* **Rendering Engine:** Mermaid.js (Version 10.9.1 stable).
* **Archetypes Supported:** `graph`, `journey`, `mindmap`, `gantt`, `sankey-beta`.
* **Architecture:** Zero-dependency, single-file HTML/JS/CSS application.
* **Privacy:** 100% Client-side; data remains in local browser memory. No external API calls are made with user data.

---

## 7. Cross-Functional Collaboration
LogicSlayer introduces the **"Source of Truth"** workflow to eliminate departmental silos:
1.  **Creation:** The PM or Architect forges the initial logic in the editor.
2.  **Verification:** Operations audits the `.mmd` source file, identifies gaps, and updates logic directly.
3.  **Sync:** Both teams commit the same `.mmd` file to a shared repository (e.g., GitHub), ensuring the visual slide and operational reality are identical.

---

## 8. Glossary of Terms
* **Node:** A single step or state, defined in code as `ID[Label]`.
* **Directed Edge:** An arrow (`-->`) showing the specific direction of flow.
* **Decision Gate:** A diamond-shaped split (`{}`) for branching logic.
* **Sankey Diagram:** A flow diagram in which the width of the arrows is proportional to the flow rate.
* **Gantt (Roadmap):** A bar chart that illustrates a project schedule and task durations.

---

## 9. Operational Use Cases
* **Standard Operating Procedures (SOPs):** Transforming text manuals into digestible horizontal flows for staff training.
* **Resource Allocation:** Using Sankey diagrams to map budget, labor, or data distribution.
* **User Experience Mapping:** Utilizing the User Journey snippet to track emotional states and pain points.



---

## 10. UI/UX Design Principles
* **Slayer Aesthetic:** Dark-mode sidebar (Drafting) vs. light-mode preview (Presenting) to help users distinguish between work-in-progress and final output.
* **3x2 Snippet Grid:** Instant access to the 6 core strategic archetypes to reduce learning friction.
* **Minimalist Toolbar:** Unified control for naming and exporting packages, keeping the workspace clutter-free.

---

## 11. Risk Assessment & Mitigations
* **Risk:** Browser blocks multiple downloads for the "Unified Export."
    * **Mitigation:** First-time users are prompted via browser native alerts to "Allow Multiple Downloads."
* **Risk:** Complexity of Mermaid syntax for non-technical users.
    * **Mitigation:** Extensive snippet library and syntax appendix provided within the documentation for quick reference.

---

## 12. Success Metrics
* **Zero-Drift Logic:** 100% of visual assets in project folders match their corresponding `.mmd` source files.
* **Efficiency:** 50% reduction in time spent on manual chart "polishing" (aligning boxes, snapping arrows).

---

## 13. Future Roadmap (V2.0)
* **Slayer Import:** Drag-and-drop `.mmd` files directly into the editor to resume editing sessions.
* **Global Theme Picker:** One-click color palette shifts for corporate branding (e.g., "Corporate Blue" or "Success Green" themes).

---

## Appendix A: Stakeholder Quick Reference
Stakeholders reviewing a LogicSlayer export should use this visual key:

* **Rectangles `[]`**: Standard Process Steps or actions.
* **Diamonds `{}`**: Decision Points (Require a choice/branch).
* **Rounded Rectangles `()`**: Entry and Exit points (Start/End).
* **Double Circles `(())`**: Major Milestones or Goals.
* **Colors**: Green (Success/Safe), Yellow (Warning/Iterate), Red (Critical/Error).



---

## Appendix B: Syntax Reference

| Syntax Element | Code Example | Output |
| :--- | :--- | :--- |
| **Horizontal Flow** | `graph LR` | Flows left to right. |
| **Labeled Edge** | `A -- Yes --> B` | Arrow with "Yes" text overlay. |
| **Outcome Styling** | `style A fill:#2ecc71` | Colors a specific node green. |
| **Roadmap** | `gantt` | Generates a timeline with date ranges. |
| **Mindmap** | `mindmap` | Generates a hierarchical discovery map. |

---

## Appendix C: Glossary of Visual Symbols

| Symbol | Syntax | Meaning in the Workflow |
| :--- | :---: | :--- |
| **Terminator** | `(Text)` | Identifies where a process begins or ends. |
| **Process** | `[Text]` | A discrete task, action, or work item. |
| **Decision** | `{Text}` | A fork in the road; check labeled arrows for conditions. |
| **Milestone** | `((Text))` | Represents a critical achievement or goal. |
| **Database** | `[(Text)]` | A point where information is stored or retrieved. |
| **Sankey Flow** | `Source, Target, Val` | Resource or data distribution path proportional to volume. |

---
**LogicSlayer v1.1** | *Complexity is the enemy. Logic is the weapon.*
