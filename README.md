<img alt="Banner explaining why Typst is better than LaTeX" src="https://raw.githubusercontent.com/dhbw-typst/oderso-template-dev/c81d3f24e453e59ed817c8bfc42fd6fffc448581/banner.jpeg" width="100%" />

# ODERSO Typst Template Mannheim DSKI

This is a university report template written in [Typst](https://typst.app/),
based on the [DHBW LaTeX Template by Prof. Dr. Pfisterer et al.](https://github.com/pfisterer/DHBW_LaTeX_Template), which is used by the Data Science and Artificial Intelligence course at DHBW Mannheim. [Why should you use Typst over LaTeX?](#-why-typst)

The template was built for DHBW Mannheim Data Science and AI course, but also has adapters for DHBW Karlsruhe and IHK.

> **Tip:** Want to see how the template looks? Download a preview PDF for [DHBW Karlsruhe](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-dhbw-ka.pdf), [DHBW Mannheim](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-dhbw-ma.pdf) or [IHK](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-ihk.pdf) to inspect the final result.


I intend to keep this fork up-to-date with changes on the original template from time to time.

## 🔧 Changes from the upstream ODERSO template

This fork adapts the look and feel of the upstream template to match the DHBW LaTeX template. You can change the font used for the document, just keep in mind that different fonts consume more (e.g. New Computer Modern) or less (e.g. Times New Roman) space for the exact same text. This might be important if you need to hit a specific number of pages in your submission.

The following changes have been made:

- **DSKI-style cover layout**: new `cover-layout-dski` toggle in the `dhbw-ma` adapter (default `true`) switches the cover sheet layout to match the cover sheet of the LaTeX template.
- **Declaration pages moved to front matter**: the statutory declaration, AI declaration, and confidentiality agreement are now rendered right after the coversheet (before the abstracts), in that order. The original template places them between the bibliography and the appendix.
- **Front-matter lists moved after the ToC**: abbreviations, glossary, list of figures, list of tables, and list of code are rendered right after the table of contents instead of at the end of the document.
- **Front-matter page numbering**: lowercase Roman (`i, ii, iii, …`) instead of uppercase.
- **Page margins**: `left: 2.55cm, rest: 2.5cm` to provide a small binding margin.
- **Line spacing**: `leading` set to `0.811em` to approximate LaTeX's `\onehalfspace`.
- **Heading sizes** (matching KOMA-Script defaults at 12pt):
  - Level 1 (chapter): 24pt
  - Level 2 (section): 17pt
  - Level 3 (subsection): 15pt
- **Bullet point and enumeration indent**: bullets and enumerations are indented by 10pt (`set list(indent: 10pt)`, `set enum(indent: 10pt)`).
- **Page header**: redesigned to match the LaTeX template: "Chapter X" on the left and the chapter title on the right. The gray separator line below the header was removed, and the header height was matched to the one from the LaTeX-Template by experimentation.
- **Header spacing**: `header-ascent: 55%` raises the header text further into the top margin so the gap between header and body matches the LaTeX's template.
- **Header toggle**: `header-show-chapter` lets you toggle if the header should display `Chapter XXX` on the left side and `Chapter Name` on the right side, or not.
- **Toggles for declaration pages**: `include-statutory-declaration` (all adapters) and `include-ai-declaration` (`dhbw-ma`) let you skip either declaration. `include-ai-declaration` defaults to `true`.
- **AI declaration digital toggle**: `ai-declaration-digital` (`dhbw-ma`) controls whether the AI declaration form renders your content digitally or shows blank lines for handwriting. Defaults to `auto`, which mirrors `digital-only`. Set to `true` to render content digitally even when submitting a printed copy and vice versa for false.
- **Page break after chapter heading toggle**: `disable-pagebreak-after-heading` lets you toggle if you want to disable page breaks after chapter (level 1) headings or not. Disabled by default.

> **Tip:** For descriptions of all functions and properties, refer to the [upstream package documentation](https://github.com/dhbw-typst/oderso-template/releases/latest/download/documentation.pdf).

## 🏃‍♂️ Getting Started

> **Tip:** If you run into any issues, check out the [troubleshooting guide](#%E2%80%8D-troubleshooting).

For the following setup guides, make sure you have installed [Visual Studio Code](https://code.visualstudio.com/).

Or if you don't want to edit your document locally, you can use the Typst web editor. Go to [typst.app](https://typst.app) to find out more.

> **Caution:** If writing a thesis at your company, make sure you are allowed to use the online editor, as this might violate a confidentiality clause you signed.

### Initialize from Template Repository

1. Click on [![Generate from template button](https://img.shields.io/badge/Generate_from_template-8A2BE2?logo=github)](https://github.com/0LGuenth/oderso-template-mannheim-dski/generate) and give your repository a telling name (e.g. `pa-1`)
2. Clone your repository to your local machine: `git clone https://github.com/<you>/pa-1.git`
3. Open this directory using VSCode and install the recommended extensions
   - Tinymist (provides completions, preview and PDF-generation for your template)
   - LTeX+ (spell checker)
4. Open the correct main file (e.g. `main-dhbw-ka.typ` for DHBW Karlsruhe). To toggle the live-preview:
   - Press the `Typst Preview: Preview Opened File` button in the top right of your file\
   OR
   - Open the command palette (<kbd>CMD</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>) and select `Typst Preview: Preview Opened File`
5. The initial document will guide you through the rest of the setup process and show you all the different features of the template
6. To generate a PDF document:
   - Press the `Show the exported PDF` button in the top right of your file\
   OR
   - Open the command palette (<kbd>CMD</kbd>+<kbd>Shift</kbd>+<kbd>P</kbd>) and select `Typst: Show exported PDF`

**Look at the preview PDF ([DHBW Karlsruhe](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-dhbw-ka.pdf), [DHBW Mannheim](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-dhbw-ma.pdf), [IHK](https://github.com/0LGuenth/oderso-template-mannheim-dski/releases/latest/download/main-ihk.pdf)) or the [original package documentation](https://github.com/dhbw-typst/oderso-template/releases/latest/download/documentation.pdf) to learn how to use the package.**

## 💡 Feedback

If you have any ideas or suggestions to **improve the template**, please [open an issue](https://github.com/0LGuenth/oderso-template-mannheim-dski-dev/issues/new) or check out the original template's [development repository](https://github.com/dhbw-typst/oderso-template-dev).

## 😵‍💫 Troubleshooting

Sometimes, Tinymist makes it a bit hard to diagnose the root cause of an issue.
Then, it can be helpful to use the `typst` program directly!
To achieve this, open the terminal inside of your VSCode project and:

1. Download and install Typst: `brew install typst` (if you don't have `homebrew`, install it as shown [here](https://brew.sh/))
2. Open a new terminal window and run `typst compile main.typ`
3. Most of the time, the original error is at the top of the program's output
4. If this doesn't help you to figure out the issue, please [open an issue](https://github.com/0LGuenth/oderso-template-mannheim-dski-dev/issues/new)

## ❓ Why Typst?

> Typst was born out of our frustration with LaTeX. Not knowing what we were in for, we decided to take matters into our own hands and started building. -Typst

Typst is a replacement for LaTeX which was designed to be **as powerful as LaTeX while being much easier to learn and use**.
It has a much simpler syntax (similar to Markdown), _actual good error messages_ (looking at you, LaTeX)
and out-of-the-box bibliography features using `.bib` or `.yaml` files (see `refs.bib`) (again, looking at you, LaTeX).

## History and Future of this Template

This template was created by students at SAP in 2023. Since then, Typst has gained significant traction as a scientific writing tool among students at SAP.

Over the years, the template has grown to include many features and now supports institutions beyond DHBW Karlsruhe.

**This template thrives on contributions from its users.** Whether it's reporting bugs, adapting to new dependency versions, or starting a discussion about potential changes, there are many ways to get involved. Don't hesitate to start your [contribution](#-Contribute) now :)

The goal of this template is to make writing your thesis at DHBW as easy as possible! That said, there are some alternatives worth knowing about:

- [clean-dhbw](https://typst.app/universe/package/clean-dhbw/): A template written by a professor of the DHBW Karlsruhe. We found it to be fairly opinionated and limited in customization. It also lacks many features this template provides.
- [supercharged-dhbw](https://typst.app/universe/package/supercharged-dhbw/): Another template for DHBW Karlsruhe students. As of May 2026, the last commit was over a year old, so outdated package versions may cause issues with the latest version of Typst. We do not recommend using an unmaintained template, especially for users less familiar with Typst.

## Assets Included in this Template

This template includes some assets that fall under different licenses than the rest of the template:

- **`placeholder-comany-logo.svg`**: [Source](https://logoipsum.com/artwork/415) · [Fair Use License](https://logoipsum.com/license)
- **`placeholder-signature.png`**: [Source](https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Friedrich_Schiller_Signature.svg/1280px-Friedrich_Schiller_Signature.svg.png) · [Public Domain](https://commons.wikimedia.org/wiki/File:Friedrich_Schiller_Signature.svg)
- **`IHK-Logo.svg`**: [Source](https://upload.wikimedia.org/wikipedia/commons/1/12/IHK-logo.svg) · [Public Domain](https://de.wikipedia.org/wiki/Datei:IHK-logo.svg) · ⚠️ Trademark of the [DIHK](https://www.dihk.de/)
- **`DHBW-Logo.svg`**: [Source](https://upload.wikimedia.org/wikipedia/de/1/1d/DHBW-Logo.svg) · ⚠️ Trademark of the [DHBW](https://www.dhbw.de/startseite)
