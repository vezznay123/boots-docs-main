
# server-side tracking

**Priority**: Low

## Overview
Server-side tracking involves setting up a server-side Google Tag Manager (GTM) container to handle tracking events and tags. Instead of directly sending tracking data from the client side, the data is sent to a server-side container, which then processes and forwards it to analytics or marketing platforms. This approach helps improve data security and reduces the impact of tracking scripts on client-side performance.

## Implementation Steps

- **Set Up a Server-Side GTM Container**: Create and configure a GTM container specifically for server-side tracking to handle and forward incoming events.
- **Send Events from Client-Side DataLayer**: Push events from the client-side dataLayer to the server-side container to centralise data handling.
- **Configure Tags in the Server-Side Container**: Define the tags within the server-side container to control what data is sent to third-party tools.

## Benefits on Performance

- **Reduced Client-Side Load**: Offloading tracking scripts to the server reduces the number of third-party scripts running in the browser, resulting in faster page load times.
- **Improved User Experience**: Since the tracking workload is moved to the server, it reduces resource consumption on the client device, leading to a smoother browsing experience.
- **Lower Impact on Core Web Vitals**: By reducing the number of client-side scripts, server-side tracking has a positive impact on metrics like Largest Contentful Paint (LCP) and First Input Delay (FID).
- **Increased Data Accuracy**: Server-side tracking reduces the risk of data being blocked by ad blockers or browser restrictions, leading to more reliable and complete tracking data.

## Example Setup

- **Client-Side Event**: A button click event is pushed to the dataLayer.
- **Server-Side Handling**: The server-side container receives the event, processes it, and sends it to Google Analytics.

## Crawler Accessibility
Server-side tracking has minimal impact on crawlers since it reduces the number of client-side scripts. This improves crawlability by ensuring faster page loads and fewer obstacles for search engines.

## SEO Impact
Implementing server-side tracking helps optimise page speed and enhances the overall user experience. These improvements in site performance contribute to better Core Web Vitals scores and, consequently, improved search engine rankings.
