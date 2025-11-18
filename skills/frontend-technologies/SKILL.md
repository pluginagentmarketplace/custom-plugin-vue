---
name: frontend-technologies
description: Master modern frontend technologies including React, Vue, Angular, CSS/HTML, TypeScript, design systems, and UI/UX principles. Use when learning frontend development, building responsive interfaces, or implementing design systems.
---

# Frontend Technologies

## Quick Start

Frontend development requires mastery across multiple domains:

```javascript
// React Example - Component with Hooks
import React, { useState, useEffect } from 'react';

export const Counter = () => {
  const [count, setCount] = useState(0);

  useEffect(() => {
    document.title = `Count: ${count}`;
  }, [count]);

  return (
    <button onClick={() => setCount(count + 1)}>
      Count: {count}
    </button>
  );
};
```

## Core Frontend Stack

### JavaScript/TypeScript Fundamentals
- **ES6+ Features**: Arrow functions, destructuring, async/await, modules
- **DOM APIs**: Element selection, event handling, manipulation
- **Browser APIs**: Fetch, LocalStorage, WebSockets, Service Workers

### HTML5 & CSS3
- **Semantic HTML**: Proper markup structure, accessibility
- **CSS Architecture**: BEM, SCSS, CSS Modules, Tailwind
- **Responsive Design**: Media queries, mobile-first approach, flexbox, grid
- **Animation**: CSS transitions, keyframes, performance optimization

### JavaScript Frameworks

#### React Ecosystem
- **Core Concepts**: Components, JSX, props, state, hooks
- **State Management**: useState, useContext, Redux, Zustand
- **Performance**: React.memo, lazy loading, suspense
- **Testing**: React Testing Library, Jest

#### Vue 3
- **Composition API**: reactive(), ref(), computed()
- **Templates**: v-bind, v-on, directives
- **State**: Pinia store management
- **Router**: Vue Router for navigation

#### Angular
- **Components**: Decorators, templates, styles
- **Services**: Dependency injection, RxJS
- **Forms**: Reactive forms, validation
- **HTTP**: HttpClient for API calls

### Advanced Frontend Concepts

#### Design Systems
- **Component Libraries**: Building reusable component patterns
- **Design Tokens**: Colors, typography, spacing systems
- **Documentation**: Storybook, component APIs, usage guidelines
- **Accessibility**: WCAG compliance, ARIA attributes

#### Performance Optimization
- **Bundle Size**: Code splitting, tree shaking, minification
- **Rendering**: Server-side rendering, static generation
- **Loading**: Image optimization, lazy loading, prefetching
- **Metrics**: Core Web Vitals, performance monitoring

#### TypeScript for Frontend
- **Type Safety**: Interfaces, generics, utility types
- **Advanced Patterns**: Discriminated unions, conditional types
- **Framework Integration**: React TypeScript, Vue 3 composition

## Learning Resources

### Official Documentation
- React: https://react.dev
- Vue: https://vuejs.org
- Angular: https://angular.io
- MDN Web Docs: https://developer.mozilla.org

### Best Practices
1. **Component Design**: Single responsibility, prop drilling reduction
2. **State Management**: Clear data flow, separation of concerns
3. **Testing**: Unit tests, integration tests, E2E tests
4. **Accessibility**: Semantic HTML, keyboard navigation, screen readers
5. **Performance**: Lazy loading, memoization, virtualization

### Common Use Cases
- Building responsive web applications
- Creating interactive dashboards
- Implementing design systems
- Optimizing app performance
- Handling complex state management
