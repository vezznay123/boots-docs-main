
# breadcrumb structured data

**Priority**: Low

## Overview

Breadcrumbs are an important feature for both users and search engines, providing a clear navigation trail that enhances the user experience and helps search engines understand the structure of your website. Implementing breadcrumb structured data using the `BreadcrumbList` schema type in JSON-LD format helps search engines interpret the hierarchy and relationship of pages, improving SEO.

## Implementation Requirements

### 1. Breadcrumb Schema Markup

- **Schema Type**: Use the `BreadcrumbList` schema type to create a structured breadcrumb trail in JSON-LD format.
- **HTML Example**:
  ```html
  <ol itemscope itemtype="https://schema.org/BreadcrumbList">
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <a itemprop="item" href="https://example.com/beauty">
        <span itemprop="name">Beauty</span>
      </a>
      <meta itemprop="position" content="1" />
    </li>
    ›
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <a itemprop="item" href="https://example.com/beauty/skincare">
        <span itemprop="name">Skincare</span>
      </a>
      <meta itemprop="position" content="2" />
    </li>
    ›
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <a itemprop="item" href="https://example.com/beauty/skincare/moisturisers">
        <span itemprop="name">Award Winners</span>
      </a>
      <meta itemprop="position" content="3" />
    </li>
  </ol>
  ```

### 2. JSON-LD Example

- **JSON-LD Format**: To ensure search engines can read the breadcrumb data effectively, use JSON-LD to provide a structured and machine-readable version.
  ```json
  {
    "@context": "https://schema.org",
    "@type": "BreadcrumbList",
    "itemListElement": [
      {
        "@type": "ListItem",
        "position": 1,
        "name": "Beauty",
        "item": "https://example.com/beauty"
      },
      {
        "@type": "ListItem",
        "position": 2,
        "name": "Skincare",
        "item": "https://example.com/beauty/skincare"
      },
      {
        "@type": "ListItem",
        "position": 3,
        "name": "Award Winners",
        "item": "https://example.com/beauty/skincare/moisturisers"
      }
    ]
  }
  ```

### 3. UI/UX Design Considerations

- **User Experience**: Ensure the breadcrumb trail is placed in a prominent location on category and product pages to aid navigation. Breadcrumbs should be clickable links to allow users to move back through the site's hierarchy easily.
- **Styling**: Apply styling that makes breadcrumbs visually appealing but subtle enough not to distract from the main content. Ensure breadcrumbs are responsive and adapt well to different screen sizes.

### 4. Best Practices

- **Hierarchy**: Ensure the breadcrumb accurately represents the site's hierarchy, starting from the homepage.
- **Self-Referencing**: For each level, include a self-referencing breadcrumb to provide a consistent navigation trail.
- **Avoid Orphan Pages**: Ensure all pages in the hierarchy are represented, avoiding orphan pages without links to parent categories.

## Conclusion

Using `BreadcrumbList` structured data in JSON-LD format enhances both the user experience and SEO by providing a clear and machine-readable navigation trail for search engines. This ensures better indexation of category pages, helping users and search engines understand the relationship between various parts of your website more effectively.
