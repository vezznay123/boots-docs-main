# Article Components

**Priority:** Medium  

## Overview  
Article components should provide clear, contextual information to enhance user experience. In addition to the existing items—estimated read time, original publish date, last reviewed date, and author bio—ensure that the article page includes:  
- A hyperlink to the author’s profile page.  
- A reference to the reviewer (if applicable), including a hyperlink to their profile or bio.  
- Display of both the publish date and the most recent review date.  
- A navigational element to the article tags page using a **pill design**.  
- A **horizontal carousel** at the bottom of the article linking to related article content.  
- Dedicated **hero image space** for visual impact at the top of the article.  
- Comprehensive **article outline/index** to improve content navigation.  
- Integration of **product feeds** and **product cards**, if relevant to the article content.  

## Implementation Requirements  

### Hero Image Space  
- Reserve prominent space at the top of the article page for a **hero image**.  
- Ensure the hero image is optimised for fast loading (`loading="lazy"`) and responsive across devices.  
- Add descriptive **alt text** for accessibility and SEO purposes.  
- Include optional image captions beneath the hero image for additional context.  

### Read Time  
- Calculate and display the estimated reading time based on word count or characters.  
- Present this near the article title or introduction for quick reference.  

### Publish Date  
- Display the original publish date prominently, typically below the article title.  
- Use a standard format (e.g., **DD Month YYYY**).  

### Last Reviewed Date  
- Include a **“Last Reviewed”** date to indicate when the content was most recently updated or verified.  
- Place this information close to the publish date for clarity.  

### Author Bio and Profile Link  
- Include a dedicated **author bio section** beneath the article.  
- Author bio should include:  
  - **Author Picture**: Use a circular image style for visual appeal.  
  - **Name and Credentials**: Display author’s name, role, and expertise.  
  - **Profile Link**: Provide a hyperlink to the author’s full profile page.  
- Include social media links or related content links authored by the same person.  

### Reviewer Reference and Bio Link (If Applicable)  
- If the article is reviewed by a subject matter expert or editor, display their name, role, and credentials.  
- Provide a hyperlink to the reviewer’s profile or biography page for credibility.  

### Article Tags Navigation 
- Display article tags in a **pill design** beneath the article content.  
- Each tag should act as a hyperlink, taking users to the respective tag’s article page.  
- Use clear, distinct styling for the pills (e.g., rounded borders, muted background colours).  

### Article Outline/Index  
- Generate an **article outline** (TOC) dynamically based on heading tags (`<h2>`, `<h3>`).  
- Place the index near the top of the article for easy navigation.  
- Use anchor links to allow users to jump to specific sections.  
- Style the outline as a collapsible component for mobile optimisation.  

### Related Article Carousel  
- Add a **horizontal carousel** at the bottom of the article to display related articles.  
- Include the following in each related article card:  
  - Thumbnail image (use `loading="lazy"` for optimisation).  
  - Title and a short excerpt or estimated reading time.  
  - A hyperlink to the related article page.  
- Ensure carousel navigation is smooth and user-friendly (e.g., arrow controls or swipe functionality).  

### Product Feed Integration (If relevant - defined in CMS)  
- Allow integration of **product feeds** within articles for content related to specific products.  
- Ensure the product feed dynamically pulls data such as product title, image, price, and description.  
- Support filtering of products based on tags, categories, or article context.  

### Product Card Integration (If relevant - defined in CMS)
- Integrate **product cards** within the article body for seamless inline product promotion.  
- Each product card should include:  
  - Product image (responsive and optimised).  
  - Product name and brief description.  
  - Price and availability.  
  - A **Call-to-Action (CTA)** button (e.g., “Buy Now” or “Learn More”) linking to the product page.  

### Heading Tag Usage  
- Use semantic and logical heading tags to structure the article content:  
  - `<h1>`: Main article title (single instance).  
  - `<h2>`: Section titles.  
  - `<h3>`: Subsections and subtopics.  
  - `<h4>`: Additional subheadings or clarifications.  
- Ensure consistent spacing and styling to maintain readability.  

### Structured Data (Schema.org Markup)  
Where possible, support these elements with structured data for enhanced search visibility and richer search results.  

**Hero Image**: Include as part of the `Article` schema:  
```json
"image": {
  "@type": "ImageObject",
  "url": "https://example.com/hero-image.jpg",
  "width": 1200,
  "height": 628
}
```  

**Author and Reviewer Data**:  
```json
"author": {
  "@type": "Person",
  "name": "Author Name",
  "url": "https://example.com/authors/author-name"
},
"reviewedBy": {
  "@type": "Person",
  "name": "Reviewer Name",
  "url": "https://example.com/reviewers/reviewer-name"
}
```  

**Product Data (If Applicable)**:  
```json
"product": {
  "@type": "Product",
  "name": "Product Name",
  "image": "https://example.com/product-image.jpg",
  "description": "Product description.",
  "offers": {
    "@type": "Offer",
    "priceCurrency": "GBP",
    "price": "19.99",
    "availability": "https://schema.org/InStock"
  }
}

```  
## Best Practices  

### Clarity  
- Use clear, consistent layouts for metadata, hero images, and article components.  

### Mobile Optimisation  
- Optimise all components (hero images, carousels, product cards, and outlines) for smaller screens.  

### Regular Updates  
- Review and update author/reviewer bios and associated images periodically.  

### Carousel Optimisation  
- Use lazy loading for images and limit the number of items displayed initially.  

---

## Conclusion  
By including a hero image, structured author/reviewer bios, article outlines, navigational tags, related article carousels, and product integrations, the article page becomes a comprehensive and engaging hub. These enhancements improve usability, content discoverability, and overall SEO performance while building credibility and increasing user engagement.
