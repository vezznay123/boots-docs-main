
# canonicalisation

**Priority**: High

## Overview

Canonicalisation is crucial for managing duplicate content issues and ensuring that search engines understand the preferred version of a page. For product listing pages (PLPs), using self-referencing canonical tags by default helps maintain consistency and prevents unintentional duplicate indexing. However, there may be scenarios where these tags need to be overridden based on content management strategies.

## Implementation Requirements

### 1. Default Self-Referencing Canonical Tags

- **Default Setting**: By default, product listing pages should include self-referencing canonical tags. This helps indicate to search engines that the PLP is the primary version of the page that should be indexed.
  - **Example**:
    ```html
    <link rel="canonical" href="https://www.example.com/category/plp" />
    ```

### 2. CMS-Defined Canonical Overrides

- **CMS Integration**: Allow for canonical tags to be overridden by CMS-defined targets. This functionality is useful in scenarios where the canonical version of a page needs to point to a different target, such as when consolidating content or promoting a specific page version.
  - **Absolute URLs**: All canonical tags must use absolute URLs, ensuring that search engines can accurately determine the preferred version without ambiguity.
  - **Parameter Stripping**: Canonical URLs should strip unnecessary parameters, such as tracking or session identifiers, to provide a clean, consistent URL.
  - **Example with Override**:
    ```html
    <link rel="canonical" href="https://www.example.com/special-offer-category" />
    ```

## Best Practices

- **Consistent Canonicalisation**: Ensure consistent canonical tag usage across all PLPs. This prevents multiple versions of the same page from competing in search engine results, reducing the risk of duplicate content penalties.
- **Dynamic Page Handling**: For pages with dynamic elements or filters, ensure that the canonical URL points to the base version of the PLP, stripping out any unnecessary query parameters.
- **Monitoring and Validation**: Regularly audit canonical tags to ensure they are properly implemented and accurately reflect the intended canonical version of each page.

## Benefits of Canonicalisation

1. **Prevent Duplicate Content Issues**: Proper use of canonical tags helps prevent search engines from indexing duplicate content, which can dilute ranking signals and reduce SEO effectiveness.
2. **Improved Search Rankings**: Canonical tags help search engines understand the preferred version of a page, which can improve the page's chances of ranking higher in search engine results.
3. **Simplified User Navigation**: By ensuring that only the preferred version of a page is indexed, users are more likely to be directed to the correct page when clicking on search engine results, providing a seamless experience.

## Conclusion

Implementing default self-referencing canonical tags on product listing pages ensures consistency and prevents duplicate content issues. By allowing for CMS-defined overrides with absolute URLs, this approach provides the flexibility needed to address specific SEO strategies, ultimately enhancing search visibility and user experience.
