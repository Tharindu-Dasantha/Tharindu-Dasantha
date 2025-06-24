<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tharindu Dasantha - Portfolio</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #2a2a4a;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            color: #f0f0f0;
            box-sizing: border-box;
        }
        .container {
            width: 100%;
            max-width: 960px; /* Max width for larger screens */
            background-color: #2a2a4a;
            padding: 20px;
            box-sizing: border-box;
        }
        /* Top Search Bar and Profile - Typing Animation */
        .typing-animation {
            margin-bottom: 25px;
        }
        .typing-animation img {
            width: 100%;
            max-width: 940px;
            height: auto;
        }
        /* Title Section */
        .title-section {
            background-color: #3b3b6b;
            border-radius: 20px;
            padding: 30px 25px;
            margin-bottom: 25px;
            position: relative;
            overflow: hidden;
        }
        .title-section .category {
            color: #a0a0d0;
            font-size: 0.8rem; /* Adjusted for responsiveness */
            margin-bottom: 5px;
        }
        .title-section .name {
            font-size: 2.8rem; /* Adjusted for responsiveness */
            font-weight: bold;
            color: #f0f0f0;
            line-height: 1.1;
            margin-bottom: 10px;
        }
        .title-section .name span {
            color: #8c8cef;
        }
        .title-section .role {
            color: #a0a0d0;
            font-size: 0.75rem; /* Adjusted for responsiveness */
            margin-bottom: 20px;
        }
        .title-section .buttons button {
            background-color: #8c8cef;
            color: white;
            padding: 10px 25px;
            border-radius: 20px;
            border: none;
            outline: none;
            font-size: 0.9rem;
            font-weight: 600;
            margin-right: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .title-section .buttons button:hover {
            background-color: #7a7acf;
        }
        .title-section .buttons button:last-child {
            background-color: #4b4b7c;
            color: #8c8cef;
        }
        .title-section .buttons button:last-child:hover {
            background-color: #5a5a8c;
        }
        .title-section .astronaut-img {
            position: absolute;
            top: 10px;
            right: -20px;
            width: 160px;
            height: auto;
            z-index: 1; /* Ensure it's above other elements if needed */
        }
        .title-section .star {
            position: absolute;
            background-color: white;
            border-radius: 50%;
            z-index: 0;
        }
        .title-section .star-1 {
            top: 10%;
            left: 5%;
            width: 5px;
            height: 5px;
        }
        .title-section .star-2 {
            bottom: 20%;
            right: 40%;
            width: 3px;
            height: 3px;
        }
        /* Who Am I Section */
        .who-am-i-section {
            background-color: #3b3b6b;
            border-radius: 20px;
            padding: 25px 20px;
            margin-bottom: 25px;
            position: relative;
            overflow: hidden; /* For the small astronaut */
        }
        .who-am-i-section h2 {
            font-size: 1.2rem;
            font-weight: bold;
            color: #f0f0f0;
            margin-bottom: 10px;
        }
        .who-am-i-section p {
            font-size: 0.9rem;
            color: #a0a0d0;
            line-height: 1.6;
        }
        .who-am-i-section p b {
            color: #f0f0f0; /* Highlight bold text */
        }
        .who-am-i-section .small-astronaut {
            position: absolute;
            top: -10px;
            right: -10px;
            width: 80px;
            height: auto;
            transform: rotate(-10deg);
            z-index: 1;
        }
        .who-am-i-section .planet-icon {
            position: absolute;
            bottom: 5px;
            left: 15px;
            background-color: #8c8cef;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
        }
        .who-am-i-section .planet-icon i {
            color: white;
            font-size: 1rem;
        }
        /* Brief Explanation Section */
        .explanation-section {
            background-color: #3b3b6b;
            border-radius: 20px;
            padding: 25px 20px;
            margin-bottom: 25px;
            position: relative;
            overflow: hidden;
        }
        .explanation-section h3 {
            font-size: 1.1rem;
            font-weight: bold;
            color: #f0f0f0;
            text-align: center;
            margin-bottom: 20px;
        }
        .explanation-cards {
            display: flex;
            flex-wrap: wrap; /* Allow cards to wrap on smaller screens */
            justify-content: space-between;
            gap: 15px; /* Gap between cards */
        }
        .explanation-card {
            background-color: #4b4b7c;
            border-radius: 15px;
            padding: 15px;
            width: calc(50% - 7.5px); /* Adjusted for gap */
            box-sizing: border-box;
            position: relative;
        }
        .explanation-card p {
            font-size: 0.8rem;
            color: #a0a0d0;
            line-height: 1.5;
            margin-bottom: 15px;
        }
        .explanation-card button {
            background-color: #2a2a4a;
            color: #8c8cef;
            padding: 8px 15px;
            border-radius: 15px;
            border: none;
            outline: none;
            font-size: 0.8rem;
            font-weight: 600;
            margin-top: 10px;
            cursor: pointer;
            display: flex;
            align-items: center;
            transition: background-color 0.3s ease;
        }
        .explanation-card button:hover {
            background-color: #3a3a5a;
        }
        .explanation-card button i {
            margin-right: 5px;
        }
        .explanation-card .planet-deco {
            position: absolute;
            top: -10px;
            left: -10px;
            width: 70px;
            height: auto;
            transform: rotate(10deg);
            z-index: 0;
        }
        .explanation-card .astronaut-rocket-deco {
            position: absolute;
            top: -15px;
            right: -15px;
            width: 80px;
            height: auto;
            z-index: 0;
        }
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 25px;
        }
        .social-icons div {
            background-color: #4b4b7c;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .social-icons div:hover {
            background-color: #5a5a8c;
        }
        .explanation-section .rocket-deco {
            position: absolute;
            bottom: -10px;
            right: -10px;
            width: 60px;
            height: auto;
            transform: rotate(-20deg);
            z-index: 0;
        }
        /* Scroll Indicator */
        .scroll-indicator {
            text-align: center;
            color: #a0a0d0;
            font-size: 0.9rem;
            margin-bottom: 25px;
        }
        .scroll-indicator i {
            margin-top: 5px;
            animation: bounce 1s infinite;
        }
        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(5px);
            }
        }
        /* Image Gallery Section */
        .image-gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); /* Responsive grid */
            gap: 15px;
            margin-bottom: 30px;
        }
        .gallery-item {
            background-color: #3b3b6b;
            border-radius: 15px;
            height: 150px;
            position: relative;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 15px;
        }
        .gallery-item button {
            position: absolute;
            bottom: 10px;
            right: 10px;
            background-color: rgba(140, 140, 239, 0.7);
            color: white;
            border-radius: 50%;
            width: 35px; /* Slightly larger button */
            height: 35px;
            border: none;
            outline: none;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
            backdrop-filter: blur(2px); /* Add a slight blur effect */
        }
        .gallery-item button:hover {
            background-color: rgba(140, 140, 239, 0.9);
        }
        .gallery-item.full-width {
            grid-column: 1 / -1; /* Make the last item span full width */
        }
        /* Footer */
        .footer {
            text-align: center;
            color: #a0a0d0;
            font-size: 0.7rem;
            margin-top: 30px;
        }
        /* Media Queries for Responsiveness */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            .title-section .name {
                font-size: 2.2rem;
            }
            .title-section .astronaut-img {
                width: 120px;
                right: -10px;
                top: 20px;
            }
            .explanation-card {
                width: 100%; /* Stack cards vertically on smaller screens */
            }
            .explanation-cards {
                flex-direction: column;
                gap: 20px;
            }
            .social-icons {
                gap: 10px;
            }
            .image-gallery {
                grid-template-columns: 1fr; /* Single column on very small screens */
            }
            .gallery-item.full-width {
                grid-column: auto;
            }
        }
        @media (max-width: 480px) {
            .title-section .name {
                font-size: 1.8rem;
            }
            .title-section .buttons button {
                padding: 8px 20px;
                font-size: 0.8rem;
                margin-right: 5px;
            }
            .title-section .astronaut-img {
                width: 100px;
                right: -5px;
                top: 25px;
            }
            .who-am-i-section h2 {
                font-size: 1rem;
            }
            .who-am-i-section p {
                font-size: 0.8rem;
            }
            .explanation-section h3 {
                font-size: 1rem;
            }
            .explanation-card p {
                font-size: 0.75rem;
            }
            .explanation-card button {
                font-size: 0.75rem;
                padding: 6px 12px;
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
            <img src="tharindu.png" alt="Astronaut" class="astronaut-img">
            <div class="star star-1"></div>
            <div class="star star-2"></div>
        </div>
        <div class="who-am-i-section">
            <h2>Who am I ?...</h2>
            <p>
                From Sri Lanka, I'm a dynamic professional excelling as both a <b>UI/UX Designer</b> and <b>Full Stack Developer</b>. My expertise spans <i>Web Development</i>, intuitive <i>UI/UX Design</i>, and robust <i>System Programming</i>, all guided by my belief that "Simplicity is the ultimate sophistication." I'm continuously expanding my knowledge in <b>Advanced React Patterns</b>, <b>System Design</b>, and <b>WebGL</b>, proving that even a `console.log` enthusiast can be a highly skilled developer.
            </p>
            <img src="https://placehold.co/80x80/4b4b7c/ffffff?text=Astronaut" alt="Small Astronaut" class="small-astronaut">
            <div class="planet-icon">
                <i class="fas fa-globe"></i>
            </div>
        </div>
        <div class="explanation-section">
            <h3>BRIEF EXPLANATION ABOUT GALAXIES</h3>
            <div class="explanation-cards">
                <div class="explanation-card">
                    <p>
                        Galaxies are typically grouped into galaxy clusters or superclusters, forming the largest known structures in the universe. These galaxies can collide through gravitational forces, which may lead to shifts or mergers of galaxies.
                    </p>
                    <button>
                        <i class="fas fa-arrow-right"></i> Continue...
                    </button>
                    <img src="https://placehold.co/70x70/4b4b7c/ffffff?text=Planet" alt="Planet" class="planet-deco">
                </div>
                <div class="explanation-card">
                    <p>
                        Galaxies are typically grouped into galaxy clusters or superclusters, forming the largest known structures in the universe. These galaxies can collide through gravitational forces, which may lead to shifts or mergers of galaxies.
                    </p>
                    <button>
                        <i class="fas fa-arrow-right"></i> That's enough.
                    </button>
                    <img src="https://placehold.co/80x80/4b4b7c/ffffff?text=Astronaut" alt="Astronaut" class="astronaut-rocket-deco">
                </div>
            </div>
            <div class="social-icons">
                <div><i class="fas fa-bookmark"></i></div>
                <div><i class="fas fa-comments"></i></div>
                <div><i class="fas fa-share-alt"></i></div>
                <div><i class="fas fa-cog"></i></div>
            </div>
            <img src="https://placehold.co/60x60/4b4b7c/ffffff?text=Rocket" alt="Rocket" class="rocket-deco">
        </div>
        <div class="scroll-indicator">
            SCROLL <br>
            <i class="fas fa-arrow-down"></i>
        </div>
        <div class="image-gallery">
            <div class="gallery-item">
                <img src="https://placehold.co/150x150/000000/ffffff?text=Black+Hole" alt="Black Hole">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/150x150/502070/ffffff?text=Nebula" alt="Nebula">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/150x150/808080/ffffff?text=Moon" alt="Moon">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item">
                <img src="https://placehold.co/150x150/606060/ffffff?text=Comet" alt="Comet">
                <button><i class="fas fa-arrow-right"></i></button>
            </div>
            <div class="gallery-item full-width">
                <img src="https://placehold.co/400x150/500090/ffffff?text=Galaxy+View" alt="Galaxy View">
                <button><i class="fas fa-plus"></i></button>
            </div>
        </div>
        <div class="footer">
            CREATED BY MUHAMMAD FAJRI
        </div>
    </div>
</body>
</html>