
# product data carousels

**Priority**: Low

## Overview

Category listing pages often contain multiple products or articles that can benefit from enhanced presentation in search engine results through carousel structured data. Implementing a carousel for category pages helps display multiple related products in a single search listing, increasing visibility and the likelihood of user engagement. Carousel structured data, specifically using JSON-LD format, can help highlight products, collections, or specific articles from your category pages in an engaging manner.

## Carousel Structured Data Implementation

Carousel structured data should be deployed to provide search engines with information about the list of products available on a category listing page. By properly implementing `ItemList` structured data, you enable the category to be indexed with better clarity, which allows search engines to feature it as a carousel in the results, potentially driving higher click-through rates.

### 1. JSON-LD Structured Data for Carousels

- **@context**: Set the context to `"https://schema.org/"`.
- **@type**: Use the type `"ItemList"` for carousels that link multiple items.
- **itemListElement**: A list of individual product items that will be presented in the carousel. Each product is represented by a `"ListItem"` object.

### Example JSON-LD for Category Listing Carousel

The following example illustrates how to mark up a category page with JSON-LD so that it may be eligible for a carousel display in Google Search results:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "ItemList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "item": {
        "@type": "Product",
        "name": "Moisturizing Cream",
        "url": "https://example.com/beauty/moisturizing-cream",
        "image": "https://example.com/photos/moisturizing-cream.jpg",
        "description": "A rich moisturizing cream that hydrates and nourishes your skin.",
        "sku": "MC123",
        "brand": {
          "@type": "Brand",
          "name": "BeautyBrand"
        },
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "25.99",
          "availability": "https://schema.org/InStock"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 2,
      "item": {
        "@type": "Product",
        "name": "Facial Cleanser",
        "url": "https://example.com/beauty/facial-cleanser",
        "image": "https://example.com/photos/facial-cleanser.jpg",
        "description": "Gentle facial cleanser for daily use.",
        "sku": "FC234",
        "brand": {
          "@type": "Brand",
          "name": "BeautyBrand"
        },
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "15.99",
          "availability": "https://schema.org/InStock"
        }
      }
    },
    {
      "@type": "ListItem",
      "position": 3,
      "item": {
        "@type": "Product",
        "name": "Anti-Aging Serum",
        "url": "https://example.com/beauty/anti-aging-serum",
        "image": "https://example.com/photos/anti-aging-serum.jpg",
        "description": "Anti-aging serum that helps reduce fine lines and wrinkles.",
        "sku": "AS345",
        "brand": {
          "@type": "Brand",
          "name": "BeautyBrand"
        },
        "offers": {
          "@type": "Offer",
          "priceCurrency": "USD",
          "price": "45.99",
          "availability": "https://schema.org/InStock"
        }
      }
    }
  ]
}
</script>
```

### Key Elements to Include

1. **Product Representation**: Use the `"Product"` schema type to represent each product within the list.
2. **Positioning**: Each product should have a `"position"` key within `"ListItem"`, indicating its rank in the carousel (starting from `1`).
3. **Essential Properties**:
   - **name**: The product name.
   - **url**: The canonical URL of the product.
   - **image**: URL to an image representing the product.
   - **description**: Brief description of the product.
   - **offers**: Detailed price and availability information.

### Best Practices

- **Relevancy**: Ensure that only highly relevant products are included in the list. The higher the relevancy, the more effective the carousel is at attracting clicks.
- **Accurate Information**: Make sure all attributes, including name, URL, image, and price information, are accurate and up-to-date to ensure a consistent experience across search results and product pages.
- **Proper Use of Positioning**: Assign positions correctly to ensure the order displayed in the carousel is consistent with the desired ranking on your category listing page.

## Conclusion

Using carousel structured data on category listing pages is an effective way to enhance visibility and user engagement through Google Search. By ensuring that relevant products are marked up correctly, your listings are more likely to be eligible for rich features, such as carousels, improving the overall search experience and increasing the chances of attracting visitors to your site.
