
# build optimisation

**Priority**: Low

## Overview

Build bundling and code splitting are essential techniques to optimise JavaScript applications. They ensure that only the necessary code is loaded, which improves page load speed and user experience. Tools like Webpack, Bun, and other bundlers can be used to bundle JavaScript effectively while also splitting code to reduce initial load times. Proper bundling and loading techniques can help keep bundle sizes small and ensure a seamless experience.

## Best Practices for Build Bundling

- **Code Splitting**: Split JavaScript bundles so that only the code required for the current page or feature is loaded. This minimises the initial payload and speeds up the page load.
- **Vendor and Application Code Separation**: Separate third-party vendor code (e.g., libraries like React or Lodash) from the application code. This allows for better caching since third-party libraries are less likely to change compared to your application's custom code.
- **Tree Shaking**: Use tree shaking to eliminate dead code and remove unused imports. This helps ensure that the final JavaScript bundle is as small as possible, improving load performance.
- **Dynamic Imports**: Use dynamic imports to load JavaScript files asynchronously based on user interaction or specific conditions. This is particularly useful for large, infrequently used components.
- **Optimise Dependencies**: Analyse and optimise package dependencies to ensure that only essential packages are bundled. Avoid bundling unused or bloated dependencies to keep bundle sizes manageable.

## Tools and Technologies

- **Webpack**: A widely-used JavaScript bundler that supports code splitting, tree shaking, and many other optimisations for efficient bundling.
- **Bun**: A newer JavaScript bundler and runtime that is highly optimised for speed, reducing the time it takes to compile and bundle code.
- **Parcel**: An alternative bundler that aims for zero-configuration bundling, with support for code splitting and caching.

## Example Implementation

### Webpack Code Splitting Example

Configure Webpack to perform code splitting by using dynamic imports and separating vendor code:

```javascript
// webpack.config.js
module.exports = {
  entry: {
    main: './src/index.js',
    vendor: ['react', 'react-dom'],
  },
  optimization: {
    splitChunks: {
      chunks: 'all',
    },
  },
};
```

### Dynamic Import Example

Use dynamic imports in a React application to load components asynchronously:

```jsx
import React, { Suspense } from 'react';

const LazyComponent = React.lazy(() => import('./LazyComponent'));

function App() {
  return (
    <div>
      <h1>Welcome to My App</h1>
      <Suspense fallback={<div>Loading...</div>}>
        <LazyComponent />
      </Suspense>
    </div>
  );
}
```

## SEO Impact

Optimising JavaScript bundles through code splitting and elegant loading ensures faster page load times, which is beneficial for Core Web Vitals and overall SEO. Search engines favour fast-loading sites, and efficient bundling practices help reduce page load times, leading to better rankings and a more positive user experience.
