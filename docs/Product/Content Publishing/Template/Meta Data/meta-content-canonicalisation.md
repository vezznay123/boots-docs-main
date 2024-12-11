# canonicalisation

**Priority:** Medium 

## Overview  
Canonicalisation helps prevent duplicate content issues by specifying the preferred version of a page. This feature involves setting a default `rel="canonical"` tag that self-refers to the page URL (exclusive of parameters), while allowing overrides via the CMS when necessary.

## Implementation Requirements  

### 1. Default Canonical URL:  
- Specify a `rel="canonical"` tag that self-refers to the page URL, excluding any query parameters.  

#### Example:  
- Canonical Tag: `<link rel="canonical" href="https://www.example.com/nutrition-tips" />`  

### 2. CMS Override:  
- Allow content editors to override the default canonical URL through the CMS.  
- Enable the Boots marketing team to input a custom canonical URL for strategic purposes or when needed for specific content.  

### 3. Output Validation:  
- Validate all canonical URLs to ensure they are well-formed, resolve correctly, and align with SEO best practices.  
- Prevent errors such as pointing canonical tags to non-existent or irrelevant pages.  

## Best Practices  
- Default to self-referencing canonical URLs to maintain consistency and prevent duplicate content issues.  
- Use custom canonical URLs sparingly and only when they provide clear SEO or business value.  
- Regularly audit canonical tags to ensure they remain accurate and relevant as site content evolves.  

## Benefits  
- Prevents duplicate content issues by defaulting to self-referencing canonical URLs.  
- Provides flexibility for the Boots marketing team to specify strategic canonical targets.  
- Enhances SEO by ensuring consistent, well-implemented canonicalisation across the site.  

## Conclusion  
A robust canonicalisation strategy, combining self-referencing defaults with CMS override capabilities, is essential for managing duplicate content and improving SEO. This approach ensures flexibility while maintaining consistency and search visibility.

