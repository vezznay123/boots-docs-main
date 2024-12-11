
# dynamic content slots

**Priority**: Medium

## Overview

The Lister Copy Slot design pattern aims to enhance user engagement and provide additional contextual information on category listing pages. By adding a text module to category listers, content can be dynamically tailored based on the selected filter variables, improving both user experience and SEO. This content can be easily managed via the content CMS, allowing for flexible and contextually relevant updates that align with product categories and specific filter combinations.

## CMS Considerations

### Defining Landing Page Address

To ensure effective implementation, the CMS should include a dedicated field in the content publishing area where a specific landing page (or ID) on the front-end can be defined. This allows content managers to directly link the text module to a relevant category or filter-based landing page. By providing the ability to specify the associated front-end URL, the CMS can dynamically determine which content should be displayed for each page and filter combination.

## Implementation Requirements

### 1. Add a Text Module to Category Listers

- **Dynamic Text Content**: Integrate a text module that can be populated through the content CMS to add descriptions or promotional copy to category listing pages. This module should support:

  - **Category Pages**: General descriptive content for the entire category.
  - **Category + Filter Paths**: Specific content for particular category-filter combinations, such as brand, product type, or feature refinement.

- **CMS Integration**: The module should be fully manageable through the content CMS, allowing non-technical users to easily modify the text to reflect changes in product focus, promotions, or seasonal campaigns.

### 2. Contextual Content Based on Filter Variables

- **Conditional Display**: Display content dynamically based on the active filters on the page, such as brand, product type, or customer preferences.

  - **Example**: If the user selects the "Waterproof" filter under the "Mascara" category, the text module could display a description or promotional content highlighting the benefits of waterproof mascaras.

- **SEO Considerations**: Ensure that each text variant is optimised for SEO by including relevant keywords and phrases based on the selected filter path, which can improve visibility in search engine results.

## Best Practices

- **Avoid Overloading**: Keep the text concise and informative. Avoid overloading the page with too much content that could distract users from browsing products.
- **SEO Optimisation**: Tailor the text content to include relevant keywords based on the active filters. This will help improve the page's relevance for long-tail keyword searches.
- **Maintain Consistency**: Ensure consistent messaging across similar category pages, while still tailoring content based on specific filter selections.

## Benefits of Lister Copy Slot

1. **Enhanced User Experience**: Providing dynamic content relevant to user-selected filters adds value by giving users more information tailored to their current interest, improving their browsing experience.
2. **Improved SEO**: Including filter-specific content helps search engines understand the page's relevance for specific queries, leading to improved rankings for category and filter combinations.
3. **Increased Engagement**: Well-crafted, contextually relevant copy can help keep users engaged, making them more likely to continue browsing and ultimately convert.

## Conclusion

The Lister Copy Slot design pattern is a flexible and effective way to enhance both user engagement and SEO performance on category listing pages. By dynamically displaying contextually relevant content based on active filter variables, the website can provide a richer user experience, improve search engine visibility, and better guide users toward products that meet their needs.
