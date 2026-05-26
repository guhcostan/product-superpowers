---
name: pm-visual-workspace
description: Use when presenting PM artifacts visually — OSTs, story maps, roadmaps, prioritization matrices, or competitive landscapes
---

# PM Visual Workspace

Browser-based visual companion for PM diagrams, matrices, and maps. When a text description doesn't do justice to spatial relationships, trade-offs, or user journeys — render them visually.

**Core principle:** Show, don't just tell. PM artifacts like story maps, prioritization matrices, and roadmap views are spatial — the user understands them better by seeing them.

**Announce at start:** "I'm using the pm-visual-workspace skill to show this visually."

## When to Use

Decide per-question: **would the user understand this better by seeing it than reading it?**

**Use the browser** for content that IS visual:
- **Opportunity Solution Trees** — hierarchical maps from outcome → opportunity → solution → experiment
- **Story Maps** — user journey backbone with prioritized stories below
- **Prioritization matrices** — 2x2 Value vs. Effort, RICE scores visualized
- **Roadmaps** — Now/Next/Later with swimlanes and dependencies
- **Competitive landscapes** — Strategic group maps, feature matrices as visual grids
- **Kano model diagrams** — Satisfaction vs. functionality plotted
- **User journey maps** — Timeline with emotions, touchpoints, pain points
- **Funnel visualizations** — AARRR with drop-off percentages

**Use the terminal** for content that is text:
- Requirements discussions
- Metric definitions
- Trade-off rationale
- Stakeholder update drafts
- Conceptual choices

## How It Works

Uses the Superpowers visual companion infrastructure. Requires the scripts from `superpowers/skills/brainstorming/scripts/`:
- `start-server.sh` — launches the browser server
- `stop-server.sh` — stops the server
- `server.cjs` — Node.js file-watching server
- `frame-template.html` — page frame with CSS and interaction
- `helper.js` — client-side selection tracking

**Install the scripts:**
```bash
# From your superpowers installation
cp -r ~/.config/claude/plugins/superpowers/skills/brainstorming/scripts/ skills/pm-visual-workspace/scripts/
```

## Starting a Session

```bash
scripts/start-server.sh --project-dir /path/to/project
# Returns: {"type":"server-started","port":52341,"url":"http://localhost:52341",
#           "screen_dir":"/path/.superpowers/brainstorm/.../content",
#           "state_dir":"/path/.superpowers/brainstorm/.../state"}
```

Save `screen_dir` and `state_dir`. Tell the user to open the URL.

## PM Visual Components

### Opportunity Solution Tree

```html
<h2>Opportunity Solution Tree — Increase Activation</h2>

<div style="font-family: monospace; padding: 2rem;">
<pre style="line-height: 1.8;">
                    <b>[OUTCOME]</b>
                  Increase Activation
                        │
     ┌──────────────────┼──────────────────┐
     │                  │                  │
[OPPORTUNITY]     [OPPORTUNITY]      [OPPORTUNITY]
Don't know        Empty state        Setup takes
what to do        overwhelming       too long
     │                  │                  │
 ┌───┴───┐        ┌───┴───┐        ┌───┴───┐
 │       │        │       │        │       │
Guided  Templates Quick-start Sample  Import  SSO
tour              templates  data    wizard  setup
 │       │            │
 │       │            │
[A/B test]  [Prototype]   [Concierge]
 3 vs 5      5 users       5 users
 steps                      manual
</pre>
</div>
```

### Story Map

```html
<h2>Story Map — Onboarding Flow</h2>

<table style="width:100%; border-collapse: collapse;">
<tr style="background:#1a1a2e; color:white;">
  <th>Sign Up</th><th>Setup</th><th>First Action</th><th>Invite</th>
</tr>
<tr style="background:#e8f5e9;">
  <td>Email + password</td><td>Create workspace</td><td>Create first project</td><td>Invite by email</td>
</tr>
<tr style="background:#e8f5e9;">
  <td>Google SSO</td><td>Import data</td><td>Use template</td><td>Share link</td>
</tr>
<tr style="background:#fff3e0; border-top: 3px dashed #ff9800;">
  <td colspan="4" style="text-align:center; color:#e65100;">⬆ MVP — above this line ⬆</td>
</tr>
<tr style="background:#f5f5f5;">
  <td>SAML SSO</td><td>Custom branding</td><td>Advanced templates</td><td>Team permissions</td>
</tr>
</table>
```

