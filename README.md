# 🍼 MamaMinder Documentation & Theme System

Welcome to the official public documentation and architectural reference for the **MamaMinder** theme system and consolidated mobile application UI. 

This repository serves as the single public source of truth (Index Page) for the visual patterns, HSL palette specifications, and core component implementations used in the secure, high-performance newborn care companion application.

---

## 📖 Table of Contents

### 1. Core Source Code Reference
* **[📦 Consolidated Theme & UI Snapshot](./consolidated_theme_ui.md)**  
  A single, consolidated, fully-annotated reference file containing the production-ready source code for the entire theme provider context, HSL colors tokens, global stylesheet helpers, and all 6 primary tracker and analytics screens.

### 2. Design System Architecture
* **Theme Context Provider**: Dynamic hooks managing user preferences, system defaults, and persistent `AsyncStorage` states.
* **Harmonious HSL Palettes**: Elegant, soft palettes for active baby-care settings in both high-contrast light and dark modes.
* **WCAG AA Compliance**: Guaranteed color contrast ratios ($\ge 4.5:1$) for critical pediatric alerts, AI anomaly lists, and timer readouts.

---

## 🎨 Visual System & Color Palettes

MamaMinder's color system is crafted to feel calm, premium, and comforting for parents during both daytime and midnight nursing sessions.

| Token | Light Mode Value | Dark Mode Value | Description |
|---|---|---|---|
| `primary` | `#FFB7A4` (Soft Salmon) | `#FF8E8E` (Warm Rose) | Accents for feeding timers, bottles, and core CTAs. |
| `secondary` | `#E2D9E2` (Soft Lavender) | `#B39EB5` (Oxidized Lavender) | Used for sleep tracking and inactive states. |
| `accent` | `#FFC8B4` (Warm Peach) | `#E29E85` (Deep Peach) | Highlights, quick action floating sheets, and highlights. |
| `voiceMic` | `#7D52B3` (Oxford Purple) | `#7D52B3` (Oxford Purple) | AI voice assistants and nursery soundscape timers. |
| `background` | `#FAF8F5` (Warm Cream) | `#1A1F2C` (Midnight Onyx) | Screen background canvas. |

---

## 🛠️ Architectural Pillars

> [!NOTE]
> All screens are built using a **single source of truth** pattern. No ad-hoc, hardcoded hex values or inline layout styles bypass this system.

### 1. Universal Adaptability
All components utilize the centralized `useThemeStyles(getStyles)` pattern. When a user switches themes, or the device triggers system dark-mode, every card, button, and warning banner transitions smoothly.

### 2. Micro-Interactions & Haptics
All key logging buttons (diaper log pills, timers, quick-log tabs) are connected to native haptic generators (`expo-haptics`) providing soft tactile confirmation for one-handed nursing.

### 3. Accessible Alert System
Conditional components (such as Pediatric Hydration alerts or AI Anomaly blocks) utilize soft, high-contrast semi-translucent container overlays that ensure complete legibility regardless of screen brightness.
