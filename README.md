<!DOCTYPE html>
<html lang="ar" dir="rtl" id="html-root">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title data-i18n="page_title">MK Creative Agency | وكالة إم كيه الإبداعية</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700;900&display=swap" rel="stylesheet">
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        :root {
            --bg-color: #f8f9fa;
            --text-color: #1a1a1a;
            --primary-color: #0056b3;
            --secondary-color: #0080ff;
            --card-bg: #ffffff;
            --nav-bg: rgba(255, 255, 255, 0.95);
            --border-color: #e0e0e0;
            --footer-bg: #111111;
            --footer-text: #cccccc;
            --transition: all 0.3s ease;
        }

        [data-theme="dark"] {
            --bg-color: #0b0f19;
            --text-color: #f3f4f6;
            --primary-color: #3b82f6;
            --secondary-color: #60a5fa;
            --card-bg: #1f2937;
            --nav-bg: rgba(15, 23, 42, 0.95);
            --border-color: #374151;
            --footer-bg: #030712;
            --footer-text: #9ca3af;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Cairo', sans-serif;
            transition: var(--transition);
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Reading Progress Bar */
        #progress-bar {
            position: fixed;
            top: 0;
            left: 0;
            height: 4px;
            background: var(--primary-color);
            width: 0%;
            z-index: 1001;
        }

        /* Top Announcement Banner */
        .announcement-banner {
            background: var(--primary-color);
            color: #fff;
            text-align: center;
            padding: 8px 15px;
            font-size: 14px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 15px;
            z-index: 1002;
            position: relative;
        }
        .announcement-banner button {
            background: none;
            border: none;
            color: #fff;
            cursor: pointer;
            font-size: 16px;
        }

        /* Navbar */
        navbar {
            position: sticky;
            top: 0;
            background-color: var(--nav-bg);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 5%;
            z-index: 1000;
        }

        .logo {
            font-size: 24px;
            font-weight: 900;
            color: var(--primary-color);
            display: flex;
            align-items: center;
            gap: 8px;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 18px;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 600;
            font-size: 14px;
        }

        .nav-links a:hover, .nav-links a.active {
            color: var(--primary-color);
        }

        .nav-actions {
            display: flex;
            gap: 8px;
            align-items: center;
            flex-wrap: wrap;
        }

        .icon-btn, .lang-btn {
            background: none;
            border: 1px solid var(--border-color);
            color: var(--text-color);
            padding: 0 10px;
            height: 38px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 5px;
        }

        .icon-btn {
            width: 38px;
            padding: 0;
            font-size: 16px;
        }

        .icon-btn:hover, .lang-btn:hover {
            border-color: var(--primary-color);
            color: var(--primary-color);
        }

        .social-icon-link {
            width: 38px;
            height: 38px;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            color: var(--text-color);
            text-decoration: none;
            font-size: 16px;
        }
        .social-icon-link:hover {
            border-color: var(--primary-color);
            color: var(--primary-color);
            background: rgba(0,86,179,0.05);
        }

        .btn-whatsapp {
            background-color: #25d366;
            color: white;
            padding: 8px 14px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            font-size: 13px;
            box-shadow: 0 4px 10px rgba(37, 211, 102, 0.3);
        }
        .btn-whatsapp:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            padding: 100px 5%;
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 50px;
            background: linear-gradient(135deg, rgba(0,86,179,0.05) 0%, rgba(0,128,255,0.05) 100%);
        }

        .hero-content {
            flex: 1;
        }

        .hero-content h1 {
            font-size: 46px;
            font-weight: 900;
            margin-bottom: 20px;
            line-height: 1.2;
        }

        .hero-content h1 span {
            color: var(--primary-color);
        }

        .hero-content p {
            font-size: 18px;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
            border: 1px solid var(--border-color);
        }

        .btn-primary {
            background-color: var(--primary-color);
            color: white;
            padding: 12px 30px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 700;
            display: inline-block;
            box-shadow: 0 4px 15px rgba(0,86,179,0.3);
            border: none;
            cursor: pointer;
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            opacity: 0.9;
        }

        /* Stats Section */
        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            padding: 50px 5%;
            background-color: var(--card-bg);
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
            text-align: center;
        }

        .stat-item h2 {
            font-size: 36px;
            font-weight: 900;
            color: var(--primary-color);
            margin-bottom: 5px;
        }

        .stat-item p {
            font-size: 14px;
            opacity: 0.8;
        }

        /* Section Titles */
        .section-title {
            text-align: center;
            margin: 60px 0 30px;
            font-size: 32px;
            font-weight: 800;
        }

        /* About Section */
        .about-section {
            padding: 80px 5%;
            background-color: var(--card-bg);
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
        }
        .about-container {
            max-width: 1000px;
            margin: 0 auto;
        }
        .about-section p {
            font-size: 17px;
            opacity: 0.9;
            margin-bottom: 20px;
            line-height: 1.8;
        }

        /* Why Us Section */
        .why-us-section {
            padding: 60px 5%;
            max-width: 1200px;
            margin: 0 auto;
        }
        .why-us-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
        }
        .why-us-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }
        .why-us-card h3 {
            color: var(--primary-color);
            font-size: 18px;
            margin-bottom: 10px;
        }
        .why-us-card p {
            font-size: 14px;
            opacity: 0.85;
        }

        /* Services Grid */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            padding: 0 5% 60px;
            max-width: 1300px;
            margin: 0 auto;
        }

        .service-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            display: flex;
            flex-direction: column;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .service-card img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .service-card-content {
            padding: 25px;
            display: flex;
            flex-direction: column;
            flex: 1;
        }

        .service-card h3 {
            font-size: 20px;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .service-card p {
            font-size: 15px;
            opacity: 0.85;
            margin-bottom: 20px;
            flex: 1;
        }

        .service-btn {
            background-color: var(--primary-color);
            color: white;
            text-align: center;
            padding: 10px;
            border-radius: 6px;
            text-decoration: none;
            font-weight: 600;
        }
        .service-btn:hover {
            opacity: 0.9;
        }

        /* Portfolio / Projects Section */
        .portfolio-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding: 0 5% 60px;
            max-width: 1300px;
            margin: 0 auto;
        }

        .portfolio-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }

        .portfolio-card img {
            width: 100%;
            height: 190px;
            object-fit: cover;
        }

        .portfolio-card-body {
            padding: 25px;
            display: flex;
            flex-direction: column;
            flex: 1;
            justify-content: space-between;
        }

        .portfolio-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
        }

        .portfolio-tag {
            display: inline-block;
            background: rgba(0,86,179,0.1);
            color: var(--primary-color);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 700;
            margin-bottom: 15px;
        }

        .portfolio-card h3 {
            font-size: 20px;
            margin-bottom: 10px;
        }

        .portfolio-card p {
            font-size: 14px;
            opacity: 0.8;
            margin-bottom: 20px;
        }

        .project-links {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .project-link-btn {
            flex: 1;
            background: var(--primary-color);
            color: white;
            text-align: center;
            padding: 8px 12px;
            border-radius: 6px;
            font-size: 13px;
            font-weight: 700;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 6px;
        }
        .project-link-btn.github {
            background: #24292e;
        }
        .project-link-btn.live {
            background: #059669;
        }
        .project-link-btn:hover {
            opacity: 0.85;
        }

        /* Future Enhancements Section */
        .enhancements-section {
            padding: 60px 5%;
            background-color: var(--card-bg);
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
            max-width: 1300px;
            margin: 0 auto 60px;
            border-radius: 12px;
        }
        .enhancements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        .enhancement-card {
            border: 1px solid var(--border-color);
            padding: 20px;
            border-radius: 8px;
            background: var(--bg-color);
        }
        .enhancement-card h4 {
            color: var(--primary-color);
            margin-bottom: 8px;
            font-size: 16px;
        }
        .enhancement-card p {
            font-size: 14px;
            opacity: 0.8;
        }

        /* Career / Join Us Section */
        .order-section {
            padding: 80px 5%;
            background: linear-gradient(135deg, rgba(0,86,179,0.08) 0%, rgba(0,128,255,0.08) 100%);
            border-top: 1px solid var(--border-color);
            border-bottom: 1px solid var(--border-color);
            text-align: center;
        }

        .order-container {
            max-width: 800px;
            margin: 0 auto;
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 40px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.05);
        }

        .order-container h3 {
            font-size: 28px;
            font-weight: 900;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .order-container p {
            font-size: 16px;
            opacity: 0.85;
            margin-bottom: 30px;
        }

        /* Testimonials Section */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            padding: 0 5% 60px;
            max-width: 1300px;
            margin: 0 auto;
        }

        .testimonial-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 30px;
            position: relative;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .testimonial-card i.fa-quote-right {
            position: absolute;
            top: 20px;
            left: 20px;
            font-size: 30px;
            color: var(--primary-color);
            opacity: 0.2;
        }

        [dir="ltr"] .testimonial-card i.fa-quote-right {
            left: auto;
            right: 20px;
        }

        .testimonial-card p {
            font-size: 15px;
            margin-bottom: 20px;
            opacity: 0.9;
        }

        .client-info h4 {
            font-size: 16px;
            font-weight: 700;
        }

        .client-info span {
            font-size: 13px;
            opacity: 0.7;
        }

        /* Articles / LinkedIn Posts Section */
        .articles-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
            padding: 0 5% 60px;
            max-width: 1300px;
            margin: 0 auto;
        }

        .article-card {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 30px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
        }

        .article-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary-color);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .article-meta {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 13px;
            color: var(--primary-color);
            margin-bottom: 15px;
            font-weight: 700;
        }

        .article-card h3 {
            font-size: 20px;
            margin-bottom: 15px;
            line-height: 1.4;
        }

        .article-card p {
            font-size: 15px;
            opacity: 0.85;
            margin-bottom: 25px;
        }

        .read-more-btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            color: var(--primary-color);
            font-weight: 700;
            text-decoration: none;
            font-size: 15px;
        }

        .read-more-btn:hover {
            text-decoration: underline;
        }

        /* FAQ Section */
        .faq-container {
            max-width: 900px;
            margin: 0 auto 60px;
            padding: 0 5%;
        }

        .faq-item {
            background-color: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            margin-bottom: 15px;
            overflow: hidden;
        }

        .faq-question {
            padding: 20px;
            font-size: 17px;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
            user-select: none;
        }

        .faq-answer {
            padding: 0 20px 20px;
            font-size: 15px;
            opacity: 0.85;
            display: none;
        }

        .faq-item.active .faq-answer {
            display: block;
        }

        .faq-item.active .faq-question i {
            transform: rotate(180deg);
        }

        /* Newsletter Section */
        .newsletter-section {
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            color: #ffffff;
            padding: 80px 5%;
            text-align: center;
        }

        .newsletter-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .newsletter-container h2 {
            font-size: 32px;
            font-weight: 900;
            margin-bottom: 15px;
        }

        .newsletter-container p {
            font-size: 16px;
            margin-bottom: 30px;
            opacity: 0.9;
        }

        .newsletter-form {
            display: flex;
            gap: 10px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .newsletter-form input {
            flex: 1;
            min-width: 280px;
            padding: 14px 20px;
            border-radius: 8px;
            border: none;
            font-size: 16px;
            outline: none;
            background-color: #ffffff;
            color: #1a1a1a;
        }

        .newsletter-form button {
            background-color: #111111;
            color: white;
            padding: 14px 30px;
            border-radius: 8px;
            font-weight: 700;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 10px rgba(0,0,0,0.2);
        }

        .newsletter-form button:hover {
            background-color: #222222;
        }

        /* Footer */
        footer {
            background-color: var(--footer-bg);
            color: var(--footer-text);
            padding: 60px 5% 30px;
            border-top: 1px solid var(--border-color);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
            max-width: 1300px;
            margin-left: auto;
            margin-right: auto;
        }

        .footer-col h4 {
            color: #fff;
            margin-bottom: 20px;
            font-size: 18px;
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 10px;
        }

        .footer-col ul li a {
            color: var(--footer-text);
            text-decoration: none;
        }

        .footer-col ul li a:hover {
            color: var(--primary-color);
        }

        .footer-socials {
            display: flex;
            gap: 10px;
            margin-top: 15px;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 14px;
            max-width: 1300px;
            margin: 0 auto;
        }

        /* Back to Top */
        #back-to-top {
            position: fixed;
            bottom: 20px;
            left: 20px;
            background: var(--primary-color);
            color: #fff;
            border: none;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            z-index: 999;
        }

        [dir="ltr"] #back-to-top {
            left: auto;
            right: 20px;
        }

        @media(max-width: 992px) {
            .nav-links {
                display: none;
            }
            .hero {
                flex-direction: column;
                text-align: center;
            }
        }
    </style>
