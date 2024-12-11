
# url standardisation

**Priority**: High

## Overview

URL normalisation is the process of standardising URLs to improve consistency and optimise search engine ranking. By enforcing consistent URL patterns through HTTP redirection, it ensures that search engines see one canonical version of a page, avoiding duplicate content issues and improving SEO. The key URL normalisation rules include enforcing HTTPS, the use of the "www" subdomain, lower-case URLs, and removing trailing slashes.

## URL Normalisation Best Practices

- **Enforce HTTPS Protocol**: Redirect all HTTP requests to HTTPS to ensure secure data transfer and maintain consistency.
- **Enforce "www" Subdomain**: Redirect URLs without the "www" subdomain to include "www" to maintain consistency across URLs.
- **Enforce Lower-Case URLs**: Convert all URL strings to lower-case to avoid duplicate content issues that can arise from case sensitivity.
- **Strip Trailing Slashes**: Remove trailing slashes from URLs for consistency unless it is a directory.

## Example Implementations

### Enforce HTTPS Protocol

**Request:**

```
http://www.boots.com/example-page
```

**301 Redirection to:**

```
https://www.boots.com/example-page
```

### Enforce "www" Subdomain

**Request:**

```
https://boots.com/example-page
```

**301 Redirection to:**

```
https://www.boots.com/example-page
```

### Enforce Lower-Case URL Strings

**Request:**

```
https://www.boots.com/Example-Page
```

**301 Redirection to:**

```
https://www.boots.com/example-page
```

### Strip Trailing Slash from URLs

**Request:**

```
https://www.boots.com/example-page/
```

**301 Redirection to:**

```
https://www.boots.com/example-page
```

## Benefits of URL Normalisation

- **Improved SEO**: Ensures that search engines only index the canonical version of a URL, preventing duplicate content issues and improving overall rankings.
- **Consistency**: Uniform URLs across the website provide a consistent experience for users and search engines.
- **Enhanced User Trust**: Enforcing HTTPS for all URLs enhances user trust by ensuring secure communication between the server and the user's browser.

## SEO Impact

Implementing URL normalisation helps search engines correctly index content by providing a single, canonical URL for each page. This avoids diluting link equity across multiple versions of a URL and leads to better rankings. HTTPS redirection also helps in meeting security requirements, which is a ranking signal for search engines.
