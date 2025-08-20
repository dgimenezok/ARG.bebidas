<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARG Bebidas Argentinas - Tienda Online</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #f8f8f8;
        }
        .title-font {
            font-family: 'Playfair Display', serif;
        }
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        .whatsapp-btn {
            background-color: #25D366;
            transition: all 0.3s;
        }
        .whatsapp-btn:hover {
            background-color: #128C7E;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="bg-gray-900 text-white py-6 shadow-lg">
        <div class="container mx-auto px-4">
            <div class="flex justify-between items-center">
                <div class="flex items-center">
                    <img src="https://placehold.co/50" alt="Logo de Licores Premium - Copa de cóctel dorada sobre fondo oscuro" class="mr-3">
                    <h1 class="title-font text-2xl md:text-3xl">ARG Bebidas Argentinas</h1>
                </div>
                <div class="relative">
                    <button id="cart-button" class="flex items-center bg-amber-700 hover:bg-amber-800 px-4 py-2 rounded-full transition">
                        <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
                        </svg>
                        <span id="cart-count" class="ml-1">0</span>
                    </button>
                    <div id="cart-dropdown" class="hidden absolute right-0 mt-2 w-72 bg-white text-gray-800 rounded-md shadow-xl z-10 p-4">
                        <h3 class="font-bold border-b pb-2 mb-2">Tu Carrito</h3>
                        <div id="cart-items" class="max-h-60 overflow-y-auto mb-2">
                            <p class="text-gray-500 text-sm">Tu carrito está vacío</p>
                        </div>
                        <div class="border-t pt-3">
                            <p class="font-bold">Total: <span id="cart-total">$0</span></p>
                            <button id="checkout-btn" class="whatsapp-btn text-white py-2 px-4 rounded-md w-full mt-2 disabled:opacity-50" disabled>
                                Finalizar Compra
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="bg-gray-900 text-white py-12 md:py-16">
        <div class="container mx-auto px-4 flex flex-col md:flex-row items-center">
            <div class="md:w-1/2 mb-8 md:mb-0">
                <h2 class="title-font text-4xl md:text-5xl mb-4">De raíz noble, de copa fina</h2>
                <p class="text-lg mb-6">Comprás fácil, recibís rápido y listo: vos ponés la compañía, nosotros ponemos la bebida.</p>
                <a href="#products" class="bg-amber-600 hover:bg-amber-700 text-white py-3 px-6 rounded-md inline-block">Ver productos</a>
            </div>
            <div class="md:w-1/2">
                <img src="https://placehold.co/600x400" alt="Barra de bar bien surtida con diversas bebidas alcohólicas premium iluminadas con luces cálidas" class="rounded-lg shadow-xl">
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="py-12 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="title-font text-3xl md:text-4xl text-center mb-12">Nuestros Productos</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Product 1 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de whisky Johnnie Walker Blue Label en primer plano con fondo desenfocado de barra de bar" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Whisky Johnnie Walker Blue Label</h3>
                        <p class="text-gray-600 mb-4">Un blend escocés de lujo con notas de chocolate, miel y frutas secas.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$120.000</span>
                            <button onclick="addToCart('Whisky Johnnie Walker Blue Label', 120000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 2 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de champagne Dom Pérignon con copas de cristal sobre mesa de mármol" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Champagne Dom Pérignon</h3>
                        <p class="text-gray-600 mb-4">Un champagne de prestigio con burbujas finas y aromas a frutos secos.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$250.000</span>
                            <button onclick="addToCart('Champagne Dom Pérignon', 250000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 3 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de vodka Grey Goose con limones y hielo en un recipiente de cristal" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Vodka Grey Goose</h3>
                        <p class="text-gray-600 mb-4">Vodka premium francés, suave y versátil para mezclar o tomar solo.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$95.000</span>
                            <button onclick="addToCart('Vodka Grey Goose', 95000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 4 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de ron Zacapa 23 años con vista de atardecer tropical de fondo" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Ron Zacapa 23 Años</h3>
                        <p class="text-gray-600 mb-4">Ron guatemalteco añejado en barricas de bourbon con notas de caramelo y especias.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$180.000</span>
                            <button onclick="addToCart('Ron Zacapa 23 Años', 180000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 5 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de tequila Don Julio 1942 con sal y rodajas de limón" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Tequila Don Julio 1942</h3>
                        <p class="text-gray-600 mb-4">Tequila añejo mexicano con sabores a vainilla, caramelo y roble.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$350.000</span>
                            <button onclick="addToCart('Tequila Don Julio 1942', 350000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Product 6 -->
                <div class="product-card bg-white rounded-lg overflow-hidden shadow-md border border-gray-100 transition duration-300">
                    <div class="h-48 overflow-hidden">
                        <img src="https://placehold.co/600x400" alt="Botella de ginebra Hendrick's con pepino y hierbas aromáticas" class="w-full h-full object-cover">
                    </div>
                    <div class="p-4">
                        <h3 class="font-bold text-xl mb-2">Ginebra Hendrick's</h3>
                        <p class="text-gray-600 mb-4">Ginebra escocesa con infusiones de pepino y rosas, ideal para gin tonics.</p>
                        <div class="flex justify-between items-center">
                            <span class="font-bold text-lg">$130.000</span>
                            <button onclick="addToCart('Ginebra Hendrick\'s', 130000, 'https://placehold.co/600x400')" class="bg-amber-600 hover:bg-amber-700 text-white py-2 px-4 rounded-full">
                                Añadir al carrito
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- WhatsApp Fixed Button -->
    <div class="fixed bottom-6 right-6 z-50">
        <a id="whatsapp-link" href="#" class="whatsapp-btn text-white p-3 rounded-full shadow-lg block">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10" viewBox="0 0 24 24" fill="currentColor">
                <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
            </svg>
        </a>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    <h3 class="title-font text-2xl mb-2">Licores Premium</h3>
                    <p class="text-gray-400">Las mejores bebidas para tus momentos especiales</p>
                </div>
                <div>
                    <p class="text-gray-400">Contáctanos:</p>
                    <p class="font-bold">info@licorespremium.com</p>
                    <p class="font-bold">+57 123 456 7890</p>
                </div>
            </div>
            <div class="border-t border-gray-800 mt-6 pt-6 text-center text-gray-400 text-sm">
                <p>© 2023 Licores Premium. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script>
        // Variables globales
        let cart = [];
        const whatsappNumber = "+571234567890"; // Reemplaza con tu número de WhatsApp
        
        // Función para agregar productos al carrito
        function addToCart(name, price, image) {
            // Buscar si el producto ya está en el carrito
            const existingProduct = cart.find(item => item.name === name);
            
            if (existingProduct) {
                existingProduct.quantity++;
            } else {
                cart.push({
                    name: name,
                    price: price,
                    quantity: 1,
                    image: image
                });
            }
            
            updateCart();
            
            // Mostrar notificación
            const notification = document.createElement('div');
            notification.className = 'fixed top-4 right-4 bg-green-500 text-white px-4 py-2 rounded-md shadow-lg';
            notification.textContent = `${name} añadido al carrito`;
            document.body.appendChild(notification);
            
            // Eliminar notificación después de 3 segundos
            setTimeout(() => {
                notification.remove();
            }, 3000);
        }
        
        // Función para actualizar el carrito y el total
        function updateCart() {
            const cartItems = document.getElementById('cart-items');
            const cartCount = document.getElementById('cart-count');
            const cartTotal = document.getElementById('cart-total');
            const checkoutBtn = document.getElementById('checkout-btn');
            
            // Actualizar contador
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            cartCount.textContent = totalItems;
            
            // Generar lista de productos en el carrito
            if (cart.length === 0) {
                cartItems.innerHTML = '<p class="text-gray-500 text-sm">Tu carrito está vacío</p>';
                checkoutBtn.disabled = true;
                cartTotal.textContent = '$0';
            } else {
                cartItems.innerHTML = '';
                let total = 0;
                
                cart.forEach(item => {
                    const itemTotal = item.price * item.quantity;
                    total += itemTotal;
                    
                    const itemElement = document.createElement('div');
                    itemElement.className = 'flex items-center py-2 border-b';
                    itemElement.innerHTML = `
                        <img src="${item.image}" alt="${item.name}" class="w-10 h-10 object-cover rounded mr-3">
                        <div class="flex-grow">
                            <p class="font-medium">${item.name}</p>
                            <p class="text-sm text-gray-600">${formatCurrency(item.price)} x ${item.quantity}</p>
                        </div>
                        <p class="font-medium">${formatCurrency(itemTotal)}</p>
                    `;
                    cartItems.appendChild(itemElement);
                });
                
                cartTotal.textContent = formatCurrency(total);
                checkoutBtn.disabled = false;
            }
        }
        
        // Función para formatear moneda
        function formatCurrency(amount) {
            return '$' + amount.toLocaleString();
        }
        
        // Función para completar la compra por WhatsApp
        function checkout() {
            if (cart.length === 0) return;
            
            let message = 'Hola, me gustaría hacer el siguiente pedido:%0A%0A';
            
            cart.forEach(item => {
                message += `✅ ${item.name} - ${item.quantity} x ${formatCurrency(item.price)}%0A`;
            });
            
            message += `%0ATotal: ${document.getElementById('cart-total').textContent}%0A%0A`;
            message += 'Por favor, confirmen disponibilidad y formas de pago. ¡Gracias!';
            
            const whatsappLink = `https://wa.me/${whatsappNumber}?text=${message}`;
            
            // Abrir WhatsApp
            window.open(whatsappLink, '_blank');
            
            // Limpiar carrito
            cart = [];
            updateCart();
            
            // Agregar mensaje al botón flotante
            document.getElementById('whatsapp-link').href = whatsappLink;
        }
        
        // Event listeners
        document.addEventListener('DOMContentLoaded', () => {
            // Mostrar/ocultar carrito
            document.getElementById('cart-button').addEventListener('click', (e) => {
                e.stopPropagation();
                document.getElementById('cart-dropdown').classList.toggle('hidden');
            });
            
            // Ocultar carrito al hacer clic fuera
            document.addEventListener('click', () => {
                document.getElementById('cart-dropdown').classList.add('hidden');
            });
            
            // Evitar que el clic en el carrito se propague
            document.getElementById('cart-dropdown').addEventListener('click', (e) => {
                e.stopPropagation();
            });
            
            // Botón de compra
            document.getElementById('checkout-btn').addEventListener('click', checkout);
            
            // Botón flotante de WhatsApp
            document.getElementById('whatsapp-link').addEventListener('click', (e) => {
                if (cart.length > 0) {
                    e.preventDefault();
                    checkout();
                }
            });
        });
    </script>
</body>
</html>
