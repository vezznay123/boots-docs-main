
# meta robots

**Priority**: High

## Overview

Meta robots directives play an important role in controlling how search engines interact with product listing pages (PLPs). By default, PLP URLs should use a meta robots directive of "follow,index" to ensure that search engines index these pages and follow the links contained within them. This is crucial for maintaining the discoverability of product pages and ensuring a smooth user experience.

## Implementation Requirements

### 1. Default Meta Robots Directive for PLPs

- **Default Setting**: Product Listing Pages should be assigned a meta robots directive of "follow,index" by default. This setting helps search engines understand that they are allowed to index the page and follow the links to other content within the website.
- **Dynamic Override from Business Manager**: The default meta robots directive should be overridden by values specified in Business Manager, if one is present. This allows for flexibility in controlling which pages should or should not be indexed based on business needs.

### 2. Custom Hook from Business Manager

- **Custom Hook Integration**: A custom hook should be developed to source meta robots information from Business Manager. This ensures that any page-level modifications made in Business Manager are applied to the meta robots tag of each PLP.
- **Conditional Logic**: The hook should implement conditional logic to determine whether to use the default meta robots value or apply an overridden value from Business Manager.
- **Example of Overriding Directive**: If a specific PLP needs to be excluded from indexing due to a temporary out-of-stock situation, the default directive "follow,index" can be overridden to "noindex,follow" using the custom hook. This ensures the page is still crawlable, but not indexed, until it becomes relevant again.

## Best Practices

- **Avoid "noindex" on Key PLPs**: Avoid using "noindex" on important product listing pages, as this can prevent valuable pages from being included in search engine results, reducing organic visibility.
- **Consistent Implementation**: Ensure consistent implementation across all PLPs to avoid discrepancies in indexing instructions, which could negatively impact SEO performance.
- **Fallback to Default**: Always fall back to the default "follow,index" directive if no specific instruction is present in Business Manager, ensuring that all PLPs remain indexed by default.

## Benefits of Meta Robots Implementation

1. **Enhanced Search Visibility**: Using "follow,index" ensures that PLPs and their links are crawled and indexed by search engines, improving the discoverability of product pages.
2. **Flexibility for SEO Management**: The ability to override meta robots settings through Business Manager provides flexibility for managing which pages should be indexed, helping to control search engine visibility based on content and marketing strategies.
3. **Efficient Crawling**: Ensuring that the correct meta robots directives are applied helps search engines efficiently crawl and index the most valuable pages, making the best use of the crawl budget.

## Conclusion

Proper meta robots implementation is essential for maintaining the visibility and indexation of product listing pages. By defaulting to "follow,index" and providing flexibility for overrides via Business Manager, this approach ensures optimal indexing while allowing for granular control over page visibility when necessary.
