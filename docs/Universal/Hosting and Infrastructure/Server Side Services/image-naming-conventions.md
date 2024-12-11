
# image filenames

**Priority**: Low

## Overview

Dynamically generating image filenames using product system variables is an effective approach to improve SEO and user experience. By creating descriptive file paths, images become more relevant to both users and search engines, improving discoverability and overall content quality. Salesforce Commerce Cloud has functionality to automatically generate such descriptive filenames and alt text based on product attributes.

## Best Practices for Image Naming Conventions

- **Use Product System Variables**: Generate image filenames dynamically using product attributes like product name, variation values, and view type to create descriptive filenames.
- **Descriptive and Concise Filenames**: Ensure that filenames are descriptive but concise, using relevant keywords that describe the product clearly.
- **Avoid Special Characters**: Use only hyphens to separate words and avoid special characters, which may cause issues in URL encoding.
- **Consistent Naming Pattern**: Maintain a consistent pattern across all image filenames to ensure uniformity throughout the website.

## Example Implementation


- **Example Default Image Filename**:

  ```text
  ${productname}-${variation_value}-${viewtype}.jpg
  ```

  For instance, an image filename could be:

  ```text
  running-shoes-blue-sideview.jpg
  ```

- **Example Default Image Alt Text**:

  ```text
  ${productname}, ${variation value}, ${viewtype}
  ```

  For example:

  ```text
  Running Shoes, Blue, Side View
  ```

- **Example Default Image Title**:

  ```text
  ${productname}, ${variation value}
  ```

  For example:

  ```text
  Running Shoes, Blue
  ```

## Benefits of Dynamic Image Naming

- **Improved SEO**: Search engines use image filenames and alt text as signals to understand the content of an image. Using descriptive names helps improve image ranking in search results.
- **Better User Experience**: Descriptive filenames and alt text improve accessibility for users who rely on screen readers, providing better context for the images.
- **Simplified Management**: Using product system variables to generate image names reduces manual effort and ensures consistency across the website.

## Salesforce Commerce Cloud Configuration

- **Automated Naming**: Configure Salesforce Commerce Cloud to use product system variables to generate image filenames automatically. This ensures that image URLs are consistently descriptive and SEO-friendly.
- **Template Integration**: Integrate the naming convention within the platform templates to apply consistent rules across all product images, ensuring that filenames and alt texts are generated dynamically based on product attributes.
- **Business Manager Configuration**: In Salesforce Commerce Cloud Business Manager, navigate to **Merchant Tools > Content > Content Assets**. Here, you can set up automated naming conventions for images using product attributes and templates to ensure consistent and descriptive image URLs.

## SEO Impact

Using descriptive image filenames and alt text improves the visibility of your images in search engines, leading to better rankings in image search results. Proper image optimisation helps boost the relevance of the page content, ultimately contributing to improved SEO performance and higher organic traffic.