</head>
<body data-theme="dark" id="home">

    <!-- Reading Progress Bar -->
    <div id="progress-bar"></div>

    <!-- Top Announcement Banner -->
    <div class="announcement-banner" id="banner">
        <span data-i18n="banner_text">🚀 انضم إلى فريقنا الآن أو تواصل عبر ديسكورد وواتساب للمشاركة في مشاريعنا!</span>
        <button onclick="document.getElementById('banner').style.display='none'">&times;</button>
    </div>

    <!-- Navbar -->
    <navbar>
        <a href="#home" class="logo">
            <i class="fa-solid fa-cube"></i> MK CREATIVE
        </a>
        <ul class="nav-links">
            <li><a href="#home" data-i18n="nav_home">الرئيسية</a></li>
            <li><a href="#about" data-i18n="nav_about">من نحن</a></li>
            <li><a href="#services" data-i18n="nav_services">خدماتنا</a></li>
            <li><a href="#portfolio" data-i18n="nav_portfolio">معرض الأعمال</a></li>
            <li><a href="#join" data-i18n="nav_join">انضم إلينا</a></li>
            <li><a href="#testimonials" data-i18n="nav_testimonials">آراء العملاء</a></li>
            <li><a href="#articles" data-i18n="nav_articles">أحدث المقالات</a></li>
            <li><a href="#faq" data-i18n="nav_faq">الأسئلة الشائعة</a></li>
        </ul>
        <div class="nav-actions">
            <!-- Language Switcher Button -->
            <button class="lang-btn" id="lang-toggle" title="Change Language / تغيير اللغة">
                <i class="fa-solid fa-globe"></i> <span id="lang-text">EN</span>
            </button>
            <!-- Discord -->
            <a href="https://discord.gg/rzXhZ7dsDF" target="_blank" class="social-icon-link" title="Discord">
                <i class="fa-brands fa-discord"></i>
            </a>
            <!-- LinkedIn -->
            <a href="https://www.linkedin.com/company/mk-creative-agency36?trk=experience-timeline" target="_blank" class="social-icon-link" title="LinkedIn">
                <i class="fa-brands fa-linkedin-in"></i>
            </a>
            <!-- F6S -->
            <a href="https://www.f6s.com/mk-creative-agency" target="_blank" class="social-icon-link" title="F6S Community">
                <i class="fa-solid fa-globe"></i>
            </a>
            <!-- Dark/Light Mode Toggle -->
            <button class="icon-btn" id="theme-toggle" title="Toggle Theme">
                <i class="fa-solid fa-moon" id="theme-icon"></i>
            </button>
            <a href="https://wa.me/201559719175" target="_blank" class="btn-whatsapp" title="WhatsApp">
                <i class="fa-brands fa-whatsapp"></i>
            </a>
        </div>
    </navbar>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1 data-i18n="hero_title">نصنع المستقبل الرقمي <span>بابتكار واحترافية</span></h1>
            <p data-i18n="hero_desc">نحن وكالة MK Creative نقدم حلولاً متكاملة في تطوير البرمجيات، تصميم الويب، صناعة المحتوى، والمونتاج الرقمي لنرتقي بمشروعك نحو القمة.</p>
            <div style="display: flex; gap: 15px; flex-wrap: wrap;">
                <a href="#join" class="btn-primary"><span data-i18n="hero_btn">انضم لفريق العمل الآن</span> <i class="fa-solid fa-arrow-left"></i></a>
                <a href="https://discord.gg/rzXhZ7dsDF" target="_blank" class="social-icon-link" style="width: 48px; height: 48px; font-size: 20px; background: var(--card-bg);" title="Discord"><i class="fa-brands fa-discord"></i></a>
            </div>
        </div>
        <div class="hero-image">
            <img src="صورة خدمات تطوير الويب.png" alt="MK Creative Agency Solutions">
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="stat-item">
            <h2>46K+</h2>
            <p data-i18n="stat_1">متابع ومهتم حول العالم</p>
        </div>
        <div class="stat-item">
            <h2>1M+</h2>
            <p data-i18n="stat_2">مشاهدات وإبداع للمحتوى الرقمي</p>
        </div>
        <div class="stat-item">
            <h2>95%</h2>
            <p data-i18n="stat_3">تقييمات رضا العملاء والشركاء</p>
        </div>
        <div class="stat-item">
            <h2>100%</h2>
            <p data-i18n="stat_4">التزام وجودة في تسليم المشاريع</p>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about-section">
        <div class="about-container">
            <h2 class="section-title" style="margin-top: 0;" data-i18n="about_title">من نحن</h2>
            <p data-i18n="about_desc_1">نحن <strong>MK CREATIVE Agency</strong>، وكالة رقمية متكاملة نشأت برؤية طموحة لتلهم وتغير شكل الويب وصناعة المحتوى الرقمي. لا نقتصر على تقديم خدمات تقليدية، بل نصنع تجارب رقمية متكاملة تدمج بين الابتكار التقني والتصميم الإبداعي.</p>
            <p data-i18n="about_desc_2">بدأت رحلتنا بشغف حقيقي بالبرمجة والتطوير وصناعة المحتوى، وتطورنا لنصبح الوجهة الأولى لكل من يبحث عن التميز الاحترافي عبر الإنترنت. فريقنا يمتلك خبرة واسعة في هندسة البرمجيات، وتصميم وتطوير واجهات الويب العصرية، والمونتاج الاحترافي لصناعة الفيديوهات التي تخطف الأنظار، بالإضافة إلى إدارة المنصات الرقمية وتقديم حلول برمجية ذكية. هدفنا الدائم هو تحويل الأفكار المعقدة إلى مشاريع رقمية سلسة، جذابة، وعالية الأداء.</p>
        </div>
    </section>

    <!-- Why Choose Us Section -->
    <section class="why-us-section">
        <h2 class="section-title" data-i18n="why_us_title">لماذا نحن؟</h2>
        <div class="why-us-grid">
            <div class="why-us-card">
                <h3 data-i18n="why_1_title">إبداع بلا حدود</h3>
                <p data-i18n="why_1_desc">نمزج بين التصميم الفني الجذاب والتطوير البرمجي القوي لنضمن لك حضوراً رقمياً فريداً ومميزاً.</p>
            </div>
            <div class="why-us-card">
                <h3 data-i18n="why_2_title">حلول تقنية متكاملة</h3>
                <p data-i18n="why_2_desc">نوفر لك كل ما تحتاجه تحت سقف واحد (تصميم ويب، برمجة، ألعاب تفاعلية، ومحتوى رقمي).</p>
            </div>
            <div class="why-us-card">
                <h3 data-i18n="why_3_title">دقة واحترافية عالية</h3>
                <p data-i18n="why_3_desc">نلتزم بأعلى معايير الجودة والدقة في تسليم المشاريع وتطوير التطبيقات في مواعيدها.</p>
            </div>
            <div class="why-us-card">
                <h3 data-i18n="why_4_title">شغف مستمر بالتطوير</h3>
                <p data-i18n="why_4_desc">نتابع دائماً أحدث التقنيات والاتجاهات العالمية في التكنولوجيا والتصميم لنبقي مشاريعك في الصدارة.</p>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2 class="section-title" data-i18n="services_title">خدماتنا الاحترافية</h2>
        <div class="services-grid">
            <div class="service-card">
                <img src="صورة خدمات تطوير الويب.png" alt="Web Development">
                <div class="service-card-content">
                    <h3 data-i18n="srv_1_title">تطوير الويب</h3>
                    <p data-i18n="srv_1_desc">نصمم ونطور مواقع ويب احترافية، سريعة وآمنة لتجربة مستخدم استثنائية.</p>
                    <a href="#join" class="service-btn" data-i18n="srv_btn">انضم للعمل معنا</a>
                </div>
            </div>
            <div class="service-card">
                <img src="صورة خدمة المونتاج .png" alt="Video Editing">
                <div class="service-card-content">
                    <h3 data-i18n="srv_2_title">خدمة المونتاج</h3>
                    <p data-i18n="srv_2_desc">نحول أفكارك إلى فيديوهات احترافية تعكس هويتك وتصل رسالتك بوضوح وجودة عالية.</p>
                    <a href="#join" class="service-btn" data-i18n="srv_btn">انضم للعمل معنا</a>
                </div>
            </div>
            <div class="service-card">
                <img src="صورة تصميم الاعلانات .png" alt="Ad Design">
                <div class="service-card-content">
                    <h3 data-i18n="srv_3_title">تصميم الإعلانات</h3>
                    <p data-i18n="srv_3_desc">تصميم إعلانات تجذب الانتباه، تبني هوية بصرية قوية وتحقق نتائج حقيقية.</p>
                    <a href="#join" class="service-btn" data-i18n="srv_btn">انضم للعمل معنا</a>
                </div>
            </div>
            <div class="service-card">
                <img src="صورة تسويق الكتروني .png" alt="Digital Marketing">
                <div class="service-card-content">
                    <h3 data-i18n="srv_4_title">التسويق عبر الإنترنت</h3>
                    <p data-i18n="srv_4_desc">نساعدك على الوصول لجمهورك المستهدف وزيادة الوعي بعلامتك التجارية عبر استراتيجيات تسويقية فعالة.</p>
                    <a href="#join" class="service-btn" data-i18n="srv_btn">انضم للعمل معنا</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Portfolio Section -->
    <section id="portfolio">
        <h2 class="section-title" data-i18n="portfolio_title">معرض الأعمال والمشاريع</h2>
        <div class="portfolio-grid">
            <!-- ChessCraft -->
            <div class="portfolio-card">
                <img src="صورة خدمات تطوير الويب.png" alt="ChessCraft">
                <div class="portfolio-card-body">
                    <div>
                        <span class="portfolio-tag" data-i18n="tag_web">تطوير الويب والمنصات</span>
                        <h3>ChessCraft</h3>
                        <p data-i18n="proj_chess_desc">تطبيق ويب تفاعلي مصمم لإرشاد المبتدئين في تعلم خطوات الشطرنج واستراتيجيات الافتتاحيات.</p>
                    </div>
                    <div class="project-links">
                        <a href="https://moamedantar8-a11y.github.io/ChessCraft-/" target="_blank" class="project-link-btn live"><i class="fa-solid fa-globe"></i> معاينة حية</a>
                        <a href="https://github.com/moamedantar8-a11y/ChessCraft-" target="_blank" class="project-link-btn github"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>
            </div>
            <!-- Mozakra Pro Platform -->
            <div class="portfolio-card">
                <img src="صورة خدمات تطوير الويب.png" alt="Mozakra Pro Platform">
                <div class="portfolio-card-body">
                    <div>
                        <span class="portfolio-tag" data-i18n="tag_edu">منصات تعليمية</span>
                        <h3>Mozakra Pro Platform</h3>
                        <p data-i18n="proj_mozakra_desc">بوابة تعليمية متكاملة للطلاب تضم اختبارات تفاعلية، منصات للمعلمين، وتصميم متجاوب وسريع.</p>
                    </div>
                    <div class="project-links">
                        <a href="https://moamedantar8-a11y.github.io/Mozakra-Pro-Platform-/" target="_blank" class="project-link-btn live"><i class="fa-solid fa-globe"></i> معاينة حية</a>
                        <a href="https://github.com/moamedantar8-a11y/Mozakra-Pro-Platform-" target="_blank" class="project-link-btn github"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>
            </div>
            <!-- MK Car Race -->
            <div class="portfolio-card">
                <img src="صورة خدمة المونتاج .png" alt="MK Car Race">
                <div class="portfolio-card-body">
                    <div>
                        <span class="portfolio-tag" data-i18n="tag_games">ألعاب وتطبيقات ترفيهية</span>
                        <h3>MK Car Race</h3>
                        <p data-i18n="proj_car_desc">لعبة سباق سيارات ممتعة وتفاعلية تم تطويرها بلغات الويب الحديثة لتجربة لعب سلسة.</p>
                    </div>
                    <div class="project-links">
                        <a href="https://moamedantar8-a11y.github.io/MK-Car-Race-/" target="_blank" class="project-link-btn live"><i class="fa-solid fa-globe"></i> تجربة اللعبة</a>
                        <a href="https://github.com/moamedantar8-a11y/MK-Car-Race-" target="_blank" class="project-link-btn github"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>
            </div>
            <!-- MK CREATIVE Games -->
            <div class="portfolio-card">
                <img src="صورة تصميم الاعلانات .png" alt="MK CREATIVE Games">
                <div class="portfolio-card-body">
                    <div>
                        <span class="portfolio-tag" data-i18n="tag_games">ألعاب وتطبيقات ترفيهية</span>
                        <h3>MK CREATIVE Games</h3>
                        <p data-i18n="proj_games_desc">منصة ومجموعة ألعاب مميزة تحت مظلة وكالة MK Creative لتوفير تجارب ترفيهية تفاعلية.</p>
                    </div>
                    <div class="project-links">
                        <a href="https://moamedantar8-a11y.github.io/Mk-CREATIVE-Games-/" target="_blank" class="project-link-btn live"><i class="fa-solid fa-globe"></i> استكشاف الألعاب</a>
                        <a href="https://github.com/moamedantar8-a11y/Mk-CREATIVE-Games-" target="_blank" class="project-link-btn github"><i class="fa-brands fa-github"></i> GitHub</a>
                    </div>
                </div>
            </div>
            <!-- Future Mall POS -->
            <div class="portfolio-card">
                <img src="صورة تسويق الكتروني .png" alt="Future Mall">
                <div class="portfolio-card-body">
                    <div>
                        <span class="portfolio-tag" data-i18n="tag_systems">برمجيات وأنظمة</span>
                        <h3>Future Mall (POS)</h3>
                        <p data-i18n="proj_mall_desc">نظام إدارة مبيعات ونقاط بيع متطور يدعم تعدد العملات، إدارة المخزون، وصلاحيات المستخدمين.</p>
                    </div>
                    <div class="project-links">
                        <a href="#join" class="project-link-btn" style="width: 100%;"><span data-i18n="proj_join_hint">ساهم في تطوير المشاريع</span> <i class="fa-solid fa-arrow-left"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Future Enhancements & Features Section -->
    <section class="enhancements-section">
        <h2 class="section-title" style="margin-top: 0;" data-i18n="enhancements_title">التطويرات القادمة في المنصة</h2>
        <p style="text-align: center; opacity: 0.85;" data-i18n="enhancements_subtitle">نحن نعمل باستمرار على تطوير موقعنا وخدماتنا لتقديم تجربة أفضل لعملائنا، وإليك أبرز الإضافات القادمة:</p>
        <div class="enhancements-grid">
            <div class="enhancement-card">
                <h4 data-i18n="enh_1_title">نظام حجز الخدمات الفوري</h4>
                <p data-i18n="enh_1_desc">أداة تفاعلية تتيح لك اختيار الخدمة وحساب التكلفة والوقت التقديري بشكل مبدئي.</p>
            </div>
            <div class="enhancement-card">
                <h4 data-i18n="enh_2_title">قسم آراء العملاء وقصص النجاح</h4>
                <p data-i18n="enh_2_desc">عرض مشاريعنا السابقة بالأرقام والنتائج المؤثرة مع تقييمات العملاء.</p>
            </div>
            <div class="enhancement-card">
                <h4 data-i18n="enh_3_title">خدمات الأمان السيبراني وحماية المواقع</h4>
                <p data-i18n="enh_3_desc">إضافة باقات متخصصة لحماية وتأمين منصات ومواقع الشركات ضد الثغرات.</p>
            </div>
            <div class="enhancement-card">
                <h4 data-i18n="enh_4_title">المدونة التقنية والإبداعية</h4>
                <p data-i18n="enh_4_desc">مركز لمعرفة أحدث المقالات والنصائح في البرمجة، المونتاج، وإدارة قنوات اليوتيوب.</p>
            </div>
        </div>
    </section>

    <!-- Join Us / Career Form Section -->
    <section id="join" class="order-section">
        <div class="order-container">
            <h3 data-i18n="join_box_title">انضم إلى فريق عمل MK Creative Agency</h3>
            <p data-i18n="join_box_desc">هل تمتلك شغفاً ومهارة في البرمجة، المونتاج، التصميم، أو صناعة المحتوى وترغب في العمل معنا؟ املأ استمارة التوظيف والبيانات الخاصة بك عبر المنصة المخصصة وسنتواصل معك قريباً.</p>
            <a href="https://surveymars.com/q/l0irKxv2M" target="_blank" class="btn-primary" style="font-size: 17px; padding: 15px 35px;">
                <i class="fa-solid id-card"></i> <span data-i18n="join_box_btn">املأ استمارة التوظيف الآن</span>
            </a>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials">
        <h2 class="section-title" data-i18n="testimonials_title">آراء العملاء والشركاء</h2>
        <div class="testimonials-grid">
            <div class="testimonial-card">
                <i class="fa-solid fa-quote-right"></i>
                <p data-i18n="test_1">"التعامل مع MK Creative Agency كان نقطة تحول حقيقية في مشروعي. سرعة في الأداء واحترافية عالية جداً في البرمجة والتصميم."</p>
                <div class="client-info">
                    <h4 data-i18n="test_1_name">أحمد محمود</h4>
                    <span data-i18n="test_1_role">رائد أعمال ومهتم بالتقنية</span>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fa-solid fa-quote-right"></i>
                <p data-i18n="test_2">"خدمة المونتاج وتعديل الفيديوهات فاقت توقعاتي بكثير. الأسلوب الإبداعي والالتزام بالمواعيد يستحق كل التقدير والاحترام."</p>
                <div class="client-info">
                    <h4 data-i18n="test_2_name">محمد عادل</h4>
                    <span data-i18n="test_2_role">صانع محتوى رقمي</span>
                </div>
            </div>
            <div class="testimonial-card">
                <i class="fa-solid fa-quote-right"></i>
                <p data-i18n="test_3">"منصة الويب التي تم برمجتها لنا تعمل بكفاءة تامة وبدون أي أخطاء. شكراً لفريق العمل على الدعم المستمر."</p>
                <div class="client-info">
                    <h4 data-i18n="test_3_name">محمود إبراهيم</h4>
                    <span data-i18n="test_3_role">مدير تسويق إلكتروني</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Latest Articles / LinkedIn Posts Section -->
    <section id="articles">
        <h2 class="section-title" data-i18n="articles_title">أحدث المقالات والمنشورات</h2>
        <div class="articles-grid">
            <div class="article-card">
                <div>
                    <div class="article-meta">
                        <i class="fa-brands fa-linkedin"></i> LinkedIn Update
                    </div>
                    <h3>MK Creative Agency Empowers the Next Generation</h3>
                    <p data-i18n="art_1_desc">استكشف كيف نقوم بتمكين الجيل القادم من المبدعين والمطورين بأحدث الأدوات والمهارات التقنية...</p>
                </div>
                <a href="https://www.linkedin.com/posts/mk-creative-agency36_mk-creative-agency-empowers-the-next-generation-activity-7501650908510879744-UNjc?utm_source=share&utm_medium=member_android&rcm=ACoAAGedAaoBHEiudTvVQc0BQ94lZLdiW48h4tA" target="_blank" class="read-more-btn">
                    <span data-i18n="read_more">Read more</span> <i class="fa-solid fa-arrow-left"></i>
                </a>
            </div>
            <div class="article-card">
                <div>
                    <div class="article-meta">
                        <i class="fa-brands fa-linkedin"></i> LinkedIn Update
                    </div>
                    <h3>Beyond Limits: How MK Creative Agency Is Growing</h3>
                    <p data-i18n="art_2_desc">نظرة عميقة على استراتيجياتنا لتجاوز الحدود التقليدية وتحقيق آفاق جديدة في عالم الإبداع الرقمي...</p>
                </div>
                <a href="https://www.linkedin.com/posts/mk-creative-agency36_beyond-limits-how-mk-creative-agency-is-activity-7501280349080023042-ZSwr?utm_source=share&utm_medium=member_android&rcm=ACoAAGedAaoBHEiudTvVQc0BQ94lZLdiW48h4tA" target="_blank" class="read-more-btn">
                    <span data-i18n="read_more">Read more</span> <i class="fa-solid fa-arrow-left"></i>
                </a>
            </div>
            <div class="article-card">
                <div>
                    <div class="article-meta">
                        <i class="fa-brands fa-linkedin"></i> LinkedIn Update
                    </div>
                    <h3>MK Creative Agency Is a Global Digital Agency</h3>
                    <p data-i18n="art_3_desc">تعرف على رؤيتنا وكيف تحولنا إلى وكالة رقمية عالمية تقدم خدمات متكاملة للمستخدمين والشركات...</p>
                </div>
                <a href="https://www.linkedin.com/posts/mk-creative-agency36_mk-creative-agency-is-a-global-digital-agency-activity-7501216617545109504-pRA7?utm_source=share&utm_medium=member_android&rcm=ACoAAGedAaoBHEiudTvVQc0BQ94lZLdiW48h4tA" target="_blank" class="read-more-btn">
                    <span data-i18n="read_more">Read more</span> <i class="fa-solid fa-arrow-left"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section id="faq">
        <h2 class="section-title" data-i18n="faq_title">الأسئلة الشائعة</h2>
        <div class="faq-container">
            <div class="faq-item">
                <div class="faq-question">
                    <span data-i18n="faq_q1">كيف يمكنني الانضمام والعمل مع الوكالة؟</span>
                    <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="faq-answer" data-i18n="faq_a1">
                    يمكنك الانتقال إلى قسم "انضم إلينا" وملء استمارة التوظيف الرسمية عبر الرابط المخصص، أو التواصل معنا مباشرة عبر ديسكورد أو واتساب.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question">
                    <span data-i18n="faq_q2">ما هي الشروط المطلوبة للانضمام لفريق العمل؟</span>
                    <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="faq-answer" data-i18n="faq_a2">
                    نبحث دائماً عن الشغف، المهارة الجيدة، والالتزام بتطوير المشاريع الرقمية والتقنية باحترافية تامة.
                </div>
            </div>
            <div class="faq-item">
                <div class="faq-question">
                    <span data-i18n="faq_q3">كيف يتم التواصل بعد تقديم الاستمارة؟</span>
                    <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="faq-answer" data-i18n="faq_a3">
                    يتم مراجعة البيانات المدخلة في الاستمارة بعناية والتواصل مع المرشحين المقبولين عبر وسائل الاتصال المتاحة.
                </div>
            </div>
        </div>
    </section>

    <!-- Newsletter Section -->
    <section class="newsletter-section">
        <div class="newsletter-container">
            <h2 data-i18n="news_title">انضم إلى MK Creative Agency Newsletters</h2>
            <p data-i18n="news_desc">احصل على أحدث التحديثات، التقارير التقنية، والعروض الحصرية مباشرة في بريدك الإلكتروني أسبوعياً.</p>
            <form class="newsletter-form" action="https://formspree.io/f/mgaezlwq" method="POST">
                <input type="email" name="email" placeholder="أدخل بريدك الإلكتروني هنا..." data-i18n-placeholder="news_placeholder" required>
                <button type="submit" data-i18n="news_btn">اشتراك الآن</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="footer-grid">
            <div class="footer-col">
                <h4>MK CREATIVE AGENCY</h4>
                <p data-i18n="footer_desc">مؤسسة رقمية رائدة متخصصة في الحلول التقنية والإبداعية.</p>
                <p style="margin-top: 10px;"><i class="fa-brands fa-discord"></i> <span data-i18n="footer_discord">ديسكورد:</span> <a href="https://discord.gg/rzXhZ7dsDF" target="_blank" style="color: #5865F2;" data-i18n="footer_discord_link">انضم لمجتمعنا</a></p>
                <p style="margin-top: 5px;"><i class="fa-brands fa-whatsapp"></i> <span data-i18n="footer_whatsapp">واتساب:</span> <a href="https://wa.me/201559719175" target="_blank" style="color: #25d366; direction: ltr; display: inline-block;">01559719175</a></p>
                <div class="footer-socials">
                    <a href="https://discord.gg/rzXhZ7dsDF" target="_blank" class="social-icon-link" title="Discord"><i class="fa-brands fa-discord"></i></a>
                    <a href="https://www.linkedin.com/company/mk-creative-agency36?trk=experience-timeline" target="_blank" class="social-icon-link" title="LinkedIn"><i class="fa-brands fa-linkedin-in"></i></a>
                    <a href="https://www.f6s.com/mk-creative-agency" target="_blank" class="social-icon-link" title="F6S"><i class="fa-solid fa-globe"></i></a>
                </div>
            </div>
            <div class="footer-col">
                <h4 data-i18n="footer_links_title">روابط سريعة</h4>
                <ul>
                    <li><a href="#home" data-i18n="nav_home">الرئيسية</a></li>
                    <li><a href="#about" data-i18n="nav_about">من نحن</a></li>
                    <li><a href="#services" data-i18n="nav_services">خدماتنا</a></li>
                    <li><a href="#portfolio" data-i18n="nav_portfolio">معرض الأعمال</a></li>
                    <li><a href="#join" data-i18n="nav_join">انضم إلينا</a></li>
                    <li><a href="#testimonials" data-i18n="nav_testimonials">آراء العملاء</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h4 data-i18n="footer_partners_title">الشركاء والفرص</h4>
                <ul>
                    <li><a href="https://discord.gg/rzXhZ7dsDF" target="_blank" data-i18n="p_discord">مجتمع ديسكورد</a></li>
                    <li><a href="https://www.linkedin.com/company/mk-creative-agency36?trk=experience-timeline" target="_blank" data-i18n="p_linkedin">صفحة لينكد إن</a></li>
                    <li><a href="https://www.f6s.com/mk-creative-agency" target="_blank">مجتمع F6S</a></li>
                    <li><a href="https://wa.me/201559719175" target="_blank" data-i18n="p_whatsapp">التواصل المباشر (واتساب)</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-bottom">
            <p data-i18n="footer_copy">&copy; 2026 MK Creative Agency. جميع الحقوق محفوظة.</p>
        </div>
    </footer>

    <!-- Back to Top -->
    <button id="back-to-top" onclick="window.scrollTo({top: 0, behavior: 'smooth'})">
        <i class="fa-solid fa-arrow-up"></i>
    </button>

    <!-- JavaScript for Interactions & Multi-Language System -->
    <script>
        const translations = {
            ar: {
                page_title: "MK Creative Agency | وكالة إم كيه الإبداعية",
                banner_text: "🚀 انضم إلى فريقنا الآن أو تواصل عبر ديسكورد وواتساب للمشاركة في مشاريعنا!",
                nav_home: "الرئيسية",
                nav_about: "من نحن",
                nav_services: "خدماتنا",
                nav_portfolio: "معرض الأعمال",
                nav_join: "انضم إلينا",
                nav_testimonials: "آراء العملاء",
                nav_articles: "أحدث المقالات",
                nav_faq: "الأسئلة الشائعة",
                hero_title: "نصنع المستقبل الرقمي <span>بابتكار واحترافية</span>",
                hero_desc: "نحن وكالة MK Creative نقدم حلولاً متكاملة في تطوير البرمجيات، تصميم الويب، صناعة المحتوى، والمونتاج الرقمي لنرتقي بمشروعك نحو القمة.",
                hero_btn: "انضم لفريق العمل الآن",
                stat_1: "متابع ومهتم حول العالم",
                stat_2: "مشاهدات وإبداع للمحتوى الرقمي",
                stat_3: "تقييمات رضا العملاء والشركاء",
                stat_4: "التزام وجودة في تسليم المشاريع",
                about_title: "من نحن",
                about_desc_1: "نحن <strong>MK CREATIVE Agency</strong>، وكالة رقمية متكاملة نشأت برؤية طموحة لتلهم وتغير شكل الويب وصناعة المحتوى الرقمي. لا نقتصر على تقديم خدمات تقليدية، بل نصنع تجارب رقمية متكاملة تدمج بين الابتكار التقني والتصميم الإبداعي.",
                about_desc_2: "بدأت رحلتنا بشغف حقيقي بالبرمجة والتطوير وصناعة المحتوى، وتطورنا لنصبح الوجهة الأولى لكل من يبحث عن التميز الاحترافي عبر الإنترنت. فريقنا يمتلك خبرة واسعة في هندسة البرمجيات، وتصميم وتطوير واجهات الويب العصرية، والمونتاج الاحترافي لصناعة الفيديوهات التي تخطف الأنظار، بالإضافة إلى إدارة المنصات الرقمية وتقديم حلول برمجية ذكية. هدفنا الدائم هو تحويل الأفكار المعقدة إلى مشاريع رقمية سلسة، جذابة، وعالية الأداء.",
                why_us_title: "لماذا نحن؟",
                why_1_title: "إبداع بلا حدود",
                why_1_desc: "نمزج بين التصميم الفني الجذاب والتطوير البرمجي القوي لنضمن لك حضوراً رقمياً فريداً ومميزاً.",
                why_2_title: "حلول تقنية متكاملة",
                why_2_desc: "نوفر لك كل ما تحتاجه تحت سقف واحد (تصميم ويب، برمجة، ألعاب تفاعلية، ومحتوى رقمي).",
                why_3_title: "دقة واحترافية عالية",
                why_3_desc: "نلتزم بأعلى معايير الجودة والدقة في تسليم المشاريع وتطوير التطبيقات في مواعيدها.",
                why_4_title: "شغف مستمر بالتطوير",
                why_4_desc: "نتابع دائماً أحدث التقنيات والاتجاهات العالمية في التكنولوجيا والتصميم لنبقي مشاريعك في الصدارة.",
                services_title: "خدماتنا الاحترافية",
                srv_1_title: "تطوير الويب",
                srv_1_desc: "نصمم ونطور مواقع ويب احترافية، سريعة وآمنة لتجربة مستخدم استثنائية.",
                srv_2_title: "خدمة المونتاج",
                srv_2_desc: "نحول أفكارك إلى فيديوهات احترافية تعكس هويتك وتصل رسالتك بوضوح وجودة عالية.",
                srv_3_title: "تصميم الإعلانات",
                srv_3_desc: "تصميم إعلانات تجذب الانتباه، تبني هوية بصرية قوية وتحقق نتائج حقيقية.",
                srv_4_title: "التسويق عبر الإنترنت",
                srv_4_desc: "نساعدك على الوصول لجمهورك المستهدف وزيادة الوعي بعلامتك التجارية عبر استراتيجيات تسويقية فعالة.",
                srv_btn: "انضم للعمل معنا",
                portfolio_title: "معرض الأعمال والمشاريع",
                tag_web: "تطوير الويب والمنصات",
                tag_edu: "منصات تعليمية",
                tag_games: "ألعاب وتطبيقات ترفيهية",
                tag_systems: "برمجيات وأنظمة",
                proj_chess_desc: "تطبيق ويب تفاعلي مصمم لإرشاد المبتدئين في تعلم خطوات الشطرنج واستراتيجيات الافتتاحيات.",
                proj_mozakra_desc: "بوابة تعليمية متكاملة للطلاب تضم اختبارات تفاعلية، منصات للمعلمين، وتصميم متجاوب وسريع.",
                proj_car_desc: "لعبة سباق سيارات ممتعة وتفاعلية تم تطويرها بلغات الويب الحديثة لتجربة لعب سلسة.",
                proj_games_desc: "منصة ومجموعة ألعاب مميزة تحت مظلة وكالة MK Creative لتوفير تجارب ترفيهية تفاعلية.",
                proj_mall_desc: "نظام إدارة مبيعات ونقاط بيع متطور يدعم تعدد العملات، إدارة المخزون، وصلاحيات المستخدمين.",
                proj_join_hint: "ساهم في تطوير المشاريع",
                enhancements_title: "التطويرات القادمة في المنصة",
                enhancements_subtitle: "نحن نعمل باستمرار على تطوير موقعنا وخدماتنا لتقديم تجربة أفضل لعملائنا، وإليك أبرز الإضافات القادمة:",
                enh_1_title: "نظام حجز الخدمات الفوري",
                enh_1_desc: "أداة تفاعلية تتيح لك اختيار الخدمة وحساب التكلفة والوقت التقديري بشكل مبدئي.",
                enh_2_title: "قسم آراء العملاء وقصص النجاح",
                enh_2_desc: "عرض مشاريعنا السابقة بالأرقام والنتائج المؤثرة مع تقييمات العملاء.",
                enh_3_title: "خدمات الأمان السيبراني وحماية المواقع",
                enh_3_desc: "إضافة باقات متخصصة لحماية وتأمين منصات ومواقع الشركات ضد الثغرات.",
                enh_4_title: "المدونة التقنية والإبداعية",
                enh_4_desc: "مركز لمعرفة أحدث المقالات والنصائح في البرمجة، المونتاج، وإدارة قنوات اليوتيوب.",
                join_box_title: "انضم إلى فريق عمل MK Creative Agency",
                join_box_desc: "هل تمتلك شغفاً ومهارة في البرمجة، المونتاج، التصميم، أو صناعة المحتوى وترغب في العمل معنا؟ املأ استمارة التوظيف والبيانات الخاصة بك عبر المنصة المخصصة وسنتواصل معك قريباً.",
                join_box_btn: "املأ استمارة التوظيف الآن",
                testimonials_title: "آراء العملاء والشركاء",
                test_1: "\"التعامل مع MK Creative Agency كان نقطة تحول حقيقية في مشروعي. سرعة في الأداء واحترافية عالية جداً في البرمجة والتصميم.\"",
                test_1_name: "أحمد محمود",
                test_1_role: "رائد أعمال ومهتم بالتقنية",
                test_2: "\"خدمة المونتاج وتعديل الفيديوهات فاقت توقعاتي بكثير. الأسلوب الإبداعي والالتزام بالمواعيد يستحق كل التقدير والاحترام.\"",
                test_2_name: "محمد عادل",
                test_2_role: "صانع محتوى رقمي",
                test_3: "\"منصة الويب التي تم برمجتها لنا تعمل بكفاءة تامة وبدون أي أخطاء. شكراً لفريق العمل على الدعم المستمر.\"",
                test_3_name: "محمود إبراهيم",
                test_3_role: "مدير تسويق إلكتروني",
                articles_title: "أحدث المقالات والمنشورات",
                art_1_desc: "استكشف كيف نقوم بتمكين الجيل القادم من المبدعين والمطورين بأحدث الأدوات والمهارات التقنية...",
                art_2_desc: "نظرة عميقة على استراتيجياتنا لتجاوز الحدود التقليدية وتحقيق آفاق جديدة في عالم الإبداع الرقمي...",
                art_3_desc: "تعرف على رؤيتنا وكيف تحولنا إلى وكالة رقمية عالمية تقدم خدمات متكاملة للمستخدمين والشركات...",
                read_more: "Read more",
                faq_title: "الأسئلة الشائعة",
                faq_q1: "كيف يمكنني الانضمام والعمل مع الوكالة؟",
                faq_a1: "يمكنك الانتقال إلى قسم \"انضم إلينا\" وملء استمارة التوظيف الرسمية عبر الرابط المخصص، أو التواصل معنا مباشرة عبر ديسكورد أو واتساب.",
                faq_q2: "ما هي الشروط المطلوبة للانضمام لفريق العمل؟",
                faq_a2: "نبحث دائماً عن الشغف، المهارة الجيدة، والالتزام بتطوير المشاريع الرقمية والتقنية باحترافية تامة.",
                faq_q3: "كيف يتم التواصل بعد تقديم الاستمارة؟",
                faq_a3: "يتم مراجعة البيانات المدخلة في الاستمارة بعناية والتواصل مع المرشحين المقبولين عبر وسائل الاتصال المتاحة.",
                news_title: "انضم إلى MK Creative Agency Newsletters",
                news_desc: "احصل على أحدث التحديثات، التقارير التقنية، والعروض الحصرية مباشرة في بريدك الإلكتروني أسبوعياً.",
                news_placeholder: "أدخل بريدك الإلكتروني هنا...",
                news_btn: "اشتراك الآن",
                footer_desc: "مؤسسة رقمية رائدة متخصصة في الحلول التقنية والإبداعية.",
                footer_discord: "ديسكورد:",
                footer_discord_link: "انضم لمجتمعنا",
                footer_whatsapp: "واتساب:",
                footer_links_title: "روابط سريعة",
                footer_partners_title: "الشركاء والفرص",
                p_discord: "مجتمع ديسكورد",
                p_linkedin: "صفحة لينكد إن",
                p_whatsapp: "التواصل المباشر (واتساب)",
                footer_copy: "&copy; 2026 MK Creative Agency. جميع الحقوق محفوظة."
            },
            en: {
                page_title: "MK Creative Agency | Digital Creative Solutions",
                banner_text: "🚀 Join our team now or connect via Discord & WhatsApp to collaborate on our projects!",
                nav_home: "Home",
                nav_about: "About Us",
                nav_services: "Services",
                nav_portfolio: "Portfolio",
                nav_join: "Join Us",
                nav_testimonials: "Testimonials",
                nav_articles: "Latest Articles",
                nav_faq: "FAQ",
                hero_title: "Building the Digital Future <span>with Innovation & Expertise</span>",
                hero_desc: "We at MK Creative Agency provide integrated solutions in software development, web design, content creation, and digital editing to elevate your project to the top.",
                hero_btn: "Join the Team Now",
                stat_1: "Followers & Tech Enthusiasts Worldwide",
                stat_2: "Views & Digital Content Creativity",
                stat_3: "Client & Partner Satisfaction Rate",
                stat_4: "Commitment & Quality in Delivery",
                about_title: "About Us",
                about_desc_1: "We are <strong>MK CREATIVE Agency</strong>, an integrated digital agency created with an ambitious vision to inspire and transform the web and digital content industry. We don't just offer traditional services, we build complete digital experiences combining technical innovation and creative design.",
                about_desc_2: "Our journey started with a true passion for programming, development, and content creation, evolving into the premier destination for professional online excellence. Our team holds wide expertise in software engineering, modern web UI/UX design, professional video editing, and managing digital platforms. Our constant goal is turning complex ideas into smooth, engaging, and high-performance digital projects.",
                why_us_title: "Why Choose Us?",
                why_1_title: "Boundless Creativity",
                why_1_desc: "We blend appealing artistic design with robust software development to guarantee a unique and prominent digital presence.",
                why_2_title: "Integrated Tech Solutions",
                why_2_desc: "We provide everything you need under one roof (web design, programming, interactive games, and digital content).",
                why_3_title: "High Precision & Professionalism",
                why_3_desc: "We commit to the highest standards of quality and precision in delivering projects and app development on time.",
                why_4_title: "Continuous Passion for Growth",
                why_4_desc: "We constantly follow global tech trends and designs to keep your projects at the forefront.",
                services_title: "Our Professional Services",
                srv_1_title: "Web Development",
                srv_1_desc: "We design and develop professional, fast, and secure websites for an exceptional user experience.",
                srv_2_title: "Video Editing",
                srv_2_desc: "We transform your ideas into professional videos that reflect your identity and deliver your message clearly.",
                srv_3_title: "Ad Design",
                srv_3_desc: "Designing eye-catching ads that build a strong visual identity and deliver real results.",
                srv_4_title: "Digital Marketing",
                srv_4_desc: "We help you reach your target audience and increase brand awareness through effective marketing strategies.",
                srv_btn: "Join Us to Work",
                portfolio_title: "Portfolio & Projects",
                tag_web: "Web & Platform Development",
                tag_edu: "Educational Platforms",
                tag_games: "Games & Entertainment Apps",
                tag_systems: "Software & Systems",
                proj_chess_desc: "An interactive web application designed to guide beginners in learning chess moves and opening strategies.",
                proj_mozakra_desc: "A comprehensive educational portal for students featuring interactive quizzes, teacher hubs, and responsive design.",
                proj_car_desc: "An entertaining and interactive car racing game developed using modern web languages for smooth gameplay.",
                proj_games_desc: "A distinct platform and collection of games under the MK Creative umbrella providing interactive entertainment.",
                proj_mall_desc: "An advanced Point of Sale (POS) system supporting multi-currency, inventory management, and role permissions.",
                proj_join_hint: "Contribute to Projects",
                enhancements_title: "Platform Future Enhancements",
                enhancements_subtitle: "We are continuously working on improving our platform and services to provide a better experience for our clients. Here are our upcoming additions:",
                enh_1_title: "Instant Service Booking System",
                enh_1_desc: "An interactive tool allowing clients to select services and estimate costs/time preliminarily.",
                enh_2_title: "Testimonials & Case Studies Section",
                enh_2_desc: "Showcasing past successful projects with measurable numbers and impactful client reviews.",
                enh_3_title: "Cybersecurity & Web Protection Services",
                enh_3_desc: "Adding specialized packages to secure and protect small business platforms and sites against vulnerabilities.",
                enh_4_title: "Tech & Creative Blog",
                enh_4_desc: "A hub for sharing latest articles and tips in programming, editing, and YouTube channel management.",
                join_box_title: "Join MK Creative Agency Team",
                join_box_desc: "Do you have passion and skills in coding, video editing, design, or content creation and want to work with us? Fill out the job application form and we will contact you soon.",
                join_box_btn: "Fill Application Form Now",
                testimonials_title: "Client & Partner Reviews",
                test_1: "\"Working with MK Creative Agency was a true turning point for my project. Fast performance and very high professionalism in coding and design.\"",
                test_1_name: "Ahmed Mahmoud",
                test_1_role: "Entrepreneur & Tech Enthusiast",
                test_2: "\"Video editing service exceeded my expectations. Creative style and deadline adherence deserve all respect.\"",
                test_2_name: "Mohamed Adel",
                test_2_role: "Digital Content Creator",
                test_3: "\"The web platform programmed for us works with full efficiency and zero errors. Thanks to the team for continuous support.\"",
                test_3_name: "Mahmoud Ibrahim",
                test_3_role: "Digital Marketing Manager",
                articles_title: "Latest Articles & Posts",
                art_1_desc: "Explore how we empower the next generation of creators and developers with the latest tools and technical skills...",
                art_2_desc: "A deep dive into our strategies to cross traditional boundaries and achieve new horizons in digital creativity...",
                art_3_desc: "Discover our vision and how we transformed into a global digital agency delivering integrated services...",
                read_more: "Read more",
                faq_title: "Frequently Asked Questions",
                faq_q1: "How can I join and work with the agency?",
                faq_a1: "You can go to the \"Join Us\" section and fill out the official job application form, or contact us directly via Discord or WhatsApp.",
                faq_q2: "What are the requirements to join the team?",
                faq_a2: "We always look for passion, strong skills, and commitment to developing digital and technical projects professionally.",
                faq_q3: "How is communication handled after submitting the form?",
                faq_a3: "The submitted data is carefully reviewed, and accepted candidates are contacted through available communication channels.",
                news_title: "Join MK Creative Agency Newsletters",
                news_desc: "Get the latest updates, tech reports, and exclusive offers directly in your inbox weekly.",
                news_placeholder: "Enter your email here...",
                news_btn: "Subscribe Now",
                footer_desc: "A leading digital organization specializing in technical and creative solutions.",
                footer_discord: "Discord:",
                footer_discord_link: "Join our community",
                footer_whatsapp: "WhatsApp:",
                footer_links_title: "Quick Links",
                footer_partners_title: "Partners & Opportunities",
                p_discord: "Discord Community",
                p_linkedin: "LinkedIn Page",
                p_whatsapp: "Direct Contact (WhatsApp)",
                footer_copy: "&copy; 2026 MK Creative Agency. All rights reserved."
            }
        };

        const langToggle = document.getElementById('lang-toggle');
        const langText = document.getElementById('lang-text');
        const htmlRoot = document.getElementById('html-root');

        let currentLang = localStorage.getItem('mk_lang') || 'ar';
        setLanguage(currentLang);

        langToggle.addEventListener('click', () => {
            currentLang = currentLang === 'ar' ? 'en' : 'ar';
            setLanguage(currentLang);
        });

        function setLanguage(lang) {
            localStorage.setItem('mk_lang', lang);
            htmlRoot.setAttribute('lang', lang);
            htmlRoot.setAttribute('dir', lang === 'ar' ? 'rtl' : 'ltr');
            langText.textContent = lang === 'ar' ? 'EN' : 'AR';

            document.querySelectorAll('[data-i18n]').forEach(el => {
                const key = el.getAttribute('data-i18n');
                if (translations[lang][key]) {
                    el.innerHTML = translations[lang][key];
                }
            });

            document.querySelectorAll('[data-i18n-placeholder]').forEach(el => {
                const key = el.getAttribute('data-i18n-placeholder');
                if (translations[lang][key]) {
                    el.setAttribute('placeholder', translations[lang][key]);
                }
            });
        }

        const themeToggle = document.getElementById('theme-toggle');
        const themeIcon = document.getElementById('theme-icon');
        const body = document.body;

        const savedTheme = localStorage.getItem('mk_theme') || 'dark';
        body.setAttribute('data-theme', savedTheme);
        updateThemeIcon(savedTheme);

        themeToggle.addEventListener('click', () => {
            let currentTheme = body.getAttribute('data-theme');
            let newTheme = currentTheme === 'dark' ? 'light' : 'dark';
            body.setAttribute('data-theme', newTheme);
            localStorage.setItem('mk_theme', newTheme);
            updateThemeIcon(newTheme);
        });

        function updateThemeIcon(theme) {
            if(theme === 'dark') {
                themeIcon.className = 'fa-solid fa-sun';
            } else {
                themeIcon.className = 'fa-solid fa-moon';
            }
        }

        document.querySelectorAll('.faq-question').forEach(question => {
            question.addEventListener('click', () => {
                const item = question.parentElement;
                item.classList.toggle('active');
            });
        });

        window.addEventListener('scroll', () => {
            let winScroll = document.documentElement.scrollTop;
            let height = document.documentElement.scrollHeight - document.documentElement.clientHeight;
            let scrolled = (winScroll / height) * 100;
            document.getElementById('progress-bar').style.width = scrolled + '%';

            const btt = document.getElementById('back-to-top');
            if (winScroll > 300) {
                btt.style.display = 'flex';
            } else {
                btt.style.display = 'none';
            }
        });
    </script>
</body>
</html>
