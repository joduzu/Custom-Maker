# Custom Maker Toolkit

Custom Maker Toolkit is a collection of browser-based tools for planning, running, and reviewing simulated clinical workflows. Each tool is delivered as a standalone HTML file that can be opened directly in any modern browser—no build step or server setup required.

## Contents

| File | Description |
| --- | --- |
| `index.html` | Hospital Patient Flow Simulator for experimenting with triage mixes, capacity settings, and routing strategies in real time. |
| `maker.html` | Configuration Maker used to author SCT (Specialized Care Team) deployment profiles and export them as `config.json`. |
| `template.html` | Assessment Template that consumes an exported configuration to review readiness checklists filtered by deployment modality. |
| `hospital-patient-flow-design.md` | Concept design brief covering the overall system vision and functional requirements for the simulator experience. |

## Getting Started

1. **Download or clone the repository.**
2. **Open the files locally.** Double-click any HTML file (for example `index.html`) or right-click and choose *Open with* followed by your preferred browser.
3. **Optional: serve over HTTP.** Some browsers limit functionality (like file downloads) when opened directly from disk. To avoid that, start a simple Python server:
   ```bash
   python3 -m http.server 8000
   ```
   Then visit `http://localhost:8000/index.html` (or the relevant file) in your browser.

## Tool Highlights

### Hospital Patient Flow Simulator (`index.html`)
- Configure patient arrival rates across emergency acuity levels and specialty cohorts.
- Build care pathways by arranging areas such as Triage, Imaging, and ICU with capacity and staffing constraints.
- Run discrete-event simulations that model Poisson arrivals, queue backlogs, staff utilization, and equipment dependencies.
- Monitor throughput, wait times, alerts, and bottleneck diagnostics in real time.

### SCT Configuration Maker (`maker.html`)
- Capture SCT deployment modalities (Embedded, Coupled, Self-sustained) and associated readiness considerations.
- Document clinical focus, staffing requirements, WASH/IPC needs, and operational dependencies.
- Export structured `config.json` files that can be imported into other SCT tools.

### Assessment Template (`template.html`)
- Load previously exported configurations to filter readiness checklists by modality or SCT profile.
- Review summarized responsibilities, coordination needs, and contingency planning guidance.

## Working with Exported Configurations

- Use **Save Configuration** in `maker.html` to download a `config.json` file. It will appear in your browser's downloads folder unless you pick a custom location.
- Open `template.html` and choose **Import Configuration** to review the same data within the assessment workflow.
- You can repeat this process to maintain multiple scenario files for different facilities or deployment plans.

## Support & Contributions

This toolkit is designed for lightweight distribution and offline use. If you have suggestions or need to report an issue, please open a ticket or contribute via pull request with a description of the proposed change.

