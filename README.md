<div align="center">

<!-- Animated Typing Banner -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=42B883&center=true&vCenter=true&multiline=true&repeat=true&width=700&height=100&lines=Vue+Development+Assistant;Vue+3.5+%7C+Composition+API+%7C+Pinia+%7C+Nuxt+3;7+Agents+%7C+7+Skills+%7C+Claude+Code+Plugin" alt="Vue Development Assistant" />

<br/>

<!-- Badge Row 1: Status Badges -->
[![Version](https://img.shields.io/badge/Version-2.0.0-42B883?style=for-the-badge&logo=vuedotjs)](https://github.com/pluginagentmarketplace/custom-plugin-vue/releases)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-brightgreen?style=for-the-badge)](#)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-blueviolet?style=for-the-badge)](#)

<!-- Badge Row 2: Content Badges -->
[![Agents](https://img.shields.io/badge/Agents-7-42B883?style=flat-square&logo=vuedotjs)](#-agents)
[![Skills](https://img.shields.io/badge/Skills-7-35495E?style=flat-square&logo=vuedotjs)](#-skills)
[![Commands](https://img.shields.io/badge/Commands-4-green?style=flat-square&logo=terminal)](#-commands)
[![Vue](https://img.shields.io/badge/Vue-3.5-42B883?style=flat-square&logo=vuedotjs)](#)

<br/>

<!-- Quick CTA Row -->
[📦 **Install Now**](#-quick-start) · [🤖 **Explore Agents**](#-agents) · [📖 **Documentation**](#-documentation) · [⭐ **Star this repo**](https://github.com/pluginagentmarketplace/custom-plugin-vue)

---

### What is this?

> **Vue Development Assistant** is a production-grade Claude Code plugin with **7 specialized agents** and **7 skills** for modern Vue.js development covering Vue 3.5, Composition API, Pinia, Vue Router, Nuxt 3, Testing (Vitest), and TypeScript.

</div>

---

## 📑 Table of Contents

<details>
<summary>Click to expand</summary>

- [Quick Start](#-quick-start)
- [Features](#-features)
- [Agents](#-agents)
- [Skills](#-skills)
- [Commands](#-commands)
- [Learning Path](#-learning-path)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

</details>

---

## 🚀 Quick Start

### Prerequisites

- Claude Code CLI v2.0.27+
- Active Claude subscription
- Node.js 18+ (for Vue development)

### Installation (Choose One)

<details open>
<summary><strong>Option 1: From Marketplace (Recommended)</strong></summary>

```bash
# Step 1️⃣ Add the marketplace
/plugin add marketplace pluginagentmarketplace/custom-plugin-vue

# Step 2️⃣ Install the plugin
/plugin install vue-development-assistant@pluginagentmarketplace-vue

# Step 3️⃣ Restart Claude Code
# Close and reopen your terminal/IDE
```

</details>

<details>
<summary><strong>Option 2: Local Installation</strong></summary>

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-vue.git
cd custom-plugin-vue

# Load locally
/plugin load .

# Restart Claude Code
```

</details>

### ✅ Verify Installation

After restart, you should see these agents:

```
vue-development-assistant:01-vue-fundamentals
vue-development-assistant:02-vue-composition
vue-development-assistant:03-vue-pinia
vue-development-assistant:04-vue-router
vue-development-assistant:05-vue-nuxt
vue-development-assistant:06-vue-testing
vue-development-assistant:07-vue-typescript
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🖼️ **Vue 3.5 Fundamentals** | Components, directives, reactivity basics |
| 🔄 **Composition API** | `setup()`, composables, `ref`/`reactive` |
| 🍍 **Pinia State** | Modern state management with stores |
| 🛣️ **Vue Router** | Navigation, guards, dynamic routes |
| ⚡ **Nuxt 3** | SSR, file-based routing, modules |
| 🧪 **Testing** | Vitest, Vue Test Utils, component testing |
| 📘 **TypeScript** | Type-safe Vue with `defineComponent` |

---

## 🤖 Agents

### 7 Specialized Vue Agents

| # | Agent | Purpose | Bonded Skill |
|---|-------|---------|--------------|
| 1 | **01-vue-fundamentals** | Vue 3.5 core concepts: SFC, directives, lifecycle hooks, reactivity basics | `vue-fundamentals` |
| 2 | **02-vue-composition** | Composition API mastery: `setup()`, `ref`, `reactive`, composables, provide/inject | `vue-composition-api` |
| 3 | **03-vue-pinia** | Pinia state management: stores, getters, actions, plugins, SSR hydration | `vue-pinia` |
| 4 | **04-vue-router** | Vue Router 4: navigation guards, dynamic routing, lazy loading, scroll behavior | `vue-router` |
| 5 | **05-vue-nuxt** | Nuxt 3 framework: SSR/SSG, file-based routing, modules, deployment | `vue-nuxt` |
| 6 | **06-vue-testing** | Testing with Vitest & Vue Test Utils: unit, component, integration tests | `vue-testing` |
| 7 | **07-vue-typescript** | TypeScript in Vue: type inference, generics, `defineComponent`, strict typing | `vue-typescript` |

### Usage Example

```bash
# Ask a Vue fundamentals question
@vue-development-assistant:01-vue-fundamentals How do I create a reusable component?

# Get Composition API help
@vue-development-assistant:02-vue-composition Create a composable for form validation

# Pinia state management
@vue-development-assistant:03-vue-pinia Set up a user authentication store

# Vue Router navigation
@vue-development-assistant:04-vue-router Implement route guards for protected pages

# Nuxt 3 SSR
@vue-development-assistant:05-vue-nuxt Configure Nuxt for SEO optimization

# Testing
@vue-development-assistant:06-vue-testing Write tests for a login component

# TypeScript
@vue-development-assistant:07-vue-typescript Type a complex Pinia store
```

---

## 🛠️ Skills

### Available Skills (Golden Format ✨)

All skills follow the **Golden Format** with real content:
- `assets/` - config.yaml, schema.json
- `scripts/` - validate.py
- `references/` - GUIDE.md, PATTERNS.md

| Skill | Description | Invoke |
|-------|-------------|--------|
| `vue-fundamentals` | Core Vue 3.5 concepts, SFC syntax, reactivity, lifecycle | `Skill("vue-development-assistant:vue-fundamentals")` |
| `vue-composition-api` | Composition API patterns, composables, `ref`/`reactive` | `Skill("vue-development-assistant:vue-composition-api")` |
| `vue-pinia` | Pinia stores, state management, plugins, devtools | `Skill("vue-development-assistant:vue-pinia")` |
| `vue-router` | Routing, navigation guards, meta fields, transitions | `Skill("vue-development-assistant:vue-router")` |
| `vue-nuxt` | Nuxt 3 SSR/SSG, auto-imports, modules, deployment | `Skill("vue-development-assistant:vue-nuxt")` |
| `vue-testing` | Vitest, Vue Test Utils, mocking, snapshot tests | `Skill("vue-development-assistant:vue-testing")` |
| `vue-typescript` | TypeScript integration, type inference, generic components | `Skill("vue-development-assistant:vue-typescript")` |

---

## ⌨️ Commands

| Command | Description |
|---------|-------------|
| `/explore-roadmap` | Explore Vue.js learning roadmap interactively |
| `/learning-path` | Get personalized Vue learning path based on your level |
| `/skill-assessment` | Assess your Vue.js skills and identify gaps |
| `/career-guidance` | Vue.js career development and guidance |

---

## 📚 Learning Path

### Recommended Progression

```
🟢 Beginner
└── 01-vue-fundamentals → Components, Directives, Reactivity Basics
    │
    ▼
🟡 Intermediate
├── 02-vue-composition → Composition API, Composables
├── 03-vue-pinia → State Management
└── 04-vue-router → Navigation & Routing
    │
    ▼
🔴 Advanced
├── 05-vue-nuxt → SSR/SSG with Nuxt 3
├── 06-vue-testing → Comprehensive Testing
└── 07-vue-typescript → Type-Safe Vue Development
```

### Estimated Learning Time

| Module | Hours | Difficulty |
|--------|-------|------------|
| Vue Fundamentals | 8h | 🟢 Beginner |
| Composition API | 6h | 🟡 Intermediate |
| Pinia | 4h | 🟡 Intermediate |
| Vue Router | 4h | 🟡 Intermediate |
| Nuxt 3 | 10h | 🔴 Advanced |
| Testing | 8h | 🔴 Advanced |
| TypeScript | 10h | 🔴 Advanced |
| **Total** | **50h** | - |

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [ARCHITECTURE.md](ARCHITECTURE.md) | Plugin architecture and design |
| [LEARNING-PATH.md](LEARNING-PATH.md) | Detailed learning progression |
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [LICENSE](LICENSE) | License information |

---

## 📁 Project Structure

<details>
<summary>Click to expand</summary>

```
custom-plugin-vue/
├── 📁 .claude-plugin/
│   ├── plugin.json          # Plugin manifest
│   └── marketplace.json     # Marketplace config
├── 📁 agents/               # 7 Vue-specialized agents
│   ├── 01-vue-fundamentals.md
│   ├── 02-vue-composition.md
│   ├── 03-vue-pinia.md
│   ├── 04-vue-router.md
│   ├── 05-vue-nuxt.md
│   ├── 06-vue-testing.md
│   └── 07-vue-typescript.md
├── 📁 skills/               # 7 skills (Golden Format)
│   ├── vue-fundamentals/
│   │   ├── SKILL.md
│   │   ├── assets/          # config.yaml, schema.json
│   │   ├── scripts/         # validate.py
│   │   └── references/      # GUIDE.md, PATTERNS.md
│   ├── vue-composition-api/
│   ├── vue-pinia/
│   ├── vue-router/
│   ├── vue-nuxt/
│   ├── vue-testing/
│   └── vue-typescript/
├── 📁 commands/             # 4 slash commands
│   ├── explore-roadmap.md
│   ├── learning-path.md
│   ├── skill-assessment.md
│   └── career-guidance.md
├── 📁 hooks/
│   └── hooks.json           # 8 intelligent hooks
├── 📄 README.md
├── 📄 ARCHITECTURE.md
├── 📄 LEARNING-PATH.md
├── 📄 CHANGELOG.md
├── 📄 CONTRIBUTING.md
└── 📄 LICENSE
```

</details>

---

## 🔧 Tech Stack Coverage

| Technology | Version | Coverage |
|------------|---------|----------|
| Vue.js | 3.5+ | ⭐⭐⭐⭐⭐ |
| Composition API | 3.x | ⭐⭐⭐⭐⭐ |
| Pinia | 2.x | ⭐⭐⭐⭐⭐ |
| Vue Router | 4.x | ⭐⭐⭐⭐⭐ |
| Nuxt | 3.x | ⭐⭐⭐⭐⭐ |
| Vitest | 1.x | ⭐⭐⭐⭐ |
| TypeScript | 5.x | ⭐⭐⭐⭐⭐ |

---

## 📅 Metadata

| Field | Value |
|-------|-------|
| **Plugin Name** | vue-development-assistant |
| **Version** | 2.0.0 |
| **Last Updated** | 2025-01 |
| **Status** | Production Ready |
| **SASMP** | v1.3.0 |
| **EQHM** | Enabled |
| **Agents** | 7 |
| **Skills** | 7 (Golden Format) |
| **Commands** | 4 |
| **Hooks** | 8 |
| **Est. Learning** | 50 hours |

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

1. Fork the repository
2. Create your feature branch
3. Follow the Golden Format for new skills
4. Ensure SASMP v1.3.0 compliance
5. Submit a pull request

---

## ⚠️ Security

> **Important:** This repository contains third-party code and dependencies.
>
> - ✅ Always review code before using in production
> - ✅ Check dependencies for known vulnerabilities
> - ✅ Follow security best practices
> - ✅ Report security issues privately via [Issues](../../issues)

---

## 📝 License

Copyright © 2025 **Dr. Umit Kacar** & **Muhsin Elcicek**

Custom License - See [LICENSE](LICENSE) for details.

---

## 👥 Contributors

<table>
<tr>
<td align="center">
<strong>Dr. Umit Kacar</strong><br/>
Senior AI Researcher & Engineer
</td>
<td align="center">
<strong>Muhsin Elcicek</strong><br/>
Senior Software Architect
</td>
</tr>
</table>

---

<div align="center">

**Made with 💚 for the Vue.js & Claude Code Community**

[![Vue](https://img.shields.io/badge/Vue.js-42B883?style=for-the-badge&logo=vuedotjs&logoColor=white)](https://vuejs.org)
[![GitHub](https://img.shields.io/badge/GitHub-pluginagentmarketplace-black?style=for-the-badge&logo=github)](https://github.com/pluginagentmarketplace)

</div>
