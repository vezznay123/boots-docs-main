
# canonical tags

**Priority**: High

## Overview

Canonical tags are an essential part of SEO strategy, used to help search engines understand which version of a page is the authoritative one when multiple versions of a page exist. This is particularly useful for managing duplicate content issues and ensuring that search engines are directed to the preferred version of the page. Proper implementation of canonical tags ensures that search engines focus on the main page, improving indexing and search rankings.

## Implementation Requirements

### 1. Self-Referential Canonical Tags

- **Self-Referential Canonical Tags**: All article pages and article category pages should include self-referential canonical tags in the `<head>` section of the HTML. This means that each page should include a canonical tag that points to itself as the preferred version, helping to establish it as the authoritative version.

### 2. Exclude URL Parameters

- **Parameter Exclusion**: The canonical tag should exclude any parameters present in the URL string, such as tracking or session parameters. This helps avoid duplicate content issues by indicating the base version of the URL as the authoritative one, regardless of any added parameters.

- **Example**:
  ```html
  <link rel="canonical" href="https://www.example.com/article-category/article-title" />
  ```
  In this example, the canonical tag points to the clean version of the URL without any parameters, ensuring that search engines understand the preferred version of the page.

## Best Practices

- **Consistency**: Ensure that all article and category pages include canonical tags consistently. Missing canonical tags on any page can lead to duplicate content issues and reduce the effectiveness of SEO efforts.
- **Canonical Tags for Duplicate Pages**: If multiple pages contain similar or duplicate content, use canonical tags to point to the main version of the content. This helps consolidate ranking signals and avoid splitting SEO value across multiple pages.
- **Avoid Conflicting Tags**: Do not include conflicting canonical tags that point to different URLs on similar content pages. This can confuse search engines and lead to improper indexing or ranking penalties.

## Benefits of Canonical Tags

1. **Avoid Duplicate Content**: Proper implementation of canonical tags helps avoid duplicate content issues by clearly indicating the preferred version of a page to search engines.
2. **Consolidated Ranking Signals**: When similar content exists on multiple URLs, canonical tags help consolidate ranking signals, improving the chances of the preferred page ranking well.
3. **Improved Crawl Efficiency**: By reducing the number of duplicate pages that need to be crawled, canonical tags help search engines allocate more crawl budget to other valuable content on the website.

## Conclusion

Canonical tags are a critical aspect of SEO, helping to manage duplicate content and direct search engines to the preferred version of a page. By implementing self-referential canonical tags on both article and category pages and excluding URL parameters, the Boots website can ensure better indexing, improved search rankings, and a more streamlined user experience.
