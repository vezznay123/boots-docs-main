
# image formats

**Priority**: Low

## Overview

Conditionally serving optimised image files based on network conditions and the requesting device/user-agent is a key technique to improve performance without sacrificing image quality. This approach ensures that users receive the most suitable image format depending on their device and network capabilities, reducing load times and enhancing user experience.

## Best Practice for Image Delivery

- **Conditional Image Serving**: Automatically serve different image formats (e.g., WebP, AVIF, JPEG) based on the user’s device, browser capabilities, and network conditions. This ensures that images are optimised for the best performance without compromising quality.
- **Modern CDN Capabilities**: Most modern content delivery networks (CDNs) can serve different media formats to different devices based on various conditions, such as network speed or device type. This helps in improving performance by reducing the file size of images while maintaining visual quality.

## Benefits of Optimised Image Delivery

- **Reduced Load Times**: Serving lighter, optimised image formats helps reduce load times, especially for users on slower networks or mobile devices.
- **Improved User Experience**: Faster image delivery leads to a more responsive and engaging experience for end-users, enhancing overall satisfaction.
- **Optimised Bandwidth Usage**: Using modern, highly compressed image formats (e.g., WebP, AVIF) helps reduce bandwidth consumption, especially for high-resolution images.

## Example Implementations

### Smart CDN for Image Optimisation

A smart CDN can automatically determine the best image format to serve based on various factors like device type, browser, and network conditions. Below is a conceptual diagram to illustrate how a smart CDN optimises image delivery:

```plaintext
                +--------------------+
Request Image   |                    |
--------------> |    Smart CDN       |
                |                    |
                +--------------------+
                        |
                        | Determine device, browser, and network conditions
                        v
                +--------------------+
                |                    |
                |   Serve Optimal    |
                |   Image Format     |
                | (e.g., WebP, AVIF, |
                |   JPEG)            |
                |                    |
                +--------------------+
                        |
                        v
               Faster Delivery of Optimised Image to User
```

A smart CDN can handle different image formats automatically, reducing the burden on developers to manually specify which format to serve for each request. This ensures that users get the best quality image that their device can handle, without unnecessary bandwidth usage.

### React with Conditional Image Loading

Use a library like **react-image** to conditionally load different image formats based on browser support. This can be combined with further optimisations, such as responsive images, to enhance user experience:

- **Responsive Images**: Use the `srcSet` attribute to serve different image sizes based on the user's screen size, which optimises performance for various devices.

```jsx
import { useState, useEffect } from 'react';

function OptimisedImage({ src, alt }) {
  const [supportsWebP, setSupportsWebP] = useState(false);

  useEffect(() => {
    const img = new Image();
    img.onload = () => setSupportsWebP(true);
    img.onerror = () => setSupportsWebP(false);
    img.src = "data:image/webp;base64,UklGRiIAAABXRUJQVlA4TCEAAAAvAAAAHAAA";
  }, []);

  const imageUrl = supportsWebP ? `${src}.webp` : `${src}.jpg`;

  return (
    <img
      src={imageUrl}
      alt={alt}
      srcSet={`${src}-small.jpg 480w, ${src}-medium.jpg 1024w, ${src}-large.jpg 1600w`}
      sizes="(max-width: 600px) 480px, (max-width: 1200px) 1024px, 1600px"
    />
  );
}
```

This example demonstrates how to combine conditional image loading with responsive images to further optimise image delivery in a React application. By leveraging modern image formats and efficient loading techniques, developers can significantly enhance both performance and user experience.

## SEO Impact

Serving optimised images improves page load speed, which directly impacts Core Web Vitals metrics and overall SEO performance. Search engines prioritise fast-loading sites, and optimised image delivery helps reduce load times, improving search engine rankings.
