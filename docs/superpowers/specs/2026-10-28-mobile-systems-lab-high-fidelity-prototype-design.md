# Mobile Systems Lab High-Fidelity Prototype Design

## Purpose

Raise the fidelity of the existing portfolio prototype so the owner can compare two plausible production directions before the information architecture is locked. The prototype remains throwaway code and answers one question: should the final portfolio use the technical credibility of Signal Console or the visual identity of Orbit Stack?

## Scope

Enhance variants A and C on the existing `prototype/mobile-systems-lab` route. Keep variant B unchanged as a comparison baseline. Continue using the existing `?variant=a|b|c` URL switcher and keyboard navigation.

The prototype uses realistic sample content. Any metric or achievement not supplied by the owner must be visibly marked as sample data so it cannot be mistaken for a professional claim.

## Shared Content Architecture

Both enhanced variants use the same content and section sequence so the owner can evaluate layout rather than copy differences:

1. Hero: name, Senior Mobile Engineer positioning, Flutter and Android focus, projects CTA, and contact CTA.
2. Credibility metrics: 5+ years plus clearly marked sample values for project count, releases, and ownership scope.
3. Three flagship projects: mobile mockup, context, ownership, technical decision, stack, and outcome.
4. Engineering approach: architecture, performance, reliability, and release workflow.
5. Experience timeline: employer, role, period, and impact summary.
6. Core stack: Flutter, Dart, Kotlin, Android SDK, state management, API/Firebase, testing, and CI/CD.
7. About: portrait placeholder, working style, mentoring, and technical leadership.
8. Contact: email placeholder, LinkedIn, GitHub, CV download, and availability.

## Variant A+: Signal Console

Signal Console communicates precision, technical depth, and production reliability.

- Use a graphite background with cyan/teal status accents.
- Use a 12-column desktop grid and a split hero: positioning on the left, realistic mobile-system dashboard on the right.
- Present projects as production case files with phone screens, operational metrics, an architecture path, stack, and impact.
- Use sans-serif display typography paired with monospace metadata.
- Use restrained status pulses, chart entry, and hover elevation. Motion must remain decorative and non-blocking.
- On mobile, stack the hero content before the system dashboard and reduce diagrams to readable vertical flows.

## Variant C+: Orbit Stack

Orbit Stack communicates a stronger personal visual identity while preserving technical credibility.

- Use a near-black background with electric-lime accents.
- Center the hero around a realistic phone mockup surrounded by API, state, testing, and release layers.
- Present each project as a large vertical “orbit” narrative rather than a repeated card grid.
- Use oversized typography and generous negative space.
- Use subtle orbit drift, layer reveal, and phone tilt. Motion must not interfere with reading or navigation.
- On mobile, convert orbit layers into labeled blocks below the phone and preserve the Problem → System → Surface → Impact sequence.

## Interaction

- The fixed prototype switcher remains visually separate from the proposed portfolio UI.
- `?variant=a`, `?variant=b`, and `?variant=c` remain reload-stable and shareable.
- Left and right arrow keys cycle variants unless an editable control has focus.
- Navigation links scroll to sections within the active variant.
- Project and contact links are non-destructive placeholders.

## Data and State

The prototype has no persistence or network dependency. A single in-memory sample content object supplies both A+ and C+ so their information density remains comparable. Variant B may keep its existing inline content because it is only the baseline.

## Validation

- `npm run prototype` serves the page locally.
- All three variant URLs load without console-breaking JavaScript errors.
- A+ and C+ contain all eight shared sections.
- Layout remains usable at desktop, tablet, and narrow mobile widths.
- Sample metrics are visibly identified.
- The floating switcher and keyboard navigation continue to work.

## Decision Gate

After previewing A+ and C+, the owner chooses one direction or specifies a hybrid using named parts. The issue remains open until that choice is recorded. The selected design decision feeds the later information-architecture ticket; the prototype branch is not merged directly into production.
