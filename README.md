Sure! Here's the code in Markdown format for GitHub:

```markdown
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Laser Engraving Wood Products</title>
  <style>
    /* CSS styling */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: pink; /* Set background color to pink */
    }
    
    header {
      background-color: #333;
      color: #fff;
      padding: 20px;
    }
    
    main {
      max-width: 800px;
      margin: 0 auto;
      padding: 20px;
    }
    
    h1 {
      font-size: 24px;
    }
    
    .product {
      display: flex;
      margin-bottom: 20px;
    }
    
    .product img {
      width: 200px;
      height: auto;
      margin-right: 20px;
    }
    
    .product-info {
      flex-grow: 1;
    }
    
    .product-name {
      font-size: 20px;
      font-weight: bold;
      margin-bottom: 10px;
    }
    
    .product-description {
      margin-bottom: 10px;
    }
    
    .product-price {
      font-size: 18px;
      color: #333;
    }
    
    .cart {
      background-color: #f5f5f5;
      padding: 20px;
      margin-bottom: 20px;
    }
    
    .cart-item {
      margin-bottom: 10px;
    }
    
    .checkout-btn {
      background-color: #333;
      color: #fff;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <header>
    <h1>Welcome to Laser Engraving Wood Products</h1>
  </header>
  
  <main>
    <div class="product">
      <img src="product1.jpg" alt="Product 1">
      <div class="product-info">
        <div class="product-name">Wooden Coasters</div>
        <div class="product-description">Set of 4 laser-engraved coasters with intricate designs.</div>
        <div class="product-price">$19.99</div>
        <button class="add-to-cart-btn" onclick="addToCart('Wooden Coasters', 19.99)">Add to Cart</button>
      </div>
    </div>
    
    <div class="product">
      <img src="product2.jpg" alt="Product 2">
      <div class="product-info">
        <div class="product-name">Personalized Cutting Board</div>
        <div class="product-description">Customizable wooden cutting board with laser-engraved names or messages.</div>
        <div class="product-price">$39.99</div>
        <button class="add-to-cart-btn" onclick="addToCart('Personalized Cutting Board', 39.99)">Add to Cart</button>
      </div>
    </div>
    
    <div class="product">
      <img src="product3.jpg" alt="Product 3">
      <div class="product-info">
        <div class="product-name">Wooden Wall Art</div>
        <div class="product-description">Beautiful laser-engraved wooden wall art for home decor.</div>
        <div class="product-price">$59.99</div>
        <button class="add-to-cart-btn" onclick="addToCart('Wooden Wall Art', 59.99)">Add to Cart</button>
      </div>
    </div>
    
    <div class="cart">
      <h2>Cart</h2>
      <div id="cart-items"></div>
      <button class="checkout-btn" onclick="checkout()">Checkout</button>
    </div>
  </main>

  <script>
    // JavaScript code
    const cartItems = [];

    function addToCart(productName, price) {
      const item = {
        name: productName,
        price: price
      };
      cartItems.push(item);
      updateCart();
    }

    function updateCart() {
      const cartItemsElement = document.getElementById('cart-items');
      cartItemsElement.innerHTML = '';

      cartItems.forEach(item => {
        const cartItemElement = document.createElement('div');
        cartItemElement.classList.add('cart-item');
        cartItemElement.innerText = `${item.name} - $${item.price}`;
        cartItems