### Prioritization Matrix (2x2)

```html
<h2>Value vs. Effort Matrix</h2>

<div style="display:grid; grid-template-columns:1fr 1fr; grid-template-rows:1fr 1fr; gap:8px; height:400px;">
  <div style="background:#e8f5e9; padding:1rem; border-radius:8px;">
    <h3>Quick Wins</h3>
    <ul><li>Add Google SSO</li><li>Fix top 5 bugs</li><li>Export CSV</li></ul>
  </div>
  <div style="background:#e3f2fd; padding:1rem; border-radius:8px;">
    <h3>Big Bets</h3>
    <ul><li>AI recommendations</li><li>Mobile app</li><li>Public API</li></ul>
  </div>
  <div style="background:#f5f5f5; padding:1rem; border-radius:8px;">
    <h3>Fill-ins</h3>
    <ul><li>Dark mode</li><li>Custom emoji</li></ul>
  </div>
  <div style="background:#ffebee; padding:1rem; border-radius:8px;">
    <h3>Time Sinks</h3>
    <ul><li>Custom reporting engine</li><li>On-prem deployment</li></ul>
  </div>
</div>
```

### Now/Next/Later Roadmap

```html
<h2>Product Roadmap</h2>

<div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:1rem;">
  <div style="background:#e8f5e9; padding:1rem; border-radius:8px;">
    <h3>Now</h3>
    <p style="color:#666; font-size:0.8rem;">High confidence</p>
    <div class="card" style="margin:0.5rem 0; padding:0.5rem;">
      <b>Onboarding redesign</b><br>
      <small>Target: +25% activation</small>
    </div>
    <div class="card" style="margin:0.5rem 0; padding:0.5rem;">
      <b>Performance sprint</b><br>
      <small>Target: P95 < 2s</small>
    </div>
  </div>
  <div style="background:#fff3e0; padding:1rem; border-radius:8px;">
    <h3>Next</h3>
    <p style="color:#666; font-size:0.8rem;">Medium confidence</p>
    <div class="card" style="margin:0.5rem 0; padding:0.5rem;">
      <b>Team collaboration</b><br>
      <small>Needs more discovery</small>
    </div>
  </div>
  <div style="background:#f5f5f5; padding:1rem; border-radius:8px;">
    <h3>Later</h3>
    <p style="color:#666; font-size:0.8rem;">Low confidence</p>
    <div class="card" style="margin:0.5rem 0; padding:0.5rem;">
      <b>Mobile app</b><br>
      <small>Exploratory</small>
    </div>
  </div>
</div>
```

### Competitive Feature Matrix

```html
<h2>Competitive Feature Comparison</h2>

<table style="width:100%; border-collapse:collapse;">
<tr style="background:#1a1a2e; color:white;">
  <th>Feature</th><th>Us</th><th>Competitor A</th><th>Competitor B</th>
</tr>
<tr><td>Real-time collaboration</td><td>✅</td><td>✅</td><td>⚠️</td></tr>
<tr><td>AI recommendations</td><td>✅</td><td>❌</td><td>❌</td></tr>
<tr><td>Offline mode</td><td>❌</td><td>✅</td><td>✅</td></tr>
<tr><td>API access</td><td>✅</td><td>✅</td><td>✅</td></tr>
<tr><td>Custom dashboards</td><td>⚠️</td><td>✅</td><td>❌</td></tr>
</table>
<p><small>✅ Full  ⚠️ Partial  ❌ Missing</small></p>
```

## Tips

- **Scale fidelity to the question** — wireframe-level for brainstorming, polished for executive review
- **2-4 options max** per comparison screen
- **Explain the question** on each page — "Which prioritization feels right?" not "Pick one"
- **Iterate before advancing** — if feedback changes the view, write a new version
- **Use real data** when it's available — placeholder content hides real issues
- **Semantic file names**: `ost-activation.html`, `story-map-v2.html`, `roadmap-q3.html`
- **Never reuse filenames** — each screen gets a fresh file

## Integration

This skill provides PM-specific visual components. The server infrastructure is shared with Superpowers' visual companion. See the full companion guide at `skills/brainstorming/visual-companion.md` (if Superpowers is installed) for details on the interaction loop, events format, CSS classes, and cleanup.

## Cleaning Up

```bash
scripts/stop-server.sh $SESSION_DIR
```
