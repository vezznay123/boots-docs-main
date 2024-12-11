
# content delivery networks

**Priority**: Medium

## Overview
A Content Delivery Network (CDN) is a distributed network of servers designed to optimise the delivery of web content to users. For headless applications, CDNs can be applied across different parts of the technology stack to enhance performance, scalability, and user experience. The primary advantage of using a CDN in this context is leveraging caching to accelerate response times and reduce server load.

## Main Requirements

- **Traffic & Bot Management**: Ensure effective traffic management by detecting and mitigating bot traffic, which helps in securing the application and optimising performance.
- **Global Zones**: Distribute content across global locations to minimise latency and ensure users receive content from the nearest server.
- **Response Caching**: Cache responses at edge locations to reduce server load, decrease latency, and provide quicker response times.
- **Delivery Optimisation**: Optimise content delivery, particularly for headless applications, to ensure assets are quickly available across different parts of the technology stack.

## Importance of Caching

The use of caching is the most valuable aspect of implementing a CDN. Caching content at edge servers allows for:

- **Reduced Server Load**: By serving cached content, the main server is accessed less frequently, which helps in maintaining better performance, especially during high-traffic periods.
- **Faster Content Delivery**: Cached assets are delivered from edge servers closer to the user, reducing latency and improving the overall user experience.
- **Scalability**: Efficient caching allows the application to handle more users simultaneously without significant degradation in performance.

## Cache Duration for MIME Types

The cache duration for each MIME type should be carefully configured to balance performance and data freshness. Below are the recommended cache durations:

- **text/css**: 1 month
- **application/javascript**: 3 days
- **image/jpeg**: 1 year
- **image/avif**: 1 year
- **image/png**: 1 year
- **image/gif**: 1 year
- **image/svg+xml**: 1 year
- **application/pdf**: 1 month
- **application/json**: 12 hours
- **audio/mpeg**: 1 month
- **video/mp4**: 1 year
- **font/woff2**: 1 year
- **application/x-font-ttf**: 1 year
- **text/html**: 6 hours (to be discussed)

### Caching Considerations

Long cache times should always be used in conjunction with validation functionality, such as ETag or Last-Modified headers, to ensure content remains up to date. Different caching rules should be applied to different caching layers throughout the application infrastructure, including edge servers, browser caches, and server-side caches. This layered caching approach helps ensure both optimal performance and data freshness.

## Example CDN Usage

- **Static Content Caching**: Images, stylesheets, and JavaScript files are cached at edge locations to ensure rapid loading for all users.
- **API Response Caching**: Frequently accessed API responses can be cached to reduce the load on backend servers and improve data retrieval times.

## Crawler Accessibility
CDNs help in maintaining website performance even during peak loads, which means that search engine crawlers can efficiently access and index content without encountering performance issues.

## SEO Impact
Implementing a CDN with effective caching enhances page speed and reduces latency, leading to improved Core Web Vitals metrics and better search engine rankings. Faster page loads and reduced response times help retain users, leading to better engagement and lower bounce rates.
