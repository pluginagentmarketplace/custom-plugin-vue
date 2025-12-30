# Changelog

All notable changes to this project are documented in this file.

Format: [Keep a Changelog](https://keepachangelog.com/)
Versioning: [Semantic Versioning](https://semver.org/)

## [Unreleased]

### Planned
- Additional language support
- Interactive exercises

## [2.0.0] - 2025-12-30

### Added - Production-Grade Upgrade
- **SASMP v1.3.0 Compliance**: All agents and skills now follow Standardized Agent Skill Marketplace Protocol
- **EQHM Framework**: Ethical, Quality, Honest, Momentum principles integrated throughout

### Agents (7 Total) - Complete Rewrite
- **Role Definitions**: Clear OWNS/DEPENDS/DELEGATES/COLLABORATES boundaries
- **TypeScript I/O Schemas**: Type-safe input/output contracts for all agents
- **Error Handling Tables**: Common errors with root causes and recovery actions
- **Token Optimization**: Cost-efficient strategies with caching and chunking
- **Observability Hooks**: Event tracking for monitoring and debugging
- **Troubleshooting Guides**: Debug checklists and diagnostic steps
- **Usage Examples**: Practical examples with expected outputs

### Skills (7 Total) - Complete Rewrite
- **Single Responsibility**: Each skill has one atomic purpose
- **Parameter Schemas**: TypeScript interfaces for all skill parameters
- **Learning Modules**: 5 modules per skill with exercises and duration
- **Validation Checkpoints**: Beginner/Intermediate/Advanced milestones
- **Retry Logic**: Exponential backoff configuration (1s, 2s, 4s)
- **Observability Tracking**: Event-based progress monitoring
- **Unit Test Templates**: Ready-to-use Vitest test examples

### Technical Improvements
- Vue 3.4/3.5 compatibility
- Nuxt 3 latest patterns
- Vitest + Playwright testing standards
- Pinia 2.1+ patterns
- Vue Router 4 advanced features
- Generic components in Vue 3.3+

### Quality Standards
- Zero orphan skills (all skills bonded to agents)
- Zero circular dependencies
- Consistent naming conventions
- Complete troubleshooting coverage

## [1.0.0] - 2025-12-29

### Added
- Initial release
- SASMP v1.3.0 compliance
- Golden Format skills
- Protective LICENSE

---

**Maintained by:** Dr. Umit Kacar & Muhsin Elcicek
