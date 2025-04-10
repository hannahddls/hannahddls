<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hannah Grace Dedeles</title>
    <style>
        body {
            font-family: Georgia, 'Times New Roman', Times, serif;
            margin: 0;
            padding: 0;
            background-color: #f5f3e7;
            overflow-x: hidden;
        }

        header {
            background-color: #a8c587;
            padding: 15px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            color: white;
            border-bottom: 3px solid #6d7b57;
            width: 100%;
            top: 0;
            z-index: 1000;
        }

        .logo {
            width: 100%;
            max-width: 50px;
            height: auto;
            border-radius: 50%;
            object-fit: cover;
        }

        h1 {
            font-size: 1.3em;
            color: #333;
            margin: 0;
            display: flex;
            align-items: center;
        }

        nav ul {
            padding: 0;
            margin: 0;
            list-style-type: none;
            display: flex;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav a {
            margin: 0 15px;
            text-decoration: none;
            color: #333;
            font-weight: bold;
            padding: 8px 15px;
            border-radius: 20px;
            transition: background-color 0.3s ease, color 0.3s ease;
        }

        nav a:hover,
        .active {
            background-color: #ebaf20;
            color: black;
        }

        /* Hamburger menu */
        .hamburger {
            display: none;
            flex-direction: column;
            justify-content: space-around;
            width: 30px;
            height: 21px;
            background: transparent;
            border: none;
            cursor: pointer;
        }

        .hamburger div {
            width: 30px;
            height: 3px;
            background-color: white;
            border-radius: 10px;
        }

        /* Hide the menu by default */
        #menu-toggle {
            display: none;
        }

        /* Show menu items when checkbox is checked */
        #menu-toggle:checked+label+nav ul {
            display: block;
            height: 150px;   
            margin: 0 250px;
            width: 255px;
            z-index: 1000;
            text-align: center;
        }

        @media (max-width: 900px) {
            nav ul {
                display: none;
                flex-direction: column;
                width: 100%;
                text-align: center;
                position: absolute;
                background-color: #a8c587;
                top: 60px;
                left: 0;
                padding: 10px 0;
                box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
            }

            nav ul li {
                display: block;
                margin: 15px 0;
            }

            .hamburger {
                display: flex;
            }
        }

        .home {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: center;
            height: auto;
            padding: 20px;
            background-color: #f5f1dc;
            margin: auto;
            animation: fadeIn 1.5s ease-in-out;
            width: 100%;
        }


        .home-text {
            max-width: 40%;
            text-align: left;
            opacity: 0;
            position: relative;
            margin-right: 6%;
            animation: slideIn 1s forwards 0.5s;
        }




        .home-text p {
            background-color: #a8c587;
            font-size: 1.2em;
            color: #333;
            line-height: 1.6;
            text-align: justify;
            padding: 15px;
            border-radius: 10px;
            transform: translate(-5%, -15%);
        }

        .home img {
            width: 550px;
            height: 430px;
            opacity: 0;
            transform: scale(0.9);
            animation: fadeInZoom 1s forwards 1s;
        }

        .welcome-container {
            padding: 20px;
            border-radius: 5px;
        }

        .welcome-text {
            font-size: 5em;
            font-weight: bold;
            color: black;
            letter-spacing: -1px;
            font-family: 'Times New Roman', Times, serif;
            text-shadow: 4px 5px 0 #ebaf2d;
            margin-left: -20px;
            transform: translate(3%, -30%);
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateX(-50px);
            }


            to {
                opacity: 1;
                transform: translateX(0);
            }
        }




        @keyframes fadeInZoom {
            0% {
                opacity: 0;
                transform: scale(0.9);
            }




            100% {
                opacity: 1;
                transform: scale(1);
            }
        }




        @media (max-width: 900px) {
            .home {
                flex-direction: column;
                text-align: center;
            }




            .home-text {
                max-width: 100%;
                margin: 10px 0;
            }




            .home img {
                width: 80%;
                height: auto;
                margin-top: 20px;
            }
        }




        .skills {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: auto;
            text-align: center;
            background-color: #c0d6a6;
            padding: 50px;
            background: linear-gradient(to bottom, #f5f1dc 40%, #a8c587 40%);
            border-top: 3px solid #000000;
            border-bottom: 3px solid #000000;
            width: 100%;
        }

        .skill-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 1300px;
            gap: 25px;
        }

        .skill {
            align-items: center;
            padding: 20px;
            width: 191px;
            text-align: center;
            transform: translate(-30%, 0%);
        }

        .skill p {
            background: white;
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-weight: bold;
            transform: translate(20%, 15%);
        }

        .skill img {
            width: 240px;
            height: 330px;
            border-radius: 20px;
            object-fit: cover;
            transform: translate(0%, 0%);
            transition: transform 0.6s ease-in-out, box-shadow 0.6s ease-in-out;
        }




        .skill img:hover {
            transform: translate(0%, -10%) scale(1.05);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.3);
        }


        .skills-desc {
            max-width: 750px;
            margin: 0 auto;
            background: whitesmoke;
            padding: 25px;
            border-radius: 20px;
            font-size: 18px;
            font-style: italic;
            text-align: justify;
            word-spacing: 3px;
            line-height: 1.4;
            align-items: center;
            transform: translate(-5%, 0%);
        }




        .left {
            width: 50%;
            padding: 20px;
            text-align: center;
            flex: 1;
        }

        .right {
            padding: 20px;
            width: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #f6c667;
            text-align: center;
            line-height: 1.2;
            text-shadow: #916c32;
            display: inline-block;
            font-size: 100px;
            font-weight: bold;
            letter-spacing: -1px;
            font-family: 'Times New Roman', Times, serif;
        }


        .outline-text {
            color: #ffebc3;
            text-shadow: 4px 5px 0 #ebaf2d;
            -webkit-text-stroke: 2px #ffebc3;
            text-shadow: -2px -2px 0 #889d59, 2px -px 0 #889d59, -2px -2px 0 #889d59, 2px 2px 0 #889d59;
        }

        .tact {
            color: transparent;
            -webkit-text-stroke: 2px #ebaf2d;
            text-shadow: -2px -2px 0 #889d59, 2px -px 0 #889d59, -2px -2px 0 #889d59, 2px 2px 0 #889d59;
        }


        /* Contact Section Styling */
        #contact {
            margin-bottom: 0;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            padding: 20px;
            background: linear-gradient(to right, #9cbe74 50%, #78915c 50%);
            width: 100%;
        }


        @media (max-width: 768px) {
            #contact {
                flex-direction: row;
                flex-wrap: wrap;
                padding: 5px 0px;
                text-align: center;
            }

            .left,
            .right {
                width: 45%;
                /* Ensure both "Social" and "Service" sections align horizontally */
                margin: 10px;
            }

            .left {
                text-align: center;
                font-size: 15px;
                /* Smaller font size for mobile */
            }

            .right {
                text-align: center;
                font-size: 40px;
                display: flex;
                flex-direction: inline;
                justify-content: center;
                /* Vertically center content */
                align-items: center;
            }

            .contact-info p {
                font-size: 14px;
                margin: 5px 0;


            }

            .section-title {
                font-size: 14px;
                padding: 6px 12px;
            }

            /* Contact Info section for better alignment on mobile */
            .contact-info {
                text-align: center;
                margin-top: 10px;
                width: 100%;
                display: block;
            }

            /* Reduce the margin between the sections */
            .right,
            .left {
                width: 100%;
                margin-top: 0;
            }
        }

        .cont-container {
            display: flex;
            justify-content: space-between;
            padding: 20px;
            background: linear-gradient(to right, #9cbe74 50%, #78915c 50%);
            margin-bottom: 0;
            /*Added margin to ensure it doesn't go under the footer */
            width: 100%;
        }

        .section-title {
            font-size: 16px;
            font-weight: bold;
            padding: 8px 15px;
            background-color: white;
            border-radius: 20px;
            display: inline-block;
            margin-top: 10px;
        }

        .contact-info {
            width: 120%;
            padding: 10px;
            text-align: justify;
            flex: 1;
        }

        .contact-info p {
            display: flex;
            gap: 5px;
            font-size: 16px;
            justify-content: left;
            transform: translate(50%, 50%);
        }

        /* Footer Social Icons */
        .footer {
            padding: 10px;
            background-color: #d2d5bb;
            border-top: 2px solid black;
            background: linear-gradient(to right, #9cbe74 51.5%, #78915c 51.5%);
            height: 20px;
            margin: 0px 0;
            text-align: center;
        }


        .footer p {
            text-align: left;
            margin: 0;
            font-size: 16px;
            color: white;
            letter-spacing: 5px;
            margin-left: 50px;
        }


        /* Social Icons Container */
        .social-icons {
            justify-content: center;
            align-items: center;
            margin-top: 10px;
            transform: translate(40%, -90%);
            display: flex;
        }


        /* Each social icon */
        .social-icons a {
            margin: 0 15px;
            /* Space between icons */
            text-decoration: none;
            color: white;
            font-size: 20px;
            /* Larger icons */
            transition: color 0.3s ease-in-out;
        }


        .social-icons a:hover {
            color: #31e44f9d;
            /* Hover effect */
        }


        /* Mobile-specific adjustments */
        @media (max-width: 768px) {


            /* Adjust icon size and layout on mobile */
            .social-icons a {
                font-size: 25px;
                /* Smaller icons on mobile */
                margin: 0 10px;
                /* Reduce margin between icons */
            }
        }

    </style>
</head>

<body>
    <header>
        <h1><img class="logo"
                src="https://scontent.fmnl4-6.fna.fbcdn.net/v/t39.30808-6/489018764_1176022010831934_8392468802601900301_n.jpg?_nc_cat=111&ccb=1-7&_nc_sid=127cfc&_nc_eui2=AeG9of_0FWtrftYTi-R1__bqV-3ARSvCPgRX7cBFK8I-BIOzShzHqp6IG2bt2d8wulY2URFgQAnetOLnHWmpoqSg&_nc_ohc=gYYXENLi7Q8Q7kNvwFVQM6i&_nc_oc=Adlff0ZzK6RA0hTekRAjhr4_r7PWHLqPhHNR9hhnNbGe7xeKK8rzG3TZabiceZnGQ6Crb4uHwFzlrDfvqsj0gnC5&_nc_zt=23&_nc_ht=scontent.fmnl4-6.fna&_nc_gid=MCjJsFzZLBQOKNMUAj_0JQ&oh=00_AfELwWMeEX3fI3PouGFyKbUxfDcd_kBs5vRRfd3kZzovcQ&oe=67FAC4E2"
                alt="Logo">HANNAH GRACE DEDELES</h1>

        <!-- Hamburger Menu Toggle -->
        <input type="checkbox" id="menu-toggle" style="display: none;">
        <label for="menu-toggle" class="hamburger">
            <div></div>
            <div></div>
            <div></div>
        </label>

        <nav>
            <ul>
                <li><a href="#home">HOME</a></li>
                <li><a href="#skills">SKILLS</a></li>
                <li><a href="#contact">CONTACT</a></li>
            </ul>
        </nav>
    </header>

    <section id="home" class="home">
        <div class="home-text">
            <h2 class="welcome-text">WELCOME!</h2>
            <p>
                Hi there! I’m a Computer Science student at Our Lady of Fatima University, passionate about technology
                and always eager to learn something new. When I'm not coding or studying, you can usually find me
                painting, playing badminton, or enjoying some time in nature. I believe in chasing my dreams, staying
                open to improvement, and working hard to achieve my goals. Someday, I hope to build a successful career
                and to travel the world.
            </p>
        </div>
        <div class="right-cont">
            <img src="https://scontent.fmnl4-1.fna.fbcdn.net/v/t39.30808-6/489801651_1176033944164074_398634896617400163_n.jpg?stp=dst-jpg_s720x720_tt6&_nc_cat=106&ccb=1-7&_nc_sid=127cfc&_nc_eui2=AeHehGUlS6XK07xubB2jFq6JRzkLBozSKHxHOQsGjNIofKXNT91HSkpusiFR6fuq2m78e47dfBADlJ7PlKv2WSxo&_nc_ohc=n2vHtft4BZ8Q7kNvwEK38zm&_nc_oc=Adm_4o-uVZ2hgtbwwvu68Ecvl5WR1DsH6ZRApFHp0WKCWSS9kwGFdMMSN93Y9jGjSm0tTS_nKw8cH0HXkisTyaMK&_nc_zt=23&_nc_ht=scontent.fmnl4-1.fna&_nc_gid=x4UceOsVndtsrOOUK1WYiw&oh=00_AfHzaWY4YU67Q6PPHreTDfpi7L6VT01dcpKlmhvYCEXWWA&oe=67FAA31E"
                alt="Hannah Grace Dedeles">
        </div>
    </section>

    <section id="skills" class="skills">
        <div class="skill-container">
            <div class="skill">
                <img src="https://i.pinimg.com/236x/61/aa/ab/61aaab4eebd8e0cd5e160c49db03dfdd.jpg"
                    alt="Time Management">
                <p>Time Management</p>
            </div>
            <div class="skill">
                <img src="https://i.pinimg.com/736x/b7/82/62/b782626b0f1eb2cbd813360c88d9e911.jpg" alt="Perceptiveness">
                <p>Perceptiveness</p>
            </div>
            <div class="skill">
                <img src="https://i.pinimg.com/236x/c7/0b/5d/c70b5d7978dd5a0e0f157b941d1352c9.jpg" alt="Organized">
                <p>Organized</p>
            </div>
            <div class="skill">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSS3gKKM7rvtfj02ptwq0FpZFDll22b7vpjnDL3tFKpjVv781qrOAFzFPPEu-PESFG-EFw&usqp=CAU"
                    alt="Flexibility">
                <p>Flexibility</p>
            </div>
            <div class="skill">
                <img src="https://aiiem.org/wp-content/uploads/2025/01/pexels-photo-5486096-5486096-683x1024.jpg"
                    alt="Collaboration">
                <p>Collaboration</p>
            </div>

            <p class="skills-desc">
                I'm great at managing my time and staying organized, with a sharp eye for detail and the ability to
                adapt to any schedule. I enjoy working with others and building strong teamwork to achieve our goals
                together.
            </p>
        </div>
    </section>

    <div id="contact" class="cont-container">
        <div class="left">
            <div class="section-title">SOCIAL</div>
            <p>Facebook</p>
            <p>Instagram</p>
            <p>YouTube</p>

            <div class="contact-info">
                <p>📍Quezon City, Philippines</p>
                <p>📧hannahgrace.dedeles@gmail.com</p>
                <p>📞63 968-539-0359</p>
            </div>
        </div>
        <div class="left">
            <div class="section-title">SERVICE</div>
            <p>Tutorials</p>
            <p>Feedback</p>
            <p>Bug Report</p>
        </div>

        <div class="right">
            <div class="tact">CONTACT</div>
            <div class="outline-text">CONTACT</div>
            <div class="tact">CONTACT</div>
        </div>
    </div>

    <div class="footer">
        <p>ALL RIGHTS RESERVED</p>
        <div class="social-icons">
            <a href="https://www.facebook.com/hannahdedeles" target="_blank" title="Facebook">
                <img src="https://upload.wikimedia.org/wikipedia/commons/5/51/Facebook_f_logo_%282019%29.svg"
                    alt="Facebook" width="30">
            </a>
            <a href="https://www.instagram.com/hannahddls/" target="_blank" title="Instagram">
                <img src="https://upload.wikimedia.org/wikipedia/commons/9/95/Instagram_logo_2022.svg" alt="Instagram"
                    width="30">
            </a>
            <a href="https://www.youtube.com/channel/UCAW8zDIn9waZSRNn5DmxorQ" target="_blank" title="YouTube">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/YouTube_icon_%282013-2017%29.png"
                    alt="YouTube" width="30">
            </a>
        </div>
    </div>

</body>

</html>
