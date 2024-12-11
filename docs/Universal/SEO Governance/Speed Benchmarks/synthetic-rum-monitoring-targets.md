
# synthetic & rum monitoring

**Priority**: High

## Overview
Synthetic and Real User Monitoring (RUM) are complementary approaches for measuring website performance. Synthetic monitoring simulates user interactions to test predefined scenarios, while RUM measures the actual experiences of real users. Together, these metrics provide a comprehensive understanding of a website's performance across multiple phases, from connection to user interaction.

## Monitoring Phases & Metrics

### 1. Connection Phase
- **DNS Resolution Time**
  - **Good**: ≤ 100 milliseconds
  - **Needs Improvement**: 100 - 500 milliseconds
  - **Poor**: > 500 milliseconds

- **TCP Connection Time**
  - **Good**: ≤ 100 milliseconds
  - **Needs Improvement**: 100 - 500 milliseconds
  - **Poor**: > 500 milliseconds

- **SSL Handshake Time**
  - **Good**: ≤ 300 milliseconds
  - **Needs Improvement**: 300 - 600 milliseconds
  - **Poor**: > 600 milliseconds

- **Initial Connection Time**
  - **Good**: ≤ 100 milliseconds
  - **Needs Improvement**: 100 - 300 milliseconds
  - **Poor**: > 300 milliseconds

### 2. Response Phase
- **Time to First Byte (TTFB)**
  - **Good**: ≤ 200 milliseconds
  - **Needs Improvement**: 200 - 600 milliseconds
  - **Poor**: > 600 milliseconds

- **Server Response Time**
  - **Good**: ≤ 200 milliseconds
  - **Needs Improvement**: 200 - 600 milliseconds
  - **Poor**: > 600 milliseconds

- **Payload Size**
  - **Good**: ≤ 100 KB
  - **Needs Improvement**: 100 - 500 KB
  - **Poor**: > 500 KB

- **Download Time**
  - **Good**: ≤ 1 second
  - **Needs Improvement**: 1 - 3 seconds
  - **Poor**: > 3 seconds

- **Number of HTTP Requests**
  - **Good**: ≤ 50
  - **Needs Improvement**: 50 - 100
  - **Poor**: > 100

### 3. Loading Phase
- **DOM Content Loaded (DCL) Time**
  - **Good**: ≤ 1 second
  - **Needs Improvement**: 1 - 3 seconds
  - **Poor**: > 3 seconds

- **Page Weight (Total Size)**
  - **Good**: ≤ 1 MB
  - **Needs Improvement**: 1 MB - 3 MB
  - **Poor**: > 3 MB

- **Resource Load Time (for critical resources)**
  - **Good**: ≤ 1 second
  - **Needs Improvement**: 1 - 3 seconds
  - **Poor**: > 3 seconds

- **JavaScript Load Time**
  - **Good**: ≤ 1 second
  - **Needs Improvement**: 1 - 2 seconds
  - **Poor**: > 2 seconds

### 4. Rendering Phase
- **Largest Contentful Paint (LCP)**
  - **Good**: ≤ 2.5 seconds
  - **Needs Improvement**: 2.5 - 4.0 seconds
  - **Poor**: > 4.0 seconds

- **First Contentful Paint (FCP)**
  - **Good**: ≤ 1.8 seconds
  - **Needs Improvement**: 1.8 - 3 seconds
  - **Poor**: > 3 seconds

### 5. User Interaction Phase
- **First Input Delay (FID)**
  - **Good**: ≤ 100 milliseconds
  - **Needs Improvement**: 100 - 300 milliseconds
  - **Poor**: > 300 milliseconds

- **Time to Interactive (TTI)**
  - **Good**: ≤ 3.8 seconds
  - **Needs Improvement**: 3.8 - 7.3 seconds
  - **Poor**: > 7.3 seconds

- **Total Blocking Time (TBT)**
  - **Good**: ≤ 200 milliseconds
  - **Needs Improvement**: 200 - 600 milliseconds
  - **Poor**: > 600 milliseconds

- **DOM Interactive Time**
  - **Good**: ≤ 2 seconds
  - **Needs Improvement**: 2 - 4 seconds
  - **Poor**: > 4 seconds

### 6. Post-Load Phase
- **Time to Fully Loaded**
  - **Good**: ≤ 5 seconds
  - **Needs Improvement**: 5 - 10 seconds
  - **Poor**: > 10 seconds

- **Asset Caching**
  - **Good**: ≥ 80% of assets cached
  - **Needs Improvement**: 50% - 80% of assets cached
  - **Poor**: < 50% of assets cached

- **Perceived Load Time**
  - **Good**: ≤ 3 seconds
  - **Needs Improvement**: 3 - 5 seconds
  - **Poor**: > 5 seconds

## Best Practices

- **Monitor Regularly**: Use a combination of synthetic and RUM tools to assess performance across different stages of the page lifecycle.
- **Set Benchmarks**: Use industry benchmarks as a guide and continually strive to achieve the 'Good' range for all metrics.
- **Optimise Critical Phases**: Focus on improving connection times, server responses, and rendering times for a seamless user experience.

## Example Performance Analysis

- **DNS Resolution Time**: Achieved 90ms, which falls under the 'Good' threshold.
- **First Input Delay (FID)**: Measured at 120ms, indicating 'Needs Improvement' for optimal user interaction.

## Crawler Accessibility
Synthetic and RUM monitoring ensure that a website performs well not only for users but also for search engine crawlers, contributing to better indexing and overall SEO.

## SEO Impact
Consistently good performance metrics across all phases lead to better user experiences and stronger SEO rankings. Faster loading times, improved interaction, and efficient asset caching help reduce bounce rates and increase user engagement.
