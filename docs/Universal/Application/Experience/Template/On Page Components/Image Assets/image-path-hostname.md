
# image hostname & urls

**Priority**: Low

## Overview

Configuring image URLs correctly is crucial for optimising content delivery and ensuring that images are served efficiently and securely. By serving images from a dedicated media server or CDN, while using the primary domain hostname, you can maintain consistency in branding and improve SEO.

## Best Practice for Image URL Configuration

- **Use a Consistent Hostname**: Ensure that images are served using the primary domain hostname (e.g., `boots.com/images/some-image.png`) instead of an external CDN path (e.g., `images.cdn-path.com/some-image.png`). This helps in maintaining consistency for SEO and provides a better user experience.
- **DNS Configuration**: Configure DNS to serve image paths from a media server or CDN while using the main domain. This allows you to use the benefits of a CDN without exposing an unrelated hostname, which can have a positive impact on SEO.

## Benefits of Using Consistent Image URLs

- **Improved SEO**: Using the primary domain hostname for images helps in consolidating domain authority. Search engines see this as a positive factor, which can contribute to better rankings.
- **Enhanced User Trust**: Serving images from the main domain instead of a third-party URL reinforces user trust by reducing the appearance of external dependencies.
- **Optimised Content Delivery**: While the images are served from a CDN, they appear as if they are hosted under the main domain, providing the advantages of a CDN, such as faster delivery, without compromising branding.

## Example Implementation

### DNS Configuration for Media Server/CDN
1. **Point Subdomain to CDN**: Configure a subdomain, such as `media.boots.com`, to point to the CDN that hosts the images. This allows you to keep the image URLs consistent while benefiting from CDN capabilities.
2. **CDN Rewrite Rules**: Set up rules in your CDN configuration to rewrite the URLs so that requests to `boots.com/images/` are directed to the appropriate media server or CDN.

### Image URL Example

- **Current Implementation**: `images.cdn-path.com/some-image.png`
- **Optimised Implementation**: `boots.com/images/some-image.png`

This approach ensures that image URLs are user-friendly, SEO-optimised, and consistent with the rest of the website.

## SEO Impact

Configuring image URLs to use the main domain hostname helps in building domain authority and ensures that search engines associate all images with the primary domain. This can result in improved SEO performance and higher rankings. Consistent URLs also reduce the likelihood of mixed content warnings, which can affect user experience and SEO negatively.
