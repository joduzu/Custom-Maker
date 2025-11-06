# Custom Maker Toolkit

This repository contains four standalone HTML tools:

- **index.html** – Interactive hospital patient flow simulator with configurable scenarios, throughput analytics, and bottleneck detection.
- **maker.html** – Configuration maker used to author SCT deployment modality guidance and export `config.json` files.
- **template.html** – Assessment template that loads exported configurations for review.
- **patient-flow-simulator.html** – Interactive prototype that models patient arrivals, area capacity, wait times, and queue-driven bottlenecks for hospital planning exercises.

 codex/propose-deployment-considerations-for-sct-tools-z8pu9e

 codex/propose-deployment-considerations-for-sct-tools-iyt36w
 main
## Capturing SCT deployment profiles

`maker.html` now lets you create **SCT Deployment Profiles**. Use the card below the modality guidance grid to:

- Document which deployment modalities (Embedded, Coupled, Self-sustained) a specific SCT can support.
- Summarize the team’s clinical focus and highlight checklist priorities such as operational support, staffing, WASH/IPCs, and clinical capabilities using the provided readiness fields.
- Record what the SCT will always provide and what the host facility must guarantee before deployment, along with coordination and contingency notes.

When you export `config.json`, these profiles are saved alongside the modality metadata. Upload the same file in `template.html` to:

- Filter checklist standards by SCT profile and/or individual deployment modality.
- Review a dedicated **SCT Profiles** tab summarizing responsibilities and readiness considerations drawn from the Comprehensive Facility Readiness Checklist.

 codex/propose-deployment-considerations-for-sct-tools-z8pu9e

 main
main
## Accessing the tools locally

1. Clone or download this repository to your computer.
2. Open the project folder in your file explorer.
3. Double-click any of the HTML files (for example, `maker.html`) to open it directly in your web browser.
4. If your browser blocks local file access, right-click the file and choose **Open with** followed by your preferred browser.

## Working with exported files

- When you press **Save Configuration** in `maker.html`, your browser downloads a `config.json` file. You can find it in your browser's default downloads folder unless you choose a different location.
- To load a previously saved configuration, click **Import Configuration** in `maker.html` and select the `config.json` file from your computer.
- The same `config.json` file can be uploaded in `template.html` to review the assessment checklist filtered by deployment modality.

## Viewing changes on a local web server (optional)

Some browsers restrict features like file downloads when running straight from the file system. To avoid this, you can serve the files through a lightweight HTTP server:

```bash
# From the repository root
python3 -m http.server 8000
```

Then visit <http://localhost:8000/maker.html> (or the relevant file) in your browser.
