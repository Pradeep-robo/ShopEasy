<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>ShopEasy - Everything You Need</title>

    <style>
        /* =========================
           GENERAL STYLES
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #f5f6f8;
            color: #333;
        }

        button {
            cursor: pointer;
            border: none;
        }


        /* =========================
           HEADER
        ========================== */

        header {
            background: #2874f0;
            color: white;
            padding: 15px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .logo {
            font-size: 28px;
            font-weight: bold;
        }

        .logo span {
            color: #ffe500;
        }

        nav {
            display: flex;
            gap: 25px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 16px;
            font-weight: bold;
        }

        nav a:hover {
            color: #ffe500;
        }


        /* =========================
           HERO SECTION
        ========================== */

        .hero {
            min-height: 430px;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 50px 20px;

            background: linear-gradient(
                135deg,
                #2874f0,
                #00b4db
            );

            color: white;
        }

        .hero-content h1 {
            font-size: 50px;
            margin-bottom: 15px;
        }

        .hero-content h1 span {
            color: #ffe500;
        }

        .hero-content p {
            font-size: 21px;
            margin-bottom: 30px;
        }

        .shop-button {
            background: #ff9f00;
            color: white;
            padding: 14px 30px;
            border-radius: 6px;
            font-size: 17px;
            font-weight: bold;
        }

        .shop-button:hover {
            background: #fb8c00;
        }


        /* =========================
           SEARCH
        ========================== */

        .search-section {
            padding: 30px 20px;
            text-align: center;
            background: white;
        }

        #searchBox {
            width: 60%;
            max-width: 600px;
            padding: 15px;
            border: 1px solid #ccc;
            border-radius: 8px;
            font-size: 16px;
            outline: none;
        }

        #searchBox:focus {
            border-color: #2874f0;
        }


        /* =========================
           CATEGORIES
        ========================== */

        .section {
            padding: 50px 7%;
        }

        .section-title {
            text-align: center;
            font-size: 32px;
            margin-bottom: 35px;
        }

        .category-container {
            display: grid;
            grid-template-columns: repeat(
                auto-fit,
                minmax(140px, 1fr)
            );
            gap: 20px;
        }

        .category {
            background: white;
            padding: 25px 15px;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: 0.3s;
        }

        .category:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.15);
        }

        .category .emoji {
            font-size: 45px;
            margin-bottom: 10px;
        }

        .category h3 {
            font-size: 17px;
        }


        /* =========================
           PRODUCTS
        ========================== */

        .product-container {
            display: grid;
            grid-template-columns: repeat(
                auto-fit,
                minmax(220px, 1fr)
            );
            gap: 25px;
        }

        .product {
            background: white;
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: 0.3s;
        }

        .product:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 15px rgba(0,0,0,0.15);
        }

        .product-image {
            font-size: 75px;
            margin-bottom: 15px;
        }

        .product h3 {
            margin-bottom: 10px;
        }

        .product .price {
            color: #2874f0;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .add-button {
            background: #2874f0;
            color: white;
            padding: 11px 20px;
            border-radius: 5px;
            font-weight: bold;
        }

        .add-button:hover {
            background: #1259c3;
        }


        /* =========================
           CART
        ========================== */

        .cart-section {
            background: white;
            margin: 30px 7%;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
        }

        .cart-section h2 {
            margin-bottom: 20px;
        }

        #cartItems {
            margin-bottom: 20px;
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5px;
            border-bottom: 1px solid #ddd;
        }

        .remove-button {
            background: #e53935;
            color: white;
            padding: 7px 12px;
            border-radius: 4px;
        }

        .total {
            font-size: 22px;
            font-weight: bold;
            margin: 20px 0;
        }

        .checkout-button {
            background: #28a745;
            color: white;
            padding: 13px 25px;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
        }

        .checkout-button:hover {
            background: #218838;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 25px;
            margin-top: 40px;
        }

        footer p {
            margin: 5px;
        }


        /* =========================
           MOBILE RESPONSIVE
        ========================== */

        @media (max-width: 700px) {

            header {
                flex-direction: column;
                gap: 15px;
            }

            nav {
                gap: 12px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .hero-content h1 {
                font-size: 35px;
            }

            .hero-content p {
                font-size: 17px;
            }

            #searchBox {
                width: 90%;
            }

            .section {
                padding: 35px 5%;
            }

            .cart-section {
                margin: 20px 5%;
            }
        }
    </style>
