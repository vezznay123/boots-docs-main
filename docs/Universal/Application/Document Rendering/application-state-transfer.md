
# state transfer and hydration

**Priority**: Medium

## Overview

Given the complexity of the Boots application and the potential performance risks associated with excessive state management, it is essential to prioritise a design that minimises reliance on client-side state management libraries. State transfer and hydration refer to the process of managing and transferring application state between the server and the client, as well as rendering interactive components in the browser after an initial server-side render.

The goal is to ensure a high-performance, highly interactive user experience while maintaining efficient use of resources. Client-side state management libraries should only be employed strategically when necessary for application bootstrapping and ensuring seamless communication between front-end and back-end services.

## State Management Best Practices

### Minimising Client-Side State

- **Limit State Size**: If state management is employed, strictly control the size and loading time of the application state. Specifically, the state document should not exceed 20 KB and should load within 0.5 seconds. These limits help minimise the negative impact on client-side performance and maintain a seamless user experience.
- **Avoid Excessive Hydration**: Avoid unnecessary rehydration of static content on the client-side. Instead, prioritise dynamic components that require user interaction for hydration to minimise the amount of state and DOM that need to be rehydrated.
- **Selective Use of State Libraries**: Use state management libraries only for critical parts of the application that require it, such as initialising interactive features or managing complex application logic that cannot be easily managed server-side.

## State Management and Hydration Considerations

- **Hydration Script Optimisation**: The hydration script should only contain JSON values needed to keep the state in sync. Passing HTML and styles through the state object should be prevented, as this causes bloat that impacts payload size and processing efficiency.

1. **Improved Performance**: By limiting the amount of client-side state and avoiding unnecessary hydration, the application can load faster and use fewer resources, resulting in a more efficient user experience.
2. **Enhanced User Experience**: Minimising reliance on client-side state management reduces the risk of performance bottlenecks, ensuring a smoother and more responsive experience for users, especially during interactions.
3. **Optimised Resource Utilisation**: Limiting the size and complexity of the state document helps reduce the processing load on users' devices, making the application more accessible to users with varying hardware capabilities.
4. **Scalability**: By strategically using state management and optimising hydration, the application can scale more efficiently, handling a larger number of concurrent users without compromising performance.

## Conclusion

For the Boots website, adopting a strategic approach to state transfer and hydration ensures optimal performance while maintaining a highly interactive user experience. By focusing on server-side rendering for critical content, dynamically loading personalised components, and minimising client-side state, the application can provide a seamless experience for users without the performance penalties often associated with excessive client-side state management.
