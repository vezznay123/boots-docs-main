
# tag & content validation

**Priority**: Medium

## Overview
The SEO Tags & Configuration Integrity Check is an automated test conducted during the build of the application. This test ensures that SEO tags and their respective values match the expected predefined outcomes, ensuring proper configuration and adherence to SEO standards.

## Best Practices

- **Define Expected SEO Tags**: Ensure that all expected SEO tags (such as meta titles, meta descriptions, canonical tags, etc.) are predefined for every page.
- **Automated Testing**: Implement automated tests to verify the presence and accuracy of SEO tags against predefined criteria.
- **Regular Updates**: Continuously update the expected outcomes for SEO tags to align with any changes made to the content or SEO strategy.

## Example Test Criteria

- Verify that the `<title>` tag matches the expected page title.
- Ensure the `<meta name="description">` value matches the predefined description for each page.
- Confirm that canonical tags are present and accurately reference the correct URL.

## Crawler Accessibility
Maintaining accurate SEO tags ensures that search engine crawlers can correctly index and rank pages, enhancing visibility and search relevance.

## SEO Impact
Accurate and consistent SEO tags help maintain the integrity of a website's SEO strategy, ensuring that pages are properly indexed and ranked, thereby maximising organic traffic and preventing misconfiguration issues.