</head>


<body>

    <!-- =========================
         HEADER
    ========================== -->

    <header>

        <div class="logo">
            Shop<span>Easy</span>
        </div>

        <nav>
            <a href="#home">Home</a>
            <a href="#categories">Categories</a>
            <a href="#products">Products</a>
            <a href="#cart">Cart 🛒</a>
        </nav>

    </header>


    <!-- =========================
         HERO
    ========================== -->

    <section class="hero" id="home">

        <div class="hero-content">

            <h1>
                Welcome to <span>ShopEasy</span>
            </h1>

            <p>
                Everything you need, all in one place!
            </p>

            <button
                class="shop-button"
                onclick="scrollToProducts()"
            >
                Shop Now
            </button>

        </div>

    </section>


    <!-- =========================
         SEARCH
    ========================== -->

    <section class="search-section">

        <input
            type="text"
            id="searchBox"
            placeholder="🔍 Search for fruits, vegetables, food..."
            onkeyup="searchProducts()"
        >

    </section>


    <!-- =========================
         CATEGORIES
    ========================== -->

    <section
        class="section"
        id="categories"
    >

        <h2 class="section-title">
            Shop by Category
        </h2>

        <div class="category-container">

            <div class="category">
                <div class="emoji">🥦</div>
                <h3>Vegetables</h3>
            </div>

            <div class="category">
                <div class="emoji">🍎</div>
                <h3>Fruits</h3>
            </div>

            <div class="category">
                <div class="emoji">🍚</div>
                <h3>Groceries</h3>
            </div>

            <div class="category">
                <div class="emoji">🍿</div>
                <h3>Snacks</h3>
            </div>

            <div class="category">
                <div class="emoji">🥛</div>
                <h3>Dairy</h3>
            </div>

            <div class="category">
                <div class="emoji">🍞</div>
                <h3>Bakery</h3>
            </div>

            <div class="category">
                <div class="emoji">🥤</div>
                <h3>Beverages</h3>
            </div>

            <div class="category">
                <div class="emoji">🧴</div>
                <h3>Personal Care</h3>
            </div>

            <div class="category">
                <div class="emoji">🧹</div>
                <h3>Household</h3>
            </div>

        </div>

    </section>


    <!-- =========================
         PRODUCTS
    ========================== -->

    <section
        class="section"
        id="products"
    >

        <h2 class="section-title">
            Popular Products
        </h2>

        <div
            class="product-container"
            id="productContainer"
        >

            <!-- Product 1 -->

            <div class="product">

                <div class="product-image">
                    🍎
                </div>

                <h3>Fresh Apples</h3>

                <p class="price">
                    ₹120 / kg
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Fresh Apples', 120)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 2 -->

            <div class="product">

                <div class="product-image">
                    🍌
                </div>

                <h3>Bananas</h3>

                <p class="price">
                    ₹60 / dozen
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Bananas', 60)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 3 -->

            <div class="product">

                <div class="product-image">
                    🍅
                </div>

                <h3>Fresh Tomatoes</h3>

                <p class="price">
                    ₹40 / kg
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Fresh Tomatoes', 40)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 4 -->

            <div class="product">

                <div class="product-image">
                    🥔
                </div>

                <h3>Potatoes</h3>

                <p class="price">
                    ₹35 / kg
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Potatoes', 35)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 5 -->

            <div class="product">

                <div class="product-image">
                    🍚
                </div>

                <h3>Rice</h3>

                <p class="price">
                    ₹70 / kg
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Rice', 70)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 6 -->

            <div class="product">

                <div class="product-image">
                    🥛
                </div>

                <h3>Milk</h3>

                <p class="price">
                    ₹60 / litre
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Milk', 60)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 7 -->

            <div class="product">

                <div class="product-image">
                    🍞
                </div>

                <h3>Fresh Bread</h3>

                <p class="price">
                    ₹45
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Fresh Bread', 45)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 8 -->

            <div class="product">

                <div class="product-image">
                    🍪
                </div>

                <h3>Biscuits</h3>

                <p class="price">
                    ₹30
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Biscuits', 30)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 9 -->

            <div class="product">

                <div class="product-image">
                    🥤
                </div>

                <h3>Fruit Juice</h3>

                <p class="price">
                    ₹80
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Fruit Juice', 80)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 10 -->

            <div class="product">

                <div class="product-image">
                    🧀
                </div>

                <h3>Cheese</h3>

                <p class="price">
                    ₹150
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Cheese', 150)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 11 -->

            <div class="product">

                <div class="product-image">
                    🍫
                </div>

                <h3>Chocolate</h3>

                <p class="price">
                    ₹50
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Chocolate', 50)"
                >
                    Add to Cart
                </button>

            </div>


            <!-- Product 12 -->

            <div class="product">

                <div class="product-image">
                    🧴
                </div>

                <h3>Shampoo</h3>

                <p class="price">
                    ₹180
                </p>

                <button
                    class="add-button"
                    onclick="addToCart('Shampoo', 180)"
                >
                    Add to Cart
                </button>

            </div>

        </div>

    </section>


    <!-- =========================
         CART
    ========================== -->

    <section
        class="cart-section"
        id="cart"
    >

        <h2>
            🛒 Shopping Cart
        </h2>

        <div id="cartItems">
            <p>Your cart is empty.</p>
        </div>

        <div class="total">
            Total: ₹<span id="total">0</span>
        </div>

        <button
            class="checkout-button"
            onclick="checkout()"
        >
            Checkout
        </button>

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

        <p>
            © 2026 ShopEasy. All Rights Reserved.
        </p>

        <p>
            Everything You Need, All in One Place.
        </p>

    </footer>


    <!-- =========================
         JAVASCRIPT
    ========================== -->

    <script>

        // Shopping cart
        let cart = [];


        // Add product to cart
        function addToCart(name, price) {

            cart.push({
                name: name,
                price: price
            });

            displayCart();

            alert(name + " added to cart!");
        }


        // Display cart
        function displayCart() {

            const cartItems =
                document.getElementById("cartItems");

            const totalElement =
                document.getElementById("total");

            if (cart.length === 0) {

                cartItems.innerHTML =
                    "<p>Your cart is empty.</p>";

                totalElement.textContent = "0";

                return;
            }


            cartItems.innerHTML = "";

            let total = 0;


            cart.forEach(function(item, index) {

                const div =
                    document.createElement("div");

                div.className = "cart-item";

                div.innerHTML = `
                    <span>
                        ${item.name} - ₹${item.price}
                    </span>

                    <button
                        class="remove-button"
                        onclick="removeFromCart(${index})"
                    >
                        Remove
                    </button>
                `;

                cartItems.appendChild(div);

                total += item.price;

            });


            totalElement.textContent = total;
        }


        // Remove product
        function removeFromCart(index) {

            cart.splice(index, 1);

            displayCart();
        }


        // Search products
        function searchProducts() {

            const searchText =
                document
                    .getElementById("searchBox")
                    .value
                    .toLowerCase();


            const products =
                document.querySelectorAll(".product");


            products.forEach(function(product) {

                const productName =
                    product
                        .querySelector("h3")
                        .textContent
                        .toLowerCase();


                if (productName.includes(searchText)) {

                    product.style.display = "block";

                } else {

                    product.style.display = "none";

                }

            });
        }


        // Scroll to products
        function scrollToProducts() {

            document
                .getElementById("products")
                .scrollIntoView({
                    behavior: "smooth"
                });
        }


        // Checkout
        function checkout() {

            if (cart.length === 0) {

                alert(
                    "Your shopping cart is empty!"
                );

                return;
            }


            alert(
                "Thank you for shopping with ShopEasy! Your order has been placed."
            );


            cart = [];

            displayCart();
        }

    </script>

</body>
</html>
