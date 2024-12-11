
# resource & load directives

**Priority**: Low

## Overview

Using resource and load directives in the `<head>` section of a webpage can significantly enhance website performance by optimising the loading process for both first-party and third-party resources. These directives help to improve user experience by minimising delays and ensuring critical assets are available as soon as they are needed. Techniques such as DNS prefetching, preconnect, and preload, as well as asynchronous script loading and lazy loading, all contribute to faster and more efficient page loads.

## Implementation Requirements

### 1. DNS Prefetching and Preconnect

- **DNS Prefetching**: Use the `dns-prefetch` directive to resolve DNS for both first-party and third-party resources. This allows the browser to start resolving domain names in advance, thereby reducing latency when the resource is requested.
  ```html
  <link rel="dns-prefetch" href="https://example.com" />
  ```

- **Preconnect**: Use the `preconnect` directive to establish early connections to required domains, reducing the time needed to establish network connections.
  ```html
  <link rel="preconnect" href="https://example.com" />
  ```

### 2. Preload Critical Assets

- **Preload**: Implement resource hints for critical assets using the `preload` attribute to make sure that important resources are available as soon as they are needed.
  - **CSS Example**:
    ```html
    <link rel="preload" href="path/to/critical.css" as="style" />
    ```
  - **JavaScript Example**:
    ```html
    <link rel="preload" href="path/to/critical.js" as="script" />
    ```
  - **Hero Image Example** (first above-the-fold image):
    ```html
    <link rel="preload" href="path/to/critical.jpg" as="image" fetchpriority="high" />
    ```
  - **Font Example** (using `crossorigin` attribute):
    ```html
    <link rel="preload" href="path/to/font.woff2" as="font" type="font/woff2" crossorigin="anonymous" />
    ```

### 3. Load Scripts Using Async and Defer Attributes

- **Async Attribute**: Load scripts asynchronously to prevent them from blocking the rendering of the page.
  ```html
  <script src="path/to/script.js" async></script>
  ```

- **Defer Attribute**: Use the `defer` attribute to ensure that non-critical JavaScript files are executed only after the HTML document has been parsed.
  ```html
  <script src="path/to/script.js" defer></script>
  ```

### 4. Lazy Loading for Images

- **Lazy Loading**: Use the `loading="lazy"` attribute for images to load them only when they are about to enter the viewport, which helps reduce the initial page load time.
  ```html
  <img src="path/to/image.jpg" alt="Image Description" loading="lazy" />
  ```

### 5. Preload Font Files

- **Font Preloading**: Preload fonts to ensure that text is rendered quickly without a noticeable delay.
  ```html
  <link rel="preload" href="path/to/font.woff2" as="font" type="font/woff2" crossorigin="anonymous" />
  ```

- **Font Display Settings**: Use the `font-display` property in CSS to control how fonts are displayed during load, optimising for either performance or appearance.
  ```css
  @font-face {
    font-family: 'CustomFont';
    src: url('path/to/font.woff2') format('woff2');
    font-display: swap; /* or 'fallback', 'block', or 'optional' depending on your preference */
  }
  ```

## Best Practices

- **Critical Resources**: Identify critical resources and implement `preload` and `preconnect` to make sure they are loaded as quickly as possible.
- **Async and Defer for JavaScript**: Use `async` for scripts that do not depend on other scripts, and `defer` for those that need to wait for the page to be parsed.
- **Minimise Render-Blocking**: Avoid using resources that block the initial rendering of the page. Implement techniques like preloading, preconnecting, and using `async` and `defer` attributes to enhance performance.

## Benefits of Resource & Load Directives

1. **Reduced Latency**: Techniques like `dns-prefetch` and `preconnect` help reduce latency by allowing the browser to resolve domain names and establish connections early.
2. **Improved Load Time**: Preloading critical assets ensures they are readily available, contributing to a faster load time for important elements like CSS, images, and fonts.
3. **Optimised User Experience**: Lazy loading non-critical assets, such as images below the fold, ensures users get a fast and responsive experience without unnecessary delays.

## Conclusion

Proper implementation of resource and load directives in the `<head>` section can significantly improve page load speed and the overall user experience. By preloading critical assets, preconnecting to important domains, and using techniques like lazy loading and asynchronous script loading, the Boots website can deliver content more efficiently and maintain a high level of performance.
