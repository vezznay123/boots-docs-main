# article components

**Priority:** High

## Overview  
Article components should provide clear, contextual information to enhance user experience. In addition to the existing items—estimated read time, original publish date, last reviewed date, and author bio—ensure that the article page includes:  
- A hyperlink to the author’s profile page.  
- A reference to the reviewer (if applicable), including a hyperlink to their profile or bio.  
- Display of both the publish date and the most recent review date.  
- A navigational element to the article tags page using a **pill design**.  
- A **horizontal carousel** at the bottom of the article linking to related article content.  

## Implementation Requirements  

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
- Include a brief author bio beneath the article or in a dedicated author section.  
- Provide a hyperlink to the author’s full profile page, allowing readers to learn more about the author’s credentials, expertise, and other published works.  

### Reviewer Reference and Bio Link (If Applicable)  
- If the article is reviewed by a subject matter expert or editor, display their name and role.  
- Provide a hyperlink to the reviewer’s profile or biography page to establish credibility and transparency.  

### Article Tags Navigation (Pill Design)  
- Display article tags in a **pill design** beneath the article content.  
- Each tag should act as a hyperlink, taking users to the respective tag’s article page.  
- Use clear, distinct styling for the pills (e.g., rounded borders, muted background colours).  

### Related Article Carousel  
- Add a **horizontal carousel** at the bottom of the article to display related articles.  
- Include the following in each related article card:  
  - Thumbnail image (use `loading="lazy"` for optimisation).  
  - Title and a short excerpt or estimated reading time.  
  - A hyperlink to the related article page.  
- Ensure carousel navigation is smooth and user-friendly (e.g., arrow controls or swipe functionality).  

### Structured Data (Schema.org Markup)  
Where possible, support these elements with structured data for enhanced search visibility and richer search results. For instance:  

Use the **Article schema** to mark up the main article content.  
Include author as a structured data property:  

```json
"author": {
  "@type": "Person",
  "name": "Author Name",
  "url": "https://example.com/authors/author-name"
}
```

Include reviewedBy (using Review or Person as appropriate) to reference the reviewer:  

```json
"reviewedBy": {
  "@type": "Person",
  "name": "Reviewer Name",
  "url": "https://example.com/reviewers/reviewer-name"
}
```

Include navigation elements and related articles in structured data using `BreadcrumbList` and `relatedLink` schemas:  

```json
"relatedLink": [
  {
    "@type": "Article",
    "headline": "Related Article Title",
    "url": "https://example.com/articles/related-article-1"
  },
  {
    "@type": "Article",
    "headline": "Another Related Article",
    "url": "https://example.com/articles/related-article-2"
  }
]
```  

Use datePublished and dateModified for publish and last reviewed dates:  

```json
"datePublished": "2023-01-15",
"dateModified": "2023-06-10"
```

---

## Best Practices  

### Accuracy  
- Ensure all displayed dates (publish and last reviewed) are current and correct.  

### Clarity  
- Locate all these elements in a consistent and clear layout on the page.  

### Regular Updates  
- Review and update author and reviewer bios periodically to maintain accuracy.  

### Carousel Optimisation  
- Use lazy loading for images and limit the number of articles displayed initially to avoid performance issues.  

---

## Benefits  

### Enhanced User Experience  
- Clear metadata, tags navigation, and related content carousels improve content discovery and engagement.  

### Credibility  
- Linking to author and reviewer profiles adds transparency and authority.  

### Engagement  
- Structured data and visual enhancements encourage exploration of related content, improving session duration.  

---

## Conclusion  
By including a hyperlink to the author’s profile, a reviewer reference and link to their bio, navigational tags using pill design, and a related article carousel, the article page will provide greater clarity, trust, and engagement for the user. Implementing structured data further supports discoverability and ensures that search engines and readers alike fully understand the article’s credibility and currency.
