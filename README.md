<img src="https://raw.githubusercontent.com/dhbw-typst/oderso-template-dev/refs/heads/main/banner.jpeg" width="100%" />

# ODERSO Typst Template Mannheim DSKI

This is a university report template written in [Typst](https://typst.app/),
based on the [DHBW LaTeX Template by Prof. Dr. Pfisterer et al.](https://github.com/pfisterer/DHBW_LaTeX_Template), which is used by the Data Science and Artificial Intelligence course at DHBW Mannheim. [Why should you use Typst over LaTeX?](#-why-typst)

The template was built for DHBW Mannheim Data Science and AI course, but also has adapters for DHBW Karlsruhe and IHK.

I intend to keep this fork up-to-date with changes on the original template from time to time.

## 🔧 Changes from the upstream ODERSO template

This fork adapts the look and feel of the upstream template to match the DHBW LaTeX template. All changes are in `template/base.typ`:

- **Bullet point indent**: bullets are indented by 10pt (`set list(indent: 10pt)`).
- **Line spacing**: `leading` set to `0.811em` to approximate LaTeX's `\onehalfspace`.
- **Heading sizes** (matching KOMA-Script defaults at 12pt):
  - Level 1 (chapter): 24pt
  - Level 2 (section): 17pt
  - Level 3 (subsection): 15pt
- **Page margins**: `left: 2.55cm, rest: 2.5cm` to provide a small binding margin.
- **Front-matter page numbering**: lowercase Roman (`i, ii, iii, …`) instead of uppercase.
- **Page header**: redesigned to match the LaTeX template: "Chapter X" on the left and the chapter title on the right. The gray separator line below the header was removed and the header height was decreased.
- **Header spacing**: `header-ascent: 55%` raises the header text further into the top margin so the gap between header and body matches the LaTeX's template.
- **Declaration pages moved to front matter**: the statutory declaration, AI declaration, and confidentiality agreement are now rendered right after the coversheet (before the abstracts), in that order. The original template places them between the bibliography and the appendix.

> [!TIP]
> This fork does not publish release PDFs. To preview the template, compile `main-dhbw-ma.typ` locally (see [Getting Started](#%E2%80%8D-getting-started)).
>
> For descriptions of all functions and properties, refer to the [upstream package documentation](https://github.com/dhbw-typst/oderso-template/releases/latest/download/documentation.pdf).

## 🏃‍♂️ Getting Started

> [!TIP]
> If you run into any issues, check out the [troubleshooting guide](#%E2%80%8D-troubleshooting).

For the following setup guide, make sure you have installed [Visual Studio Code](https://code.visualstudio.com/).

1. Click on [![Generate](https://img.shields.io/badge/Generate_from_template-8A2BE2?logo=github)](https://github.com/dhbw-typst/oderso-template/generate) and give your repository a telling name (e.g. `pa-1`)
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

**To learn how to use the package, compile `main-dhbw-ma.typ` locally and refer to the [upstream package documentation](https://github.com/dhbw-typst/oderso-template/releases/latest/download/documentation.pdf).**

## 💡 Feedback

If you have any idea on how to **improve the template**, please check out the original template
[development repository](https://github.com/dhbw-typst/oderso-template-dev).

## 😵‍💫 Troubleshooting

Sometimes, Tinymist makes it a bit hard to diagnose the root cause of an issue.
Then, it can be helpful to use the `typst` program directly!
To achieve this, open the terminal inside of your VSCode project and:

1. Download and install Typst: `brew install typst` (if you don't have `homebrew`, install it as shown [here](https://brew.sh/))
2. Open a new terminal window and run `typst compile main.typ`
3. Most of the time, the original error is at the top of the program's output
4. If this doesn't help you to figure out the issue, please [open an issue](https://github.com/dhbw-typst/oderso-template-dev/issues/new)

## 🌐 Web-IDE (typst.app)

You can use the typst web editor to edit your typst document. Go to [typst.app](https://typst.app) to find out more.

> [!CAUTION]
> If writing a thesis at your company, make sure you are allowed to use the online editor, as this might violate a confidentiality clause you signed.

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
