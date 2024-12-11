
# product structured data

**Priority**: High

## Overview

Including Product structured data in the `<head>` tag of product detail pages provides search engines with detailed product information, enhancing search visibility and providing rich snippets in search results. Product structured data helps search engines better understand the content, making your products more attractive and informative in search listings, ultimately driving higher click-through rates.

## Implementation Requirements

### 1. Basic Product Information

- **@context**: The schema context, set to `"https://schema.org/"`.
- **@type**: The type of schema, set to `"Product"`.
- **name**: The name of the product.
- **image**: An array of URLs to product images.
- **description**: A description of the product.
- **sku**: The stock keeping unit (SKU) of the product.
- **mpn**: The manufacturer part number of the product.
- **brand**: An object describing the brand of the product.
  - **@type**: The type of the brand, set to `"Brand"`.
  - **name**: The name of the brand.

### 2. Aggregate Rating

- **aggregateRating**: An object describing the aggregate rating of the product.
  - **@type**: Set to `"AggregateRating"`.
  - **ratingValue**: The average rating value.
  - **reviewCount**: The total number of reviews.

### 3. Product Attributes

- **color**: The colour of the product.
- **size**: The size of the product.
- **additionalProperty**: An array of additional property objects.
  - **@type**: Set to `"PropertyValue"`.
  - **name**: The name of the property.
  - **value**: The value of the property.

### 4. Product Variants (Offers)

- **offers**: An array of offer objects for product variants.
  - **@type**: Set to `"Offer"`.
  - **url**: The URL of the product variant.
  - **sku**: The SKU of the product variant.
  - **priceCurrency**: The currency of the price.
  - **price**: The price of the product variant.
  - **itemCondition**: The condition of the product variant (e.g., `"https://schema.org/NewCondition"`).

## Example Product Structured Data

Include the following JSON-LD script within the `<head>` tag of the product detail page:

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org/",
  "@type": "Product",
  "name": "Example Product Name",
  "image": [
    "https://example.com/photos/1x1/photo.jpg",
    "https://example.com/photos/4x3/photo.jpg",
    "https://example.com/photos/16x9/photo.jpg"
  ],
  "description": "This is an example product description.",
  "sku": "0446310786",
  "mpn": "925872",
  "brand": {
    "@type": "Brand",
    "name": "Example Brand"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.4",
    "reviewCount": "89"
  },
  "offers": {
    "@type": "AggregateOffer",
    "lowPrice": "119.99",
    "highPrice": "199.99",
    "priceCurrency": "USD",
    "offerCount": "5",
    "offers": [
      {
        "@type": "Offer",
        "url": "https://example.com/product",
        "priceCurrency": "USD",
        "price": "119.99",
        "priceValidUntil": "2024-12-31",
        "itemCondition": "https://schema.org/NewCondition",
        "availability": "https://schema.org/InStock",
        "seller": {
          "@type": "Organization",
          "name": "Example Store"
        }
      }
    ]
  },
  "color": "Red",
  "size": "M",
  "additionalProperty": [
    {
      "@type": "PropertyValue",
      "name": "Material",
      "value": "Cotton"
    },
    {
      "@type": "PropertyValue",
      "name": "Pattern",
      "value": "Solid"
    }
  ],
  "offers": [
    {
      "@type": "Offer",
      "url": "https://example.com/product/variant1",
      "sku": "0446310786-1",
      "priceCurrency": "USD",
      "price": "119.99",
      "itemCondition": "https://schema.org/NewCondition",
      "availability": "https://schema.org/InStock"
    },
    {
      "@type": "Offer",
      "url": "https://example.com/product/variant2",
      "sku": "0446310786-2",
      "priceCurrency": "USD",
      "price": "129.99",
      "itemCondition": "https://schema.org/NewCondition",
      "availability": "https://schema.org/InStock"
    }
  ]
}
</script>
```

## Conclusion

Implementing Product structured data helps search engines better understand your product information, which can lead to enhanced search result visibility, such as rich snippets or product carousels. This increased visibility improves the chances of attracting potential customers to your product pages.
