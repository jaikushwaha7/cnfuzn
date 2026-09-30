# cnfuzn.ai

> **Diagnose confusion. See its shape. Find the next step.**

**cnfuzn.ai** is an experimental framework for turning confusion into something you can inspect, structure, and act on.

**Live site:**
https://jaikushwaha7.github.io/cnfuzn/

The core idea is simple:

**Confusion → Diagnosis → Disk Tree → Method → Next Step**

Instead of treating confusion as one large, undefined feeling, cnfuzn.ai breaks it into smaller causes, sizes their relative weight, applies a matching method, and ends with a concrete next action.

---

## The idea

Confusion can appear at many scales.

At the human level, it can come from conflicting information, competing goals, uncertainty, emotion, identity, or difficult decisions.

The project also explores a larger question:

> **How does uncertainty and complexity change as we move from microbes to organisms, humans, societies, planets, galaxies, and the universe?**

This creates two connected visual journeys:

```text
PERSONAL CONFUSION

Confusion
    ↓
What is happening?
    ↓
What is causing it?
    ↓
How large is each cause?
    ↓
Which method fits?
    ↓
What is the next step?
```

and:

```text
FROM CONFUSION TO COMPLEXITY

Microbe
   ↓
Insect
   ↓
Bird
   ↓
Human
   ↓
Society
   ↓
Ecosystem
   ↓
Planet
   ↓
Solar System
   ↓
Galaxy
   ↓
Cosmic Structure
```

At the smaller scales, "confusion" can describe uncertainty or competing signals in an organism.

At larger physical scales, the language shifts from **confusion** toward **complexity, uncertainty, feedback, interaction, and emergence**.

---

## The core workflow

```text
┌─────────────────────┐
│       CONFUSION     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│      DIAGNOSE       │
│ What is actually    │
│ unclear?            │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│      DISK TREE      │
│ Size the causes     │
│ by relative weight  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│       METHOD        │
│ Apply the matching  │
│ way of thinking     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│     NEXT STEP       │
│ What can I do now?  │
└─────────────────────┘
```

The **disk tree** is the project's main way of making confusion visible: instead of seeing one large problem, you see the relative size of its underlying causes.

---

## Five roots of confusion

The current framework organizes personal confusion around five recurring questions:

| Root          | Question                 |
| ------------- | ------------------------ |
| **Truth**     | What is true?            |
| **Want**      | What do I actually want? |
| **Action**    | What should I do?        |
| **Identity**  | Who am I?                |
| **Direction** | Where am I going?        |

These roots can overlap. The purpose is not to force every problem into one category, but to provide a starting structure for diagnosis.

---

## From confusion to complexity

The project includes a visual experiment that zooms across scales:

```text
MICROBE
  ↓
SIGNAL
  ↓
INSECT / ANIMAL
  ↓
SENSORY INFORMATION
  ↓
BIRD
  ↓
NAVIGATION
  ↓
HUMAN
  ↓
COGNITION
  ↓
SOCIETY
  ↓
COLLECTIVE UNCERTAINTY
  ↓
EARTH
  ↓
COMPLEX SYSTEMS
  ↓
SOLAR SYSTEM
  ↓
DYNAMICAL COMPLEXITY
  ↓
GALAXY
  ↓
EMERGENCE
  ↓
COSMIC STRUCTURE
```

### Why this matters

The same word should not be applied literally at every scale.

A microorganism can respond to competing chemical gradients.

An animal can receive conflicting sensory information.

A human can consciously experience uncertainty.

A society can experience distributed disagreement and collective uncertainty.

A planet, solar system, or galaxy does not "feel confused." Instead, its behavior emerges from interacting physical systems.

The visual journey explores this transition:

**signal → uncertainty → decision → interaction → feedback → complexity → emergence**

---

# Project structure

