# cnfuzn.ai
link[site 'https://jaikushwaha7.github.io/cnfuzn/']
Diagnose a confusion, size it as a disk tree, apply the matching method, finish with a next step.

| Path | What it is |
|---|---|
| `index.html` | The cnfuzn.ai site and working engine (open in a browser; no server, no account). |
| `diagrams/*.mmd` | Mermaid flow sources (master flow, five roots, disk-tree sizing). |
| `hyperframes/confusion-flow/index.html` | HyperFrames composition: a 24s explainer video of the product flow. |
| `hyperframes/confusion-to-complexity/index.html` | HyperFrames composition: a 57s zoom from microbe to cosmic web ("From confusion to complexity"). Original vector art, deterministic (seeded), 1920x1080. |
| `assets/` | Web encodes of the rendered journey for the site: `journey.mp4` (player, 1280p), `journey-bg.mp4` (soft blurred page background, 480p), and a poster. The full 1080p render lives in `hyperframes/confusion-to-complexity/renders/`. |
| `diagrams/scale-journey.mmd` | Mermaid map of the nine scales in that video. |
| `.claude/skills/confusion-ai/` | Claude skill anyone can install. |
| `clarity-compass.html` | Earlier "Clarity Compass" prototype. |

## Run the site locally
The page loads videos from `assets/`, so serve the folder instead of opening the file directly:
```
python -m http.server 8765
```
then open http://localhost:8765. The background video is skipped automatically for visitors who prefer reduced motion or have data saver on.

## Install the skill
Copy `.claude/skills/confusion-ai/` to `~/.claude/skills/` (all projects) or keep it in a project's `.claude/skills/`. Then ask Claude: "I'm confused about…".

## Render the video
Needs Node 22+ and FFmpeg.
```
cd hyperframes/confusion-to-complexity   # or hyperframes/confusion-flow
npx hyperframes lint
npx hyperframes preview
npx hyperframes render
```
