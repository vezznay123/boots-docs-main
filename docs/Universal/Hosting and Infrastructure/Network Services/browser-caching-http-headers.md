
# browser caching

**Priority**: Medium

## Overview
Browser caching allows assets to be stored locally in a user's browser, reducing the need to repeatedly download the same files each time a page is loaded. This significantly improves load times and reduces the overall burden on the server. Different caching rules may need to be applied depending on whether content is being cached by a browser or a CDN.

## Best Practice

- **Predefined Caching Rules**: Set up predefined caching rules for different MIME types to manage caching durations effectively. Adjust these rules based on the requirements for browser caching versus CDN caching.

## MIME Types and Browser Cache Duration

- **text/css**: 1 month
- **application/javascript**: 1 week
- **image/jpeg**: 1 year
- **image/avif**: 1 year
- **image/png**: 1 year
- **image/gif**: 1 year
- **image/svg+xml**: 1 year
- **application/pdf**: 1 month
- **application/json**: 0 seconds (Do not cache)
- **audio/mpeg**: 1 year
- **video/mp4**: 1 year
- **font/woff2**: 1 year
- **application/x-font-ttf**: 1 year

## Caching Considerations

- **Different Rules for CDN vs Browser**: While CDN caching focuses on reducing latency globally by serving cached resources closer to users, browser caching focuses on reusing local copies of resources to avoid repeated downloads.
- **Review Cache Durations**: Cache durations should be carefully reviewed and tested to strike a balance between content freshness and performance. Content like `application/json` should not be cached to ensure users always receive up-to-date data.

## Benefits of Browser Caching

- **Reduced Server Load**: By storing assets locally, browser caching reduces the need for frequent requests to the server, improving performance during high traffic periods.
- **Faster Load Times**: Assets such as images, stylesheets, and scripts load much faster when they are served from the browser cache, leading to improved user experience.
- **Optimised User Experience**: A faster-loading site enhances the overall user experience, especially for returning visitors, as assets are already cached.

## Example Implementation

- **Server Configuration**: Define cache control headers for different file types to set the caching duration for browsers. Below is an example of Apache configuration:

  ```apache
  <FilesMatch "\.(css|js|jpg|jpeg|avif|png|gif|svg|pdf|mp3|mp4|woff2|ttf)$">
      Header set Cache-Control "max-age=2592000, public"
  </FilesMatch>

  # No caching for JSON
  <FilesMatch "\.json$">
      Header set Cache-Control "no-store, no-cache, must-revalidate, max-age=0"
  </FilesMatch>
  ```

## Crawler Accessibility
Browser caching has minimal direct impact on search engine crawlers, as they typically do not cache resources the way user browsers do. However, optimised page load times resulting from efficient caching can improve crawl efficiency and the overall SEO of the website.

## SEO Impact
Browser caching is an important aspect of improving page speed and Core Web Vitals scores, which are significant factors for search engine ranking. Faster page loads improve user engagement and reduce bounce rates, positively impacting SEO performance.
