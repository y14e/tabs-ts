# tabs.ts (v0)

WAI-ARIA compliant [tabs](https://www.w3.org/WAI/ARIA/apg/patterns/tabs/) pattern implementation in TypeScript.

## Usage

```ts
import Tabs from './tabs';

new Tabs(root, options);
// => Tabs
//
// root: HTMLElement
// options (optional): TabsOptions
```

## 🪄 Options

```ts
interface TabsOptions {
  animation?: {
    content?: {
      crossFade?: boolean;   // default: true
      duration?: number;     // ms (default: 300)
      easing?: string;       // <easing-function> (default: 'ease')
      fade?: boolean;        // default: false
    };
    indicator?: {
      duration?: number;     // ms (default: 300)
      easing?: string;       // <easing-function> (default: 'ease')
    };
  };
  avoidDuplicates?: boolean; // default: true
  manual?: boolean;          // default: false
  selector?: {
    content?: string;        // default: '[role="tablist"] + *'
    indicator?: string;      // default: '[data-tabs-indicator]'
    list?: string;           // default: '[role="tablist"]'
    panel?: string;          // default: '[role="tabpanel"]'
    tab?: string;            // default: '[role="tab"]'
  };
  vertical?: boolean;        // default: false
}
```

## 📦 APIs

### `activate`

```ts
tabs.activate(tab);
// => void
//
// tab: HTMLElement
```

### `destroy`

Destroys the instance and cleans up all event listeners.

```ts
tabs.destroy(force);
// => Promise<void>
//
// force (optional): If true, skips waiting for animations to finish.
```

## Demo

https://y14e.github.io/tabs-ts/
