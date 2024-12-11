
# transfer protocols

**Priority**: Low

## Overview
HTTP transfer protocols determine how data is transmitted over the internet. Using modern protocols like HTTP/2 or HTTP/3 enhances website performance and security by making data transmission faster and more efficient compared to older versions of HTTP.

## Best Practice

- **Protocol Upgrade**: The protocol used by both the origin server and application should be HTTP/2 or higher (such as HTTP/3).

## Benefits of HTTP/2 and HTTP/3

- **Multiplexing**: HTTP/2 allows multiple requests and responses to be sent concurrently over a single connection, reducing latency and improving load times.
- **Header Compression**: HTTP/2 includes header compression, which reduces the overhead of HTTP headers, leading to faster data transfer.
- **Connection Reuse**: HTTP/2 and HTTP/3 allow a single connection to be used for multiple resources, resulting in fewer open connections and a reduction in resource consumption.
- **Faster and More Reliable**: HTTP/3 is based on QUIC, which uses UDP rather than TCP, making connections faster and more reliable, especially for mobile users and unstable networks.

## Example Implementation

- **Upgrade Origin Server**: Ensure that the origin server supports HTTP/2 or HTTP/3. Most modern web servers (e.g., Apache, Nginx) support these protocols with configuration adjustments.
- **CDN Configuration**: Confirm that the Content Delivery Network (CDN) used for your application also supports HTTP/2 or HTTP/3 for optimal performance.

## Crawler Accessibility
Using HTTP/2 or HTTP/3 helps search engine crawlers access resources more efficiently, leading to improved crawling speed and better indexing of content.

## SEO Impact
Enhanced data transmission via HTTP/2 or HTTP/3 results in faster load times, improved Core Web Vitals, and better user experience—all of which are critical ranking factors for search engines.
