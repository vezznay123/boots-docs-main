
# category urls

**Priority**: High

## Overview

Creating user-friendly and descriptive URL structures is crucial for both SEO and user experience. URLs for category listing pages should be simple, descriptive, and follow a consistent pattern. Proper structuring of URLs helps search engines crawl the site effectively and provides a clear understanding of the site's content hierarchy.

## URL Structuring Guidelines

### 1. URL Structuring for Level 1 Product Listing Page (PLP)

- **Structure**: Include the name of the Level 1 PLP within the URL.
- **Formatting**: Use forward slashes (`/`) to separate each level of the URL, and separate words within a level using a dash (`-`).
- **Avoid**: Avoid query strings (e.g. `/category?type=teaser&id=44`) and stop words (e.g., "and", "or", "the").
- **Lowercase and Consistent**: URLs should be in lowercase, without special characters. Use or omit trailing slashes consistently.

**Example**:

```
/beauty-products
```

### 2. URL Structuring for Level 2 Product Listing Page (PLP)

- **Structure**: Include the names of both Level 1 and Level 2 PLPs in the URL, separated by a forward slash.
- **Formatting**: Follow the same formatting guidelines as the Level 1 PLP.

**Example**:

```
/beauty-products/skincare
```

### 3. URL Structuring for Level 3 Product Listing Page (PLP)

- **Structure**: Include the names of Level 1, Level 2, and Level 3 PLPs in order, separated by forward slashes.
- **Formatting**: Follow the same rules as above.

**Example**:

```
/beauty-products/skincare/moisturizers
```

### 4. URL Structuring for Level 4 Product Listing Page (PLP)

- **Structure**: Include the names of Level 1, Level 2, Level 3, and Level 4 PLPs in order.
- **Formatting**: Maintain the same formatting for consistency.

**Example**:

```
/beauty-products/skincare/moisturizers/natural
```

### 5. URL Structuring for Brand Product Listing Page (PLP)

- **Brand Pages**: Each brand should have its own top-level landing page, using the brand name in the URL.

**Example**:

```
/brands/clarins
```

### 6. URL Structuring for Brand PLP with a Level 2 Category Facet Selected

- **Facet Navigation**: For links on a top-level Brand PLP, point to the Level 2 PLP with the category facet appended on a parameter URL. This approach grants flexibility to prevent search engine spiders from accessing the parameter URL paths that return content that would be duplicated given generic category route throughout the site structure.

**Example**:

```
/brands/clarins?skincare
```

### 7. URL Structuring for Level 2 PLP with Brand Facet Selected

- **Structure**: Include the Level 1 and Level 2 PLPs in the URL, followed by the brand facet.

**Example**:

```
/beauty-products/skincare/clarins
```

### 8. URL Structuring for Level 2 PLP with a Facet Selected

- **Facet Addition**: Add an additional facet (e.g., a specific condition) at the end of the URL.

**Example**:

```
/beauty-products/skincare/dry-skin
```

### 9. URL Structuring for Level 2 PLP with a Facet and a Brand Selected

- **Combination**: Add the condition facet first, followed by the brand.

**Example**:

```
/beauty-products/skincare/dry-skin/clarins
```

### 10. URL Structuring for Level 2 Sales PLP

- **Sale Type Prefix**: Add the sale type at the beginning of the URL (e.g., `sale`, `offers`, `2-for-1`).

**Example**:

```
/sale/beauty-products/skincare
```

### 11. URL Structuring for Level 2 Seasonal PLP

- **Seasonal Prefix**: Add the seasonal type at the beginning of the URL (e.g., `black-friday-deals`, `mothers-day-gifts`).

**Example**:

```
/black-friday-deals/beauty-products/skincare
```

## Best Practices Summary

1. **Descriptive and Concise**: URLs should be descriptive, representing the page content clearly.
2. **Avoid Query Strings**: URLs for important pages should not include query strings or unnecessary parameters.
3. **Consistent Formatting**: Use lowercase letters, dashes for word separation, and consistent trailing slash usage.
4. **Facet Hierarchy**: For faceted navigation, ensure facets are placed in a consistent order to prevent duplicate URLs and improve indexing.
5. **Avoid Stop Words**: Avoid using stop words in URLs to keep them concise and more SEO-friendly.

## Conclusion

Creating clean, descriptive, and hierarchical URL structures for category listing pages improves both SEO and user experience. By following these guidelines, you ensure that search engines can easily crawl and understand your category pages, while users benefit from intuitive and readable URLs.
