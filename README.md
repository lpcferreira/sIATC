# sIATC - Statement of Intellectual Accountability and Transparency for Content

[![Original sIfA DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20285993.svg)](https://doi.org/10.5281/zenodo.20285993)

A browser-based tool for declaring how AI tools contributed to a piece of written content, mapped onto a nine-stage content-production taxonomy. Produces a structured table and a single-page visualization, the sIATC figure, that can be attached to an article, report, essay, post, book chapter, newsletter, institutional text, presentation, or other editorial output.

> **sIATC** retains its lineage from the original sIfA tool, but this content-focused adaptation uses the framing **Statement of Intellectual Accountability and Transparency for Content**.
> "Intellectual accountability" means that the human author remains responsible for control, review, verification, and final approval of the content. "Transparency" means that AI use should be described clearly, stage by stage, without treating AI systems as authors, tools, moral agents, or responsible parties. 

sIATC is a modified derivative of the original **sIfA Tool - Statement of Intellectual Fellowship and Accountability**, created by Mareike Schomerus / Busara and released under the Apache License 2.0.

This naming choice is deliberate: we have adapted the terminology for content production by emphasizing intellectual accountability and transparency rather than fellowship. This avoids treating AI systems as authors, collaborators, or moral agents. sIATC does not attribute authorship, agency, intention, moral standing, or responsibility to AI systems. AI is treated as a technology used in the content-production process, always subject to human supervision, review, verification, and accountability. 

The original sIfA was created for research and knowledge-production outputs, using the CRediT contributor-role taxonomy. sIATC adapts the same reflection logic for written content while emphasizing intellectual accountability, transparency, and human responsibility. It replaces the research contributor-role taxonomy with a nine-stage taxonomy designed for content creation:

- Conception & Angle
- Research & Sourcing
- Structure
- Drafting
- Editing & Refinement
- Revision
- Translation
- Fact-checking & Verification
- Visuals & Design

The tool is a single self-contained HTML file. No install, no server, no account, and no build step are required for end users.

---

## Languages

- [English](#english)
- [Português](#português)
- [Español](#español)

---

# English

## Why sIATC exists

AI use in writing and content production is expanding faster than the conventions for declaring it. Generic free-text disclosures such as "AI was used in the preparation of this text" are too vague to be useful. They do not show where AI entered the process, whether it shaped the argument, whether it helped with structure, whether it generated language, whether it translated, whether it verified claims, or whether it only helped polish sentences.

sIATC gives authors, editors, researchers, communicators, publishers, organizations, and readers a shared, structured way to describe how AI interacted with a piece of content.

It is designed for content, not only for research.

The original sIfA was developed to support reflection on human/AI interaction in knowledge production, especially research outputs. It uses contribution roles associated with research processes. sIATC keeps the same core idea of reflection and accountability, but adapts the terminology for content production by emphasizing intellectual accountability and transparency rather than fellowship. This avoids treating AI systems as authors, tools, moral agents, or responsible parties. It also changes the unit of analysis from research contribution roles to the stages of creating written content.

That change matters. An article, report, book, LinkedIn post, institutional statement, newsletter, or opinion essay may involve research, but it also involves editorial choices that are not fully captured by research taxonomies. A content author may need to reflect on how AI helped define the angle, organize the sequence, draft passages, refine tone, translate, check facts, or create visuals. These are distinct forms of participation. They should not be collapsed into a single disclosure note.

sIATC is therefore a self-assessment tool. It is not an audit tool. It does not certify the quality, truthfulness, authorship, originality, or ethical status of a piece of content. It invites the author to pause, reflect, document, and disclose.

The human author remains accountable for the final output.

## Relationship to the original sIfA tool

sIATC is a modified derivative of:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

The original sIfA tool is released under the Apache License 2.0. sIATC preserves the attribution to Mareike Schomerus / Busara and carries forward the license obligations required for redistribution and modification.

### What sIATC keeps from sIfA

sIATC keeps the core reflective logic of the original tool:

- AI use is declared across defined stages rather than hidden in a generic note.
- The author records the extent of AI interaction using a simple 0/1/2 scale.
- The tool produces a visual figure that makes human/AI interaction recognizable at a glance.
- The tool produces structured, machine-readable data.
- The figure retains the human brain visual metaphor: the orange outer field represents the human author, while the purple center represents AI interaction.
- Human accountability remains explicit.
- The tool is distributed as a single HTML file that can run locally in a browser.
- The original brain-figure artwork is reused under the Apache 2.0 license.

### What sIATC changes

sIATC changes the application domain, taxonomy, and workflow.

The original sIfA is primarily designed for research and knowledge-production outputs, with the CRediT contributor-role taxonomy as a major reference point. sIATC is designed specifically for content creation.

The main changes are:

- The 14-role CRediT research taxonomy is replaced by a nine-stage taxonomy for written content.
- Research-specific contributor roles are removed.
- The focus shifts from multi-contributor research attribution to content-process self-assessment.
- The flow is simplified for a single author or responsible author.
- Each content stage can be marked as "not applicable" when it did not occur.
- The tool is framed for articles, reports, posts, essays, newsletters, books, chapters, institutional texts, scripts, presentations, and other editorial formats.
- The disclosure emphasizes how AI interacted with the creation of content, not how it contributed to a research project.

sIATC is therefore not a replacement for sIfA. It is an adaptation for a different use case.

Use sIfA when the main object is a research output and the CRediT-style contribution structure is appropriate. Use sIATC when the main object is written content and the relevant question is how AI interacted with the stages of content production.

## Table of contents

- [For authors and content creators](#for-authors-and-content-creators)
  - [Quick start](#quick-start)
  - [How the tool is structured](#how-the-tool-is-structured)
  - [The nine content stages](#the-nine-content-stages)
  - [AI extent scale](#ai-extent-scale)
  - [How to judge the extent of AI use](#how-to-judge-the-extent-of-ai-use)
  - [Saving and exporting](#saving-and-exporting)
  - [Worked example](#worked-example)
  - [What is not sent anywhere](#what-is-not-sent-anywhere)
  - [Suggested disclosure wording](#suggested-disclosure-wording)
- [For editors, publishers, and organizations](#for-editors-publishers-and-organizations)
  - [When to request a sIATC](#when-to-request-a-sIATC)
  - [How to read a sIATC figure](#how-to-read-a-sIATC-figure)
  - [What sIATC can and cannot prove](#what-sIATC-can-and-cannot-prove)
- [For developers](#for-developers)
  - [Repository layout](#repository-layout)
  - [Running and editing](#running-and-editing)
  - [Architecture in one paragraph](#architecture-in-one-paragraph)
  - [State model](#state-model)
  - [Changing the content stages](#changing-the-content-stages)
  - [Build and offline use](#build-and-offline-use)
  - [Known limitations](#known-limitations)
- [Citation and attribution](#citation-and-attribution)
  - [Citing sIATC](#citing-sIATC)
  - [Citing the original sIfA tool](#citing-the-original-sifa-tool)
  - [Derivative-work notice](#derivative-work-notice)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## For authors and content creators

### Quick start

1. Download the latest `sIATC_vX.X.html` file from the [Releases](../../releases) page.
2. Open the file in any modern browser by double-clicking it. Chrome, Edge, Safari, Firefox, and other modern browsers should work.
3. Enter the title or description of the piece of content.
4. Enter the author name, if desired.
5. For each content stage, choose one of three AI-use levels:
   - 0 = none
   - 1 = some
   - 2 = extensive
6. Mark a stage as "not applicable" if it did not happen in the production process.
7. Add the AI tool or service used, when relevant.
8. Add a short note explaining how AI was used.
9. Export the figure as SVG or PNG, or export the data as a `.sIATC.json` file.

That is the whole loop. The tool is a single HTML page. There is no install, no account, no upload, and no server.

### How the tool is structured

The interface is a single page with four main parts:

- **Metadata fields** for the content title and author.
- **A stage-by-stage assessment table** covering the nine stages of written content production.
- **A brain-shaped figure** showing the degree of AI interaction across the active content stages.
- **Export buttons** for downloading the figure or exporting the structured data.

The figure fills outward from the center as AI involvement grows. The orange brain represents the human author. The purple center represents AI interaction. Each axis corresponds to one content stage. The farther the purple shape extends along a stage, the greater the declared AI involvement in that part of the process.

Stages marked "not applicable" are excluded from the figure.

The tool also includes a responsibility statement:

> After using any tools or services, the author(s) reviewed and edited the content as needed and take(s) full responsibility for the content of the publication.

This statement can be adapted depending on the publication context, but the principle should remain: the human author is responsible for the final content.

### The nine content stages

sIATC uses a nine-stage taxonomy for written content. The taxonomy is not meant to describe every possible editorial process with perfect precision. It is a practical structure for reflection, disclosure, and comparison.

| Stage | What it means | Examples of AI interaction |
| --- | --- | --- |
| **Conception & Angle** | The core idea, angle, and message of the content: what the piece is about and why it is worth making. | Brainstorming angles or hooks; pressure-testing an argument; generating framing options; sharpening the takeaway. |
| **Research & Sourcing** | The facts, references, examples, and background material the content rests on. | Summarizing background reading; finding supporting data or quotes; gathering prior material; mapping what has been said. |
| **Structure** | Outline, sequence, section logic, and narrative flow. | Drafting or reordering an outline; proposing a narrative arc; testing whether the flow works; adapting structure to a format. |
| **Drafting** | Producing original text: turning idea and outline into prose. | Generating a first draft from a brief; drafting sections; expanding notes into prose; producing alternative phrasings. |
| **Editing & Refinement** | Line-level work on language, tone, clarity, concision, and voice. | Copy-editing for clarity; adapting tone; rewriting unclear passages; cutting to length. |
| **Revision** | Substantive reworking of content or argument after feedback, review, or a fresh read. | Incorporating reviewer comments; reworking an argument; reconciling feedback; deciding what to cut, expand, or reorder. |
| **Translation** | Rendering the content into another language, including localization and terminology consistency. | Refining machine translation; adapting idioms and cultural references; applying a glossary; back-translation to check fidelity. |
| **Fact-checking & Verification** | Confirming that claims, numbers, citations, quotes, names, dates, and sources are accurate. | Verifying AI-suggested facts against sources; checking attributions; flagging possible hallucinations; reviewing for bias. |
| **Visuals & Design** | The visual layer that supports or presents the content. | Generating or sourcing images; drafting layouts; creating charts or diagrams; adapting visuals to a platform or format. |

A stage can be marked as "not applicable" when it did not occur. For example, if the piece was not translated, the Translation stage can be excluded. If no visuals were produced, Visuals & Design can be excluded.

### AI extent scale

sIATC uses a three-level scale to describe how much AI interacted with each content stage.

| AI extent | Meaning | Typical interpretation |
| --- | --- | --- |
| **0 - None** | No AI was used in this stage. | The stage was performed without AI tools. |
| **1 - Some** | AI assisted the author but did not drive the stage. | AI helped with suggestions, alternatives, summaries, corrections, or limited support. The author substantially controlled and produced the outcome. |
| **2 - Extensive** | AI played a substantial role in the stage. | AI generated, transformed, structured, translated, analyzed, or materially shaped the output, which the author then reviewed, edited, verified, and accepted. |

The 0/1/2 scale is intentionally simple. It is designed for reflection and communication, not exact measurement. The purpose is to make AI interaction visible enough to support accountability, learning, comparison, and better disclosure norms.

### How to judge the extent of AI use

The author should use judgment when assigning a level. The following guidance may help.

Use **0 - None** when:

- no AI tool was used in that stage;
- AI was used elsewhere, but not for that stage;
- the stage did not involve AI-generated, AI-assisted, or AI-transformed material.

Use **1 - Some** when:

- AI suggested options, but the author selected, rejected, or substantially rewrote them;
- AI helped with clarity, tone, grammar, concision, or formatting;
- AI summarized material that the author had already selected and checked;
- AI helped brainstorm possibilities but did not determine the final direction;
- AI was used as a sounding board or critique partner.

Use **2 - Extensive** when:

- AI generated a first draft or substantial passages;
- AI produced a translation that became the basis for the final version;
- AI materially shaped the structure or argument;
- AI synthesized source material into usable content;
- AI created visual elements used in the final output;
- AI performed a major part of fact-checking, verification, classification, or editorial revision, subject to human review;
- the final stage outcome would be materially different without AI.

The author should be transparent about uncertainty. If a stage sits between "some" and "extensive," choose the level that best reflects how dependent the stage was on AI and explain the choice in the note field.

### Saving and exporting

sIATC supports multiple forms of export.

- **Download figure as SVG**: exports the visual figure in a scalable vector format suitable for publication, websites, repositories, and documents.
- **Download figure as PNG**: exports the figure as an image file for easier use in slides, posts, or platforms that do not handle SVG well.
- **Export data as `.sIATC.json`**: exports the structured data behind the assessment, including the content metadata, stage-level scores, AI tools, notes, and timestamp.
- **Browser-local interaction**: the tool runs in the browser. No server is required.

The exported `.sIATC.json` file can be used as a machine-readable record of the self-assessment. The SVG or PNG figure can be attached to the content itself, included in a repository, added to supplementary material, or published alongside the piece.

### Worked example

A fictional sIATC for a long-form article about the effect of AI on professional writing:

| Stage | AI extent | Tool / service | How AI was used |
| --- | --- | --- | --- |
| Conception & Angle | 1 | ChatGPT | Used to test possible angles and identify weak framings. Final angle selected by the author. |
| Research & Sourcing | 1 | Perplexity, Google Search, ChatGPT | Used to map relevant debates and identify possible sources. Sources were checked manually before inclusion. |
| Structure | 2 | Claude | Used to propose several outlines and reorganize the argument. Author selected and modified the final structure. |
| Drafting | 0 | - | No AI used to generate the first draft. |
| Editing & Refinement | 1 | ChatGPT | Used to identify unclear passages and suggest tighter phrasing. Author rewrote manually. |
| Revision | 1 | Claude | Used to compare reviewer feedback against the draft and identify sections needing expansion. |
| Translation | Not applicable | - | The piece was not translated. |
| Fact-checking & Verification | 1 | ChatGPT, manual source review | Used to flag claims requiring verification. Final checking was performed manually against sources. |
| Visuals & Design | 2 | DALL-E, Canva | Used to generate visual concepts and adapt them for the publication format. |

In this example, the exported sIATC figure would show no AI interaction for Drafting, no axis for Translation if marked as not applicable, and stronger AI interaction in Structure and Visuals & Design.

### What is not sent anywhere

The tool runs entirely in your browser. Nothing is uploaded by the tool to a server.

Specifically:

- The title of your piece stays on your computer.
- The author name stays on your computer.
- Your stage-level assessments stay on your computer.
- The tools and services you list stay on your computer.
- Your notes on how AI was used stay on your computer.
- The exported `.sIATC.json` file is yours to keep, publish, attach, archive, or delete.

The tool does not provide analytics, user tracking, accounts, cloud storage, or remote validation.

If you use a third-party AI service while producing the content, that service may have its own data-use policies. sIATC does not control those services. sIATC only records your self-assessment of how they were used.

### Suggested disclosure wording

A short disclosure may look like this:

> This piece includes a sIATC statement documenting how AI tools interacted with the production of the content. AI use was self-assessed across the stages of conception, research, structure, drafting, editing, revision, translation, verification, and visuals. After using any tools or services, the author reviewed and edited the content as needed and takes full responsibility for the final publication.

A more detailed disclosure may look like this:

> The author used sIATC, the Statement of Intellectual Fellowship and Accountability for Content, to document the interaction between human authorship and AI tools during the production of this piece. The assessment records the extent of AI use across nine stages of content creation: Conception & Angle; Research & Sourcing; Structure; Drafting; Editing & Refinement; Revision; Translation; Fact-checking & Verification; and Visuals & Design. The sIATC figure and structured data are provided as a transparency record. The author reviewed, edited, verified, and approved the final content and remains fully responsible for it.

A repository note may look like this:

> This repository includes the sIATC HTML tool and related documentation. sIATC is a modified derivative of the original sIfA Tool by Mareike Schomerus / Busara, released under the Apache License 2.0. The adaptation replaces the CRediT research taxonomy with a nine-stage taxonomy for written content and simplifies the workflow for content self-assessment.

## For editors, publishers, and organizations

### When to request a sIATC

Editors, publishers, institutions, and organizations may request a sIATC when they want a more structured disclosure of AI use than a generic statement can provide.

sIATC may be useful for:

- articles;
- reports;
- opinion pieces;
- books and book chapters;
- essays;
- newsletters;
- institutional statements;
- policy briefs;
- scripts;
- presentations;
- white papers;
- long-form posts;
- research communication pieces;
- communication and marketing materials;
- educational content.

A sIATC is especially useful when the content is published in a context where trust, authorship, intellectual process, citation, accuracy, or accountability matters.

### How to read a sIATC figure

The sIATC figure is a visual summary of the author's self-assessment.

- The orange brain represents the human author.
- The purple center represents AI interaction.
- Each axis represents one content stage.
- A larger purple extension along an axis means higher declared AI involvement in that stage.
- A stage marked "not applicable" is excluded from the figure.
- The figure should be read together with the table or JSON data when detail is needed.

The figure is not a quality score. A larger purple shape does not automatically mean the content is better or worse. It means the author declared more AI interaction in the production process.

### What sIATC can and cannot prove

sIATC can support:

- more transparent AI disclosure;
- better reflection by authors;
- clearer editorial conversations;
- machine-readable records of AI interaction;
- comparison across pieces of content;
- institutional learning about how AI is being used;
- more specific accountability statements.

sIATC cannot prove:

- that the author disclosed everything;
- that no undisclosed AI use occurred;
- that the content is accurate;
- that the content is original;
- that the content is free of hallucinations;
- that the content is ethically acceptable;
- that copyright and data-protection issues were resolved;
- that the final text meets editorial standards.

sIATC is a structured self-assessment. It should be treated as a transparency practice, not as a forensic audit or certification system.

## For developers

### Repository layout

A suggested repository layout for sIATC:

```text
.
├── sIATC_vX.X.html                    # Main browser-based tool
├── README.md                          # Repository documentation
├── LICENSE                            # Apache License 2.0
├── NOTICE                             # Attribution notice, including original sIfA attribution
├── CHANGELOG.md                       # Version history
├── CONTRIBUTING.md                    # Contribution guidelines
├── CITATION.cff                       # Machine-readable citation file
├── HOW_TO_CITE.md                     # Suggested attribution and citation text
├── docs/
│   ├── SCHEMA.md                      # .sIATC.json format, human-readable overview
│   └── sIATC.schema.json              # JSON Schema for .sIATC.json, if maintained
├── examples/
│   ├── example.sIATC.json             # Example self-assessment data
│   └── example.svg                    # Example exported figure
└── .github/
    └── ISSUE_TEMPLATE/
```

The exact repository structure may be simplified. Since sIATC is distributed as a single HTML file, the minimum viable repository can contain only:

```text
.
├── sIATC_vX.X.html
├── README.md
├── LICENSE
└── NOTICE
```

However, for public reuse, citation, derivative tracking, and machine-readable disclosure, the fuller structure is recommended.

### Running and editing

There is no installation step for end users. Open the HTML file in a browser.

For local development:

```bash
# Option 1: open the file directly
open "sIATC_vX.X.html"

# Option 2: serve the directory locally
python3 -m http.server 8000

# Then visit
http://localhost:8000/sIATC_vX.X.html
```

The current tool is designed as a self-contained browser application. It can be edited by modifying the HTML, CSS, and JavaScript inside the file.

Depending on the version, external libraries may be loaded from a CDN or embedded directly in the file. If offline use is important, distribute a version with all required dependencies embedded.

### Architecture in one paragraph

sIATC is a single-page browser application. It holds the user's self-assessment state in the browser, renders the interface as editable stage cards or table-like sections, and generates the sIATC figure as an SVG. Exports are produced client-side by serializing the SVG or the structured JSON data into downloadable files. There is no backend, no login system, no database, and no remote storage. The tool is designed for portability, transparency, and ease of redistribution.

### State model

The main editable state can be understood as one object containing metadata about the piece and one entry per content stage.

A simplified conceptual model:

```js
const sIATC = {
  version: "1.2",
  type: "sIATC-content-statement",
  created_at: "2026-01-01T00:00:00Z",
  piece: {
    title: "Example article title",
    author: "Author name"
  },
  stages: {
    conception: {
      label: "Conception & Angle",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Used to brainstorm possible angles."
    },
    research: {
      label: "Research & Sourcing",
      applicable: true,
      extent: 1,
      tool: "Perplexity, Google Search",
      note: "Used to identify possible sources, checked manually."
    },
    structure: {
      label: "Structure",
      applicable: true,
      extent: 2,
      tool: "Claude",
      note: "Used to propose and reorganize outlines."
    },
    drafting: {
      label: "Drafting",
      applicable: true,
      extent: 0,
      tool: "",
      note: "No AI used in drafting."
    },
    editing: {
      label: "Editing & Refinement",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Used to identify unclear passages."
    },
    revision: {
      label: "Revision",
      applicable: true,
      extent: 1,
      tool: "Claude",
      note: "Used to compare feedback against the draft."
    },
    translation: {
      label: "Translation",
      applicable: false,
      extent: 0,
      tool: "",
      note: "Not applicable."
    },
    verification: {
      label: "Fact-checking & Verification",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Used to flag claims requiring manual verification."
    },
    visuals: {
      label: "Visuals & Design",
      applicable: true,
      extent: 2,
      tool: "DALL-E, Canva",
      note: "Used to generate and adapt visual concepts."
    }
  },
  accountability_statement: "After using any tools or services, the author reviewed and edited the content as needed and takes full responsibility for the content of the publication.",
  derived_from: {
    name: "sIfA Tool - Statement of Intellectual Fellowship and Accountability",
    creator: "Mareike Schomerus / Busara",
    doi: "10.5281/zenodo.20285993",
    license: "Apache-2.0"
  }
};
```

Actual implementation details may differ. The key principle is that the exported record should preserve:

- the content title or identifier;
- the author or responsible party, when provided;
- the active taxonomy;
- each stage's applicability;
- each stage's AI-use extent;
- the tool or service used;
- the author's explanation of how AI was used;
- the timestamp or version, when available;
- the derivative attribution to the original sIfA tool.

### Changing the content stages

The default sIATC taxonomy contains nine stages:

```js
const STAGES = [
  {
    id: "conception",
    label: "Conception & Angle",
    definition: "The core idea, angle and message."
  },
  {
    id: "research",
    label: "Research & Sourcing",
    definition: "The facts, references and examples the piece rests on."
  },
  {
    id: "structure",
    label: "Structure",
    definition: "Outline, sequence and narrative flow."
  },
  {
    id: "drafting",
    label: "Drafting",
    definition: "Producing the original text."
  },
  {
    id: "editing",
    label: "Editing & Refinement",
    definition: "Language, tone, clarity, concision and voice."
  },
  {
    id: "revision",
    label: "Revision",
    definition: "Substantive reworking of content and argument."
  },
  {
    id: "translation",
    label: "Translation",
    definition: "Rendering the piece into another language."
  },
  {
    id: "verification",
    label: "Fact-checking & Verification",
    definition: "Confirming claims, quotes, figures and sources."
  },
  {
    id: "visuals",
    label: "Visuals & Design",
    definition: "The visual layer that presents or supports the words."
  }
];
```

Changing the taxonomy should be done carefully. A stable taxonomy makes different sIATC statements easier to compare. If a derivative version changes the taxonomy, it should:

- change the tool name or version;
- document the change in the README;
- document the change in the source comments;
- preserve attribution to sIfA if the derivative still uses the original tool structure or visual assets;
- update example files and schema files accordingly.

### Build and offline use

sIATC is intended to be easy to redistribute as a single HTML file.

A public release may include:

- an online version that loads dependencies from a CDN;
- an offline version that embeds all dependencies directly in the HTML;
- example `.sIATC.json` files;
- example exported figures;
- citation and attribution files.

If an offline build script is used, document it here. A typical offline-build script would:

1. Read the main `sIATC_vX.X.html` file.
2. Download or read cached JavaScript dependencies.
3. Inline those dependencies into the HTML file.
4. Write a standalone offline HTML file.
5. Preserve the license and attribution comments in the generated file.

The offline file is usually larger, but it is more useful in low-connectivity environments and for archival purposes.

### Known limitations

- sIATC is based on self-assessment. It depends on the author's honest and careful reflection.
- The 0/1/2 scale is intentionally simple and does not capture every nuance of AI interaction.
- The figure is a visual summary, not a precise measurement.
- The tool does not verify whether the disclosure is complete.
- The tool does not check factual accuracy.
- The tool does not detect plagiarism or copyright violations.
- The tool does not inspect prompts, logs, files, or AI outputs unless the author records them manually.
- The tool does not upload, store, or validate data remotely.
- Browser behavior may vary for downloads, especially between Chromium-based browsers, Safari, and Firefox.
- If external libraries are loaded from a CDN, internet access may be required unless an offline version is provided.
- The taxonomy is designed for written content. Highly visual, audiovisual, software, data, or research-heavy projects may require a different taxonomy or the original sIfA tool.

## Citation and attribution

### Citing sIATC

Once sIATC has its own DOI, cite it as:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. [Repository or publisher]. https://doi.org/[ADD-sIATC-DOI]

Until a sIATC DOI is created, cite the GitHub repository and version tag:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. GitHub. [ADD-REPOSITORY-URL]

A machine-readable version of the same information can be provided in `CITATION.cff`, which GitHub uses to populate the "Cite this repository" button.

### Citing the original sIfA tool

Because sIATC is a derivative of the original sIfA tool, the original should also be credited:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

### Derivative-work notice

Suggested derivative-work notice:

> sIATC is a modified derivative of the sIfA Tool - Statement of Intellectual Fellowship and Accountability, created by Mareike Schomerus / Busara and released under the Apache License 2.0. sIATC replaces the CRediT research contributor-role taxonomy with a nine-stage taxonomy for written content and simplifies the flow for content self-assessment. The adaptation does not treat AI systems as authors, collaborators, moral agents, or responsible parties. The original brain-figure artwork is reused under the same license. sIATC additions are released under the Apache License 2.0.

Suggested short attribution:

> Based on the sIfA Tool by Mareike Schomerus / Busara, Apache License 2.0, DOI: 10.5281/zenodo.20285993.

Suggested figure caption:

> sIATC figure generated with the Statement of Intellectual Fellowship and Accountability for Content, a derivative of the sIfA Tool by Mareike Schomerus / Busara, released under Apache 2.0.

## License

Released under the **Apache License 2.0**. See `LICENSE` for the full license text and `NOTICE` for attribution notices that travel with redistributions.

In short, you can use, modify, and distribute sIATC freely, including in commercial settings, provided that:

- you include a copy of the Apache License 2.0 with any redistribution;
- you preserve copyright, patent, trademark, and attribution notices;
- you preserve the relevant contents of the `NOTICE` file;
- you clearly note modified files;
- you do not remove attribution to the original sIfA tool where original material or derivative structure remains present.

The original sIfA tool is copyright © 2026 Mareike Schomerus / Busara and licensed under the Apache License 2.0.

sIATC additions are copyright © 2026 Luis Ferreira and released under the Apache License 2.0.

The software is provided on an "AS IS" basis, without warranties or conditions of any kind, either express or implied.

## Acknowledgements

sIATC is based on the original sIfA Tool - Statement of Intellectual Fellowship and Accountability, created by Mareike Schomerus / Busara. sIATC preserves the attribution and derivative lineage while adopting a content-specific framing centered on intellectual accountability and transparency.

The original sIfA tool introduced a practical and visual way to reflect on how humans and AI interact in producing knowledge. sIATC adapts that idea for written content and editorial production.

Special acknowledgement is due to Mareike Schomerus / Busara for releasing the original tool under an open-source license, making derivative work possible.

sIATC also acknowledges the broader community working on AI transparency, responsible AI use, authorship disclosure, publication ethics, machine-readable accountability statements, and reflective practice in knowledge and content production.

---

# Português

# sIATC - Declaração de Responsabilidade Intelectual e Transparência no Uso de IA em Conteúdo

[![DOI original do sIfA](https://zenodo.org/badge/DOI/10.5281/zenodo.20285993.svg)](https://doi.org/10.5281/zenodo.20285993)

Uma ferramenta em HTML para declarar como ferramentas de IA contribuíram para a produção de um conteúdo escrito, usando uma taxonomia de nove etapas de criação de conteúdo. A ferramenta gera uma tabela estruturada e uma visualização em página única, a figura sIATC, que pode ser anexada a artigos, relatórios, ensaios, posts, capítulos de livros, newsletters, textos institucionais, apresentações e outros materiais editoriais.

> **sIATC** preserva sua linhagem a partir da ferramenta sIfA original, mas esta adaptação voltada a conteúdo usa o enquadramento **Declaração de Responsabilidade Intelectual e Transparência no Uso de IA em Conteúdo**.

"Responsabilidade intelectual" indica que a autoria humana mantém o controle, a revisão, a verificação e a aprovação final do conteúdo. "Transparência" indica que o uso de IA deve ser descrito com clareza, etapa por etapa, sem tratar sistemas de IA como autores, ferramentas, agentes morais ou partes responsáveis.

O sIATC é uma derivação modificada do **sIfA Tool - Statement of Intellectual Fellowship and Accountability**, criado por Mareike Schomerus / Busara e distribuído sob a licença Apache 2.0.

Essa escolha de terminologia é deliberada: Adaptamos a terminologia para produção de conteúdo, enfatizando a responsabilidade intelectual e a transparência em vez da colaboração. Isso evita tratar os sistemas de IA como autores, colaboradores ou agentes morais. O sIATC não atribui autoria, agência, intenção, condição moral ou responsabilidade a sistemas de IA. A IA é tratada como tecnologia usada no processo de produção de conteúdo, sempre sujeita à supervisão, revisão, verificação e responsabilidade humana.

O sIfA original foi criado para pesquisa e produção de conhecimento, usando a taxonomia CRediT de papéis de contribuição. O sIATC adapta a mesma lógica de reflexão para conteúdos escritos, enfatizando responsabilidade intelectual, transparência e responsabilidade humana. Ele substitui a taxonomia de papéis de contribuição em pesquisa por uma taxonomia de nove etapas de criação de conteúdo:

- Concepção e Ângulo
- Pesquisa e Fontes
- Estrutura
- Redação
- Edição e Refinamento
- Revisão
- Tradução
- Checagem e Verificação
- Imagens e Design

A ferramenta consiste em um único arquivo HTML. Não exige instalação, servidor, conta ou etapa de compilação para usuários finais.

## Por que o sIATC existe

O uso de IA na escrita e na produção de conteúdo está crescendo mais rápido do que as convenções para declará-lo. Declarações genéricas, como "foi usada IA na preparação deste texto", são vagas demais. Elas não mostram onde a IA entrou no processo, se moldou o argumento, se ajudou na estrutura, se gerou linguagem, se traduziu, se verificou afirmações ou se apenas ajudou a polir frases.

O sIATC oferece a autores, editores, pesquisadores, comunicadores, organizações e leitores uma forma compartilhada e estruturada de descrever como a IA interagiu com uma peça de conteúdo.

Ele foi desenhado para conteúdo, não apenas para pesquisa.

O sIfA original foi desenvolvido para apoiar a reflexão sobre interação humano/IA na produção de conhecimento, especialmente em outputs de pesquisa. Ele usa papéis de contribuição associados a processos de pesquisa. O sIATC mantém a ideia central de reflexão e responsabilidade, mas adapta a terminologia para a produção de conteúdo ao enfatizar responsabilidade intelectual e transparência, em vez de parceria ou companheirismo. Essa escolha evita tratar sistemas de IA como autores, ferramentas, agentes morais ou partes responsáveis. Também muda a unidade de análise: sai a lógica de papéis de contribuição em pesquisa, entra a lógica das etapas de produção de conteúdo escrito.

Essa mudança é relevante. Um artigo, relatório, livro, post de LinkedIn, texto institucional, newsletter ou ensaio de opinião pode envolver pesquisa, mas também envolve escolhas editoriais que não cabem integralmente em taxonomias de pesquisa. A autoria pode precisar refletir sobre como a IA ajudou a definir o ângulo, organizar a sequência, redigir trechos, refinar o tom, traduzir, checar fatos ou criar elementos visuais. Essas são formas distintas de participação e não deveriam ser reduzidas a uma única nota genérica.

O sIATC é, portanto, uma ferramenta de autoavaliação. Não é uma ferramenta de auditoria. Ele não certifica a qualidade, veracidade, autoria, originalidade ou condição ética de um conteúdo. Ele convida a autoria a pausar, refletir, documentar e declarar.

A autoria humana permanece responsável pelo resultado final.

## Relação com o sIfA original

O sIATC é uma derivação modificada de:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

O sIfA original é distribuído sob a licença Apache 2.0. O sIATC preserva a atribuição a Mareike Schomerus / Busara e carrega as obrigações de licença exigidas para redistribuição e modificação.

### O que o sIATC preserva do sIfA

O sIATC preserva a lógica reflexiva central da ferramenta original:

- o uso de IA é declarado por etapas definidas, em vez de ficar escondido em uma nota genérica;
- a autoria registra a extensão da interação com IA em uma escala simples de 0/1/2;
- a ferramenta produz uma figura visual que torna a interação humano/IA reconhecível rapidamente;
- a ferramenta produz dados estruturados e legíveis por máquina;
- a figura mantém a metáfora visual do cérebro humano: o campo laranja representa a autoria humana, enquanto o centro roxo representa a interação com IA;
- a responsabilidade humana permanece explícita;
- a ferramenta é distribuída como um único arquivo HTML, que pode rodar localmente no navegador;
- a arte original da figura do cérebro é reutilizada sob a licença Apache 2.0.

### O que o sIATC muda

O sIATC muda o domínio de aplicação, a taxonomia e o fluxo.

O sIfA original foi desenhado principalmente para pesquisa e produção de conhecimento, tendo a taxonomia CRediT como referência importante. O sIATC foi desenhado especificamente para criação de conteúdo.

As principais mudanças são:

- a taxonomia CRediT de 14 papéis de contribuição em pesquisa é substituída por uma taxonomia de nove etapas de conteúdo escrito;
- os papéis específicos de pesquisa são removidos;
- o foco passa de atribuição de contribuição em pesquisa para autoavaliação do processo de criação de conteúdo;
- o fluxo é simplificado para autoria única ou autoria responsável;
- cada etapa de conteúdo pode ser marcada como "não se aplica" quando não ocorreu;
- a ferramenta é enquadrada para artigos, relatórios, posts, ensaios, newsletters, livros, capítulos, textos institucionais, roteiros, apresentações e outros formatos editoriais;
- a declaração enfatiza como a IA interagiu com a criação do conteúdo, não como contribuiu para um projeto de pesquisa.

O sIATC, portanto, não substitui o sIfA. Ele é uma adaptação para outro caso de uso.

Use o sIfA quando o objeto principal for um output de pesquisa e a estrutura de contribuição estilo CRediT for adequada. Use o sIATC quando o objeto principal for conteúdo escrito e a pergunta relevante for como a IA interagiu com as etapas de produção desse conteúdo.

## Sumário

- [Para autores e criadores de conteúdo](#para-autores-e-criadores-de-conteúdo)
  - [Início rápido](#início-rápido)
  - [Como a ferramenta está estruturada](#como-a-ferramenta-está-estruturada)
  - [As nove etapas de conteúdo](#as-nove-etapas-de-conteúdo)
  - [Escala de extensão de uso de IA](#escala-de-extensão-de-uso-de-ia)
  - [Como avaliar a extensão do uso de IA](#como-avaliar-a-extensão-do-uso-de-ia)
  - [Salvando e exportando](#salvando-e-exportando)
  - [Exemplo prático](#exemplo-prático)
  - [O que não é enviado para lugar nenhum](#o-que-não-é-enviado-para-lugar-nenhum)
  - [Texto sugerido de declaração](#texto-sugerido-de-declaração)
- [Para editores, publicadores e organizações](#para-editores-publicadores-e-organizações)
  - [Quando solicitar um sIATC](#quando-solicitar-um-sIATC)
  - [Como ler uma figura sIATC](#como-ler-uma-figura-sIATC)
  - [O que o sIATC pode e não pode provar](#o-que-o-sIATC-pode-e-não-pode-provar)
- [Para desenvolvedores](#para-desenvolvedores)
  - [Layout do repositório](#layout-do-repositório)
  - [Executando e editando](#executando-e-editando)
  - [Arquitetura em um parágrafo](#arquitetura-em-um-parágrafo)
  - [Modelo de estado](#modelo-de-estado)
  - [Alterando as etapas de conteúdo](#alterando-as-etapas-de-conteúdo)
  - [Build e uso offline](#build-e-uso-offline)
  - [Limitações conhecidas](#limitações-conhecidas)
- [Citação e atribuição](#citação-e-atribuição)
  - [Como citar o sIATC](#como-citar-o-sIATC)
  - [Como citar o sIfA original](#como-citar-o-sifa-original)
  - [Aviso de obra derivada](#aviso-de-obra-derivada)
- [Licença](#licença)
- [Agradecimentos](#agradecimentos)

## Para autores e criadores de conteúdo

### Início rápido

1. Baixe a versão mais recente do arquivo `sIATC_vX.X.html` na página de [Releases](../../releases).
2. Abra o arquivo em qualquer navegador moderno clicando duas vezes nele. Chrome, Edge, Safari, Firefox e outros navegadores modernos devem funcionar.
3. Informe o título ou descrição da peça de conteúdo.
4. Informe o nome da autoria, se desejar.
5. Para cada etapa de conteúdo, escolha um dos três níveis de uso de IA:
   - 0 = nenhum
   - 1 = algum
   - 2 = extenso
6. Marque uma etapa como "não se aplica" quando ela não tiver ocorrido no processo de produção.
7. Adicione a ferramenta ou serviço de IA usado, quando relevante.
8. Adicione uma nota breve explicando como a IA foi usada.
9. Exporte a figura como SVG ou PNG, ou exporte os dados como um arquivo `.sIATC.json`.

Esse é todo o fluxo. A ferramenta é uma única página HTML. Não há instalação, conta, upload ou servidor.

### Como a ferramenta está estruturada

A interface é uma única página com quatro partes principais:

- **Campos de metadados** para o título do conteúdo e a autoria.
- **Uma avaliação etapa por etapa** cobrindo as nove etapas de produção de conteúdo escrito.
- **Uma figura em forma de cérebro** mostrando o grau de interação com IA nas etapas ativas.
- **Botões de exportação** para baixar a figura ou exportar os dados estruturados.

A figura se preenche do centro para fora à medida que a participação da IA aumenta. O cérebro laranja representa a autoria humana. O centro roxo representa a interação com IA. Cada eixo corresponde a uma etapa de conteúdo. Quanto mais a forma roxa avança em uma etapa, maior é o envolvimento declarado da IA naquela parte do processo.

Etapas marcadas como "não se aplica" são excluídas da figura.

A ferramenta também inclui uma declaração de responsabilidade:

> Após usar quaisquer ferramentas ou serviços, a autoria revisou e editou o conteúdo conforme necessário e assume total responsabilidade pelo conteúdo da publicação.

Essa declaração pode ser adaptada conforme o contexto de publicação, mas o princípio deve permanecer: a autoria humana é responsável pelo conteúdo final.

### As nove etapas de conteúdo

O sIATC usa uma taxonomia de nove etapas para conteúdo escrito. A taxonomia não pretende descrever todo processo editorial com precisão perfeita. Ela é uma estrutura prática para reflexão, declaração e comparação.

| Etapa | O que significa | Exemplos de interação com IA |
| --- | --- | --- |
| **Concepção e Ângulo** | A ideia central, o ângulo e a mensagem do conteúdo: sobre o que é a peça e por que vale a pena produzi-la. | Explorar ângulos ou ganchos; testar um argumento; gerar opções de enquadramento; afinar a mensagem principal. |
| **Pesquisa e Fontes** | Os fatos, referências, exemplos e materiais de base em que o conteúdo se apoia. | Resumir leituras; encontrar dados ou citações de apoio; reunir material prévio; mapear o que já foi dito. |
| **Estrutura** | Roteiro, sequência, lógica das seções e fluxo narrativo. | Esboçar ou reordenar um roteiro; propor um arco narrativo; testar se o fluxo funciona; adaptar a estrutura a um formato. |
| **Redação** | Produzir texto original: transformar ideia e roteiro em prosa. | Gerar um primeiro rascunho a partir de um briefing; redigir seções; expandir notas em prosa; produzir formulações alternativas. |
| **Edição e Refinamento** | Trabalho de linguagem, tom, clareza, concisão e voz. | Editar para dar clareza; adaptar tom; reescrever passagens truncadas; enxugar para o tamanho adequado. |
| **Revisão** | Reformulação substantiva do conteúdo ou argumento após feedback, releitura ou nova avaliação. | Incorporar comentários; reformular argumento; conciliar feedbacks; decidir o que cortar, expandir ou reorganizar. |
| **Tradução** | Verter o conteúdo para outro idioma, incluindo localização e consistência terminológica. | Refinar tradução automática; adaptar expressões idiomáticas e referências culturais; aplicar glossário; fazer retrotradução para conferir fidelidade. |
| **Checagem e Verificação** | Confirmar que afirmações, números, citações, nomes, datas e fontes estão corretos. | Verificar fatos sugeridos por IA contra fontes; conferir atribuições; sinalizar possíveis alucinações; revisar vieses. |
| **Imagens e Design** | A camada visual que apoia ou apresenta o conteúdo. | Gerar ou buscar imagens; esboçar layouts; criar gráficos ou diagramas; adaptar visuais a uma plataforma ou formato. |

Uma etapa pode ser marcada como "não se aplica" quando não ocorreu. Por exemplo, se o conteúdo não foi traduzido, a etapa Tradução pode ser excluída. Se nenhum visual foi produzido, Imagens e Design pode ser excluída.

### Escala de extensão de uso de IA

O sIATC usa uma escala de três níveis para descrever o quanto a IA interagiu com cada etapa.

| Extensão de IA | Significado | Interpretação típica |
| --- | --- | --- |
| **0 - Nenhum** | Nenhuma IA foi usada nesta etapa. | A etapa foi realizada sem ferramentas de IA. |
| **1 - Algum** | A IA auxiliou a autoria, mas não conduziu a etapa. | A IA ajudou com sugestões, alternativas, resumos, correções ou apoio limitado. A autoria controlou e produziu substancialmente o resultado. |
| **2 - Extenso** | A IA teve papel substancial na etapa. | A IA gerou, transformou, estruturou, traduziu, analisou ou moldou materialmente o resultado, que depois foi revisado, editado, verificado e aceito pela autoria. |

A escala 0/1/2 é intencionalmente simples. Ela foi desenhada para reflexão e comunicação, não para medição exata. O objetivo é tornar a interação com IA visível o suficiente para apoiar responsabilidade, aprendizado, comparação e melhores práticas de declaração.

### Como avaliar a extensão do uso de IA

A autoria deve usar julgamento ao atribuir um nível. As orientações abaixo podem ajudar.

Use **0 - Nenhum** quando:

- nenhuma ferramenta de IA foi usada naquela etapa;
- a IA foi usada em outra etapa, mas não naquela;
- a etapa não envolveu material gerado, assistido ou transformado por IA.

Use **1 - Algum** quando:

- a IA sugeriu opções, mas a autoria selecionou, rejeitou ou reescreveu substancialmente;
- a IA ajudou com clareza, tom, gramática, concisão ou formatação;
- a IA resumiu material que a autoria já havia selecionado e conferido;
- a IA ajudou a explorar possibilidades, sem determinar a direção final;
- a IA foi usada como interlocutora para teste, crítica ou revisão.

Use **2 - Extenso** quando:

- a IA gerou um primeiro rascunho ou trechos substanciais;
- a IA produziu uma tradução que virou base da versão final;
- a IA moldou materialmente a estrutura ou o argumento;
- a IA sintetizou material de fonte em conteúdo utilizável;
- a IA criou elementos visuais usados no resultado final;
- a IA realizou parte importante da checagem, verificação, classificação ou revisão editorial, sujeita a revisão humana;
- o resultado final daquela etapa seria materialmente diferente sem a IA.

A autoria deve ser transparente sobre incertezas. Quando uma etapa ficar entre "algum" e "extenso", escolha o nível que melhor represente a dependência da etapa em relação à IA e explique a escolha no campo de nota.

### Salvando e exportando

O sIATC permite diferentes formas de exportação.

- **Baixar figura como SVG**: exporta a figura em formato vetorial escalável, adequado para publicação, sites, repositórios e documentos.
- **Baixar figura como PNG**: exporta a figura como imagem, facilitando o uso em slides, posts e plataformas que não lidam bem com SVG.
- **Exportar dados como `.sIATC.json`**: exporta os dados estruturados da avaliação, incluindo metadados do conteúdo, notas por etapa, ferramentas de IA, explicações e data/hora.
- **Interação local no navegador**: a ferramenta roda no navegador. Não há servidor.

O arquivo `.sIATC.json` exportado pode ser usado como registro legível por máquina da autoavaliação. A figura SVG ou PNG pode ser anexada ao próprio conteúdo, incluída em um repositório, adicionada como material suplementar ou publicada junto com a peça.

### Exemplo prático

Um sIATC fictício para um artigo longo sobre o efeito da IA na escrita profissional:

| Etapa | Extensão de IA | Ferramenta / serviço | Como a IA foi usada |
| --- | --- | --- | --- |
| Concepção e Ângulo | 1 | ChatGPT | Usada para testar possíveis ângulos e identificar enquadramentos fracos. O ângulo final foi escolhido pela autoria. |
| Pesquisa e Fontes | 1 | Perplexity, Google Search, ChatGPT | Usadas para mapear debates relevantes e identificar fontes possíveis. As fontes foram conferidas manualmente antes da inclusão. |
| Estrutura | 2 | Claude | Usada para propor diferentes roteiros e reorganizar o argumento. A autoria selecionou e modificou a estrutura final. |
| Redação | 0 | - | Nenhuma IA usada para gerar o primeiro rascunho. |
| Edição e Refinamento | 1 | ChatGPT | Usada para identificar passagens pouco claras e sugerir formulações mais enxutas. A autoria reescreveu manualmente. |
| Revisão | 1 | Claude | Usada para comparar feedbacks de revisão com o rascunho e identificar seções que exigiam expansão. |
| Tradução | Não se aplica | - | O texto não foi traduzido. |
| Checagem e Verificação | 1 | ChatGPT, revisão manual de fontes | Usada para sinalizar afirmações que exigiam verificação manual. |
| Imagens e Design | 2 | DALL-E, Canva | Usadas para gerar conceitos visuais e adaptá-los ao formato de publicação. |

Nesse exemplo, a figura sIATC exportada mostraria nenhuma interação com IA em Redação, nenhum eixo para Tradução caso marcada como não se aplica, e interação mais forte em Estrutura e Imagens e Design.

### O que não é enviado para lugar nenhum

A ferramenta roda inteiramente no navegador. Nada é enviado pela ferramenta a um servidor.

Especificamente:

- o título do conteúdo permanece no seu computador;
- o nome da autoria permanece no seu computador;
- as avaliações por etapa permanecem no seu computador;
- as ferramentas e serviços listados permanecem no seu computador;
- as notas sobre como a IA foi usada permanecem no seu computador;
- o arquivo `.sIATC.json` exportado é seu para guardar, publicar, anexar, arquivar ou apagar.

A ferramenta não oferece analytics, rastreamento de usuários, contas, armazenamento em nuvem ou validação remota.

Se você usar um serviço de IA de terceiros durante a produção do conteúdo, esse serviço pode ter suas próprias políticas de uso de dados. O sIATC não controla esses serviços. O sIATC apenas registra sua autoavaliação sobre como eles foram usados.

### Texto sugerido de declaração

Uma declaração curta pode ser:

> Este conteúdo inclui uma declaração sIATC documentando como ferramentas de IA interagiram com o processo de produção. O uso de IA foi autoavaliado nas etapas de concepção, pesquisa, estrutura, redação, edição, revisão, tradução, verificação e imagens. Após usar quaisquer ferramentas ou serviços, a autoria revisou e editou o conteúdo conforme necessário e assume total responsabilidade pela publicação final.

Uma declaração mais detalhada pode ser:

> A autoria usou o sIATC, Statement of Intellectual Fellowship and Accountability for Content, para documentar a interação entre autoria humana e ferramentas de IA durante a produção deste conteúdo. A avaliação registra a extensão do uso de IA em nove etapas de criação de conteúdo: Concepção e Ângulo; Pesquisa e Fontes; Estrutura; Redação; Edição e Refinamento; Revisão; Tradução; Checagem e Verificação; e Imagens e Design. A figura sIATC e os dados estruturados são fornecidos como registro de transparência. A autoria revisou, editou, verificou e aprovou o conteúdo final, permanecendo integralmente responsável por ele.

Uma nota de repositório pode ser:

> Este repositório inclui a ferramenta HTML sIATC e sua documentação. O sIATC é uma derivação modificada do sIfA Tool, criado por Mareike Schomerus / Busara e distribuído sob a licença Apache 2.0. A adaptação substitui a taxonomia CRediT de pesquisa por uma taxonomia de nove etapas para conteúdo escrito e simplifica o fluxo para autoavaliação de conteúdo.

## Para editores, publicadores e organizações

### Quando solicitar um sIATC

Editores, publicadores, instituições e organizações podem solicitar um sIATC quando quiserem uma declaração de uso de IA mais estruturada do que uma nota genérica.

O sIATC pode ser útil para:

- artigos;
- relatórios;
- artigos de opinião;
- livros e capítulos;
- ensaios;
- newsletters;
- textos institucionais;
- policy briefs;
- roteiros;
- apresentações;
- white papers;
- posts longos;
- peças de comunicação científica;
- materiais de comunicação e marketing;
- conteúdo educacional.

Um sIATC é especialmente útil quando o conteúdo é publicado em um contexto no qual confiança, autoria, processo intelectual, citação, precisão ou responsabilidade importam.

### Como ler uma figura sIATC

A figura sIATC é um resumo visual da autoavaliação da autoria.

- O cérebro laranja representa a autoria humana.
- O centro roxo representa a interação com IA.
- Cada eixo representa uma etapa de conteúdo.
- Uma extensão roxa maior em um eixo significa maior envolvimento declarado da IA naquela etapa.
- Uma etapa marcada como "não se aplica" é excluída da figura.
- A figura deve ser lida junto com a tabela ou os dados JSON quando houver necessidade de detalhe.

A figura não é uma nota de qualidade. Uma forma roxa maior não significa automaticamente que o conteúdo é melhor ou pior. Significa que a autoria declarou maior interação com IA no processo de produção.

### O que o sIATC pode e não pode provar

O sIATC pode apoiar:

- uma declaração mais transparente de uso de IA;
- melhor reflexão por parte da autoria;
- conversas editoriais mais claras;
- registros legíveis por máquina sobre interação com IA;
- comparação entre diferentes peças de conteúdo;
- aprendizado institucional sobre como a IA está sendo usada;
- declarações de responsabilidade mais específicas.

O sIATC não pode provar:

- que a autoria declarou tudo;
- que não houve uso não declarado de IA;
- que o conteúdo é preciso;
- que o conteúdo é original;
- que o conteúdo está livre de alucinações;
- que o conteúdo é eticamente aceitável;
- que questões de direitos autorais e proteção de dados foram resolvidas;
- que o texto final atende a padrões editoriais.

O sIATC é uma autoavaliação estruturada. Deve ser tratado como prática de transparência, não como auditoria forense ou sistema de certificação.

## Para desenvolvedores

### Layout do repositório

Um layout recomendado para o repositório sIATC:

```text
.
├── sIATC_vX.X.html                    # Ferramenta principal em HTML
├── README.md                          # Documentação do repositório
├── LICENSE                            # Licença Apache 2.0
├── NOTICE                             # Aviso de atribuição, incluindo o sIfA original
├── CHANGELOG.md                       # Histórico de versões
├── CONTRIBUTING.md                    # Diretrizes de contribuição
├── CITATION.cff                       # Arquivo de citação legível por máquina
├── HOW_TO_CITE.md                     # Textos sugeridos de citação e atribuição
├── docs/
│   ├── SCHEMA.md                      # Visão geral do formato .sIATC.json
│   └── sIATC.schema.json              # JSON Schema para .sIATC.json, se mantido
├── examples/
│   ├── example.sIATC.json             # Exemplo de dados de autoavaliação
│   └── example.svg                    # Exemplo de figura exportada
└── .github/
    └── ISSUE_TEMPLATE/
```

A estrutura exata pode ser simplificada. Como o sIATC é distribuído como um único arquivo HTML, o repositório mínimo pode conter apenas:

```text
.
├── sIATC_vX.X.html
├── README.md
├── LICENSE
└── NOTICE
```

Para reuso público, citação, rastreamento de obra derivada e declaração legível por máquina, a estrutura mais completa é recomendada.

### Executando e editando

Não há etapa de instalação para usuários finais. Basta abrir o arquivo HTML em um navegador.

Para desenvolvimento local:

```bash
# Opção 1: abrir o arquivo diretamente
open "sIATC_vX.X.html"

# Opção 2: servir o diretório localmente
python3 -m http.server 8000

# Depois acessar
http://localhost:8000/sIATC_vX.X.html
```

A ferramenta atual foi desenhada como uma aplicação de navegador autocontida. Ela pode ser editada modificando HTML, CSS e JavaScript dentro do próprio arquivo.

Dependendo da versão, bibliotecas externas podem ser carregadas por CDN ou embutidas diretamente no arquivo. Se o uso offline for importante, distribua uma versão com todas as dependências embutidas.

### Arquitetura em um parágrafo

O sIATC é uma aplicação de navegador de página única. Ele mantém o estado da autoavaliação no navegador do usuário, renderiza a interface como cartões ou seções editáveis por etapa, e gera a figura sIATC como SVG. As exportações são produzidas do lado do cliente, serializando o SVG ou os dados estruturados em JSON para arquivos baixáveis. Não há backend, sistema de login, banco de dados ou armazenamento remoto. A ferramenta foi desenhada para portabilidade, transparência e facilidade de redistribuição.

### Modelo de estado

O estado principal pode ser entendido como um objeto com metadados sobre a peça e uma entrada por etapa de conteúdo.

Modelo conceitual simplificado:

```js
const sIATC = {
  version: "1.2",
  type: "sIATC-content-statement",
  created_at: "2026-01-01T00:00:00Z",
  piece: {
    title: "Título do conteúdo",
    author: "Nome da autoria"
  },
  stages: {
    conception: {
      label: "Conception & Angle",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para explorar possíveis ângulos."
    },
    research: {
      label: "Research & Sourcing",
      applicable: true,
      extent: 1,
      tool: "Perplexity, Google Search",
      note: "Usado para identificar possíveis fontes, conferidas manualmente."
    },
    structure: {
      label: "Structure",
      applicable: true,
      extent: 2,
      tool: "Claude",
      note: "Usado para propor e reorganizar roteiros."
    },
    drafting: {
      label: "Drafting",
      applicable: true,
      extent: 0,
      tool: "",
      note: "Nenhuma IA usada na redação."
    },
    editing: {
      label: "Editing & Refinement",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para identificar passagens pouco claras."
    },
    revision: {
      label: "Revision",
      applicable: true,
      extent: 1,
      tool: "Claude",
      note: "Usado para comparar feedbacks com o rascunho."
    },
    translation: {
      label: "Translation",
      applicable: false,
      extent: 0,
      tool: "",
      note: "Não se aplica."
    },
    verification: {
      label: "Fact-checking & Verification",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para sinalizar afirmações que exigiam verificação manual."
    },
    visuals: {
      label: "Visuals & Design",
      applicable: true,
      extent: 2,
      tool: "DALL-E, Canva",
      note: "Usado para gerar e adaptar conceitos visuais."
    }
  },
  accountability_statement: "Após usar quaisquer ferramentas ou serviços, a autoria revisou e editou o conteúdo conforme necessário e assume total responsabilidade pelo conteúdo da publicação.",
  derived_from: {
    name: "sIfA Tool - Statement of Intellectual Fellowship and Accountability",
    creator: "Mareike Schomerus / Busara",
    doi: "10.5281/zenodo.20285993",
    license: "Apache-2.0"
  }
};
```

A implementação real pode variar. O princípio central é que o registro exportado deve preservar:

- o título ou identificador do conteúdo;
- a autoria ou parte responsável, quando informada;
- a taxonomia ativa;
- a aplicabilidade de cada etapa;
- a extensão de uso de IA em cada etapa;
- a ferramenta ou serviço usado;
- a explicação da autoria sobre como a IA foi usada;
- a data/hora ou versão, quando disponível;
- a atribuição derivada ao sIfA original.

### Alterando as etapas de conteúdo

A taxonomia padrão do sIATC contém nove etapas:

```js
const STAGES = [
  {
    id: "conception",
    label: "Conception & Angle",
    definition: "The core idea, angle and message."
  },
  {
    id: "research",
    label: "Research & Sourcing",
    definition: "The facts, references and examples the piece rests on."
  },
  {
    id: "structure",
    label: "Structure",
    definition: "Outline, sequence and narrative flow."
  },
  {
    id: "drafting",
    label: "Drafting",
    definition: "Producing the original text."
  },
  {
    id: "editing",
    label: "Editing & Refinement",
    definition: "Language, tone, clarity, concision and voice."
  },
  {
    id: "revision",
    label: "Revision",
    definition: "Substantive reworking of content and argument."
  },
  {
    id: "translation",
    label: "Translation",
    definition: "Rendering the piece into another language."
  },
  {
    id: "verification",
    label: "Fact-checking & Verification",
    definition: "Confirming claims, quotes, figures and sources."
  },
  {
    id: "visuals",
    label: "Visuals & Design",
    definition: "The visual layer that presents or supports the words."
  }
];
```

Alterações na taxonomia devem ser feitas com cuidado. Uma taxonomia estável facilita a comparação entre diferentes declarações sIATC. Se uma versão derivada alterar a taxonomia, ela deve:

- alterar o nome ou a versão da ferramenta;
- documentar a mudança no README;
- documentar a mudança nos comentários do código-fonte;
- preservar a atribuição ao sIfA se a derivação ainda usar a estrutura ou os ativos visuais originais;
- atualizar exemplos e arquivos de schema, quando houver.

### Build e uso offline

O sIATC foi pensado para ser facilmente redistribuído como um único arquivo HTML.

Uma versão pública pode incluir:

- uma versão online que carrega dependências por CDN;
- uma versão offline que incorpora todas as dependências no HTML;
- arquivos `.sIATC.json` de exemplo;
- figuras exportadas de exemplo;
- arquivos de citação e atribuição.

Se um script de build offline for usado, documente-o nesta seção. Um script típico faria:

1. Ler o arquivo principal `sIATC_vX.X.html`.
2. Baixar ou ler do cache as dependências JavaScript.
3. Embutir essas dependências no HTML.
4. Gerar um arquivo HTML offline autocontido.
5. Preservar os comentários de licença e atribuição no arquivo gerado.

O arquivo offline costuma ser maior, mas é mais útil em ambientes de baixa conectividade e para fins de arquivamento.

### Limitações conhecidas

- O sIATC se baseia em autoavaliação. Ele depende da reflexão honesta e cuidadosa da autoria.
- A escala 0/1/2 é intencionalmente simples e não captura todas as nuances da interação com IA.
- A figura é um resumo visual, não uma medição precisa.
- A ferramenta não verifica se a declaração está completa.
- A ferramenta não checa precisão factual.
- A ferramenta não detecta plágio ou violações de direitos autorais.
- A ferramenta não inspeciona prompts, logs, arquivos ou outputs de IA, salvo quando a autoria registra manualmente.
- A ferramenta não envia, armazena ou valida dados remotamente.
- O comportamento de download pode variar entre navegadores, especialmente entre navegadores baseados em Chromium, Safari e Firefox.
- Se bibliotecas externas forem carregadas por CDN, pode ser necessário acesso à internet, a menos que uma versão offline seja fornecida.
- A taxonomia foi desenhada para conteúdo escrito. Projetos altamente visuais, audiovisuais, de software, de dados ou fortemente orientados à pesquisa podem exigir outra taxonomia ou o uso do sIfA original.

## Citação e atribuição

### Como citar o sIATC

Quando o sIATC tiver seu próprio DOI, cite assim:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. [Repository or publisher]. https://doi.org/[ADD-sIATC-DOI]

Até que o DOI do sIATC seja criado, cite o repositório GitHub e a tag de versão:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. GitHub. [ADD-REPOSITORY-URL]

Uma versão legível por máquina da mesma informação pode ser fornecida em `CITATION.cff`, usado pelo GitHub para preencher o botão "Cite this repository".

### Como citar o sIfA original

Como o sIATC é uma derivação do sIfA original, o original também deve ser creditado:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

### Aviso de obra derivada

Aviso sugerido:

> sIATC is a modified derivative of the sIfA Tool - Statement of Intellectual Fellowship and Accountability, created by Mareike Schomerus / Busara and released under the Apache License 2.0. sIATC replaces the CRediT research contributor-role taxonomy with a nine-stage taxonomy for written content and simplifies the flow for content self-assessment. The adaptation does not treat AI systems as authors, collaborators, moral agents, or responsible parties. The original brain-figure artwork is reused under the same license. sIATC additions are released under the Apache License 2.0.

Atribuição curta sugerida:

> Based on the sIfA Tool by Mareike Schomerus / Busara, Apache License 2.0, DOI: 10.5281/zenodo.20285993.

Legenda sugerida para figura:

> sIATC figure generated with the Statement of Intellectual Fellowship and Accountability for Content, a derivative of the sIfA Tool by Mareike Schomerus / Busara, released under Apache 2.0.

## Licença

Distribuído sob a **Apache License 2.0**. Consulte `LICENSE` para o texto completo da licença e `NOTICE` para os avisos de atribuição que acompanham redistribuições.

Em resumo, você pode usar, modificar e distribuir o sIATC livremente, inclusive em contextos comerciais, desde que:

- inclua uma cópia da Apache License 2.0 em qualquer redistribuição;
- preserve avisos de copyright, patente, marca e atribuição;
- preserve o conteúdo relevante do arquivo `NOTICE`;
- indique claramente os arquivos modificados;
- mantenha a atribuição ao sIfA original quando material original ou estrutura derivada permanecerem presentes.

O sIfA original é copyright © 2026 Mareike Schomerus / Busara e licenciado sob a Apache License 2.0.

Os acréscimos do sIATC são copyright © 2026 Luis Ferreira e licenciados sob a Apache License 2.0.

O software é fornecido "COMO ESTÁ", sem garantias ou condições de qualquer tipo, expressas ou implícitas.

## Agradecimentos

O sIATC é baseado no sIfA Tool - Statement of Intellectual Fellowship and Accountability, criado por Mareike Schomerus / Busara. O sIATC preserva a atribuição e a linhagem derivada, mas adota um enquadramento específico para conteúdo, centrado em responsabilidade intelectual e transparência.

O sIfA original introduziu uma forma prática e visual de refletir sobre como humanos e IA interagem na produção de conhecimento. O sIATC adapta essa ideia para conteúdo escrito e produção editorial.

Agradecimento especial a Mareike Schomerus / Busara por distribuir a ferramenta original sob uma licença open-source, tornando possível o desenvolvimento de obras derivadas.

O sIATC também reconhece a comunidade mais ampla que trabalha com transparência em IA, uso responsável de IA, declaração de autoria, ética editorial, declarações de responsabilidade legíveis por máquina e prática reflexiva na produção de conhecimento e conteúdo.

---

# Español

# sIATC - Declaración de Responsabilidad Intelectual y Transparencia en el Uso de IA en Contenidos

[![DOI original de sIfA](https://zenodo.org/badge/DOI/10.5281/zenodo.20285993.svg)](https://doi.org/10.5281/zenodo.20285993)

Una herramienta en HTML para declarar cómo las herramientas de IA contribuyeron a la producción de un contenido escrito, usando una taxonomía de nueve etapas de creación de contenido. La herramienta genera una tabla estructurada y una visualización de una sola página, la figura sIATC, que puede adjuntarse a artículos, informes, ensayos, publicaciones, capítulos de libros, newsletters, textos institucionales, presentaciones y otros materiales editoriales.

> **sIATC** conserva su linaje a partir de la herramienta sIfA original, pero esta adaptación orientada a contenidos usa el encuadre **Declaración de Responsabilidad Intelectual y Transparencia en el Uso de IA en Contenidos**.

"Responsabilidad intelectual" indica que la autoría humana mantiene el control, la revisión, la verificación y la aprobación final del contenido. "Transparencia" indica que el uso de IA debe describirse con claridad, etapa por etapa, sin tratar los sistemas de IA como autores, herramientas, agentes morales o partes responsables.

sIATC es una derivación modificada de **sIfA Tool - Statement of Intellectual Fellowship and Accountability**, creado por Mareike Schomerus / Busara y distribuido bajo la licencia Apache 2.0.

Esta elección terminológica es deliberada: Hemos adaptado la terminología para la producción de contenido, haciendo hincapié en la responsabilidad intelectual y la transparencia, en lugar de la colaboración. Esto evita tratar a los sistemas de IA como autores, colaboradores o agentes morales. sIATC no atribuye autoría, agencia, intención, condición moral ni responsabilidad a los sistemas de IA. La IA se trata como una tecnología usada en el proceso de producción de contenidos, siempre sujeta a supervisión, revisión, verificación y responsabilidad humana.

El sIfA original fue creado para investigación y producción de conocimiento, usando la taxonomía CRediT de roles de contribución. sIATC adapta la misma lógica de reflexión para contenidos escritos, enfatizando responsabilidad intelectual, transparencia y responsabilidad humana. Sustituye la taxonomía de roles de contribución en investigación por una taxonomía de nueve etapas de creación de contenido:

- Concepción y Enfoque
- Investigación y Fuentes
- Estructura
- Redacción
- Edición y Refinamiento
- Revisión
- Traducción
- Verificación de Datos
- Imágenes y Diseño

La herramienta consiste en un único archivo HTML. No exige instalación, servidor, cuenta ni etapa de compilación para usuarios finales.

## Por qué existe sIATC

El uso de IA en la escritura y en la producción de contenido está creciendo más rápido que las convenciones para declararlo. Declaraciones genéricas, como "se utilizó IA en la preparación de este texto", son demasiado vagas. No muestran dónde entró la IA en el proceso, si moldeó el argumento, si ayudó con la estructura, si generó lenguaje, si tradujo, si verificó afirmaciones o si solo ayudó a pulir frases.

sIATC ofrece a autores, editores, investigadores, comunicadores, organizaciones y lectores una forma compartida y estructurada de describir cómo la IA interactuó con una pieza de contenido.

Fue diseñado para contenido, no solo para investigación.

El sIfA original fue desarrollado para apoyar la reflexión sobre la interacción humano/IA en la producción de conocimiento, especialmente en productos de investigación. Usa roles de contribución asociados a procesos de investigación. sIATC mantiene la idea central de reflexión y responsabilidad, pero adapta la terminología para la producción de contenidos al enfatizar responsabilidad intelectual y transparencia, en lugar de compañerismo o colaboración. Esta elección evita tratar los sistemas de IA como autores, herramientas, agentes morales o partes responsables. También cambia la unidad de análisis: sale la lógica de roles de contribución en investigación y entra la lógica de las etapas de producción de contenido escrito.

Ese cambio es relevante. Un artículo, informe, libro, post de LinkedIn, texto institucional, newsletter o ensayo de opinión puede involucrar investigación, pero también involucra decisiones editoriales que no encajan plenamente en taxonomías de investigación. La autoría puede necesitar reflexionar sobre cómo la IA ayudó a definir el enfoque, organizar la secuencia, redactar fragmentos, refinar el tono, traducir, verificar datos o crear elementos visuales. Estas son formas distintas de participación y no deberían reducirse a una única nota genérica.

sIATC es, por lo tanto, una herramienta de autoevaluación. No es una herramienta de auditoría. No certifica la calidad, veracidad, autoría, originalidad ni condición ética de un contenido. Invita a la autoría a detenerse, reflexionar, documentar y declarar.

La autoría humana permanece responsable del resultado final.

## Relación con el sIfA original

sIATC es una derivación modificada de:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

El sIfA original se distribuye bajo la licencia Apache 2.0. sIATC preserva la atribución a Mareike Schomerus / Busara y mantiene las obligaciones de licencia exigidas para redistribución y modificación.

### Qué conserva sIATC del sIfA

sIATC conserva la lógica reflexiva central de la herramienta original:

- el uso de IA se declara por etapas definidas, en lugar de quedar oculto en una nota genérica;
- la autoría registra la extensión de la interacción con IA en una escala simple de 0/1/2;
- la herramienta produce una figura visual que hace reconocible rápidamente la interacción humano/IA;
- la herramienta produce datos estructurados y legibles por máquina;
- la figura mantiene la metáfora visual del cerebro humano: el campo naranja representa la autoría humana, mientras que el centro morado representa la interacción con IA;
- la responsabilidad humana permanece explícita;
- la herramienta se distribuye como un único archivo HTML, que puede ejecutarse localmente en el navegador;
- el arte original de la figura del cerebro se reutiliza bajo la licencia Apache 2.0.

### Qué cambia sIATC

sIATC cambia el dominio de aplicación, la taxonomía y el flujo.

El sIfA original fue diseñado principalmente para investigación y producción de conocimiento, con la taxonomía CRediT como referencia importante. sIATC fue diseñado específicamente para creación de contenido.

Los principales cambios son:

- la taxonomía CRediT de 14 roles de contribución en investigación se sustituye por una taxonomía de nueve etapas de contenido escrito;
- se eliminan los roles específicos de investigación;
- el foco pasa de la atribución de contribución en investigación a la autoevaluación del proceso de creación de contenido;
- el flujo se simplifica para autoría única o autoría responsable;
- cada etapa de contenido puede marcarse como "no aplica" cuando no ocurrió;
- la herramienta se enmarca para artículos, informes, posts, ensayos, newsletters, libros, capítulos, textos institucionales, guiones, presentaciones y otros formatos editoriales;
- la declaración enfatiza cómo la IA interactuó con la creación del contenido, no cómo contribuyó a un proyecto de investigación.

sIATC, por lo tanto, no sustituye a sIfA. Es una adaptación para otro caso de uso.

Use sIfA cuando el objeto principal sea un producto de investigación y la estructura de contribución tipo CRediT sea adecuada. Use sIATC cuando el objeto principal sea contenido escrito y la pregunta relevante sea cómo la IA interactuó con las etapas de producción de ese contenido.

## Índice

- [Para autores y creadores de contenido](#para-autores-y-creadores-de-contenido)
  - [Inicio rápido](#inicio-rápido)
  - [Cómo está estructurada la herramienta](#cómo-está-estructurada-la-herramienta)
  - [Las nueve etapas de contenido](#las-nueve-etapas-de-contenido)
  - [Escala de extensión de uso de IA](#escala-de-extensión-de-uso-de-ia)
  - [Cómo evaluar la extensión del uso de IA](#cómo-evaluar-la-extensión-del-uso-de-ia)
  - [Guardar y exportar](#guardar-y-exportar)
  - [Ejemplo práctico](#ejemplo-práctico)
  - [Qué no se envía a ningún lugar](#qué-no-se-envía-a-ningún-lugar)
  - [Texto sugerido de declaración](#texto-sugerido-de-declaración)
- [Para editores, publicadores y organizaciones](#para-editores-publicadores-y-organizaciones)
  - [Cuándo solicitar un sIATC](#cuándo-solicitar-un-sIATC)
  - [Cómo leer una figura sIATC](#cómo-leer-una-figura-sIATC)
  - [Qué puede y no puede probar sIATC](#qué-puede-y-no-puede-probar-sIATC)
- [Para desarrolladores](#para-desarrolladores)
  - [Estructura del repositorio](#estructura-del-repositorio)
  - [Ejecutar y editar](#ejecutar-y-editar)
  - [Arquitectura en un párrafo](#arquitectura-en-un-párrafo)
  - [Modelo de estado](#modelo-de-estado)
  - [Cambiar las etapas de contenido](#cambiar-las-etapas-de-contenido)
  - [Build y uso offline](#build-y-uso-offline)
  - [Limitaciones conocidas](#limitaciones-conocidas)
- [Citación y atribución](#citación-y-atribución)
  - [Cómo citar sIATC](#cómo-citar-sIATC)
  - [Cómo citar el sIfA original](#cómo-citar-el-sifa-original)
  - [Aviso de obra derivada](#aviso-de-obra-derivada)
- [Licencia](#licencia)
- [Agradecimientos](#agradecimientos)

## Para autores y creadores de contenido

### Inicio rápido

1. Descargue la versión más reciente del archivo `sIATC_vX.X.html` desde la página de [Releases](../../releases).
2. Abra el archivo en cualquier navegador moderno haciendo doble clic. Chrome, Edge, Safari, Firefox y otros navegadores modernos deberían funcionar.
3. Ingrese el título o descripción de la pieza de contenido.
4. Ingrese el nombre de la autoría, si lo desea.
5. Para cada etapa de contenido, elija uno de los tres niveles de uso de IA:
   - 0 = ninguno
   - 1 = algo
   - 2 = extenso
6. Marque una etapa como "no aplica" cuando no haya ocurrido en el proceso de producción.
7. Agregue la herramienta o servicio de IA utilizado, cuando corresponda.
8. Agregue una nota breve explicando cómo se usó la IA.
9. Exporte la figura como SVG o PNG, o exporte los datos como un archivo `.sIATC.json`.

Ese es todo el flujo. La herramienta es una única página HTML. No hay instalación, cuenta, carga de archivos ni servidor.

### Cómo está estructurada la herramienta

La interfaz es una única página con cuatro partes principales:

- **Campos de metadatos** para el título del contenido y la autoría.
- **Una evaluación etapa por etapa** que cubre las nueve etapas de producción de contenido escrito.
- **Una figura con forma de cerebro** que muestra el grado de interacción con IA en las etapas activas.
- **Botones de exportación** para descargar la figura o exportar los datos estructurados.

La figura se llena desde el centro hacia afuera a medida que aumenta la participación de la IA. El cerebro naranja representa la autoría humana. El centro morado representa la interacción con IA. Cada eje corresponde a una etapa de contenido. Cuanto más avanza la forma morada en una etapa, mayor es la participación declarada de la IA en esa parte del proceso.

Las etapas marcadas como "no aplica" se excluyen de la figura.

La herramienta también incluye una declaración de responsabilidad:

> Después de usar cualquier herramienta o servicio, la autoría revisó y editó el contenido según fuera necesario y asume plena responsabilidad por el contenido de la publicación.

Esta declaración puede adaptarse según el contexto de publicación, pero el principio debe permanecer: la autoría humana es responsable del contenido final.

### Las nueve etapas de contenido

sIATC usa una taxonomía de nueve etapas para contenido escrito. La taxonomía no pretende describir todo proceso editorial con precisión perfecta. Es una estructura práctica para reflexión, declaración y comparación.

| Etapa | Qué significa | Ejemplos de interacción con IA |
| --- | --- | --- |
| **Concepción y Enfoque** | La idea central, el enfoque y el mensaje del contenido: de qué trata la pieza y por qué vale la pena producirla. | Explorar enfoques o ganchos; probar un argumento; generar opciones de encuadre; afinar el mensaje principal. |
| **Investigación y Fuentes** | Los hechos, referencias, ejemplos y materiales de base en los que se apoya el contenido. | Resumir lecturas; encontrar datos o citas de apoyo; reunir material previo; mapear lo que ya se ha dicho. |
| **Estructura** | Guion, secuencia, lógica de secciones y flujo narrativo. | Esbozar o reordenar un guion; proponer un arco narrativo; probar si el flujo funciona; adaptar la estructura a un formato. |
| **Redacción** | Producir texto original: transformar idea y guion en prosa. | Generar un primer borrador a partir de un briefing; redactar secciones; expandir notas en prosa; producir formulaciones alternativas. |
| **Edición y Refinamiento** | Trabajo de lenguaje, tono, claridad, concisión y voz. | Editar para dar claridad; adaptar tono; reescribir pasajes poco claros; ajustar al tamaño adecuado. |
| **Revisión** | Reformulación sustantiva del contenido o argumento después de feedback, relectura o nueva evaluación. | Incorporar comentarios; reformular argumentos; conciliar feedbacks; decidir qué cortar, ampliar o reorganizar. |
| **Traducción** | Verter el contenido a otro idioma, incluyendo localización y consistencia terminológica. | Refinar traducción automática; adaptar expresiones idiomáticas y referencias culturales; aplicar glosario; hacer retrotraducción para verificar fidelidad. |
| **Verificación de Datos** | Confirmar que afirmaciones, números, citas, nombres, fechas y fuentes son correctos. | Verificar hechos sugeridos por IA contra fuentes; revisar atribuciones; señalar posibles alucinaciones; revisar sesgos. |
| **Imágenes y Diseño** | La capa visual que apoya o presenta el contenido. | Generar o buscar imágenes; esbozar layouts; crear gráficos o diagramas; adaptar visuales a una plataforma o formato. |

Una etapa puede marcarse como "no aplica" cuando no ocurrió. Por ejemplo, si el contenido no fue traducido, la etapa Traducción puede excluirse. Si no se produjo ningún elemento visual, Imágenes y Diseño puede excluirse.

### Escala de extensión de uso de IA

sIATC usa una escala de tres niveles para describir cuánto interactuó la IA con cada etapa.

| Extensión de IA | Significado | Interpretación típica |
| --- | --- | --- |
| **0 - Ninguno** | No se usó IA en esta etapa. | La etapa se realizó sin herramientas de IA. |
| **1 - Algo** | La IA asistió a la autoría, pero no condujo la etapa. | La IA ayudó con sugerencias, alternativas, resúmenes, correcciones o apoyo limitado. La autoría controló y produjo sustancialmente el resultado. |
| **2 - Extenso** | La IA tuvo un papel sustancial en la etapa. | La IA generó, transformó, estructuró, tradujo, analizó o moldeó materialmente el resultado, que luego fue revisado, editado, verificado y aceptado por la autoría. |

La escala 0/1/2 es intencionalmente simple. Fue diseñada para reflexión y comunicación, no para medición exacta. El objetivo es hacer visible la interacción con IA lo suficiente como para apoyar responsabilidad, aprendizaje, comparación y mejores prácticas de declaración.

### Cómo evaluar la extensión del uso de IA

La autoría debe usar su criterio al asignar un nivel. Las siguientes orientaciones pueden ayudar.

Use **0 - Ninguno** cuando:

- ninguna herramienta de IA fue usada en esa etapa;
- la IA fue usada en otra etapa, pero no en esa;
- la etapa no involucró material generado, asistido o transformado por IA.

Use **1 - Algo** cuando:

- la IA sugirió opciones, pero la autoría seleccionó, rechazó o reescribió sustancialmente;
- la IA ayudó con claridad, tono, gramática, concisión o formato;
- la IA resumió material que la autoría ya había seleccionado y verificado;
- la IA ayudó a explorar posibilidades, sin determinar la dirección final;
- la IA fue usada como interlocutora para prueba, crítica o revisión.

Use **2 - Extenso** cuando:

- la IA generó un primer borrador o fragmentos sustanciales;
- la IA produjo una traducción que se convirtió en la base de la versión final;
- la IA moldeó materialmente la estructura o el argumento;
- la IA sintetizó material de fuentes en contenido utilizable;
- la IA creó elementos visuales usados en el resultado final;
- la IA realizó una parte importante de la verificación, clasificación o revisión editorial, sujeta a revisión humana;
- el resultado final de esa etapa sería materialmente distinto sin la IA.

La autoría debe ser transparente sobre las incertidumbres. Cuando una etapa quede entre "algo" y "extenso", elija el nivel que mejor represente la dependencia de esa etapa respecto de la IA y explique la decisión en el campo de nota.

### Guardar y exportar

sIATC permite diferentes formas de exportación.

- **Descargar figura como SVG**: exporta la figura en formato vectorial escalable, adecuado para publicación, sitios web, repositorios y documentos.
- **Descargar figura como PNG**: exporta la figura como imagen, facilitando su uso en presentaciones, posts y plataformas que no manejan bien SVG.
- **Exportar datos como `.sIATC.json`**: exporta los datos estructurados de la evaluación, incluyendo metadatos del contenido, notas por etapa, herramientas de IA, explicaciones y fecha/hora.
- **Interacción local en el navegador**: la herramienta se ejecuta en el navegador. No hay servidor.

El archivo `.sIATC.json` exportado puede usarse como registro legible por máquina de la autoevaluación. La figura SVG o PNG puede adjuntarse al propio contenido, incluirse en un repositorio, agregarse como material suplementario o publicarse junto con la pieza.

### Ejemplo práctico

Un sIATC ficticio para un artículo largo sobre el efecto de la IA en la escritura profesional:

| Etapa | Extensión de IA | Herramienta / servicio | Cómo se usó la IA |
| --- | --- | --- | --- |
| Concepción y Enfoque | 1 | ChatGPT | Usada para probar posibles enfoques e identificar encuadres débiles. El enfoque final fue elegido por la autoría. |
| Investigación y Fuentes | 1 | Perplexity, Google Search, ChatGPT | Usadas para mapear debates relevantes e identificar fuentes posibles. Las fuentes fueron verificadas manualmente antes de su inclusión. |
| Estructura | 2 | Claude | Usada para proponer distintos guiones y reorganizar el argumento. La autoría seleccionó y modificó la estructura final. |
| Redacción | 0 | - | No se usó IA para generar el primer borrador. |
| Edición y Refinamiento | 1 | ChatGPT | Usada para identificar pasajes poco claros y sugerir formulaciones más concisas. La autoría reescribió manualmente. |
| Revisión | 1 | Claude | Usada para comparar comentarios de revisión con el borrador e identificar secciones que requerían ampliación. |
| Traducción | No aplica | - | El texto no fue traducido. |
| Verificación de Datos | 1 | ChatGPT, revisión manual de fuentes | Usada para señalar afirmaciones que requerían verificación manual. |
| Imágenes y Diseño | 2 | DALL-E, Canva | Usadas para generar conceptos visuales y adaptarlos al formato de publicación. |

En este ejemplo, la figura sIATC exportada mostraría ninguna interacción con IA en Redacción, ningún eje para Traducción si está marcada como no aplica, y una interacción más fuerte en Estructura e Imágenes y Diseño.

### Qué no se envía a ningún lugar

La herramienta se ejecuta completamente en el navegador. Nada es enviado por la herramienta a un servidor.

Específicamente:

- el título del contenido permanece en su computadora;
- el nombre de la autoría permanece en su computadora;
- las evaluaciones por etapa permanecen en su computadora;
- las herramientas y servicios listados permanecen en su computadora;
- las notas sobre cómo se usó la IA permanecen en su computadora;
- el archivo `.sIATC.json` exportado es suyo para guardar, publicar, adjuntar, archivar o eliminar.

La herramienta no ofrece analytics, rastreo de usuarios, cuentas, almacenamiento en la nube ni validación remota.

Si usa un servicio de IA de terceros durante la producción del contenido, ese servicio puede tener sus propias políticas de uso de datos. sIATC no controla esos servicios. sIATC solo registra su autoevaluación sobre cómo fueron usados.

### Texto sugerido de declaración

Una declaración breve puede ser:

> Este contenido incluye una declaración sIATC que documenta cómo herramientas de IA interactuaron con el proceso de producción. El uso de IA fue autoevaluado en las etapas de concepción, investigación, estructura, redacción, edición, revisión, traducción, verificación e imágenes. Después de usar cualquier herramienta o servicio, la autoría revisó y editó el contenido según fuera necesario y asume plena responsabilidad por la publicación final.

Una declaración más detallada puede ser:

> La autoría usó sIATC, Statement of Intellectual Fellowship and Accountability for Content, para documentar la interacción entre autoría humana y herramientas de IA durante la producción de este contenido. La evaluación registra la extensión del uso de IA en nueve etapas de creación de contenido: Concepción y Enfoque; Investigación y Fuentes; Estructura; Redacción; Edición y Refinamiento; Revisión; Traducción; Verificación de Datos; e Imágenes y Diseño. La figura sIATC y los datos estructurados se proporcionan como registro de transparencia. La autoría revisó, editó, verificó y aprobó el contenido final, permaneciendo plenamente responsable por él.

Una nota de repositorio puede ser:

> Este repositorio incluye la herramienta HTML sIATC y su documentación. sIATC es una derivación modificada del sIfA Tool, creado por Mareike Schomerus / Busara y distribuido bajo la licencia Apache 2.0. La adaptación sustituye la taxonomía CRediT de investigación por una taxonomía de nueve etapas para contenido escrito y simplifica el flujo para autoevaluación de contenido.

## Para editores, publicadores y organizaciones

### Cuándo solicitar un sIATC

Editores, publicadores, instituciones y organizaciones pueden solicitar un sIATC cuando quieran una declaración de uso de IA más estructurada que una nota genérica.

sIATC puede ser útil para:

- artículos;
- informes;
- artículos de opinión;
- libros y capítulos;
- ensayos;
- newsletters;
- textos institucionales;
- policy briefs;
- guiones;
- presentaciones;
- white papers;
- posts largos;
- piezas de comunicación científica;
- materiales de comunicación y marketing;
- contenido educativo.

Un sIATC es especialmente útil cuando el contenido se publica en un contexto en el que confianza, autoría, proceso intelectual, citación, precisión o responsabilidad importan.

### Cómo leer una figura sIATC

La figura sIATC es un resumen visual de la autoevaluación de la autoría.

- El cerebro naranja representa la autoría humana.
- El centro morado representa la interacción con IA.
- Cada eje representa una etapa de contenido.
- Una extensión morada mayor en un eje significa mayor participación declarada de la IA en esa etapa.
- Una etapa marcada como "no aplica" se excluye de la figura.
- La figura debe leerse junto con la tabla o los datos JSON cuando se necesite detalle.

La figura no es una nota de calidad. Una forma morada mayor no significa automáticamente que el contenido sea mejor o peor. Significa que la autoría declaró mayor interacción con IA en el proceso de producción.

### Qué puede y no puede probar sIATC

sIATC puede apoyar:

- una declaración más transparente del uso de IA;
- mejor reflexión por parte de la autoría;
- conversaciones editoriales más claras;
- registros legibles por máquina sobre interacción con IA;
- comparación entre distintas piezas de contenido;
- aprendizaje institucional sobre cómo se está usando la IA;
- declaraciones de responsabilidad más específicas.

sIATC no puede probar:

- que la autoría declaró todo;
- que no hubo uso no declarado de IA;
- que el contenido es preciso;
- que el contenido es original;
- que el contenido está libre de alucinaciones;
- que el contenido es éticamente aceptable;
- que se resolvieron cuestiones de derechos de autor y protección de datos;
- que el texto final cumple con estándares editoriales.

sIATC es una autoevaluación estructurada. Debe tratarse como una práctica de transparencia, no como auditoría forense ni sistema de certificación.

## Para desarrolladores

### Estructura del repositorio

Una estructura recomendada para el repositorio sIATC:

```text
.
├── sIATC_vX.X.html                    # Herramienta principal en HTML
├── README.md                          # Documentación del repositorio
├── LICENSE                            # Licencia Apache 2.0
├── NOTICE                             # Aviso de atribución, incluido el sIfA original
├── CHANGELOG.md                       # Historial de versiones
├── CONTRIBUTING.md                    # Directrices de contribución
├── CITATION.cff                       # Archivo de citación legible por máquina
├── HOW_TO_CITE.md                     # Textos sugeridos de citación y atribución
├── docs/
│   ├── SCHEMA.md                      # Descripción general del formato .sIATC.json
│   └── sIATC.schema.json              # JSON Schema para .sIATC.json, si se mantiene
├── examples/
│   ├── example.sIATC.json             # Ejemplo de datos de autoevaluación
│   └── example.svg                    # Ejemplo de figura exportada
└── .github/
    └── ISSUE_TEMPLATE/
```

La estructura exacta puede simplificarse. Como sIATC se distribuye como un único archivo HTML, el repositorio mínimo puede contener solo:

```text
.
├── sIATC_vX.X.html
├── README.md
├── LICENSE
└── NOTICE
```

Para reutilización pública, citación, rastreo de obra derivada y declaración legible por máquina, se recomienda la estructura más completa.

### Ejecutar y editar

No hay etapa de instalación para usuarios finales. Basta abrir el archivo HTML en un navegador.

Para desarrollo local:

```bash
# Opción 1: abrir el archivo directamente
open "sIATC_vX.X.html"

# Opción 2: servir el directorio localmente
python3 -m http.server 8000

# Luego acceder a
http://localhost:8000/sIATC_vX.X.html
```

La herramienta actual fue diseñada como una aplicación de navegador autocontenida. Puede editarse modificando HTML, CSS y JavaScript dentro del propio archivo.

Dependiendo de la versión, bibliotecas externas pueden cargarse desde un CDN o incorporarse directamente en el archivo. Si el uso offline es importante, distribuya una versión con todas las dependencias incorporadas.

### Arquitectura en un párrafo

sIATC es una aplicación de navegador de página única. Mantiene el estado de la autoevaluación en el navegador del usuario, renderiza la interfaz como tarjetas o secciones editables por etapa, y genera la figura sIATC como SVG. Las exportaciones se producen del lado del cliente, serializando el SVG o los datos estructurados en JSON para archivos descargables. No hay backend, sistema de login, base de datos ni almacenamiento remoto. La herramienta fue diseñada para portabilidad, transparencia y facilidad de redistribución.

### Modelo de estado

El estado principal puede entenderse como un objeto con metadatos sobre la pieza y una entrada por etapa de contenido.

Modelo conceptual simplificado:

```js
const sIATC = {
  version: "1.2",
  type: "sIATC-content-statement",
  created_at: "2026-01-01T00:00:00Z",
  piece: {
    title: "Título del contenido",
    author: "Nombre de la autoría"
  },
  stages: {
    conception: {
      label: "Conception & Angle",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para explorar posibles enfoques."
    },
    research: {
      label: "Research & Sourcing",
      applicable: true,
      extent: 1,
      tool: "Perplexity, Google Search",
      note: "Usado para identificar posibles fuentes, verificadas manualmente."
    },
    structure: {
      label: "Structure",
      applicable: true,
      extent: 2,
      tool: "Claude",
      note: "Usado para proponer y reorganizar guiones."
    },
    drafting: {
      label: "Drafting",
      applicable: true,
      extent: 0,
      tool: "",
      note: "No se usó IA en la redacción."
    },
    editing: {
      label: "Editing & Refinement",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para identificar pasajes poco claros."
    },
    revision: {
      label: "Revision",
      applicable: true,
      extent: 1,
      tool: "Claude",
      note: "Usado para comparar feedbacks con el borrador."
    },
    translation: {
      label: "Translation",
      applicable: false,
      extent: 0,
      tool: "",
      note: "No aplica."
    },
    verification: {
      label: "Fact-checking & Verification",
      applicable: true,
      extent: 1,
      tool: "ChatGPT",
      note: "Usado para señalar afirmaciones que exigían verificación manual."
    },
    visuals: {
      label: "Visuals & Design",
      applicable: true,
      extent: 2,
      tool: "DALL-E, Canva",
      note: "Usado para generar y adaptar conceptos visuales."
    }
  },
  accountability_statement: "Después de usar cualquier herramienta o servicio, la autoría revisó y editó el contenido según fuera necesario y asume plena responsabilidad por el contenido de la publicación.",
  derived_from: {
    name: "sIfA Tool - Statement of Intellectual Fellowship and Accountability",
    creator: "Mareike Schomerus / Busara",
    doi: "10.5281/zenodo.20285993",
    license: "Apache-2.0"
  }
};
```

La implementación real puede variar. El principio central es que el registro exportado debe preservar:

- el título o identificador del contenido;
- la autoría o parte responsable, cuando se informe;
- la taxonomía activa;
- la aplicabilidad de cada etapa;
- la extensión de uso de IA en cada etapa;
- la herramienta o servicio usado;
- la explicación de la autoría sobre cómo se usó la IA;
- la fecha/hora o versión, cuando esté disponible;
- la atribución derivada al sIfA original.

### Cambiar las etapas de contenido

La taxonomía predeterminada de sIATC contiene nueve etapas:

```js
const STAGES = [
  {
    id: "conception",
    label: "Conception & Angle",
    definition: "The core idea, angle and message."
  },
  {
    id: "research",
    label: "Research & Sourcing",
    definition: "The facts, references and examples the piece rests on."
  },
  {
    id: "structure",
    label: "Structure",
    definition: "Outline, sequence and narrative flow."
  },
  {
    id: "drafting",
    label: "Drafting",
    definition: "Producing the original text."
  },
  {
    id: "editing",
    label: "Editing & Refinement",
    definition: "Language, tone, clarity, concision and voice."
  },
  {
    id: "revision",
    label: "Revision",
    definition: "Substantive reworking of content and argument."
  },
  {
    id: "translation",
    label: "Translation",
    definition: "Rendering the piece into another language."
  },
  {
    id: "verification",
    label: "Fact-checking & Verification",
    definition: "Confirming claims, quotes, figures and sources."
  },
  {
    id: "visuals",
    label: "Visuals & Design",
    definition: "The visual layer that presents or supports the words."
  }
];
```

Los cambios en la taxonomía deben hacerse con cuidado. Una taxonomía estable facilita la comparación entre distintas declaraciones sIATC. Si una versión derivada cambia la taxonomía, debe:

- cambiar el nombre o la versión de la herramienta;
- documentar el cambio en el README;
- documentar el cambio en los comentarios del código fuente;
- preservar la atribución a sIfA si la derivación aún usa la estructura o los activos visuales originales;
- actualizar ejemplos y archivos de schema, cuando existan.

### Build y uso offline

sIATC fue pensado para redistribuirse fácilmente como un único archivo HTML.

Una versión pública puede incluir:

- una versión online que carga dependencias desde CDN;
- una versión offline que incorpora todas las dependencias en el HTML;
- archivos `.sIATC.json` de ejemplo;
- figuras exportadas de ejemplo;
- archivos de citación y atribución.

Si se usa un script de build offline, documéntelo en esta sección. Un script típico haría lo siguiente:

1. Leer el archivo principal `sIATC_vX.X.html`.
2. Descargar o leer desde caché las dependencias JavaScript.
3. Incorporar esas dependencias en el HTML.
4. Generar un archivo HTML offline autocontenido.
5. Preservar los comentarios de licencia y atribución en el archivo generado.

El archivo offline suele ser más grande, pero es más útil en ambientes de baja conectividad y para fines de archivo.

### Limitaciones conocidas

- sIATC se basa en autoevaluación. Depende de la reflexión honesta y cuidadosa de la autoría.
- La escala 0/1/2 es intencionalmente simple y no captura todos los matices de la interacción con IA.
- La figura es un resumen visual, no una medición precisa.
- La herramienta no verifica si la declaración está completa.
- La herramienta no verifica precisión factual.
- La herramienta no detecta plagio ni violaciones de derechos de autor.
- La herramienta no inspecciona prompts, logs, archivos ni outputs de IA, salvo cuando la autoría los registra manualmente.
- La herramienta no envía, almacena ni valida datos remotamente.
- El comportamiento de descarga puede variar entre navegadores, especialmente entre navegadores basados en Chromium, Safari y Firefox.
- Si bibliotecas externas se cargan desde CDN, puede ser necesario acceso a internet, salvo que se proporcione una versión offline.
- La taxonomía fue diseñada para contenido escrito. Proyectos altamente visuales, audiovisuales, de software, de datos o fuertemente orientados a investigación pueden requerir otra taxonomía o el uso del sIfA original.

## Citación y atribución

### Cómo citar sIATC

Cuando sIATC tenga su propio DOI, cite así:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. [Repository or publisher]. https://doi.org/[ADD-sIATC-DOI]

Hasta que se cree el DOI de sIATC, cite el repositorio GitHub y la etiqueta de versión:

> Ferreira, Luis. *sIATC - Statement of Intellectual Accountability and Transparency for Content.* Version X.X. 2026. GitHub. [ADD-REPOSITORY-URL]

Una versión legible por máquina de la misma información puede proporcionarse en `CITATION.cff`, usado por GitHub para completar el botón "Cite this repository".

### Cómo citar el sIfA original

Como sIATC es una derivación del sIfA original, el original también debe acreditarse:

> Schomerus, Mareike. *sIfA Tool (Tool to create a Statement of Intellectual Fellowship and Accountability).* Version 1.2. 2026. Busara. https://doi.org/10.5281/zenodo.20285993

### Aviso de obra derivada

Aviso sugerido:

> sIATC is a modified derivative of the sIfA Tool - Statement of Intellectual Fellowship and Accountability, created by Mareike Schomerus / Busara and released under the Apache License 2.0. sIATC replaces the CRediT research contributor-role taxonomy with a nine-stage taxonomy for written content and simplifies the flow for content self-assessment. The adaptation does not treat AI systems as authors, collaborators, moral agents, or responsible parties. The original brain-figure artwork is reused under the same license. sIATC additions are released under the Apache License 2.0.

Atribución breve sugerida:

> Based on the sIfA Tool by Mareike Schomerus / Busara, Apache License 2.0, DOI: 10.5281/zenodo.20285993.

Leyenda sugerida para figura:

> sIATC figure generated with the Statement of Intellectual Fellowship and Accountability for Content, a derivative of the sIfA Tool by Mareike Schomerus / Busara, released under Apache 2.0.

## Licencia

Distribuido bajo la **Apache License 2.0**. Consulte `LICENSE` para el texto completo de la licencia y `NOTICE` para los avisos de atribución que acompañan redistribuciones.

En resumen, puede usar, modificar y distribuir sIATC libremente, incluso en contextos comerciales, siempre que:

- incluya una copia de la Apache License 2.0 en cualquier redistribución;
- preserve avisos de copyright, patente, marca y atribución;
- preserve el contenido relevante del archivo `NOTICE`;
- indique claramente los archivos modificados;
- mantenga la atribución al sIfA original cuando material original o estructura derivada sigan presentes.

El sIfA original es copyright © 2026 Mareike Schomerus / Busara y está licenciado bajo la Apache License 2.0.

Los añadidos de sIATC son copyright © 2026 Luis Ferreira y están licenciados bajo la Apache License 2.0.

El software se proporciona "TAL CUAL", sin garantías ni condiciones de ningún tipo, expresas o implícitas.

## Agradecimientos

sIATC se basa en el sIfA Tool - Statement of Intellectual Fellowship and Accountability, creado por Mareike Schomerus / Busara. sIATC preserva la atribución y el linaje derivado, pero adopta un encuadre específico para contenidos, centrado en responsabilidad intelectual y transparencia.

El sIfA original introdujo una forma práctica y visual de reflexionar sobre cómo humanos e IA interactúan en la producción de conocimiento. sIATC adapta esa idea para contenido escrito y producción editorial.

Un agradecimiento especial a Mareike Schomerus / Busara por distribuir la herramienta original bajo una licencia open-source, haciendo posible el desarrollo de obras derivadas.

sIATC también reconoce a la comunidad más amplia que trabaja con transparencia en IA, uso responsable de IA, declaración de autoría, ética editorial, declaraciones de responsabilidad legibles por máquina y práctica reflexiva en la producción de conocimiento y contenido.
