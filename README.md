# Guide: AI-Augmented Resume Builder (2026 Edition)
## Leveraging WebMCP, Chrome DevTools MCP, and Playwright

This guide outlines a high-performance workflow for Software Engineers to automate and optimize their career documents using an autonomous browser agent stack.

---

## 1. The Architecture
To build a resume that survives 2026 ATS filters, the agent must operate across three layers:
* **Action Layer (Playwright):** Navigates job boards and career portals.
* **Observation Layer (Chrome DevTools MCP):** Inspects hidden metadata, network payloads, and console logs for deep job requirement discovery.
* **Interaction Layer (WebMCP):** Communicates natively with career sites using standardized AI-to-web protocols.



---

## 2. Environment Setup
Ensure your local environment meets the 2026 technical requirements:

1.  **Browser:** Chrome 146+ with `#experimental-web-platform-features` enabled in `chrome://flags`.
2.  **MCP Servers:** Run the following bridges in your terminal:
    * Playwright: `npx @playwright/mcp@latest`.
    * DevTools: `npx chrome-devtools-mcp@latest`.
3.  **Polyfill:** Ensure the WebMCP polyfill is injected into the browser context to access `navigator.modelContext`.

---

## 3. Step-by-Step Execution Workflow

### Step 1: Intelligent Prompting
Start with a prompt that grants the agent "Executive Authority" over the browser.
> **Prompt:** "Navigate to [Target URL]. Use **Chrome DevTools MCP** to intercept the background JSON response for 'job_requirements'. Identify the primary tech stack and culture keywords. Cross-reference this with my **MERN stack** experience and generate a tailored LaTeX resume draft."

### Step 2: Automated Research (Playwright)
The agent uses Playwright to perform `browser_navigate` and `page.textContent`. It doesn't just read the text; it identifies the **DOM structure** to see how the site prioritizes information.

### Step 3: Deep Inspection (DevTools MCP)
The agent "listens" to the network traffic.
* **Hidden Keywords:** It looks for `Network.getResponseBody` to find tags used by the internal ATS that aren't visible on the frontend.
* **System Health:** It monitors the console for errors that might indicate an outdated or specific version of an ATS (e.g., Workday, Greenhouse).

### Step 4: Native Skill Mapping (WebMCP)
If the career portal supports WebMCP, the agent bypasses manual scraping.
* It calls `navigator.modelContext.listTools()` to see if the site provides a native `get_job_schema` tool.
* This ensures 100% accuracy in keyword alignment before the draft is generated.

### Step 5: Final Generation & Verification
The agent generates a **LaTeX** code block.
* **Formatting:** Single-column, ATS-optimized structure.
* **Validation:** It uses Playwright to upload the generated PDF to a "Shadow ATS" to verify that every keyword (e.g., **React.js, Node.js, Redux**) is being parsed correctly.

---

## 4. Key 2026 Metrics for Success
* [cite_start]**Load Time Impact:** Emphasize quantifiable wins (e.g., "Achieved a 40% reduction in load times")[cite: 9, 23].
* [cite_start]**Performance:** Highlight app performance increases (e.g., "30% increase in performance")[cite: 9, 25].
* [cite_start]**Framework Proficiency:** Explicitly list **React.js, MongoDB, and Express** to differentiate from legacy vanilla JS roles[cite: 8, 15, 30].

---

*Created by Pratham Bindal*
