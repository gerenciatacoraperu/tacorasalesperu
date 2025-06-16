# tacorasalesperu
ventas y compras por internet
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tacora Sales</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
        }

        .header {
            background: linear-gradient(45deg, #fff, #f8f9fa);
            padding: 20px 0;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        .logo-container {
            text-align: center;
            margin-bottom: 20px;
        }

        .logo {
            font-size: 4rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .logo .t { color: #1e5aa8; }
        .logo .a1 { color: #d4af37; }
        .logo .c { color: #dc143c; }
        .logo .o { color: #1e5aa8; }
        .logo .r { color: #d4af37; }
        .logo .a2 { color: #7cb342; }

        .sales-badge {
            background: linear-gradient(45deg, #ff9500, #ffb347);
            color: white;
            padding: 15px 40px;
            border-radius: 50px;
            font-size: 2.5rem;
            font-weight: bold;
            display: inline-block;
            box-shadow: 0 8px 25px rgba(255, 149, 0, 0.3);
        }

        .nav-menu {
            background: #1e5aa8;
            padding: 15px 0;
        }

        .nav-menu ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 30px;
        }

        .nav-menu a {
            color: white;
            text-decoration: none;
            padding: 10px 20px;
            border-radius: 25px;
            transition: all 0.3s ease;
            font-weight: 500;
        }

        .nav-menu a:hover {
            background: rgba(255,255,255,0.2);
            transform: translateY(-2px);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .admin-panel {
            background: white;
            padding: 20px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .admin-panel h3 {
            color: #1e5aa8;
            margin-bottom: 15px;
            font-size: 1.5rem;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
            color: #333;
        }

        .form-group input, .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 14px;
        }

        .form-group input:focus, .form-group textarea:focus {
            border-color: #1e5aa8;
            outline: none;
        }

        .btn-primary {
            background: linear-gradient(45deg, #1e5aa8, #4a90e2);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(30, 90, 168, 0.3);
        }

        .btn-secondary {
            background: linear-gradient(45deg, #dc143c, #ff6b6b);
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 20px;
            cursor: pointer;
            font-size: 12px;
            margin-left: 10px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .product-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-bottom: 3px solid #ff9500;
        }

        .product-info {
            padding: 20px;
        }

        .product-title {
            font-size: 1.3rem;
            font-weight: bold;
            color: #1e5aa8;
            margin-bottom: 10px;
        }

        .product-price {
            font-size: 1.8rem;
            font-weight: bold;
            color: #dc143c;
            margin-bottom: 15px;
        }

        .product-description {
            color: #666;
            margin-bottom: 15px;
            line-height: 1.5;
        }

        .product-video {
            width: 100%;
            height: 200px;
            border-radius: 8px;
            margin-bottom: 15px;
        }

        .edit-controls {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .footer {
            background: #1e5aa8;
            color: white;
            text-align: center;
            padding: 40px 20px;
            margin-top: 50px;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: #ff9500;
        }

        .footer-social {
            margin: 20px 0;
        }

        .social-icons {
            display: flex;
            justify-content: center;
            gap: 15px;
        }

        .social-icon {
            width: 40px;
            height: 40px;
            background: #ff9500;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .social-icon:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 149, 0, 0.3);
        }

        .hidden {
            display: none;
        }

        @media (max-width: 768px) {
            .logo {
                font-size: 2.5rem;
            }
            
            .sales-badge {
                font-size: 1.8rem;
                padding: 10px 30px;
            }
            
            .nav-menu ul {
                flex-direction: column;
                gap: 10px;
            }
            
            .footer-links {
                flex-direction: column;
                gap: 15px;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="logo-container">
            <div class="logo">
                <span class="t">t</span><span class="a1">a</span><span class="c">c</span><span class="o">o</span><span class="r">r</span><span class="a2">a</span>
            </div>
            <div class="sales-badge">sales</div>
        </div>
        
        <nav class="nav-menu">
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#ofertas">Ofertas</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li><a href="#" onclick="toggleAdmin()">Admin</a></li>
            </ul>
        </nav>
    </header>

    <div class="container">
        <div id="adminPanel" class="admin-panel hidden">
            <h3>Panel de Administración</h3>
            <form id="productForm">
                <div class="form-group">
                    <label for="productName">Nombre del Producto:</label>
                    <input type="text" id="productName" required>
                </div>
                
                <div class="form-group">
                    <label for="productPrice">Precio:</label>
                    <input type="text" id="productPrice" placeholder="$0.00" required>
                </div>
                
                <div class="form-group">
                    <label for="productImage">Imagen del Producto:</label>
                    <input type="file" id="productImage" accept="image/*">
                </div>
                
                <div class="form-group">
                    <label for="productDescription">Descripción:</label>
                    <textarea id="productDescription" rows="3"></textarea>
                </div>
                
                <div class="form-group">
                    <label for="productVideo">Video del Producto:</label>
                    <input type="file" id="productVideo" accept="video/*">
                </div>
                
                <button type="submit" class="btn-primary">Agregar Producto</button>
            </form>
        </div>

        <div class="products-grid" id="productsGrid">
            <!-- Producto de ejemplo -->
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1549298916-b41d501d3772?w=400&h=250&fit=crop" alt="Globos de Fiesta" class="product-image" onerror="this.src='data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAwIiBoZWlnaHQ9IjI1MCIgdmlld0JveD0iMCAwIDQwMCAyNTAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSI0MDAiIGhlaWdodD0iMjUwIiBmaWxsPSIjRjVGNUY1Ii8+CjxwYXRoIGQ9Ik0yMDAgMTI1TDE2MCA5NUwyNDAgOTVMMjAwIDEyNVoiIGZpbGw9IiNEREREREQiLz4KPHN2Zz4='">
                <div class="product-info">
                    <h3 class="product-title">Globos de Fiesta Premium</h3>
                    <div class="product-price">$25.99</div>
                    <p class="product-description">Globos de alta calidad para fiestas y celebraciones especiales. Disponibles en múltiples colores.</p>
                    <div class="edit-controls">
                        <button class="btn-primary" onclick="editProduct(this)">Editar</button>
                        <button class="btn-secondary" onclick="deleteProduct(this)">Eliminar</button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <footer class="footer">
        <div class="footer-content">
            <div class="footer-links">
                <a href="#sobre-nosotros">Sobre Nosotros</a>
                <a href="#politicas">Políticas de Privacidad</a>
                <a href="#terminos">Términos y Condiciones</a>
                <a href="#envios">Información de Envíos</a>
                <a href="#devoluciones">Devoluciones</a>
                <a href="#ayuda">Centro de Ayuda</a>
            </div>
            
            <div class="footer-social">
                <div class="social-icons">
                    <a href="#" class="social-icon">📘</a>
                    <a href="#" class="social-icon">📷</a>
                    <a href="#" class="social-icon">🐦</a>
                    <a href="#" class="social-icon">📱</a>
                </div>
            </div>
            
            <div style="border-top: 1px solid rgba(255,255,255,0.1); padding-top: 20px; margin-top: 20px;">
                <p>&copy; 2025 Tacora Sales. Todos los derechos reservados.</p>
                <p style="margin-top: 10px; font-size: 14px; opacity: 0.8;">
                    Contacto: info@tacorasales.com | Teléfono: +1 (555) 123-4567
                </p>
                <p style="margin-top: 5px; font-size: 12px; opacity: 0.6;">
                    Dirección: 123 Commerce Street, Business District, Ciudad
                </p>
            </div>
        </div>
    </footer>

    <script>
        let products = [];
        let editingIndex = -1;

        function toggleAdmin() {
            const panel = document.getElementById('adminPanel');
            panel.classList.toggle('hidden');
        }

        function addProduct(name, price, imageUrl, description, videoUrl) {
            const product = {
                name: name,
                price: price,
                image: imageUrl,
                description: description,
                video: videoUrl
            };
            
            if (editingIndex >= 0) {
                products[editingIndex] = product;
                editingIndex = -1;
                document.querySelector('#productForm button[type="submit"]').textContent = 'Agregar Producto';
            } else {
                products.push(product);
            }
            
            renderProducts();
        }

        function renderProducts() {
            const grid = document.getElementById('productsGrid');
            
            // Mantener el producto de ejemplo y agregar los nuevos
            const exampleProduct = grid.children[0];
            grid.innerHTML = '';
            grid.appendChild(exampleProduct);
            
            products.forEach((product, index) => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                productCard.innerHTML = `
                    <img src="${product.image || 'data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAwIiBoZWlnaHQ9IjI1MCIgdmlld0JveD0iMCAwIDQwMCAyNTAiIGZpbGw9Im5vbmUiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxyZWN0IHdpZHRoPSI0MDAiIGhlaWdodD0iMjUwIiBmaWxsPSIjRjVGNUY1Ii8+CjxwYXRoIGQ9Ik0yMDAgMTI1TDE2MCA5NUwyNDAgOTVMMjAwIDEyNVoiIGZpbGw9IiNEREREREQiLz4KPHN2Zz4='}" alt="${product.name}" class="product-image">
                    <div class="product-info">
                        <h3 class="product-title">${product.name}</h3>
                        <div class="product-price">${product.price}</div>
                        <p class="product-description">${product.description}</p>
                        ${product.video ? `<video class="product-video" controls><source src="${product.video}" type="video/mp4">Tu navegador no soporta videos.</video>` : ''}
                        <div class="edit-controls">
                            <button class="btn-primary" onclick="editProduct(this, ${index})">Editar</button>
                            <button class="btn-secondary" onclick="deleteProduct(this, ${index})">Eliminar</button>
                        </div>
                    </div>
                `;
                
                grid.appendChild(productCard);
            });
        }

        function editProduct(button, index) {
            if (index !== undefined) {
                const product = products[index];
                document.getElementById('productName').value = product.name;
                document.getElementById('productPrice').value = product.price;
                document.getElementById('productDescription').value = product.description;
                editingIndex = index;
                document.querySelector('#productForm button[type="submit"]').textContent = 'Actualizar Producto';
                
                // Mostrar panel de admin
                document.getElementById('adminPanel').classList.remove('hidden');
            }
        }

        function deleteProduct(button, index) {
            if (index !== undefined) {
                products.splice(index, 1);
                renderProducts();
            } else {
                // Para el producto de ejemplo
                button.closest('.product-card').remove();
            }
        }

        document.getElementById('productForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('productName').value;
            const price = document.getElementById('productPrice').value;
            const description = document.getElementById('productDescription').value;
            const imageFile = document.getElementById('productImage').files[0];
            const videoFile = document.getElementById('productVideo').files[0];
            
            let imageUrl = '';
            let videoUrl = '';
            
            if (imageFile) {
                imageUrl = URL.createObjectURL(imageFile);
            }
            
            if (videoFile) {
                videoUrl = URL.createObjectURL(videoFile);
            }
            
            addProduct(name, price, imageUrl, description, videoUrl);
            
            // Limpiar formulario
            this.reset();
            document.getElementById('adminPanel').classList.add('hidden');
        });

        // Smooth scroll para navegación
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                if (this.getAttribute('href') !== '#') {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth'
                        });
                    }
                }
            });
        });
    </script>
</body>
</html>