| Path                                           | Description                                                                                                                   |
| ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `index.html`                                   | Main cnfuzn.ai site and working engine. Runs directly in a browser; no server or account required for the application itself. |
| `diagrams/`                                    | Mermaid source files for the project's flows and system diagrams.                                                             |
| `diagrams/master-flow.mmd`                     | Main product/workflow diagram.                                                                                                |
| `diagrams/five-roots.mmd`                      | Map of the five roots of confusion.                                                                                           |
| `diagrams/disk-tree.mmd`                       | Disk-tree model for sizing confusion.                                                                                         |
| `diagrams/scale-journey.mmd`                   | Map of the nine-scale visual journey.                                                                                         |
| `hyperframes/confusion-flow/`                  | HyperFrames composition for the 24-second product-flow explainer.                                                             |
| `hyperframes/confusion-to-complexity/`         | HyperFrames composition for the 57-second "From confusion to complexity" visual journey.                                      |
| `hyperframes/confusion-to-complexity/renders/` | Full-resolution video renders.                                                                                                |
| `assets/`                                      | Web-ready video assets used by the site.                                                                                      |
| `assets/journey.mp4`                           | Main journey video used by the page.                                                                                          |
| `assets/journey-bg.mp4`                        | Soft, blurred background version of the journey video.                                                                        |
| `assets/poster.*`                              | Poster image for the video.                                                                                                   |
| `.claude/skills/confusion-ai/`                 | Claude skill for using the cnfuzn framework in other projects.                                                                |
| `clarity-compass.html`                         | Earlier Clarity Compass prototype.                                                                                            |

---

# Run locally

The site loads video assets from `assets/`, so serve the repository through a local HTTP server rather than opening `index.html` directly.

```bash
python -m http.server 8765
```

Then open:

**http://localhost:8765**

The site automatically avoids the background video for visitors who prefer reduced motion or have data-saving settings enabled.

---

# Install the Claude skill

The repository includes a reusable Claude skill:

```text
.claude/skills/confusion-ai/
```

Install it globally:

```bash
cp -R .claude/skills/confusion-ai ~/.claude/skills/
```

Or keep it inside a specific project's:

```text
.claude/skills/
```

Then ask Claude something like:

```text
I'm confused about choosing between two career paths.
```

The skill applies the cnfuzn framework to help structure the problem.

---

# Render the animations

The animations are built with **HyperFrames**.

Requirements:

* Node.js 22+
* FFmpeg

For the product-flow animation:

```bash
cd hyperframes/confusion-flow
npx hyperframes lint
npx hyperframes preview
npx hyperframes render
```

For the full **From Confusion to Complexity** journey:

```bash
cd hyperframes/confusion-to-complexity
npx hyperframes lint
npx hyperframes preview
npx hyperframes render
```

The second composition produces a **1920×1080** deterministic animation using seeded/original vector artwork.

---

# Design philosophy

cnfuzn.ai is built around a few principles:

### 1. Make the invisible visible

Confusion feels amorphous when all its causes are mixed together.

The disk tree turns those causes into visible structure.

### 2. Separate diagnosis from action

First understand what is happening.

Then decide what to do.

```text
Diagnosis ≠ Decision
```

### 3. Match the method to the problem

Different kinds of confusion require different ways of thinking.

```text
Fact uncertainty    → Evidence
Goal uncertainty    → Values
Decision uncertainty → Options / trade-offs
Identity uncertainty → Reflection
Complexity           → Systems thinking
```

### 4. End with movement

The goal is not to eliminate every uncertainty.

The goal is to identify a useful **next step**.

---

# Status

**Experimental / evolving**

cnfuzn.ai is a design and research project exploring how interfaces, visualizations, cognitive frameworks, and generative tools can help people navigate uncertainty.

The models are intentionally experimental and should be treated as thinking tools rather than clinical, scientific, or psychological diagnostic instruments.

---

# Explore

**Live site:**
https://jaikushwaha7.github.io/cnfuzn/

**Repository:**
https://github.com/jaikushwaha7/cnfuzn

If you experiment with the project, the most useful contributions are new visualizations, better interaction patterns, additional methods for different types of confusion, and clearer ways to move from uncertainty to action.
