<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> My Website Portfolio </title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&display=swap" rel="stylesheet">
    <style>
        html {
            scroll-behavior: smooth; /* Enables smooth scrolling for anchor links */
        }
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* Dark background for the whole page */
            color: #E5E7EB; /* Light gray text */
        }
        .hero-section {
            background-color: #1F2937; /* Slightly lighter dark for hero */
        }
        .content-section { /* Basic styling for new sections */
            min-height: 80vh; /* Give them some height to see scrolling */
            padding-top: 4rem; /* Add padding for sticky header */
            padding-bottom: 4rem;
        }
        .contact-bar {
            background-color: #374151; /* Even lighter dark for contact bar */
        }
        .logo-accent {
            color: #10B981; /* Tailwind's green-500 */
        }
        .cta-button {
            background-color: #10B981; /* Tailwind's green-500 */
            transition: background-color 0.3s ease;
        }
        .cta-button:hover {
            background-color: #059669; /* Tailwind's green-600 */
        }
        .nav-link.active { /* Will need JS to dynamically set active based on scroll */
            color: #10B981;
            font-weight: 600;
        }
        .nav-link:hover {
            color: #34D399; /* Lighter green for hover */
        }
        .blinking-cursor::after {
            content: '|';
            animation: blink 1s step-start infinite;
        }
        @keyframes blink {
            50% {
                opacity: 0;
            }
        }
        /* Custom scrollbar for webkit browsers */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #1F2937; /* Dark background for track */
        }
        ::-webkit-scrollbar-thumb {
            background: #10B981; /* Green thumb */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #059669; /* Darker green on hover */
        }
        .hero-image-container {
            position: relative;
        }
        .scroll-indicator {
            position: absolute;
            bottom: 2rem; /* Adjust as needed */
            right: 2rem; /* Adjust as needed */
            width: 24px; /* Size of the outer circle */
            height: 40px; /* Height of the mouse shape */
            border: 2px solid #9CA3AF; /* Gray border */
            border-radius: 12px; /* Rounded shape */
            /* display: flex; -- This will be handled by Tailwind if needed */
            justify-content: center;
            padding-top: 6px; /* Position the inner dot */
        }
        .scroll-indicator-dot {
            width: 6px;
            height: 6px;
            background-color: #9CA3AF; /* Gray dot */
            border-radius: 50%;
            animation: scroll-dot-animation 1.5s infinite ease-in-out;
        }
        @keyframes scroll-dot-animation {
            0% {
                opacity: 1;
                transform: translateY(0);
            }
            50% {
                opacity: 0.5;
                transform: translateY(8px); /* Move dot down */
            }
            100% {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .skill-item {
            background-color: #374151; /* bg-gray-700 */
            color: #D1D5DB; /* text-gray-300 */
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            border: 1px solid #4B5563; /* border-gray-600 */
            transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease; /* Added border-color transition */
        }
        .skill-item:hover {
            border-color: #10B981; /* Highlight with accent color on hover */
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1), 0 0 0 4px rgba(16, 185, 129, 0.2); /* More pronounced shadow with green glow */
        }
        .skill-icon { /* Styling for the <img> icons */
            width: 6rem; 
            height: 6rem; 
            margin-bottom: 0.75rem; 
            object-fit: contain; 
        }
    </style>
</head>
<body class="antialiased">

    <header class="py-6 sticky top-0 z-50 bg-gray-900/80 backdrop-blur-md shadow-lg">
        <div class="container mx-auto px-6 lg:px-8 flex justify-between items-center">
            <a href="#home" class="text-3xl font-bold text-white"> My Portfolio <span class="logo-accent"></span>
            </a>
            <nav>
                <ul class="flex space-x-6 md:space-x-8 items-center">
                    <li><a href="#home" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300 active">Home</a></li>
                    <li><a href="#resume" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Resume</a></li>
                    <li><a href="#skills" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Skills</a></li>
                    <li><a href="#projects" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Projects</a></li>
                    <li><a href="#tools" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Languages & Tools</a></li>
                    <li><a href="#contact" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section id="home" class="hero-section relative min-h-screen flex items-center overflow-hidden">
            <div class="container mx-auto px-6 lg:px-8 py-16 md:py-24">
                <div class="grid md:grid-cols-2 gap-12 items-center">
                    <div class="text-center md:text-left">
                        <p class="text-xl md:text-2xl text-gray-400 mb-3">Hi There!</p>
                        <h1 class="text-5xl sm:text-6xl md:text-7xl font-extrabold text-white mb-4 leading-tight">
                            I'm Monique Telan<span id="cursor" class="blinking-cursor logo-accent"></span>
                        </h1>
                        <p class="text-xl md:text-2xl text-gray-300 mb-8">
                            A future DevOps Engineer.
                        </p>
                        <a href="#contact" class="cta-button text-white font-semibold py-3 px-8 rounded-lg text-lg inline-block shadow-md hover:shadow-lg transform hover:scale-105">
                            Send me a message
                        </a>
                    </div>

                    <div class="hero-image-container block relative w-full h-full min-h-[300px] md:min-h-[500px]">
                        <img src="Profile.jpg.jpg" alt="Developer Portrait"
                             class="absolute inset-0 w-full h-full object-cover rounded-lg shadow-2xl opacity-70"
                             onerror="this.onerror=null;this.src='https://placehold.co/800x1000/2D3748/E2E8F0?text=Image+Error&font=inter';">
                        <div class="scroll-indicator flex"> <div class="scroll-indicator-dot"></div>
                        </div>
                    </div>
                    </div>
            </div>
        </section>

        <section id="resume" class="content-section bg-gray-800">
            <div class="container mx-auto px-6 lg:px-8">
                <h2 class="text-4xl font-bold text-center mb-12 text-white">My Resume</h2>
                <p class="text-lg text-center text-gray-300">Resume content will go here. You can embed a PDF, list experiences, etc.</p>
                </div>
        </section>

        <section id="skills" class="content-section bg-gray-700">
            <div class="container mx-auto px-6 lg:px-8">
                <h2 class="text-4xl font-bold text-center mb-12 text-white">Skills</h2>
                <p class="text-center text-gray-400 mb-10 max-w-2xl mx-auto">Here are the tools and programming languages that I know. </p>
                <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-6 text-center max-w-4xl mx-auto">
                <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="JAVA.png" 
                             alt="Java Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=J&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">Java</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="Python.png"
                             alt="Python Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=P&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">Python</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="HTML.png"
                             alt="HTML Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=H&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">HTML</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="CSS-Logo-2011.png" 
                             alt="CSS Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=C&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">CSS</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="Linux.png"
                             alt="Linux Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=L&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">Linux</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="bash.png" 
                             alt="Bash Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=B&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">Bash</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="git.png"
                             alt="GIT Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=G&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">GIT</h3>
                    </div>
                    <div class="skill-item p-6 rounded-lg shadow-lg transform hover:scale-105">
                        <img src="mysql.png"
                             alt="MySQL Icon"
                             class="skill-icon"
                             onerror="this.onerror=null;this.src='https://placehold.co/64x64/CCCCCC/9CA3AF?text=S&font=inter';">
                        <h3 class="text-xl font-semibold mt-2">MySQL</h3>
                    </div>
                </div>
            </div>
        </section>

        <section id="projects" class="content-section bg-gray-800">
            <div class="container mx-auto px-6 lg:px-8">
                <h2 class="text-4xl font-bold text-center mb-12 text-white">Projects</h2>
                <p class="text-lg text-center text-gray-300">Showcase your projects here. Include descriptions, images, and links.</p>
                </div>
        </section>

        <section id="tools" class="content-section bg-gray-700">
            <div class="container mx-auto px-6 lg:px-8">
                <h2 class="text-4xl font-bold text-center mb-12 text-white">Languages & Tools</h2>
                <p class="text-lg text-center text-gray-300">List any events, hackathons, workshops, or other participations here.</p>
                </div>
        </section>

        <section id="contact" class="contact-bar py-12 md:py-16">
            <div class="container mx-auto px-6 lg:px-8">
                <div class="grid md:grid-cols-3 gap-8 text-center md:text-left">
                    <div class="contact-item p-4 rounded-lg hover:bg-gray-700/50 transition-colors">
                        <h3 class="text-sm font-semibold text-gray-400 uppercase tracking-wider mb-1">Email</h3>
                        <a href="mailto:nickotelan3@gmail.com" class="text-lg text-green-400 hover:text-green-300 transition-colors">nickotelan3@gmail.com</a>
                    </div>
                    <div class="contact-item p-4 rounded-lg hover:bg-gray-700/50 transition-colors">
                        <h3 class="text-sm font-semibold text-gray-400 uppercase tracking-wider mb-1">Phone</h3>
                        <a href="tel:+639123924549" class="text-lg text-green-400 hover:text-green-300 transition-colors">+639123924549</a>
                    </div>
                    <div class="contact-item p-4 rounded-lg hover:bg-gray-700/50 transition-colors">
                        <h3 class="text-sm font-semibold text-gray-400 uppercase tracking-wider mb-1">Location</h3>
                        <p class="text-lg text-gray-200">Pembo, Taguig City </p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <footer class="text-center py-8 bg-gray-900">
        <p class="text-gray-500">&copy; <span id="currentYear"></span> Telan, Monique. All rights reserved.</p> </footer>

    <script>
        // JavaScript for current year in footer
        document.getElementById('currentYear').textContent = new Date().getFullYear();

        // Optional: JavaScript for dynamically updating active nav link on scroll
        const sections = document.querySelectorAll('section[id]');
        const navLinks = document.querySelectorAll('header nav ul li a');

        window.addEventListener('scroll', () => {
            let current = '';
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                // const sectionHeight = section.clientHeight; // Not strictly needed for this logic
                // Adjusting for sticky header height (approx 84px for py-6 + font size, might need tweaking)
                if (pageYOffset >= (sectionTop - 90)) { 
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href').substring(1) === current) {
                    link.classList.add('active');
                }
            });
            // If no section is "current" (e.g., at the very top before #home is fully in view, or at the very bottom)
            // ensure the home link is active if at the top.
            if (!current && pageYOffset < sections[0].offsetTop - 90) { // Check if near the top
                const homeLink = document.querySelector('header nav ul li a[href="#home"]');
                if (homeLink) {
                    // Remove active from all others first
                    navLinks.forEach(l => l.classList.remove('active'));
                    homeLink.classList.add('active');
                }
            }
        });

    </script>

</body>
</html>
