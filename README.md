

# Pulling Products from a Collection in Shopify

## Explanation

### Pulling Products from a Collection:
- I use the `assign` tag to define `collection_handle`, which references the handle of a specific collection in my Shopify store.
- The second `assign` statement fetches the collection's products using `collections[collection_handle]`.
- I use the `if` block to check whether the collection contains products (i.e., `collection.products.size > 0`).

### Looping Through Products:
- Inside the loop (`for product in collection.products`), each product's details are accessed and displayed. The details include:
  - Product image
  - Title
  - Price
  - Variant ID

### HTML Structure:
- A grid layout is used for displaying the products, with each product wrapped in a `product-card` `<div>`.
- Each product card contains:
  1. A link to the product page: `{{ product.url }}`
  2. The product image: `{{ product.featured_image | img_url: 'medium' }}`
  3. The product title: `{{ product.title }}`
  4. The product price formatted as currency: `{{ product.price | money }}`
  5. An "Add to Cart" button with a form that submits the selected product variant to the cart.

### Error Handling:
- If no products are found in the collection, an error message is displayed:



# Explanation of CSS for Product List

## Styles for the Product List Section

### `.products-list-section`:
- Add padding and background color to the entire product list section to enhance the overall layout.

### `.products-wrapper`:
- Centers the content within a maximum width of 1200px.
- Uses auto margins to ensure proper alignment in the center of the page.

### `.products-grid`:
- Displays products in a flexible grid layout.
- Provides gaps between the product cards to give a neat and organized appearance.

### `.product-card`:
- Add padding to create space inside each product card.
- Provides a border and background color to make the product card stand out.
- Ensures a clean and structured display for each product.

### `.product-image`:
- Ensures that the product image fits the container.
- Maintains the aspect ratio of the image to avoid distortion.

### `.product-title` & `.product-price`:
- Styles the product title and price with appropriate font sizes.
- Ensures proper spacing between the title and price for readability.

### `.add-to-cart-btn`:
- Styles the "Add to Cart" button with:
  - A blue background.
  - White text for contrast and readability.
  - Hover effects to enhance user interaction and make the button visually engaging.
