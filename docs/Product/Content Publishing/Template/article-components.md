# Article Information

**Priority:** Medium  

## Overview  
Article components should provide clear, contextual information to enhance user experience. In addition to the existing items—estimated read time, original publish date, last reviewed date, and author bio—ensure that the article page includes:  
- A hyperlink to the author’s profile page.  
- A reference to the reviewer (if applicable), including a hyperlink to their profile or bio.  
- Display of both the publish date and the most recent review date.  

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

---

## Benefits  

### Enhanced User Experience  
- Clear metadata and author/reviewer references build trust.  

### Credibility  
- Linking to author and reviewer profiles adds transparency and authority.  

### Engagement  
- Structured data may improve search engine visibility, potentially increasing readership.  

---

## Conclusion  
By including a hyperlink to the author’s profile, a reviewer reference and link to their bio, and prominently displaying publish and last review dates, the article page will provide greater clarity, trust, and engagement for the user. Implementing structured data further supports discoverability and ensures that search engines and readers alike fully understand the article’s credibility and currency.
