
### sponsored products

**Priority:** Medium

**Overview**
Sponsored products provide a route of navigation into promotional content, offering an additional opportunity for product exposure without directly impacting organic search visibility. This brief differs from other product recommendation features as the integration will be fully client-side loaded, which ensures crawler access can be blocked. This approach is beneficial for controlling how promotional content is indexed by search engines.

**Implementation Requirements**

1. **Client-Side Loading**
   - **Visibility Control:** Fetch and display sponsored product data exclusively on the client-side to minimise visibility to web crawlers. This helps ensure that sponsored content does not impact search engine indexing while still providing value to users.

2. **Data Selection**
   - **Relevant Sponsored Products:** Determine the first 10 relevant sponsored products related to the current Product Detail Page (PDP). The selection should focus on products that are complementary or likely to be of interest to users viewing the current product.

3. **Carousel Presentation**
   - **Display Sponsored Products:** Showcase these products in a horizontally swipeable carousel, with each card displaying the product image, name, average review rating, price, and any applicable "Advantage Card" discount.

4. **Lazy Loading**
   - **Incremental Product Loading:** Implement client-side lazy loading to fetch and append an additional 20 sponsored products to the carousel upon user interaction (e.g., scrolling or swiping to the end). The data should be retrieved via an API call to optimise initial page load performance.

**Best Practices**

- **Control Crawler Access:** Ensure that sponsored products are exclusively client-side loaded, preventing them from being crawled and indexed by search engines.
- **User Relevance:** Ensure that sponsored products are highly relevant to the current product to maximise engagement.
- **Optimise Performance:** Use lazy loading to minimise the impact on initial page load and keep the user experience smooth.

**Benefits of Sponsored Products**

- **Increased Visibility for Advertised Products:** Sponsored products provide an additional channel to highlight specific products, potentially driving more sales.
- **Maintains SEO Integrity:** By loading content client-side and restricting crawler access, the impact on organic search performance is minimised.
- **Engaging User Experience:** Carousels with sponsored products help keep users engaged, offering them related options without overwhelming them with irrelevant suggestions.

**Conclusion**
The implementation of sponsored products as a client-side feature ensures promotional items are visible to users without affecting SEO. By presenting these products in a responsive carousel and leveraging lazy loading, Boots can boost product exposure while maintaining an optimal user experience.
