
# error management: 5xx

**Priority**: High

## Overview

Handling 5XX errors, particularly 500 errors, is important for maintaining user trust and ensuring a smooth user experience even during server issues. A well-designed 500 error page can provide users with helpful navigation options and avoid frustration when the server is experiencing difficulties.

## Best Practices for 500 Error Page Design

- **HTTP Status Code**: Ensure that the server returns a `500 Internal Server Error` status code for server-related issues. This helps search engines properly identify and handle server errors.
- **Stay on Requested URL**: Load the 500 page on the same URL without redirection. This avoids confusion for users and search engines.
- **Clear Error Message**: Provide a friendly and clear message informing users that there is a server issue. Use language that is approachable and suggests that the issue is temporary.
- **Call to Action (CTA)**: Include prominent CTAs to help users find other valuable content. Links to the homepage, popular pages, or support are good options.
- **Search Bar**: Include a search bar directly on the 500 page, allowing users to easily find alternative content.
- **No Canonicalisation**: Avoid adding a canonical tag on 500 error pages. This prevents search engines from misunderstanding the purpose of the page.
- **Analytics Tracking**: Implement tracking for 500 errors to monitor server issues and understand where users are encountering problems. This helps in proactively resolving server-side issues and improving the overall stability of the website.

## Example 500 Page Layout

### Elements to Include:

1. **Friendly Error Message**:
   ```
   Oops! Something went wrong on our end. Please try again later.
   ```

2. **Call to Action Links**:
   - **Homepage**: A link back to the homepage to allow users to start fresh.
   - **Popular Pages**: Links to popular or recently updated pages to guide users to content that may still be available.
   - **Support**: A link to contact support for further assistance.

3. **Search Bar**:
   - A search bar prominently placed on the page to help users find relevant content quickly.

4. **Visual Design**:
   - Include an engaging image or graphic to make the page feel less like an error and more like a temporary inconvenience.

## Benefits of Effective 500 Error Management

- **Improved User Trust**: A well-designed 500 page helps users understand that the issue is temporary and provides them with options to continue their journey on the website, reducing frustration.
- **Proactive Issue Resolution**: Analytics tracking provides insight into server issues, allowing for proactive resolution and improving the overall stability of the website.
- **Reduced Bounce Rates**: By providing navigation options, users are more likely to stay on the site rather than leave, which helps in maintaining engagement.

## SEO Impact

Handling 500 errors correctly ensures that search engines recognise server issues without penalising the site for content quality problems. By providing helpful navigation elements, users are encouraged to explore other areas of the website, which can help mitigate the negative impact of server errors on user experience and SEO.
