# meta description fields 

**Priority:** High  

## Overview  
Meta descriptions are essential for improving SEO and click-through rates by providing a concise summary of page content in search engine results. This feature offers a dedicated field within the CMS for content editors to input and manage custom meta descriptions for article pages, ensuring they align with best practices and are optimised for user engagement.  

## Implementation Requirements  

### 1. **Meta Description Field in CMS:**  
- Provide a dedicated field within the content editor interface to input meta descriptions for article pages.  
- Display the current character count dynamically as the editor types to ensure compliance with SEO guidelines.  

### 2. **UI Indication and Validation:**  
- Clearly indicate when a meta description has been set or is missing through visual cues (e.g., checkmarks or warning icons).  
- Implement character count limits (e.g., 150-160 characters) with a warning if the limit is exceeded.  
- Validate that the description field is not left blank before publishing.  

### 3. **Default Description Logic:**  
- Automatically generate a default meta description using a predefined formula when the field is left blank.  
  - Formula Example: `Learn about {Article Name} and get insights on {Content Hub Name}. Visit Boots {Locale}.`  
  - Example Output: "Learn about Nutrition Tips and get insights on Health Hub. Visit Boots UK."  
- Allow editors to override the default description with custom inputs for greater flexibility.  

## SEO Considerations  
- Enforce a character limit of 150-160 characters to ensure the meta description displays fully in search results.  
- Encourage the use of primary keywords within the meta description to boost relevance.  
- Avoid duplication of meta descriptions across different pages to minimise SEO cannibalisation.  

## Best Practices  
- Write concise, engaging descriptions that summarise the page content effectively.  
- Use action-oriented language to encourage users to click through.  
- Regularly audit and update meta descriptions to align with current SEO trends and user intent.  

## Benefits  
- Improves SEO by providing search engines with optimised, relevant meta descriptions.  
- Increases click-through rates by presenting compelling and descriptive summaries in search results.  
- Offers flexibility for content editors to customise descriptions or rely on automated generation.  

## Conclusion  
A well-designed CMS meta description management feature is vital for improving SEO and driving traffic to article pages within the Content Hubs. By enabling editors to manage custom descriptions while providing an automated fallback, this feature ensures consistent, engaging, and optimised meta descriptions across the site.