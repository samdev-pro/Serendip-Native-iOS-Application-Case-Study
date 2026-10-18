# Serendip — Native iOS Application Case Study

**Swift · SwiftUI · MVVM · Supabase · PostgreSQL · External API Integration**

> **Portfolio case study — not an open-source release.** This repository documents selected engineering and design work. Application source code, internal data structures, proprietary functionality, and commercial plans are intentionally excluded.

## 🧭 Overview

Serendip is a native iOS application for organizing a personal book library and discovering books to read. I began the project to solve problems I experienced firsthand: remembering books I had read or wanted to read, and finding a straightforward alternative to cluttered book-management interfaces.

I took the project from initial UX concepts through implementation of a working MVP, combining native iOS development with backend services and third-party book metadata integration.

**Project status:** Working MVP; further development and validation are ongoing.

**Project milestone:** Presented the MVP to a prospective partner, demonstrating the application and discussing its core experience. This presentation does not imply a formal partnership.

<!-- SCREENSHOT NOTE: Place one polished, CURRENT MVP screenshot immediately below this paragraph. Prefer the Library screen with real book covers, clear hierarchy, and no personal/account data. Use a screenshot from the running iOS app, not an early Adobe XD mockup. Replace the placeholder path once exported. -->
 <img src="./screenshots/mvp-intro-iphone.jpg" alt="Intro screen" width="300">

## 👨‍💻 My Role

I am responsible for the product's design and development, including:

- Defining application requirements and user workflows
- Designing the interface and interaction patterns
- Developing native iOS functionality with Swift and SwiftUI
- Organizing presentation and application logic using MVVM principles
- Integrating backend persistence and external book metadata services
- Debugging, testing, and refining the MVP

I use AI-assisted development tools as part of my workflow, alongside direct design, implementation review, troubleshooting, and validation. The case study describes my actual contributions rather than implying that every line of code was written without assistance.

## 🛠️ Technology & Tools

| Area | Technologies / approach |
| --- | --- |
| iOS application | Swift, SwiftUI |
| Application structure | MVVM |
| Backend and persistence | Supabase, PostgreSQL |
| Book metadata | Google Books API |
| Design | Adobe XD; iterative UI refinement |
| Development workflow | Xcode, Git/GitHub, Cursor, ChatGPT |

The technologies above describe the project's stack, not a claim of equal independent proficiency in each tool.

## 📱 Selected Application Screens

These examples show a small portion of the implemented experience. The intent is to demonstrate application quality and engineering scope without documenting the full product.

### Library

<!-- IMAGE PRESENTATION NOTE: Consider placing this and the other screenshots inside matching, straight-on iPhone frames. Use the same frame, scale, and padding for each; avoid perspective or decorative backgrounds. Keep screen contents readable. Replace the existing PNG assets with framed exports using the SAME filenames, or update paths below. Do not add a fake status bar or crop functional content. -->
<!-- SCREENSHOT NOTE: Insert CURRENT MVP Library screenshot here. Choose either the All Books or Shelves view—whichever best shows populated data, readable controls, and visual consistency. Avoid showing both if they reveal unnecessary product details. -->

<img src="./screenshots/mvp-library-iphone.png" alt="Library All Books screen" width="300">

A book-centered interface designed to make a personal collection easy to browse and manage.

### Add a Book via Search

<!-- SCREENSHOT NOTE: Insert CURRENT MVP book-search or add-book screen here. Prefer a neutral search result and the clearest example of a working data-driven flow. Avoid revealing unreleased capture features or internal diagnostic overlays. -->

<img src="./screenshots/mvp-add-book-iphone.png" alt="Add Book screen" width="300">

An input workflow that prioritizes clear actions and avoids unnecessary steps. This is one of several methods of entry.

### Book Detail

<!-- SCREENSHOT NOTE: Insert CURRENT MVP Book Detail screenshot here, ideally showing basic metadata and an ordinary reading-status control. Crop out any private account information or unpublished functionality. -->

<img src="./screenshots/mvp-book-iphone.png" alt="Individual Book screen" width="300">

A focused detail view that presents book information and relevant library actions.

### Discover (Optional)

<!-- SCREENSHOT NOTE: Include this fourth screenshot ONLY if the current Discover screen is implemented, representative of the MVP, and you are comfortable making it public. Otherwise OMIT this entire subsection. Do not publish proprietary recommendation logic or unreleased workflows. -->

<img src="./screenshots/mvp-discover-iphone.png" alt="Discover screen" width="300">

A browsing experience emphasizing visual clarity and ease of exploration.

## 🏗️ Engineering Approach

### Native, State-Driven Interfaces

I used SwiftUI to develop a native interface where visible content responds to application state. The goal was to keep interactions predictable and minimize redundant navigation while maintaining a consistent experience across views.

### Separation of Concerns

The application follows MVVM principles to organize presentation, state, and data-related responsibilities. This supports clearer reasoning about UI behavior and makes ongoing changes easier to manage.

