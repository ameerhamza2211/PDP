My Task Summary

I set up a custom curtain product page in Shopify where customers can select the Width from a dropdown, and the system automatically connects it to the correct Fabric Panel variant in the background. This helps show the right price dynamically.

What I Did

1- Product Setup

    In Shopify admin, I created a product with two variant options:

       - Fabric Panels (1, 2, 3, 4)

       - Drop (100cm, 120cm, 140cm, 180cm)

    Then I added all variant combinations and set their final prices.

2- Metafield Setup

        I went to Settings → Custom data → Products and created a metafield called Width to Panel Map with type JSON.

        On the product, I added a JSON mapping that connects width ranges to fabric panels (for example, “Up to 120cm” = “1 panel”, “121cm–180cm” = “2 panels”).

3- Custom Dropdown on Product Page

        In the theme code (product-variant-picker.liquid), I added a new dropdown for Width that uses the metafield data.

        I hide the original Fabric Panels option so customers only see the Width selector, not the panel count.

4- JavaScript Functionality

        In the main-product.liquid section, I added a small script that listens for changes in the Width dropdown.

        When a customer selects a Width, the script automatically updates the hidden Fabric Panels dropdown with the correct value and triggers Shopify’s price update system.

5- Final Result

Now the product page shows a clean and simple Width dropdown.
When a user selects a Width, it automatically selects the right Fabric Panel variant in the background and updates the price instantly, without showing the customer any extra fields.
