<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #0d1117;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            overflow: hidden;
        }
        
        .github-banner {
            width: 1280px;
            height: 320px;
            background: 
                /* Subtle pattern */
                url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23ffffff' fill-opacity='0.07' fill-rule='evenodd'/%3E%3C/svg%3E"),
                /* Modern gradient */
                linear-gradient(135deg, rgba(35, 134, 54, 0.9) 0%, rgba(46, 160, 67, 0.85) 35%, rgba(63, 185, 80, 0.8) 100%);
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            display: flex;
            align-items: center;
            padding: 0 50px;
        }
        
        /* Binary rain animation */
        .binary-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            overflow: hidden;
            z-index: 1;
        }
        
        .binary {
            position: absolute;
            color: rgba(255, 255, 255, 0.15);
            font-family: 'Courier New', monospace;
            font-size: 16px;
            animation: binaryRain 15s linear infinite;
            user-select: none;
        }
        
        @keyframes binaryRain {
            0% {
                transform: translateY(-100%);
            }
            100% {
                transform: translateY(1000%);
            }
        }
        
        .content {
            display: flex;
            width: 100%;
            justify-content: space-between;
            align-items: center;
            z-index: 3;
        }
        
        .text-content {
            max-width: 60%;
            z-index: 3;
        }
        
        .intro-text {
            font-size: 20px;
            color: rgba(255, 255, 255, 0.8);
            margin-bottom: 10px;
            font-weight: 400;
        }
        
        .name {
            font-size: 52px;
            font-weight: 800;
            color: #fff;
            margin-bottom: 15px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .title {
            font-size: 28px;
            color: rgba(255, 255, 255, 0.9);
            font-weight: 500;
            display: flex;
            align-items: center;
            margin-bottom: 25px;
        }
        
        .title::before {
            content: "👨‍💻";
            margin-right: 12px;
            font-size: 24px;
        }
        
        .cta-buttons {
            display: flex;
            gap: 15px;
            margin-top: 25px;
        }
        
        .cta-button {
            padding: 12px 24px;
            border-radius: 30px;
            font-weight: 600;
            font-size: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
            text-decoration: none;
        }
        
        .primary-button {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .primary-button:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .secondary-button {
            background: transparent;
            color: white;
            border: 1px solid rgba(255, 255, 255, 0.3);
        }
        
        .secondary-button:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .code-window {
            width: 400px;
            height: 240px;
            background: #1a1f29;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.4);
            z-index: 3;
            animation: floatWindow 8s ease-in-out infinite;
        }
        
        @keyframes floatWindow {
            0%, 100% {
                transform: translateY(0);
            }
            50% {
                transform: translateY(-10px);
            }
        }
        
        .window-header {
            height: 40px;
            background: #0d1117;
            display: flex;
            align-items: center;
            padding: 0 15px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .window-buttons {
            display: flex;
            gap: 8px;
        }
        
        .window-button {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .close { background: #ff5f56; }
        .minimize { background: #ffbd2e; }
        .maximize { background: #27c93f; }
        
        .window-title {
            color: rgba(255, 255, 255, 0.6);
            font-size: 14px;
            margin-left: 15px;
            font-family: 'Courier New', monospace;
        }
        
        .window-content {
            height: calc(100% - 40px);
            padding: 15px;
            background: #0d1117;
            overflow: hidden;
            position: relative;
        }
        
        .code-editor {
            font-family: 'Courier New', monospace;
            font-size: 12px;
            line-height: 1.5;
            color: #c9d1d9;
        }
        
        .code-line {
            margin-bottom: 5px;
            white-space: nowrap;
            overflow: hidden;
        }
        
        .code-keyword {
            color: #ff7b72;
        }
        
        .code-function {
            color: #d2a8ff;
        }
        
        .code-string {
            color: #a5d6ff;
        }
        
        .code-comment {
            color: #8b949e;
        }
        
        .code-number {
            color: #79c0ff;
        }
        
        .cursor {
            display: inline-block;
            width: 8px;
            height: 16px;
            background: rgba(255, 255, 255, 0.8);
            animation: blink 1s infinite;
            vertical-align: middle;
        }
        
        @keyframes blink {
            0%, 100% { opacity: 1; }
            50% { opacity: 0; }
        }
        
        .floating-element {
            position: absolute;
            z-index: 2;
        }
        
        .circle-1 {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            top: -40px;
            right: 100px;
            animation: pulse 8s ease-in-out infinite;
        }
        
        .circle-2 {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            bottom: -30px;
            left: 150px;
            animation: pulse 6s ease-in-out infinite;
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
                opacity: 0.5;
            }
            50% {
                transform: scale(1.2);
                opacity: 0.7;
            }
        }
        
        @media (max-width: 1350px) {
            .github-banner {
                width: 100%;
                height: 280px;
                padding: 0 30px;
            }
            
            .name {
                font-size: 42px;
            }
            
            .title {
                font-size: 22px;
            }
            
            .code-window {
                width: 350px;
                height: 210px;
            }
        }
    </style>
</head>
<body>
    <div class="github-banner">
        <!-- Binary rain animation -->
        <div class="binary-container" id="binaryContainer"></div>
        
        <div class="floating-element circle-1"></div>
        <div class="floating-element circle-2"></div>
        
        <div class="content">
            <div class="text-content">
                <p class="intro-text">Hello, my name is</p>
                <h1 class="name">Mohamed Ourhouch</h1>
                <p class="title">Software developer</p>
                
                <div class="cta-buttons">
                    <a href="#" class="cta-button primary-button">
                        <i class="fab fa-github"></i> View Projects
                    </a>
                    <a href="https://www.linkedin.com/in/mohamed-ourhouch-616799293/" class="cta-button secondary-button">
                        <i class="fas fa-envelope"></i> Contact Me
                    </a>
                </div>
            </div>
            
            <div class="code-window">
                <div class="window-header">
                    <div class="window-buttons">
                        <div class="window-button close"></div>
                        <div class="window-button minimize"></div>
                        <div class="window-button maximize"></div>
                    </div>
                    <div class="window-title">ourhouch.js</div>
                </div>
                <div class="window-content">
                    <div class="code-editor">
                        <div class="code-line">&nbsp;&nbsp;<span class="code-function">create</span>() {</div>
                        <div class="code-line">&nbsp;&nbsp;&nbsp;&nbsp;<span class="code-keyword">return</span> <span class="code-string">"Amazing digital experiences"</span>;</div>
                        <div class="code-line">&nbsp;&nbsp;}</div>
                        <div class="code-line"></div>
                        <div class="code-line"><span class="code-comment">// Let's build something great together!</span></div>
                        <div class="code-line"><span class="code-keyword">const</span> me = <span class="code-keyword">new</span> <span class="code-function">Developer</span>();</div>
                        <div class="code-line">me.create();<span class="cursor"></span></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        // Create binary rain animation
        function createBinaryRain() {
            const container = document.getElementById('binaryContainer');
            const characters = '01010101010101010101010101010101';
            const fontSize = 16;

            const columnCount = Math.floor(1280 / fontSize);
            
            for (let i = 0; i < columnCount; i++) {
                const binary = document.createElement('div');
                binary.className = 'binary';
                binary.style.left = (i * fontSize) + 'px';
                
                // Randomize animation duration and delay
                const duration = 10 + Math.random() * 20;
                const delay = Math.random() * 5;
                
                binary.style.animationDuration = duration + 's';
                binary.style.animationDelay = delay + 's';
                
                // Generate random binary text
                let binaryText = '';
                const rowCount = Math.floor(320 / fontSize) + 5;
                
                for (let j = 0; j < rowCount; j++) {
                    const randomIndex = Math.floor(Math.random() * characters.length);
                    binaryText += characters[randomIndex] + '<br>';
                }
                
                binary.innerHTML = binaryText;
                container.appendChild(binary);
            }
        }
        
        createBinaryRain();
    </script>
</body>
</html>
<!-- <img align="right" alt="Coding" width="400" src="https://camo.githubusercontent.com/190e7d3bb2ff91e8d67d7ddddf458fede09c5f391dc0e66c290c2bb9e84106fa/68747470733a2f2f6d656469612e67697068792e636f6d2f6d656469612f38333648694a633770677a7938694e58436e2f67697068792e676966"> -->
<h3>student at <a href="https://42.fr/en/homepage/">42</a>. login: mourhouc</h3>

<h3 align="left">Connect with me 💬🖋️</h3>
<p align="left">
    <a href="https://www.linkedin.com/in/mohamed-ourhouch-616799293" target="blank">
        <img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="mohamed ourhouch" height="30" width="40" />
    </a>
</p>
<p align="right" dir="auto"><img align="right" src="https://github-readme-stats.vercel.app/api/top-langs?username=ourhouchmohamed97&show_icons=true&locale=en&layout=compact" alt="card" style="width: 400px; height: 200px;" /></p>

<h3 align="left">Languages and Tools 👨‍💻🌐</h3>
<p align="left">
    <a href="https://www.gnu.org/software/bash/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4b/Bash_Logo_Colored.svg/1024px-Bash_Logo_Colored.svg.png?20180723054350" alt="bash" width="40" height="40" /> </a>
    <a href="https://getbootstrap.com" target="_blank" rel="noreferrer"> <img src="https://getbootstrap.com/docs/5.3/assets/brand/bootstrap-logo-shadow@2x.png" alt="bootstrap" width="40" height="40" /> </a>
    <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40" /> </a>
    <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40" /> </a>
    <a href="https://dart.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" alt="dart" width="40" height="40" /> </a>
    <a href="https://react.dev/" target="_blank" rel="noreferrer"> <img src="https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-1024.png" alt="react" width="40" height="40" /> </a>
    <a href="https://www.figma.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/figma/figma-icon.svg" alt="figma" width="40" height="40" /> </a>
    <a href="https://firebase.google.com/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/c/cf/Firebase_icon.svg" alt="firebase" width="40" height="40" /> </a>
    <a href="https://flutter.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" width="40" height="40" /> </a>
    <a href="https://git-scm.com/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg" alt="git" width="40" height="40" /> </a>
    <a href="https://golang.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" alt="go" width="40" height="40" /> </a>
    <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40" /> </a>
    <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40" /> </a>
    <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer">
        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40" />
    </a>
    <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40" /> </a>
    <a href="https://nextjs.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/devicons/devicon/blob/master/icons/nextjs/nextjs-original.svg" alt="nextjs" width="40" height="40" /> </a>
    <a href="https://tailwindcss.com/" target="_blank" rel="noreferrer"> <img src="https://tailwindcss.com/_next/static/media/tailwindcss-mark.d52e9897.svg" alt="tailwind" width="40" height="40" /> </a>
    <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" alt="typescript" width="40" height="40" /> </a>
</p>
<br />

<p align="center" dir="auto">
    <a target="_blank" rel="noopener noreferrer nofollow" href="https://raw.githubusercontent.com/Elanza-48/Elanza-48/main/resources/img/github-contribution-grid-snake.svg">
        <img src="https://raw.githubusercontent.com/Elanza-48/Elanza-48/main/resources/img/github-contribution-grid-snake.svg" alt="example" style="max-width: 100%;" />
    </a>
</p>

<h3 align="left">GitHub Trophies 🥇🏆</h3>
<p align="left">
  
![](https://github-trophies.vercel.app/?username=ourhouchmohamed97&theme=radical&no-frame=false&no-bg=false&margin-w=4)
</p>