### Data Integration & Persistence

The MVP combines externally sourced book metadata with application-managed library information, using Supabase and PostgreSQL for backend services and persistence. This required coordinating user-facing workflows with asynchronous data operations and persisted application state.

<!-- EDITOR NOTE: Confirm the precise responsibilities of each layer and the persistence behavior against the current Xcode project before publication. Avoid claims about caching, offline support, synchronization guarantees, security hardening, or production-scale performance unless verified. -->

## ⚙️ Engineering Decisions & Tradeoffs

### 1. Simplifying Common User Actions

**Problem:** Existing book tracking apps felt unnecessarily complex for routine tasks such as finding and saving a book.

**Approach:** Prioritize direct, clearly labeled actions and consistent interface patterns instead of adding steps for their own sake.

**Result:** A working MVP with a focused set of core library workflows that are easily accessible.

### 2. Architectural Decision: Organizing Application State with MVVM

**Context:** Multiple application views and user actions benefit from clearly defined responsibilities for presentation and state.

**Decision:** Apply SwiftUI’s declarative UI model and MVVM principles to separate presentation from application state and related responsibilities.

**Outcome:** An organizational approach intended to make UI behavior easier to reason about and refine as the MVP evolves.

### 3. Engineering Decision: Integrating External Book Data with Persistent User Records

**Context:** External book metadata and user-managed library records serve different purposes in the application.

**Decision:** Connect the external book metadata service with backend persistence while keeping the book-search and save experience straightforward.

**Outcome:** The MVP supports book search and management of saved personal library records.

<!-- EDITOR NOTE: Sections 2 and 3 are engineering decisions, NOT claims that these were bugs or difficult incidents. These are deliberately high-level descriptions. Before publishing, replace at least ONE with a specific, interview-defensible example from your actual implementation: the issue encountered, alternatives considered, your decision, and how you verified the outcome. Do not include source code, schemas, internal matching rules, or confidential algorithms. -->

## ✅ Verification & Current Status

The MVP has been developed to support account creation, book search, adding books to a personal library, updating reading status, and retrieving saved information in subsequent sessions.

<!-- VERIFICATION REQUIRED: You said you BELIEVE each workflow works end-to-end. Before making the statement above publicly, manually test the full sequence: create/sign in to an account -> search -> add -> change status -> fully close/relaunch -> sign back in if needed -> confirm the saved book/status persists. If any step fails, revise this section to state only what has been verified. -->

The MVP has also been demonstrated to a prospective partner. This is an active development project, not a claim of a publicly released production application. I am not presenting unmeasured performance, adoption, or reliability statistics as outcomes.

## 🎨 UX/UI Principles

- **Clarity:** Put the primary task ahead of decorative or distracting interface elements.
- **Consistency:** Reuse interaction and presentation patterns where appropriate.
- **Efficiency:** Reduce avoidable steps in common workflows.
- **Readability:** Use clear hierarchy, spacing, and legible book metadata.
- **Restraint:** Keep the interface focused rather than adding engagement mechanics unrelated to the task.

<!-- OPTIONAL SCREENSHOT NOTE: If the README feels too text-heavy, use a compact two-image comparison of CURRENT Library and Book Detail screens here. Avoid duplicating screenshots already shown above; usually the three primary screenshots are sufficient. -->

## 🎯 What This Project Demonstrates

- End-to-end ownership of an application project, from requirements and interface design through a working MVP
- Native iOS implementation using Swift and SwiftUI
- Application organization using MVVM principles
- Integration of external APIs and backend persistence
- Practical tradeoffs between interface simplicity and evolving requirements
- Iterative development, debugging, and review using contemporary development tools

## 🔒 Scope of This Case Study

This repository contains documentation and selected screenshots only. It does **not** include application source code, proprietary implementation details, database schemas, credentials, unreleased feature specifications, internal product analytics, or commercial strategy.

<!-- PUBLICATION CHECKLIST (remove or retain as an HTML comment):
[ ] Confirm all technical claims against the current codebase.
[ ] Run and verify the end-to-end workflow described above.
[ ] Replace all image placeholders with selected current screenshots.
[ ] Remove personal information, internal URLs, test credentials, and unreleased features from images.
[ ] Check repository history for accidentally committed sensitive files; deleting from the latest commit is not sufficient.
[ ] Confirm links and contact information are current.
[ ] Review the complete public repository as a stranger would see it.
-->

## 🔗 Other Work

- [Data Center QC Dashboard](https://github.com/samdev-pro/Data-Center-QC-Dashboard)
- [KPI Construction Bot](https://github.com/samdev-pro/KPI-Construction-Bot)

## 🤝 Contact

Interested in discussing iOS development, application engineering, or software development opportunities?

[Email](mailto:sam@samhuss.dev) · [LinkedIn](https://www.linkedin.com/in/samhuss/)
