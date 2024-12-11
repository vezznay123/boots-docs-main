# related products (category id) for product listing page

    **Priority:** Medium

    **Overview:**
    Related products enhance the user experience by suggesting additional items of interest, potentially increasing sales. This feature allows administrators to override default related product logic with a specific category ID.

    **Implementation Requirements:**

    1. **Default Related Products Logic:**
       - Define the default method for determining related products (e.g., same category, shared attributes).

    2. **Category ID Override Field:**
       - Add a field for inputting the desired category ID for related products.
       - Validate input and optionally provide a dropdown menu for selection.
       - Ensure the manually selected category ID takes precedence over default logic.

    3. **UI Indication:**
       - Clearly indicate when a category ID override is set.
       - Display a message if no override is provided, indicating default logic use.

    4. **Fallback Behaviour:**
       - Define behaviour if no products are found (e.g., hide section, display message, or show fallback products).

    **Best Practices:**

    - Ensure related products are relevant and add value.
    - Regularly review and update related product links.
    - Optimize layout for user engagement.

    **Benefits:**

    - Enhances user experience with relevant product suggestions.
    - Increases potential sales through cross-selling.
    - Provides flexibility for administrators to customize related products.

    **Conclusion:**
    Related products are essential for enhancing user experience and increasing sales, offering control over product suggestions.
