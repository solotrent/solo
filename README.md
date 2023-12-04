# solo<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Marketplace</title>
</head>
<body>
    <header>
        <h1>Marketplace</h1>
    </header>

    <section id="products">
        <!-- Product listings go here -->
    </section>

    <footer>
        <p>&copy; 2023 Marketplace</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header, footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1em;
}

#products {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}

.product {
    border: 1px solid #ddd;
    padding: 1em;
    margin: 1em;
    width: 200px;
}

footer {
    position: fixed;
    bottom: 0;
    width: 100%;
}
// Sample data for products
const products = [
    { name: 'Product 1', price: 50 },
    { name: 'Product 2', price: 75 },
    // Add more products as needed
];

// Function to display products on the page
function displayProducts() {
    const productsContainer = document.getElementById('products');
    productsContainer.innerHTML = '';

    products.forEach(product => {
        const productElement = document.createElement('div');
        productElement.classList.add('product');
        productElement.innerHTML = `<h3>${product.name}</h3><p>$${product.price}</p>`;
        productsContainer.appendChild(productElement);
    });
}

// Call the function to display products when the page loads
document.addEventListener('DOMContentLoaded', displayProducts);
