
```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ممدرسة الفن والهندسة</title>
    <!-- استدعاء خط عربي جميل (Tajawal) -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&display=swap" rel="stylesheet">
    <!-- مكتبة الأيقونات FontAwesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* === إعدادات عامة === */
        :root {
            --primary-color: #0f3460; /* أزرق داكن */
            --secondary-color: #16213e; /* أزرق أغمق للفوتر */
            --accent-color: #e94560; /* لون تمييزي (اختياري) */
            --light-bg: #f5f7fa;
            --white: #ffffff;
            --text-color: #333;
            --shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Tajawal', sans-serif;
            background-color: var(--light-bg);
            color: var(--text-color);
            line-height: 1.6;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        /* === الهيدر (القائمة العلوية) === */
        header {
            background-color: var(--white);
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .top-bar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            border-bottom: 1px solid #eee;
        }

        .logo-container {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo-img {
            width: 60px;
            height: 60px;
            background-color: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 30px;
        }

        .school-name h1 {
            color: var(--primary-color);
            font-size: 1.5rem;
            font-weight: 800;
        }

        .school-name span {
            font-size: 0.9rem;
            color: #777;
        }

        /* === شريط التنقل === */
        nav ul {
            display: flex;
            list-style: none;
            gap: 30px;
        }

        nav ul li a {
            font-weight: 700;
            color: var(--primary-color);
            font-size: 1.1rem;
            padding: 10px 15px;
            border-radius: 8px;
            transition: 0.3s;
        }

        nav ul li a:hover, nav ul li a.active {
            background-color: var(--primary-color);
            color: var(--white);
        }

        /* === قسم الصورة الرئيسية (Hero) === */
        .hero-section {
            position: relative;
            width: 100%;
            height: 500px;
            overflow: hidden;
        }

        .hero-section img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            /* فلتر خفيف لتغميق الصورة قليلاً */
            filter: brightness(0.95);
        }

        /* === قسم البطاقات (Cards) === */
        .cards-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: -80px; /* سحب البطاقات للأعلى لتتداخل مع الصورة */
            padding: 0 5%;
            position: relative;
            z-index: 10;
            flex-wrap: wrap;
        }

        .card {
            background: var(--white);
            flex: 1;
            min-width: 280px;
            max-width: 350px;
            padding: 40px 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-10px);
        }

        .card-icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 20px;
        }

        .card h3 {
            color: var(--primary-color);
            font-size: 1.4rem;
            margin-bottom: 10px;
        }

        .card p {
            color: #666;
            font-size: 0.95rem;
        }

        /* === الفوتر (تذييل الصفحة) === */
        footer {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 40px 5% 20px;
            margin-top: 80px;
            text-align: center;
        }

        .footer-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            border-bottom: 1px solid rgba(255,255,255,0.1);
            padding-bottom: 20px;
            margin-bottom: 20px;
        }

        .contact-info p {
            margin: 5px 0;
            font-size: 0.9rem;
        }
        
        .contact-info i {
            margin-left: 8px;
            color: #4da6ff;
        }

        .social-icons a {
            color: var(--white);
            font-size: 1.2rem;
            margin: 0 10px;
            transition: 0.3s;
        }

        .social-icons a:hover {
            color: #4da6ff;
        }

        .copyright {
            font-size: 0.8rem;
            opacity: 0.8;
        }

        /* === التجاوب مع الجوال === */
        @media (max-width: 768px) {
            .top-bar {
                flex-direction: column;
                gap: 20px;
            }
            
            nav ul {
                gap: 10px;
                flex-wrap: wrap;
                justify-content: center;
            }

            .cards-container {
                margin-top: 20px;
            }
            
            .footer-content {
                flex-direction: column;
                gap: 20px;
                text-align: center;
            }
        }
    </style>
</head>
<body>

    <!-- الهيدر -->
    <header>
        <div class="top-bar">
            <div class="logo-container">
                <!-- أيقونة شعار مؤقتة -->
                <div class="logo-img">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <div class="school-name">
                    <h1>مدرسة المستقبل</h1>
                    <span>للتميز والابتكار</span>
                </div>
            </div>

            <nav>
                <ul>
                    <li><a href="#" class="active">الرئيسية</a></li>
                    <li><a href="#">عن المدرسة</a></li>
                    <li><a href="#">الأقسام الدراسية</a></li>
                    <li><a href="#">الأنشطة</a></li>
                    <li><a href="#">التواصل</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- صورة الغلاف -->
    <section class="hero-section">
        <!-- صورة توضيحية من الإنترنت -->
        <img src="https://images.unsplash.com/photo-1524178232363-1fb2b075b655?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80" alt="طلاب في الفصل">
    </section>

    <!-- البطاقات الثلاثة -->
    <section class="cards-container">
        <!-- البطاقة الأولى -->
        <div class="card">
            <div class="card-icon">
                <i class="fas fa-school"></i>
            </div>
            <h3>المراحل الدراسية</h3>
            <p>نقدم برامج تعليمية متكاملة من الروضة وحتى المرحلة الثانوية بأحدث المناهج.</p>
        </div>

        <!-- البطاقة الثانية -->
        <div class="card">
            <div class="card-icon">
                <i class="fas fa-user-graduate"></i>
            </div>
            <h3>التسجيل والقبول</h3>
            <p>انضم إلينا الآن. افتح باب التسجيل للعام الدراسي الجديد واستفد من العروض.</p>
        </div>

        <!-- البطاقة الثالثة -->
        <div class="card">
            <div class="card-icon">
                <i class="fas fa-users"></i>
            </div>
            <h3>شؤون المعلمين</h3>
            <p>بوابة خاصة للمعلمين للوصول إلى الجداول والموارد التعليمية والقرارات الإدارية.</p>
        </div>
    </section>

    <!-- الفوتر -->
    <footer>
        <div class="footer-content">
            <div class="contact-info">
                <p><i class="fas fa-phone"></i> هاتف: 965 1234 5678+</p>
                <p><i class="fas fa-envelope"></i> البريد: info@school.edu.kw</p>
                <p><i class="fas fa-map-marker-alt"></i> العنوان: الكويت، حولي، شارع التعليم</p>
            </div>
            <div class="social-icons">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
                <a href="#"><i class="fab fa-youtube"></i></a>
            </div>
        </div>
        <div class="copyright">
            <p>جميع الحقوق محفوظة © 2023 مدرسة المستقبل</p>
        </div>
    </footer>

</body>
</html>
```
