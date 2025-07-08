<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Your English Mentor (YEM) - Nâng Tầm Tiếng Anh</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Montserrat:wght@600;700&display=swap" rel="stylesheet" />
    <style>
        :root {
            --primary-color: #00897B; /* Teal - Màu xanh ngọc lam chủ đạo */
            --secondary-color: #FF7043; /* Coral - Màu cam đào, năng động */
            --accent-color: #FFC107; /* Amber/Gold - Vàng hổ phách cho điểm nhấn/CTA */
            --text-dark: #37474F; /* Dark Slate Gray - Màu chữ tối, ấm */
            --text-light: #ECF0F1; /* Light Gray - Màu chữ sáng */
            --bg-light: #F8F9FA; /* Off-white background */
            --bg-medium: #E0F2F1; /* Light Teal for alternating sections */
            --bg-dark: #263238; /* Dark Blue Gray for footer */
            --card-bg: #FFFFFF; /* White for content cards */
            --header-gradient: linear-gradient(135deg, #004D40 0%, #00897B 100%); /* Giữ nguyên xanh ban đầu cho header */
            --sale-gradient: linear-gradient(135deg, #FF5722 0%, #FFAB91 100%); /* Orange Red to Light Orange */
        }

        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            background-color: var(--bg-light);
            color: var(--text-dark);
            line-height: 1.6;
            scroll-behavior: smooth;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }
        
        /* --- Navigation Bar --- */
        .navbar {
            background-color: white;
            padding: 15px 20px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar .logo {
            font-family: 'Montserrat', sans-serif;
            font-size: 1.8em;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .navbar ul {
            list-style: none;
            margin: 0;
            padding: 0;
            display: flex;
        }

        .navbar ul li {
                margin-left: 30px;
        }

        .navbar ul li a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 600;
            font-size: 1.1em;
            transition: color 0.3s ease;
        }

        .navbar ul li a:hover {
            color: var(--primary-color);
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            flex-direction: column;
            cursor: pointer;
            z-index: 1001;
        }

        .menu-toggle span {
            height: 3px;
            width: 25px;
            background-color: var(--text-dark);
            margin-bottom: 4px;
            border-radius: 2px;
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: flex;
            }
            .navbar ul {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 60px; /* Adjust based on navbar height */
                left: 0;
                width: 100%;
                background-color: white;
                box-shadow: 0 8px 16px rgba(0,0,0,0.1);
                padding: 20px 0;
                border-top: 1px solid #eee;
            }
            .navbar ul.active {
                display: flex;
            }
            .navbar ul li {
                margin: 10px 20px;
                text-align: center;
            }
            .navbar ul li a {
                padding: 10px 0;
                display: block;
            }
        }


        /* --- Header --- */
        header {
            background: var(--header-gradient); /* Giữ nguyên gradient xanh ban đầu */
            color: white;
            padding: 100px 20px 80px;
            text-align: center;
            position: relative;
            overflow: hidden;
            animation: fadeIn 1s ease-out;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        header h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 4em;
            margin: 0;
            letter-spacing: 2px;
            text-shadow: 2px 2px 5px rgba(0,0,0,0.3);
        }

        header p {
            font-size: 1.6em;
            margin-top: 20px;
            font-weight: 300;
            opacity: 0.9;
        }

        .button {
            display: inline-block;
            background: var(--accent-color);
            color: var(--text-dark);
            padding: 15px 35px;
            border-radius: 50px;
            margin-top: 30px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1em;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            border: none;
        }

        .button:hover {
            background: #FFD254; /* Lighter amber on hover */
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.3);
        }
        section {
            padding: 60px 20px;
            max-width: 900px;
            margin: auto;
            text-align: center;
        }
        section:nth-of-type(even) {
            background: var(--bg-alt);
        }
        section h2 {
            font-family: 'Montserrat', sans-serif;
            font-size: 2.5em; /* TO HƠN */
            color: var(--primary-color);
            margin-bottom: 25px;
        }
        section h3 {
            font-size: 1.5em; /* TO HƠN */
            color: var(--accent-color);
            margin-top: 25px;
        }
        section p, section li {
            font-size: 1.2em; /* TO HƠN */
            max-width: 700px;
            margin: 10px auto;
        }
        section ul {
            list-style: none;
            padding-left: 0;
        }
        section li::before {
            content: "• ";
            color: var(--primary-color);
            font-weight: bold;
        }
        footer {
            background: #263238;
            color: var(--text-light);
            padding: 30px 20px;
            font-size: 1em;
            text-align: center;
        }
        footer a {
            color: var(--accent-color);
            text-decoration: none;
        }
        footer a:hover {
            color: #FFD180;
        }
        @media (max-width: 768px) {
            body {
                font-size: 1.1em;
            }
            header h1 {
                font-size: 2.2em;
            }
            header p {
                font-size: 1.2em;
            }
            section h2 {
                font-size: 2em;
            }
            section h3 {
                font-size: 1.3em;
            }
            section p, section li {
                font-size: 1.1em;
            }
            .menu-toggle {
                display: flex;
            }
            .nav-links {
                display: none;
                flex-direction: column;
                background: var(--bg-light);
                position: absolute;
                top: 70px;
                right: 20px;
                padding: 10px;
                border-radius: 8px;
                box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            }
            .nav-links.active {
                display: flex;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <a href="#home" class="logo">YEM</a>
        <div class="menu-toggle" id="mobile-menu">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <ul class="nav-links">
            <li><a href="a.html">HOME</a></li>
            <li><a href="about.html">GIỚI THIỆU</a></li>
            <li><a href="courses.html">KHÓA HỌC</a></li>
        </ul>
    </nav>

    <header id="home">
        <h1>Your English Mentor</h1>
        <p>Nâng tầm tiếng Anh, kiến tạo tương lai cùng IELTS!</p>
    </header>

    <section>
        <h2>GIỚI THIỆU VỀ YEM</h2>
        <h3>Giải pháp toàn diện cho hành trình học IELTS của bạn</h3>
        <p>Với đội ngũ giáo viên và mentor IELTS từ 7.5 trở lên, giàu kinh nghiệm và nhiệt huyết, YEM cam kết đồng hành cùng bạn xuyên suốt quá trình học, giúp bạn chinh phục IELTS một cách dễ dàng và hiệu quả.</p>
        <p>Chúng tôi áp dụng phương pháp giảng dạy hiện đại như Sơ đồ tư duy, Kỹ thuật Logic, Đọc hiểu nhanh, Liên tưởng hình ảnh và Học siêu tốc để bạn tiếp thu kiến thức tự nhiên, dễ nhớ, dễ ứng dụng vào bài thi thực tế.</p>
        <p>Đặc biệt, bạn sẽ được làm đề test IELTS 4 kỹ năng miễn phí và nhận lộ trình học tập cá nhân hóa, được thiết kế riêng bởi đội ngũ mentor của YEM, đảm bảo phù hợp với mục tiêu và năng lực của bạn.</p>
        <h3>Tầm nhìn của YEM</h3>
        <p>Trở thành nền tảng EdTech đào tạo tiếng Anh hàng đầu cho người Việt, giúp người học nâng cao kỹ năng tiếng Anh học thuật và ứng dụng trong công việc, cuộc sống, chinh phục chứng chỉ quốc tế và vươn xa ra thế giới.</p>
        <h3>Sứ mệnh của YEM</h3>
        <ul>
            <li>Đồng hành cùng người học chinh phục IELTS với lộ trình tối ưu, phương pháp khoa học và chi phí phù hợp.</li>
            <li>Tạo ra cộng đồng học tập tiếng Anh tích cực, hỗ trợ nhau phát triển toàn diện.</li>
            <li>Nâng cao năng lực tiếng Anh cho thế hệ trẻ Việt Nam, mở rộng cơ hội học tập và làm việc toàn cầu.</li>
        </ul>
    </section>

    <footer>
        <p><strong>Your English Mentor (YEM)</strong> - Nâng tầm tiếng Anh của bạn!</p>
        <p>Liên hệ: <a href="mailto:yourenglishmentor.vn@gmail.com">yourenglishmentor.vn@gmail.com</a> | Hotline: <a href="tel:0822901266">0822 901 266 (Ms Mai Anh)</a></p>
        <p>© 2025 Your English Mentor. All rights reserved.</p>
    </footer>

    <script>
        const mobileMenu = document.getElementById('mobile-menu');
        const navLinks = document.querySelector('.nav-links');
        mobileMenu.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
    </script>
</body>
</html>
