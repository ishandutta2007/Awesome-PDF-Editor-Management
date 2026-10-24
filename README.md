# Awesome-PDF-Editor-Management

# Awesome-PDF-Editor-Management

## Top PDF Editor & Management Tools Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Self-Hosted Toolkits, Browser-Local Editing & Page-Level Management*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **PDF Editor & Management Tools**. These tools handle the practical work around PDFs — merging, splitting, compressing, annotating, signing, OCR-ing, and organizing pages — with a spectrum running from polished commercial suites to self-hosted web toolkits and browser-local editors that never upload your files.

**Examples** include Stirling-PDF, PDFsam Basic, PdfDing, LibreOffice Draw, and Xournal++ (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, privacy-preserving local processing, and transparent file handling — ideal for teams handling contracts, invoices, or sensitive documents that shouldn't leave the building just to get split in half.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Acrobat Pro** — **The reference commercial PDF editor.** Full editing, OCR, form creation, redaction, and e-signatures. **Standard at $12.99/month or $155.88 annually**; **Pro at $19.99/month**. **Trade-offs**: resource-heavy background processes, subscription lock-in, and cloud dependency for many features. **Best for enterprises standardized on Adobe** needing the most complete editing toolchain.

- **Foxit PDF Editor** — Commercial PDF editor with fast rendering, annotation, and form tools. Free Reader available; paid Editor for full editing. **Best for Windows users** wanting Adobe compatibility without Adobe's resource footprint.

- **PDF-XChange Editor** — Windows-focused PDF editor with strong annotation, OCR, and optimization tools. **One-time purchase** or subscription options. **Best for Windows power users** wanting deep feature sets without Adobe's pricing.

- **Smallpdf / PDF Candy / Sejda** — Browser-based utility suites for merge, split, compress, and convert. **Free tiers with task limits**; subscriptions for unlimited use. **Trade-offs**: uploads documents to their servers — unsuitable for confidential material. **Best for quick one-off tasks** on non-sensitive files.

## Open-Source GitHub Projects

- **Stirling-PDF** — **The most comprehensive self-hosted PDF toolkit on GitHub.** Open-core licensed, **50+ tools in one Docker container**: merge, split, rotate, reorganize, compress, repair, OCR, convert to/from images, Word, PowerPoint, HTML, Markdown, and CSV, add/remove passwords, watermark, certify/sign, redact, flatten, extract images, and compare two PDFs [citation:2]. **v2.12.0** introduced a JPDFium enhancement for merge and split that reduces memory consumption by up to **99%**, folder-based file storage with a "my files" UI, and desktop multi-window support [citation:3]. **Privacy by architecture**: files exist only client-side, in server memory during task execution, or temporarily on disk — downloaded files are deleted from the server [citation:2]. **Deployment**: `docker run -p 8080:8080 docker.stirlingpdf.com/stirlingtools/stirling-pdf` with **2 GB RAM minimum, 4 GB recommended** [citation:2]. **Desktop clients** are available for Windows, macOS, and Linux that package the web app and a local server into one native app [citation:2]. **Licensing**: free for individuals and teams up to 5 users; commercial license required for larger organizations. **Best for teams wanting a private, self-hosted Acrobat replacement** with the broadest tool coverage in one place.

- **PDFsam Basic** — **The free, open-source desktop tool for page-level PDF management.** AGPL-3.0 licensed, **cross-platform** on Windows, macOS, and Linux [citation:6]. **Core operations**: **Merge** (with page selection, bookmark handling, and AcroForm merging), **Split** (by predefined pages, specific pages, size, or bookmark level), **Mix** (alternate pages from two files), **Rotate** (90/180/270 degrees), and **Extract pages** [citation:6]. **Works entirely offline** — no internet connection required, no file uploads, no watermarks, and no limits on file size [citation:6]. **Since 2006** — mature and stable. **The honest limitation**: **it does not edit text or images inside pages** — PDFsam sells separate commercial editor tiers for that . **Best for desktop users** wanting reliable merge/split/rotate/extract operations without a web service or Docker deployment.

- **PdfDing** — **The self-hosted PDF management and annotation tool.** Docker-deployable, with **cross-device browser-based reading**, **memory of reading position**, **multi-level tags, favorites, and archiving**, **annotation, highlighting, and drawing**, **export of highlights and comments**, **dark mode and custom themes**, **SSO via OIDC**, **share links with access controls**, and **reading progress bars** . **More document shelf/reader than arbitrary content editor** — it manages your PDF library and annotation layer rather than rewriting existing text . **Best for individuals and teams** wanting a personal PDF library with reading management and light annotation, not a full Acrobat replacement.

- **LibreOffice Draw** — **The free desktop PDF editor bundled with LibreOffice.** **Opens foreign PDFs as graphical documents** — text and images become selectable snippets (Shape Text frames) rather than continuous text [citation:2][citation:4]. **Editing works best on simpler documents**: you can replace images, edit text line-by-line, add text boxes, annotate, sign, and manage pages (resize, rotate, delete, duplicate, add) [citation:4]. **Tight integration with other LibreOffice apps** lets you copy charts and diagrams directly into the PDF [citation:11]. **The honest limitations**: **complex layouts may require manual cleanup** — text reflow can break when replacing multiple lines; **no built-in merge or split**; **no PDF compression or conversion to Word** [citation:4]. **Best for quick fixes and simple edits** where you already have LibreOffice installed, accepting that it is not a purpose-built PDF editor.

- **Xournal++** — **The handwriting-first PDF annotation tool.** GPL-licensed, **cross-platform** on Linux, macOS, and Windows [citation:5]. **Pen input support** with pressure-sensitive styluses, **annotate on top of PDFs**, **select text from the background PDF and copy/highlight/underline/strikethrough**, **follow links from the background PDF**, **sidebar with page previews, bookmarks, and layers**, and **export to SVG, PNG, and PDF** [citation:5]. **Best for tablet users annotating documents** with a stylus — not a text editor, but an excellent annotation layer.

### Additional Strong Open-Source Options

- **PDF Arranger** — **The simple page organizer.** Fork of PDF-Shuffler, allows reordering, merging, splitting, rotating, cropping, and deleting pages, plus editing metadata and adding blank or image pages [citation:2]. **You cannot edit existing content** — it's a page-level manipulation tool [citation:2]. **Best for quick page reorganization** before or after other editing.
- **Inkscape** — **The precision vector editor that opens PDFs.** Handles graphics-intensive PDFs better than LibreOffice Draw by converting them into editable vector objects, with a helpful PDF import dialog for missing fonts, gradients, and boundaries [citation:2]. **Lacks OCR, advanced security, and interactive PDF features** [citation:2]. **Best for design-level edits** to vector-heavy PDFs.
- **Apache PDFBox** — **The open-source Java library for PDF creation and manipulation.** Apache 2.0 licensed, with creation of new PDFs, manipulation of existing documents, text extraction, and command-line utilities [citation:13]. **Best for Java developers** embedding PDF generation or extraction into applications, not for end-user editing.
- **pdf-lib** — **The JavaScript library for creating and modifying PDFs.** MIT licensed, with add/remove/copy pages, draw text/images/vector paths, create/fill/flatten forms, embed fonts, and manage metadata [citation:9]. **Best for web developers** building browser-based PDF tools.

**Frameworks for building custom systems**: Combine **Stirling-PDF** for a self-hosted web UI covering 50+ operations with Docker deployment, **PDFsam Basic** for offline desktop page management, **PdfDing** for a personal PDF library with reading and annotation, **LibreOffice Draw** for quick desktop edits, and **Xournal++** for stylus annotation — to build a PDF editor and management stack tailored to your need for breadth versus simplicity, web versus desktop, and privacy requirements.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- PDF editing tools differ significantly in editing depth, deployment model, and privacy posture. **Stirling-PDF processes files server-side** (though deletes them after task completion) — suitable for self-hosted infrastructure you control, not for shared hosting [citation:2]. **PDFsam Basic works entirely offline** with no file uploads and no limits, but **cannot edit existing text or images** [citation:6]. **PdfDing is a management and annotation tool**, not a full PDF editor . **LibreOffice Draw's editing is limited on complex PDFs** — text reflow can break, and foreign PDFs become graphical snippets rather than editable text [citation:4]. **Xournal++ is for stylus annotation**, not text editing [citation:5]. **Browser-based SaaS tools upload documents to their servers** — unsuitable for confidential material.
- Self-hosted open-source solutions require proper resource allocation (Stirling-PDF needs 4 GB RAM for comfortable use), Docker deployment configuration, and awareness that OCR of large archives is CPU-intensive.

---

**Made for teams and individuals handling PDFs without handing them to a stranger's server.**
Let's make PDF editing and management more open, privacy-preserving, and self-hostable.
