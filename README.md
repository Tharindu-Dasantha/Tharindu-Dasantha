<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tharindu Dasantha - Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', sans-serif;
            background: linear-gradient(135deg, #1a1a3a 0%, #2a2a4a 50%, #3a3a5a 100%);
            min-height: 100vh;
            color: #f0f0f0;
            overflow-x: hidden;
        }
        /* Animated background stars */
        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(2px 2px at 20px 30px, #fff, transparent),
                radial-gradient(2px 2px at 40px 70px, rgba(255,255,255,0.8), transparent),
                radial-gradient(1px 1px at 90px 40px, #fff, transparent),
                radial-gradient(1px 1px at 130px 80px, rgba(255,255,255,0.6), transparent),
                radial-gradient(2px 2px at 160px 30px, #fff, transparent);
            background-repeat: repeat;
            background-size: 200px 100px;
            animation: sparkle 20s linear infinite;
            pointer-events: none;
            z-index: 1;
        }
        @keyframes sparkle {
            from { transform: translateX(0); }
            to { transform: translateX(200px); }
        }
        .container {
            width: 100%;
            max-width: 960px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
            z-index: 2;
        }
        /* Enhanced typing animation */
        .typing-animation {
            margin-bottom: 30px;
            text-align: center;
            padding: 20px;
            background: rgba(59, 59, 107, 0.3);
            border-radius: 25px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(140, 140, 239, 0.2);
        }
        .typing-animation img {
            width: 100%;
            max-width: 940px;
            height: auto;
            filter: drop-shadow(0 4px 20px rgba(140, 140, 239, 0.3));
        }
        /* Enhanced title section */
        .title-section {
            background: linear-gradient(135deg, rgba(59, 59, 107, 0.9) 0%, rgba(75, 75, 124, 0.8) 100%);
            border-radius: 25px;
            padding: 40px 30px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(20px);
            border: 1px solid rgba(140, 140, 239, 0.3);
            box-shadow: 0 8px 32px rgba(140, 140, 239, 0.1);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        .title-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(140, 140, 239, 0.1), transparent);
            animation: rotate 20s linear infinite;
            z-index: -1;
        }
        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
        .title-section .category {
            color: #a0a0d0;
            font-size: 0.85rem;
            font-weight: 500;
            letter-spacing: 2px;
            margin-bottom: 8px;
            text-transform: uppercase;
        }
        .title-section .name {
            font-size: 3.2rem;
            font-weight: 800;
            color: #f0f0f0;
            line-height: 1.1;
            margin-bottom: 12px;
            text-shadow: 0 4px 20px rgba(140, 140, 239, 0.3);
        }
        .title-section .name span {
            background: linear-gradient(135deg, #8c8cef 0%, #a855f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        .title-section .role {
            color: #a0a0d0;
            font-size: 0.9rem;
            font-weight: 400;
            margin-bottom: 25px;
            opacity: 0.9;
        }
        .title-section .buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        .title-section .buttons button {
            background: linear-gradient(135deg, #8c8cef 0%, #a855f7 100%);
            color: white;
            padding: 12px 28px;
            border-radius: 25px;
            border: none;
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(140, 140, 239, 0.3);
            position: relative;
            overflow: hidden;
        }
        .title-section .buttons button::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.2), transparent);
            transition: left 0.5s;
        }
        .title-section .buttons button:hover::before {
            left: 100%;
        }
        .title-section .buttons button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 25px rgba(140, 140, 239, 0.4);
        }
        .title-section .buttons button:last-child {
            background: rgba(75, 75, 124, 0.8);
            color: #8c8cef;
            border: 2px solid rgba(140, 140, 239, 0.3);
        }
        .title-section .buttons button:last-child:hover {
            background: rgba(140, 140, 239, 0.2);
            border-color: #8c8cef;
        }
        .title-section .astronaut-img {
            position: absolute;
            top: 15px;
            right: -15px;
            width: 160px;
            height: auto;
            z-index: 1;
            filter: drop-shadow(0 4px 20px rgba(140, 140, 239, 0.3));
            animation: float 6s ease-in-out infinite;
        }
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-10px) rotate(2deg); }
        }
        .title-section .star {
            position: absolute;
            background: radial-gradient(circle, #fff 0%, rgba(255,255,255,0.8) 70%, transparent 100%);
            border-radius: 50%;
            z-index: 0;
            animation: twinkle 2s ease-in-out infinite alternate;
        }
        @keyframes twinkle {
            from { opacity: 0.3; transform: scale(1); }
            to { opacity: 1; transform: scale(1.2); }
        }
        .title-section .star-1 {
            top: 15%;
            left: 8%;
            width: 6px;
            height: 6px;
            animation-delay: 0s;
        }
        .title-section .star-2 {
            bottom: 25%;
            right: 45%;
            width: 4px;
            height: 4px;
            animation-delay: 1s;
        }
        /* Enhanced sections */
        .section {
            background: linear-gradient(135deg, rgba(59, 59, 107, 0.8) 0%, rgba(75, 75, 124, 0.6) 100%);
            border-radius: 25px;
            padding: 30px 25px;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(15px);
            border: 1px solid rgba(140, 140, 239, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
        }
        .section h2, .section h3 {
            font-weight: 700;
            color: #f0f0f0;
            margin-bottom: 15px;
            text-shadow: 0 2px 10px rgba(140, 140, 239, 0.2);
        }
        .section h2 {
            font-size: 1.4rem;
        }
        .section h3 {
            font-size: 1.2rem;
            text-align: center;
            margin-bottom: 25px;
        }
        .section p {
            font-size: 0.95rem;
            color: #b0b0e0;
            line-height: 1.7;
            font-weight: 400;
        }
        .section p b {
            color: #f0f0f0;
            font-weight: 600;
        }
        .section p i {
            color: #8c8cef;
            font-style: normal;
            font-weight: 500;
        }
        /* Enhanced explanation cards */
        .explanation-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }
        .explanation-card {
            background: linear-gradient(135deg, rgba(75, 75, 124, 0.8) 0%, rgba(59, 59, 107, 0.9) 100%);
            border-radius: 20px;
            padding: 25px 20px;
            position: relative;
            border: 1px solid rgba(140, 140, 239, 0.2);
            transition: all 0.3s ease;
            overflow: hidden;
        }
        .explanation-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 2px;
            background: linear-gradient(90deg, #8c8cef, #a855f7);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        .explanation-card:hover::before {
            transform: scaleX(1);
        }
        .explanation-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 40px rgba(140, 140, 239, 0.2);
        }
        .explanation-card p {
            font-size: 0.9rem;
            color: #b0b0e0;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        .explanation-card button {
            background: linear-gradient(135deg, rgba(42, 42, 74, 0.9) 0%, rgba(59, 59, 107, 0.8) 100%);
            color: #8c8cef;
            padding: 10px 18px;
            border-radius: 20px;
            border: 1px solid rgba(140, 140, 239, 0.3);
            font-size: 0.85rem;
            font-weight: 600;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
        }
        .explanation-card button:hover {
            background: linear-gradient(135deg, #8c8cef 0%, #a855f7 100%);
            color: white;
            transform: translateX(5px);
        }
        /* Enhanced social icons */
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }
        .social-icons div {
            background: linear-gradient(135deg, rgba(75, 75, 124, 0.8) 0%, rgba(59, 59, 107, 0.9) 100%);
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #8c8cef;
            font-size: 1.2rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid rgba(140, 140, 239, 0.2);
            position: relative;
            overflow: hidden;
        }
        .social-icons div::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #8c8cef 0%, #a855f7 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        .social-icons div:hover::before {
            opacity: 1;
        }
        .social-icons div:hover {
            transform: translateY(-3px) scale(1.1);
            color: white;
            box-shadow: 0 8px 25px rgba(140, 140, 239, 0.3);
        }
        .social-icons div i {
            position: relative;
            z-index: 1;
        }
        /* Enhanced scroll indicator */
        .scroll-indicator {
            text-align: center;
            color: #a0a0d0;
            font-size: 0.9rem;
            margin: 40px 0;
            font-weight: 500;
            letter-spacing: 1px;
        }
        .scroll-indicator i {
            margin-top: 8px;
            animation: bounce 2s infinite;
            color: #8c8cef;
            font-size: 1.1rem;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-8px); }
            60% { transform: translateY(-4px); }
        }
        /* Enhanced image gallery */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }
        .gallery-item {
            background: linear-gradient(135deg, rgba(59, 59, 107, 0.8) 0%, rgba(75, 75, 124, 0.6) 100%);
            border-radius: 20px;
            height: 180px;
            position: relative;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            border: 1px solid rgba(140, 140, 239, 0.2);
            transition: all 0.3s ease;
        }
        .gallery-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(140, 140, 239, 0.2);
        }
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 20px;
            transition: transform 0.3s ease;
        }
        .gallery-item:hover img {
            transform: scale(1.05);
        }
        .gallery-item button {
            position: absolute;
            bottom: 15px;
            right: 15px;
            background: linear-gradient(135deg, rgba(140, 140, 239, 0.9) 0%, rgba(168, 85, 247, 0.9) 100%);
            color: white;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            border: none;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            backdrop-filter: blur(10px);
            box-shadow: 0 4px 15px rgba(140, 140, 239, 0.3);
        }
        .gallery-item button:hover {
            transform: scale(1.1);
            box-shadow: 0 6px 20px rgba(140, 140, 239, 0.4);
        }
        .gallery-item.full-width {
            grid-column: 1 / -1;
            height: 200px;
        }
        /* Enhanced footer */
        .footer {
            text-align: center;
            color: #a0a0d0;
            font-size: 0.8rem;
            margin-top: 40px;
            padding: 20px;
            font-weight: 400;
            letter-spacing: 1px;
            opacity: 0.8;
        }
        /* Decorative elements */
        .small-astronaut, .planet-icon, .planet-deco, .astronaut-rocket-deco, .rocket-deco {
            filter: drop-shadow(0 4px 15px rgba(140, 140, 239, 0.2));
        }
        .planet-icon {
            position: absolute;
            bottom: 15px;
            left: 20px;
            background: linear-gradient(135deg, #8c8cef 0%, #a855f7 100%);
            border-radius: 50%;
            width: 35px;
            height: 35px;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
            box-shadow: 0 4px 15px rgba(140, 140, 239, 0.3);
        }
        .planet-icon i {
            color: white;
            font-size: 1.1rem;
        }
        /* Responsive design */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            .title-section .name {
                font-size: 2.5rem;
            }
            .title-section .astronaut-img {
                width: 120px;
                right: -10px;
                top: 20px;
            }
            .explanation-cards {
                grid-template-columns: 1fr;
                gap: 20px;
            }
            .social-icons {
                gap: 15px;
            }
            .image-gallery {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            }
        }
        @media (max-width: 480px) {
            .title-section .name {
                font-size: 2rem;
            }
            .title-section .buttons {
                flex-direction: column;
                align-items: flex-start;
            }
            .title-section .buttons button {
                padding: 10px 24px;
                font-size: 0.85rem;
            }
            .title-section .astronaut-img {
                width: 100px;
                right: -5px;
                top: 25px;
            }
            .image-gallery {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="typing-animation">
            <div align="center">
                <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=32&duration=2800&pause=2000&color=A855F7&center=true&vCenter=true&width=940&lines=UI%2FUX+Designer+%26+Full+Stack+Developer;Crafting+Digital+Experiences+with+Code;Passionate+about+Clean+Code+%26+Beautiful+Design;Always+Learning%2C+Always+Building" alt="Typing SVG" />
            </div>
        </div>
        <div class="title-section">
            <div class="category">UI/UX DESIGN • WEB DEVELOPMENT</div>
            <div class="name">
                Tharindu <br>
                <span>Dasantha</span>
            </div>
            <div class="role">Full Stack Web Developer</div>
            <div class="buttons">
                <button>Portfolio</button>
                <button>Behance</button>
            </div>
            <!-- <img src="tharindu.png" alt="Astronaut" class="astronaut-img"> -->
            <div class="star star-1"></div>
            <div class="star star-2"></div>
        </div>
        <div class="section">
            <h2>Who am I ?...</h2>
            <p>
                From Sri Lanka, I'm a dynamic professional excelling as both a <b>UI/UX Designer</b> and <b>Full Stack Developer</b>. My expertise spans <i>Web Development</i>, intuitive <i>UI/UX Design</i>, and robust <i>System Programming</i>, all guided by my belief that "Simplicity is the ultimate sophistication." I'm continuously expanding my knowledge in <b>Advanced React Patterns</b>, <b>System Design</b>, and <b>WebGL</b>, proving that even a `console.log` enthusiast can be a highly skilled developer.
            </p>
            <img src="astro.jpg" alt="Small Astronaut" class="small-astronaut" style="position: absolute; top: -10px; right: -10px; width: 80px; height: auto; transform: rotate(-10deg); z-index: 1;">
            <div class="planet-icon">
                <i class="fas fa-globe"></i>
            </div>
        </div>
        <div class="section">
            <h3>BRIEF EXPLANATIONS ABOUT MY WORK</h3>
            <div class="explanation-cards">
                <div class="explanation-card">
                    <p>
                        Great software starts with understanding people’s needs. I focus on making user experiences that are not only easy to use but also enjoyable. From first steps to advanced features, I aim for clear, accessible, and smooth interactions. My goal is to turn complex tasks into simple, elegant designs users love.
                    </p>
                    <button>
                        <i class="fas fa-check"></i> Design Philosophy
                    </button>
                </div>
                <div class="explanation-card">
                    <p>
                        I focus on building strong, scalable web apps that support modern digital needs. I enjoy designing systems that handle high traffic, adapt over time, and run smoothly. From front-end to back-end, I aim for clean code and smart design that keeps things stable, easy to maintain, and ready to grow.
                    </p>
                    <button>
                        <i class="fas fa-check"></i> Development Focus
                    </button>
                </div>
                <div class="explanation-card">
                    <p>
                        I enjoy tackling complex problems and turning them into simple, effective solutions. I start by understanding the root cause, then take a thoughtful, creative approach to solve it. My goal is always to build solutions that work seamlessly in the real world.
                    </p>
                    <button>
                        <i class="fas fa-check"></i> Problem Solver
                    </button>
                </div>
                <div class="explanation-card">
                    <p>
                        The tech world is always changing, and I’m passionate about keeping up. I constantly learn new tools, languages, and methods to stay current and improve my work. This helps me bring fresh, effective solutions to every project.
                    </p>
                    <button>
                        <i class="fas fa-check"></i> Continuous Learner
                    </button>
                </div>
            </div>
            <div class="social-icons">
                <div><i class="fab fa-linkedin"></i></div>
                <div><i class="fab fa-medium"></i></div>
                <div><i class="fas fa-bug"></i></div>
                <div><i class="fab fa-instagram"></i></div>
            </div>
            <img src="tharindu.png" alt="Rocket" class="rocket-deco" style="position: absolute; bottom: -10px; right: -10px; width: 60px; height: auto; transform: rotate(-20deg); z-index: 0;">
        </div>
        <div class="scroll-indicator">
            Coming Soon.... <br>
            <i class="fas fa-arrow-down"></i>
        </div>
        <!-- <div class="image-gallery">
            <div class="gallery-item">
                <img src="https://placehold.co/180x180/000000/ffffff?text=Black+Hole" alt="Black Hole">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/180x180/502070/ffffff?text=Nebula" alt="Nebula">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/180x180/808080/ffffff?text=Moon" alt="Moon">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/180x180/606060/ffffff?text=Comet" alt="Comet">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item full-width">
                <img src="https://placehold.co/400x200/500090/ffffff?text=Galaxy+View" alt="Galaxy View">
                <button><i class="fas fa-plus"></i></button>
            </div>
        </div> -->
        <div class="footer">
            CREATED BY Dasantha Edirisinghe
        </div>
    </div>
</body>
</html>