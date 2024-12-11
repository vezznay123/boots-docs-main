
# page rendering

**Priority**: Medium

## Overview

Page rendering involves different patterns that impact the user experience and search engine bot interaction. The choice of rendering pattern determines how quickly users see meaningful content and how well search engines can index the website. The primary rendering patterns are server-side rendering (SSR), client-side rendering (CSR), and hybrid rendering. Each of these patterns has specific advantages and drawbacks, depending on the content type and user requirements. Understanding the implications of these approaches helps in selecting the best strategy for both users and bots.

## Rendering Patterns Explained

### 1. Server-Side Rendering (SSR)

**Definition**: Server-side rendering is the process of generating the full HTML for a page on the server and delivering it directly to the browser. This technique is beneficial for loading static and core content rapidly, allowing search engines to quickly index key parts of the site.

**Benefits**:

- **SEO Optimisation**: SSR ensures that search engine crawlers receive complete HTML, which helps with effective indexing.
- **Faster First Contentful Paint (FCP)**: Since the content is generated server-side, users see meaningful content sooner, leading to better user experience and performance metrics.
- **Efficient Rendering for Static Content**: Ideal for static content such as product information, category details, and core landing pages.

### 2. Client-Side Rendering (CSR)

**Definition**: Client-side rendering involves generating the page content in the user's browser, typically using JavaScript frameworks. The HTML delivered is minimal, and JavaScript is used to populate the dynamic content.

**Benefits**:

- **Dynamic and Personalised Content**: CSR allows dynamic user interactions and personalised content to be loaded as needed, such as user-specific product recommendations or personal shopping carts.
- **Reduced Server Load**: CSR can offload some rendering tasks to the client, reducing the burden on the server.

### 3. Hybrid Rendering with Application Shell

**Definition**: Hybrid rendering, combined with an application shell pattern, leverages both server-side and client-side rendering to optimise the delivery of content. The application shell is a lightweight HTML, CSS, and JavaScript scaffold that loads quickly and provides a consistent base for the website. Static or essential content is rendered server-side, while personalised or dynamic content is rendered client-side.

**Benefits**:

- **Balanced Performance**: Provides fast initial page load times with the application shell pattern (cached on the edge) and SSR for static content, while allowing interactive, dynamic features to load seamlessly in the background using CSR.
- **Optimised SEO and User Experience**: Essential static content is made immediately available to crawlers, while dynamic content is added later for users, leading to better SEO performance and user engagement.
- **Service Worker Integration**: Service workers can intercept network requests and serve the cached application shell immediately, ensuring a rapid initial load while other content is fetched and rendered.

**Use Case**: For the Boots website, core product information and category data can be server-side rendered for faster load times and SEO purposes, while personalised recommendations and shopping cart updates are handled on the client-side. The application shell pattern ensures a rapid, consistent experience by caching the base structure at the edge.

## Rendering Strategy Recommendations

### Hybrid Rendering with Application Shell for Boots Website

- **Application Shell Pattern**: Use an application shell pattern cached on the edge to provide a quick initial load. The shell includes core UI elements such as the header, footer, and navigation, ensuring users see a consistent structure immediately.
- **Server-Side Rendering for Static Content**: Render the main body of the page, including product details and catalogue information, server-side. This ensures a fast initial load and improved SEO visibility.
- **Client-Side Rendering for Dynamic Content**: Use client-side rendering for personalised and dynamic content, such as user-specific recommendations or real-time price updates. This allows for a more engaging and responsive experience.

### CDN and Caching Integration

- **CDN Integration**: Cache HTML content on the Content Delivery Network (CDN) to improve performance and reduce server load.
- **Service Worker Caching**: Use Service Workers to cache static assets and frequently used API responses, implementing a stale-while-revalidate strategy to ensure users get fast content delivery while keeping data relatively fresh. The service worker can also intercept requests for the application shell and return it from the cache, ensuring a rapid load.
- **Background Updates**: Fetch updates for dynamic content in the background to enhance the user experience without interrupting page interaction.

### Cache Invalidation Strategies

- **Event-Driven Cache Invalidation**: Use event-driven cache invalidation based on webhooks from Salesforce Commerce Cloud to ensure the cache remains up-to-date when critical data changes. This ensures consistency across the site without unnecessary stale content.

## Advantages of the Recommended Strategy

1. **Improved SEO**: By serving static, crawlable content with SSR, search engines can easily index the website. Dynamic, user-specific content rendered on the client-side still provides a rich, personalised experience without compromising SEO.
2. **Better Performance**: SSR speeds up initial page loads, while CSR allows dynamic elements to load only when needed, resulting in faster interaction times and improved overall page performance.
3. **Scalability**: Hybrid rendering allows the website to handle large volumes of requests by leveraging CDN caching and service worker caching to reduce server strain and improve scalability during peak periods.
4. **Enhanced User Experience**: Users benefit from fast initial loads combined with smooth interactions, ensuring that the content they need is presented efficiently while more personalised features are dynamically loaded.

## Conclusion

Adopting a hybrid rendering strategy with an application shell offers a balance of speed, SEO, and dynamic capabilities. By utilising SSR for static content and CSR for personalised features, combined with an application shell cached at the edge and supported by a service worker, a website can effectively serve both users and search engine crawlers while maintaining high performance and scalability.
