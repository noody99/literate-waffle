#input****

<!DOCTYPE html>
<html lang="ar" dir="rtl">
****<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Noody Sweet | نودي سويت</title>
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <style>


        :root {
            --bg-color: #FFFDF0;
            --primary-yellow: #FFC107;
            --secondary-yellow: #FFECB3;
            --dark-brown: #3E2723;
            --medium-brown: #5D4037;
            --light-brown: #8D6E63;
            --accent-gold: #D4AF37;
            --white: #FFFFFF;
            --shadow: 0 10px 30px rgba(62, 39, 35, 0.08);
            --radius: 20px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
            -webkit-tap-highlight-color: transparent;
        }

        body {
            background-color: var(--bg-color);
            color: var(--dark-brown);
            line-height: 1.6;
            padding-bottom: 40px;
        }

        .container {
            max-width: 480px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Header / Hero */
        .hero {
            background: linear-gradient(135deg, var(--dark-brown) 0%, var(--medium-brown) 100%);
            color: var(--white);
            text-align: center;
            padding: 40px 20px 30px;
            border-bottom-left-radius: 35px;
            border-bottom-right-radius: 35px;
            box-shadow: 0 10px 25px rgba(62, 39, 35, 0.2);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50px;
            right: -50px;
            width: 150px;
            height: 150px;
            background: rgba(255, 193, 7, 0.15);
            border-radius: 50%;
        }

        .logo-avatar {
            width: 95px;
            height: 95px;
            background: linear-gradient(135deg, #FFF, var(--secondary-yellow));
            border: 4px solid var(--primary-yellow);
            border-radius: 50%;
            margin: 0 auto 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 42px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
        }

        .brand-name {
            font-size: 26px;
            font-weight: 800;
            color: var(--primary-yellow);
            letter-spacing: 0.5px;
            margin-bottom: 4px;
        }

        .handle {
            font-size: 14px;
            color: var(--secondary-yellow);
            direction: ltr;
            margin-bottom: 12px;
            font-weight: 500;
            opacity: 0.9;
        }

        .bio {
            font-size: 14px;
            color: #EFEBE9;
            max-width: 320px;
            margin: 0 auto;
            font-weight: 400;
        }

        /* Section Styling */
        .section-title {
            text-align: center;
            margin: 30px 0 20px;
            position: relative;
        }

        .section-title h2 {
            font-size: 20px;
            color: var(--dark-brown);
            display: inline-block;
            background: var(--bg-color);
            padding: 0 15px;
            position: relative;
            z-index: 1;
            font-weight: 700;
        }

        .section-title::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 10%;
            right: 10%;
            height: 2px;
            background: var(--secondary-yellow);
            z-index: 0;
        }

        /* Products Grid */
        .products-grid {
            display: flex;
            flex-direction: column;
            gap: 18px;
        }

        .product-card {
            background: var(--white);
            border-radius: var(--radius);
            padding: 18px;
            display: flex;
            align-items: center;
            gap: 16px;
            box-shadow: var(--shadow);
            border: 1px solid rgba(255, 193, 7, 0.25);
            transition: transform 0.2s, box-shadow 0.2s;
        }

        .product-card:active {
            transform: scale(0.98);
        }

        .product-icon {
            width: 75px;
            height: 75px;
            background: var(--secondary-yellow);
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 38px;
            flex-shrink: 0;
            border: 1px dashed var(--primary-yellow);
        }

        .product-details {
            flex-grow: 1;
        }

        .product-title {
            font-size: 17px;
            font-weight: 700;
            color: var(--dark-brown);
            margin-bottom: 4px;
        }

        .product-desc {
            font-size: 12px;
            color: var(--light-brown);
            margin-bottom: 10px;
            line-height: 1.4;
        }

        .product-bottom {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .product-price {
            font-size: 16px;
            font-weight: 800;
            color: var(--dark-brown);
            background: var(--secondary-yellow);
            padding: 3px 10px;
            border-radius: 10px;
        }

        .order-btn-sm {
            background: var(--dark-brown);
            color: var(--primary-yellow);
            text-decoration: none;
            padding: 6px 14px;
            border-radius: 12px;
            font-size: 13px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 5px;
            transition: background 0.3s;
        }

        /* Quick Action Links */
        .links-section {
            margin-top: 25px;
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .action-link {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background: var(--white);
            border: 2px solid var(--primary-yellow);
            padding: 14px 20px;
            border-radius: var(--radius);
            color: var(--dark-brown);
            text-decoration: none;
            font-weight: 700;
            font-size: 15px;
            box-shadow: var(--shadow);
            transition: all 0.2s ease;
        }

        .action-link.whatsapp {
            background: #25D366;
            color: var(--white);
            border-color: #25D366;
        }

        .action-link.instagram {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            color: var(--white);
            border-color: transparent;
        }

        .link-icon {
            font-size: 20px;
        }

        /* Footer */
        .footer {
            text-align: center;
            margin-top: 35px;
            font-size: 12px;
            color: var(--light-brown);
        }

        .footer p {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>

    <!-- Hero Header -->
    <div class="hero">
        <div class="logo-avatar">🍰</div>
        <h1 class="brand-name">Noody Sweet</h1>
        <div class="handle">@noody_sweet99</div>
        <p class="bio">لذة الحلى بلمسة خاصة ✨ الأصناف مميزة وتُصنع بكل حب 💕</p>
    </div>

    <div class="container">
       
        <!-- Menu Section -->
        <div class="section-title">
            <h2>قائمة الحلويات 📋</h2>
        </div>

        <div class="products-grid">
           
            <!-- Saffron Cake -->
            <div class="product-card">
                <div class="product-icon">🍮</div>
                <div class="product-details">
                    <div class="product-title">كيكة الزعفران</div>
                    <div class="product-desc">كيكة هشة وغنية بنكهة الزعفران الفاخرة مع الصوص الخاص.</div>
                    <div class="product-bottom">
                        <span class="product-price">1.300 ر.ع.</span>
                        <a href="https://wa.me/?text=مرحباً،%20أود%20طلب%20كيكة%20الزعفران" class="order-btn-sm">اطلب 💬</a>
                    </div>
                </div>
            </div>

            <!-- Chocolate Cake -->
            <div class="product-card">
                <div class="product-icon">🍫</div>
                <div class="product-details">
                    <div class="product-title">كيكة الشوكولاتة</div>
                    <div class="product-desc">كيكة شوكولاتة غنية ولذيذة جداً تذوب بالظرف.</div>
                    <div class="product-bottom">
                        <span class="product-price">1.300 ر.ع.</span>
                        <a href="https://wa.me/?text=مرحباً،%20أود%20طلب%20كيكة%20الشوكولاتة" class="order-btn-sm">اطلب 💬</a>
                    </div>
                </div>
            </div>

        </div>

        <!-- Quick Links -->
        <div class="section-title">
            <h2>التواصل والطلب 📲</h2>
        </div>

        <div class="links-section">
            <a href="https://wa.me/" class="action-link whatsapp" target="_blank">
                <span>💬 للطلب المباشر عبر الواتساب</span>
                <span class="link-icon">←</span>
            </a>

            <a href="https://instagram.com/noody_sweet99" class="action-link instagram" target="_blank">
                <span>📸 متابعتنا على الإنستغرام</span>
                <span class="link-icon">←</span>
            </a>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p>جميع الحقوق محفوظة لـ Noody Sweet © 2026</p>
            <p>صُنع بكل حب 💛 brown & yellow edition</p>
        </div>

    </div>

        </body>
        </html>


