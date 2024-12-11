# page title fields 

**Priority:** High  

## Overview  
Page titles are a critical element of SEO and user engagement, serving as the first impression in search engine results and browser tabs. This feature provides a dedicated and intuitive field within the CMS for content editors to input and manage custom page titles, ensuring optimal performance and relevance for article pages in the Content Hubs.  

## Implementation Requirements  

### 1. **Page Title Field in CMS:**  
- Provide a dedicated field within the content editor interface to input custom page titles for article pages.  
- Display the current character count dynamically as the editor types to ensure compliance with SEO guidelines.  

### 2. **UI Indication and Validation:**  
- Clearly indicate when a page title has been set or is missing through visual cues (e.g., checkmarks or warning icons).  
- Implement character count limits (e.g., 60-70 characters) with a warning if the limit is exceeded.  
- Validate that the title field is not left blank before publishing.  

### 3. **Default Title Logic:**  
- Automatically generate a default page title using a predefined formula when the field is left blank.  
  - Formula Example: `{Article Name} | {Content Hub Name} | Boots {Locale}`  
  - Example Output: "Nutrition Tips | Health Hub | Boots UK"  
- Allow editors to override the default title with custom inputs for greater flexibility.  

## SEO Considerations  
- Enforce a character limit of 60-70 characters to prevent truncation in search engine results.  
- Encourage the use of primary keywords near the beginning of the title for optimal relevance.  
- Avoid duplication of titles across different pages to minimise SEO cannibalisation.  

## Best Practices  
- Use strategic keywords in page titles to boost search rankings.  
- Ensure titles are descriptive, engaging, and directly relevant to the page content.  
- Regularly audit and update page titles to reflect evolving SEO trends and user behaviour.  

## Benefits  
- Enhances SEO by optimising page titles for search engines.  
- Increases user engagement with relevant, tailored, and compelling titles.  
- Provides content editors with the flexibility to customise or rely on automated title generation.  

## Conclusion  
A robust CMS title tag population feature is vital for improving SEO and user engagement. By providing intuitive tools for managing page titles and adhering to SEO best practices, this feature ensures that article pages within the Content Hubs maximise their visibility and relevance.
