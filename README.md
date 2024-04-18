# Design for an Ecommerce Website Using Flask

## HTML Files
- **index.html**: This serves as the homepage of the website.
  - Contains links to pages for product listing, cart, and checkout.
  - Displays a banner or carousel to highlight featured products.

- **products.html**: Lists all available products.
  - Each product includes an image, name, price, and "Add to Cart" button.
  - Supports filtering and sorting of products.

- **cart.html**: Displays the contents of the user's shopping cart.
  - Shows the product image, name, quantity, and subtotal.
  - Includes options to update quantities, remove items, and proceed to checkout.

- **checkout.html**: Allows users to complete the checkout process.
  - Collects billing and shipping information.
  - Processes payment and generates an order confirmation.

## Routes

- **Home Page**:
  - `@app.route('/')`
  - Renders the `index.html` template.

- **Product Listing**:
  - `@app.route('/products')`
  - Renders the `products.html` template, passing in the product data.

- **Add to Cart**:
  - `@app.route('/add_to_cart/<product_id>')`
  - Adds the specified product to the user's cart and redirects to the `cart.html` page.

- **View Cart**:
  - `@app.route('/cart')`
  - Renders the `cart.html` template with the current cart items.

- **Checkout**:
  - `@app.route('/checkout')`
  - Renders the `checkout.html` template.

- **Process Payment**:
  - `@app.route('/process_payment', methods=['POST'])`
  - Handles the payment processing logic and redirects to the order confirmation page.