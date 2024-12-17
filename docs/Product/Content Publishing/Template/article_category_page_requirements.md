# article category components
**Priority: High**  

## Overview  

The article category page acts as a content hub, offering an organised and accessible gateway for users to browse articles within a specific category. Categories are structured using article tags, and the page will display all articles assigned to a particular tag. Author pages will function similarly, effectively acting as tags to filter content authored by specific individuals. The page must balance user experience and search engine optimisation (SEO) to ensure seamless navigation, improved content discovery, and indexability.  

## Objectives  

- Enhance user engagement through intuitive design, rich visuals, and content previews.  
- Ensure crawlability for search engines with effective pagination and structured data.  
- Optimise performance for fast loading and responsive displays.  
- Facilitate content discovery with enhanced on-page features such as filtering, sorting, and search functionality.  

## Implementation Requirements  

### 1. Article Listings  

Each article displayed must include the following components:  

- **Display up to 30 articles on each page** to balance performance and usability.  

**Thumbnail Image**  
- Use optimised, compressed images for faster load times.  
- Use lazy loading (`loading="lazy"`) to defer off-screen images.  
- Link images directly to the full article page.  
- Include clear, descriptive alt text for accessibility and SEO.  
- Apply image placeholders (e.g., blurred loading effect) to improve perceived load time.  

**Title and Hyperlink**  
- Display the article title prominently.  
- Use semantic HTML (e.g., `<h2>` or `<h3>`) for clear page structure.  
- Ensure the title link has a hover effect (e.g., underlining, colour change).  

**Excerpt**  
- Provide a concise, original summary (50–100 words) of the article.  
- Avoid using the first paragraph verbatim to prevent content duplication.  
- Ensure truncation with ellipsis for uniformity in layout.  

**Estimated Reading Time**  
- Calculate the reading time based on an average of 200–250 words per minute.  
- Display it near the title or within the metadata section (e.g., “5 min read”).  

**Metadata**  
- **Publication Date**: Use `DD Month YYYY` format (e.g., 12 January 2024).  
- **Last Reviewed Date**: Optional; display if the article has been updated.  
- Display subtle metadata styling (smaller fonts, muted colours).  

**Tags and Categories**  
Tags serve as the primary method for structuring articles and categories on the page. Show clickable tags or subcategories beneath the excerpt to encourage further exploration.  
- Use visual pills, badges, or icons to distinguish tags.  

### 2. Design and On-Page Features  

**Layout Options**  
Provide two layout options for users to switch between:  
- **Grid View**: Thumbnails displayed with short excerpts.  
- **List View**: Larger excerpts for readers who prefer more detail.  

Maintain clear hierarchy:  
**Title > Image > Excerpt > Metadata (dates, tags, reading time).**  

**Filters and Sorting**  
Add dynamic filters and sorting options for improved content discovery:  
- **Sort By**: “Newest,” “Oldest,” “Most Popular,” “Shortest Read Time.”  
- **Filters**: Tags, subcategories, topics (multi-select), date range, and author.  

Tags are the primary method for structuring articles and categories on the page, while author filters function similarly to tags, ensuring consistency in functionality.  
- Use sticky or collapsible filters to maintain usability on mobile devices.  

**Search Functionality**  
Include a category-specific search bar above the article listings.  
- Use placeholder text (e.g., “Search articles in this category...”).  

**Article Card Visual Enhancements**  
- Ensure uniform thumbnail sizes with responsive image scaling.  
- Include reading indicators: E.g. Add a visual progress bar (e.g., thin line under the thumbnail) to denote estimated reading time.  

**Breadcrumb Navigation**  
Implement breadcrumbs at the top of the page for hierarchical navigation:  
`Home > Articles > Category`  
- Ensure breadcrumbs reflect the tag-based structure for consistency with content organisation and filtering.  
- Style breadcrumbs subtly (e.g., smaller font with arrows `>` or slashes `/`).  

**Pagination Design**  
Design user-friendly, intuitive pagination controls:  
- Clearly labelled “Next,” “Previous,” and numbered pages.  
- Use infinite scroll as an optional feature with a “Load More” button for user control.  

When using a "Load More" button to fetch articles via an API, ensure that search engines can access all content by including standard paginated hyperlinks that reflect the tag and category structure for improved clarity and crawlability.  

**Call-to-Action (CTA)**  
Include CTAs for user engagement at strategic points:  
- **Newsletter Sign-Up**: “Stay updated with our latest articles.”  
- **Banner Space**: Include ad placement opportunities to promote relevant content or advertisements across specific article categories.  

### 3. Structured Data (Schema.org Markup)  

Ensure rich snippets and search engine comprehension with well-structured data.  
- Use `CollectionPage` or `ItemList` schema for article listings.  
- Ensure metadata (e.g., title, URL, image, publication dates) is included accurately.  
- Add support for `breadcrumbList` schema to enhance navigation visibility in search engines.  

### 4. Performance Optimisation  

- **Lazy Loading**: Apply lazy loading for images, embeds, and non-critical elements.  
- **Critical Asset Preloading**: Preload essential assets (e.g., fonts, hero images) for faster rendering.  
- **Responsive Image Delivery**: Use `srcset` and WebP/AVIF formats for optimal resolution across devices.  
- **Pagination Load Balance**: Limit content per page (10–20 articles) to prevent heavy page loads.  
- **Caching**: Implement browser and CDN caching for static resources.  

### Accessibility Features  

- Use semantic HTML tags (`<h2>`, `<nav>`, `<section>`) for screen reader compatibility.  
- Include high-contrast colour combinations for readability.  
- Provide descriptive alt attributes for all images.  

### Heading Tag Usage  

- Use a single `<h1>` for the main page title to maintain proper document hierarchy.  
- Use `<h2>` for article links (article titles) and section titles, and `<h3>` for subsections to create a logical structure.  

### Enhanced Design Best Practices  

- **Grid/List Toggle**: Allow users to toggle between grid and list views for personalised browsing preferences.  
- **Sticky Navigation and Filters**: Keep filters or the navigation bar sticky when scrolling, particularly on mobile.  
- Display the current page number clearly within the pagination element.  

## Conclusion  

By incorporating interactive features, strong design elements, and on-page enhancements, the article category page will not only provide a visually engaging experience but also improve usability, discoverability, and SEO performance.  

This approach ensures the page serves as an effective content hub, driving both user satisfaction and search engine visibility.  
