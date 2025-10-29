# GlobalPlatform Card Specification — Parts II & III  
### Engineering Presentation Markdown Package (v2.3.1)

---

## 📘 Purpose

This package contains Markdown-based presentation material derived from the  
**GlobalPlatform Card Specification v2.3.1 (Public Release)** — specifically  
**Chapters 2–6 and Appendix A**.

It is intended for **technical audiences** (engineers, developers, architects)  
to support internal presentations, training sessions, or wiki documentation.

Each file includes:
- Full section numbering matching the official specification  
- Inline **Mermaid diagrams** for architecture and flow visualization  
- **Presenter notes** embedded as HTML comments  
- **Figure** and **Table placeholders** for later replacement with official diagrams  

---

## 📂 File Structure

```
GlobalPlatform_CardSpec_PartII-III_Markdown_Presentation/
│
├── 00_Session_Overview.md
├── 02_System_Architecture.md
├── 03_Card_Architecture.md
├── 04_Security_Architecture.md
├── 05_Lifecycle_Models.md
├── 06_GlobalPlatform_Environment.md
├── Appendix_A_APDU_Flow_Examples.md
└── README.md
```

---

## 🧩 Contents Overview

| File | Description |
|------|--------------|
| `00_Session_Overview.md` | Session objectives, schedule, and outcomes |
| `02_System_Architecture.md` | System roles, secure channel architecture |
| `03_Card_Architecture.md` | Security Domains, OPEN, and card content |
| `04_Security_Architecture.md` | Security roles, SCP protocols, and cryptographic model |
| `05_Lifecycle_Models.md` | Card, App, and SD lifecycles |
| `06_GlobalPlatform_Environment.md` | OPEN dispatch, logical channels, privileges |
| `Appendix_A_APDU_Flow_Examples.md` | SCP03 and LOAD/INSTALL APDU sequences |

---

## 🧠 Presenter Usage

Each chapter includes embedded HTML comments like:

```html
<!-- presenter note: Highlight secure channel initialization sequence -->
```

These can be viewed in raw Markdown or ignored in rendered views.  
They provide key talking points for live presentations.

---

## 🧩 Mermaid Diagram Rendering

### On **GitHub / GitLab Wiki**
- Mermaid syntax is natively supported inside code fences:
graph TD
A --> B
- Ensure parentheses are escaped (`\(` and `\)`) in node labels for GitHub compatibility.

### On **Confluence**
- Use the *Mermaid for Confluence* plugin or macro.

### On **MkDocs / Docusaurus**
Add these extensions in your `mkdocs.yml`:
```yaml
markdown_extensions:
- pymdownx.superfences
- pymdownx.tabbed
- pymdownx.details
- pymdownx.highlight
- pymdownx.keys
- pymdownx.emoji
- pymdownx.arithmatex
- pymdownx.tasklist
- pymdownx.inlinehilite
- pymdownx.mark
- pymdownx.superfences:
    custom_fences:
      - name: mermaid
        class: mermaid
        format: !!python/name:pymdownx.superfences.fence_code_format
```

### On **Marp / Slides**
Use Marp’s Mermaid plugin or export diagrams to SVG.

---

## 🛠️ Editing Notes

- Keep all diagram code blocks fenced in triple backticks (` ```mermaid `).  
- Replace `<!-- Figure X-Y -->` and `<!-- Table X-Y -->` placeholders with official GlobalPlatform figures if available.  
- All diagrams have been checked for GitHub-safe syntax (escaped parentheses).  
- You can merge these `.md` files into your company wiki directly.

---

## 📄 License and Attribution

This package reinterprets content from the  
**GlobalPlatform Card Specification v2.3.1 (Public Release)**  
for educational and internal engineering purposes.

All GlobalPlatform trademarks and materials remain property of  
**GlobalPlatform, Inc.**

---

## ✅ Recommended Use Flow

1. Upload `.md` files to your internal wiki (GitHub Wiki, Confluence, or GitLab).  
2. Verify Mermaid diagrams render correctly.  
3. Use presenter notes as talking prompts during training.  
4. Optionally replace diagrams with high-fidelity images from the official PDF.

---

<!-- presenter note:
Introduce this README as a quick reference for other engineers who use or maintain the presentation material.
Encourage consistency with the official GP specification and internal security guidelines.
-->
