
# robots.txt

**Priority**: High

## Overview

The `robots.txt` file is a critical component for controlling how search engine crawlers interact with your website. Proper management of this file ensures that search engines can access important parts of the website while restricting access to areas that should not be indexed. Managing the `robots.txt` file through a content management system (CMS) or Salesforce Commerce Cloud allows for easier updates and greater consistency.

## Best Practices for Robots.txt Management

- **Centralised Management**: Manage the `robots.txt` file within Salesforce Commerce Cloud or a content management platform to streamline updates. This approach ensures that all changes are centrally controlled, reducing the risk of errors.
- **Automated Overwriting**: Configure the CMS or Commerce Cloud platform to automatically create or overwrite the existing `robots.txt` file on the server, ensuring that any manual changes are not inadvertently overwritten.
- **Consistent Updates**: Schedule regular reviews of the `robots.txt` file to ensure that any new pages, directories, or features are appropriately included or excluded from crawling.

## Example Robots.txt Configuration

```plaintext
User-agent: *
Disallow: /checkout/
Disallow: /account/
Disallow: /admin/
Allow: /products/

Sitemap: https://www.boots.com/sitemap.xml
```

In this example:

- **Disallow**: Blocks crawlers from accessing sensitive pages like checkout, account, and admin areas.
- **Allow**: Allows crawlers to access the products section, which is important for indexing product pages.
- **Sitemap**: Provides a link to the XML sitemap, helping search engines discover the important URLs.

## Benefits of Centralised Robots.txt Management

- **Consistency**: Managing the `robots.txt` file through a central platform ensures consistent updates across all environments, reducing the chance of discrepancies.
- **Reduced Manual Errors**: Automating the creation and management of the `robots.txt` file minimises the likelihood of human errors that could lead to accidental blocking or unintentional exposure of sensitive areas.
- **Simplified Updates**: The use of a CMS or Salesforce Commerce Cloud allows non-technical users to update the `robots.txt` file without needing direct server access.

## SEO Impact

Proper management of the `robots.txt` file helps guide search engines to the content that should be indexed while restricting access to sensitive or redundant areas. This ensures that search engines focus their resources on the most valuable parts of the website, leading to better crawl efficiency and improved SEO performance.
