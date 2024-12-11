
# image alt text attribute 

**Priority**: Medium

## Overview

Image alt text attributes are essential for both SEO and accessibility. Alt text provides a textual alternative to images, allowing screen readers to convey information to visually impaired users and helping search engines understand the content and context of images on a webpage. Using template functionality in Business Manager to populate alt and title tags within the image attribute for all products ensures consistency and enhances user experience, as well as improves search engine visibility.

## Implementation Requirements

### 1. Populate Alt and Title Tags

- **Business Manager Integration**: Use template functionality in Business Manager to dynamically generate and embed the alt and title attributes for all product images. This ensures that each product image is described clearly and consistently.
- **Alt Text for Products**: The alt text should provide a concise, descriptive summary of the image content. Include product names and relevant attributes to make it informative for users and search engines.

### 2. Example of Unoptimised vs Optimised Image Tags

- **Unoptimised Image Tag**:
  ```html
  <img src="https://boots.scene7.com/is/image/Boots/10339713?op_sharpen=1" alt="" class="oct-image oct-image--lazy" data-testid="lazy-image" decoding="async" loading="lazy">
  ```
  The absence of alt text means the image is not accessible to screen readers and provides no information to search engines, reducing the overall effectiveness of the content.

- **Optimised Image Tag**:
  ```html
  <img src="https://boots.scene7.com/is/image/Boots/10339713?op_sharpen=1" alt="L'Oréal Paris Bright Reveal Dark Spot UV Fluid SPF 50+ Niacinamide 50ml Product Image" class="oct-image oct-image--lazy" data-testid="lazy-image" decoding="async" loading="lazy">
  ```
  The optimised version includes a descriptive alt attribute that improves accessibility and helps search engines understand the context of the image.

## Best Practices

- **Concise and Descriptive**: Alt text should be concise yet descriptive, providing enough information to understand the image's content without being overly verbose.
- **Avoid Keyword Stuffing**: While it's important to include relevant keywords in alt text, avoid stuffing keywords unnaturally. The text should be useful to users and make logical sense.
- **Unique Alt Text**: Ensure that each product image has a unique alt text. Avoid using generic or repetitive descriptions, as this can hinder both SEO and user experience.

## Benefits of Optimised Alt Text

1. **Improved Accessibility**: Alt text allows visually impaired users to understand the content of images using screen readers, enhancing overall accessibility and compliance with web accessibility standards.
2. **Enhanced SEO**: Well-written alt text helps search engines understand the content and relevance of images, improving the chances of images appearing in search results, such as Google Image Search.
3. **Better User Experience**: If an image cannot be loaded for any reason, the alt text will be displayed in place of the image, providing context to users about the content that should be present.

## Conclusion

Proper implementation of alt text attributes is crucial for enhancing accessibility, SEO, and user experience. By leveraging template functionality in Business Manager to ensure all product images have optimised alt and title tags, the Boots website can provide a more inclusive experience and improve its search engine visibility.
