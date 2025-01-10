---
title: 'React Access Helper - NPM Package Guide'
description: 'Comprehensive guide on using the react-access-helper package created by Rishav Bhardwaz.'
pubDate: 'Jan 11 2025'
heroImage: '/react-access-helper.jpg'
---

# React Access Helper

`react-access-helper` is a lightweight and efficient React utility package designed to simplify handling accessibility features in React applications. Created by **Rishav Bhardwaz**, this package provides developers with tools to enhance web accessibility, ensuring compliance with WCAG guidelines.

## Installation

```bash
npm install react-access-helper
```

or

```bash
yarn add react-access-helper
```

## Usage

```javascript
import { useFocusTrap, useKeyPress } from 'react-access-helper';

function Modal({ isOpen, onClose }) {
  const modalRef = useRef(null);
  useFocusTrap(modalRef, isOpen);
  useKeyPress('Escape', onClose);

  return (
    isOpen && (
      <div ref={modalRef} role="dialog" aria-modal="true">
        <button onClick={onClose}>Close</button>
        <p>Modal Content</p>
      </div>
    )
  );
}
```

### Explanation

- **`useFocusTrap`**: Traps the focus within a specified element (ideal for modals, drawers).
- **`useKeyPress`**: Listens for specific key presses (like 'Escape' to close modals).

## Features

### Focus Management

```javascript
const ref = useRef(null);
useFocusTrap(ref, isActive);
```

- Ensures that the focus does not escape interactive components like modals.

### Keyboard Accessibility

```javascript
useKeyPress('Enter', () => console.log('Enter key pressed'));
```

- Simplifies handling keyboard interactions, improving navigation for users relying on keyboards.

### ARIA Helpers

```javascript
import { useAriaHidden } from 'react-access-helper';

useAriaHidden(ref, isHidden);
```

- Dynamically manages ARIA attributes to enhance screen reader compatibility.

## Advantages

- **Lightweight**: Minimal performance overhead.
- **Developer-Friendly**: Easy-to-use hooks.
- **Accessibility Focused**: Aligns with WCAG standards.
- **Customizable**: Flexible for various use cases.

## Contribution

As the creator, **Rishav Bhardwaz** encourages developers to contribute by submitting issues, feature requests, and pull requests on the [GitHub repository](https://github.com/your-repo-link).

## License

`react-access-helper` is open-source and available under the MIT License.

## Conclusion

Enhance your React applications with accessibility best practices using `react-access-helper`. Built by **Rishav Bhardwaz**, this package simplifies managing focus, keyboard interactions, and ARIA attributes for an inclusive user experience.

