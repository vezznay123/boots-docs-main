# related product recommendations

**Priority:** medium

**Overview**
Related product recommendations are crucial for improving user experience and boosting conversions. Displaying products that are similar or complementary to the current product can increase the average order value and help users discover more of what Boots offers. Implementing well-placed recommendations throughout the user journey can also improve internal linking and overall SEO value.

**Implementation Requirements**

1. **Product Detail Page Recommendations**
   - **Similar Products:** Include a section for related or similar products on the Product Detail Page (PDP). These recommendations should be based on factors such as product category, attributes, or customer behaviour.

#### Related Content: Customers Who Bought This Item Also Bought
**Priority:** Medium

**Overview**
Create opportunities for further navigation within the site by offering recommendations for products frequently bought together. This helps guide users to discover additional products, potentially increasing the average order value and improving internal linking.

**Implementation Requirements**

1. **Internal Linking Opportunities:** Create opportunities for further navigation within the site through internal links grouped under 'Customers Also Bought' linking components.
2. **Data-Driven Selection:** Utilise sales data to identify the top 15 products frequently purchased alongside the current product.
3. **Initial Display:** Embed these 15 related products directly within the initial HTML response, ensuring immediate visibility upon page load.
4. **Carousel Presentation:** Showcase these products in a horizontally swipeable carousel, each card displaying the product image, name, average review rating, price, and any applicable "Advantage Card" discount.
5. **Lazy Loading:** Implement client-side lazy loading to fetch and append an additional 20 related products to the carousel upon user interaction (e.g., scrolling or swiping to the end). This data should be retrieved via an API call to optimise initial page load performance.

#### Related Content: Customers Who Viewed This Also Viewed
**Priority:** Medium

**Overview**
Guide users to similar products by offering recommendations based on browsing behaviour. This strategy can help retain user interest and provide contextually relevant product options, improving the likelihood of conversion.

**Implementation Requirements**

1. **Internal Linking Opportunities:** Create opportunities for further navigation within the site through internal links grouped under 'Customers Who Viewed This Also Viewed' linking components.
2. **Data-Driven Selection:** Analyse related product data to identify the top 15 products with both high sales volume and high-profit margins. This selection should prioritise products that are relevant to the current product being viewed.
3. **Initial Display:** Embed these 15 recommended products directly within the initial HTML response, ensuring immediate visibility upon page load.
4. **Carousel Presentation:** Showcase these products in a horizontally swipeable carousel, each card displaying the product image, name, average review rating, price, and any applicable "Advantage Card" discount.
5. **Lazy Loading:** Implement client-side lazy loading to fetch and append an additional 20 recommended products to the carousel upon user interaction (e.g., scrolling or swiping to the end). This data should be retrieved via an API call to optimise initial page load performance.

**Best Practices**

- **Maintain Relevance:** Ensure that recommended products are highly relevant to the current product to maximise engagement.
- **Use Sales Data:** Leverage historical sales and browsing data to make recommendations that are more likely to lead to conversions.
- **Optimise for Mobile:** Ensure that recommendation carousels are fully responsive and provide a smooth experience on all devices.

**Benefits of Related Product Recommendations**

- **Increased Average Order Value:** Cross-selling and upselling related products can lead to higher order values.
- **Improved User Engagement:** Providing relevant product recommendations helps users discover more products, increasing the time spent on site and the likelihood of conversion.
- **Enhanced Internal Linking:** Well-implemented recommendations create more internal links, which can improve SEO performance by helping search engines better understand site structure.

**Conclusion**
Implementing related product recommendations effectively is a powerful way to improve user experience, drive conversions, and enhance SEO. By strategically placing related content on PDPs and utilising data-driven carousels, Boots can increase customer satisfaction and sales while optimising site navigation.
