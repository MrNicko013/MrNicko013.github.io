<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THEPRO - Developer Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #111827; /* Dark background for the whole page */
            color: #E5E7EB; /* Light gray text */
        }
        .hero-section {
            background-color: #1F2937; /* Slightly lighter dark for hero */
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
        .nav-link.active {
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
            display: flex;
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
    </style>
</head>
<body class="antialiased">

    <header class="py-6 sticky top-0 z-50 bg-gray-900/80 backdrop-blur-md shadow-lg">
        <div class="container mx-auto px-6 lg:px-8 flex justify-between items-center">
            <a href="#" class="text-3xl font-bold text-white">
                THE<span class="logo-accent">PRO</span>
            </a>
            <nav>
                <ul class="flex space-x-6 md:space-x-8 items-center">
                    <li><a href="#" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300 active">Home</a></li>
                    <li><a href="#" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Resume</a></li>
                    <li><a href="#" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Skills</a></li>
                    <li><a href="#" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Projects</a></li>
                    <li><a href="#" class="nav-link text-gray-300 hover:text-green-400 transition-colors duration-300">Events & Participations </a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <section class="hero-section relative min-h-screen flex items-center overflow-hidden">
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

                    <div class="hero-image-container hidden md:block relative w-full h-full min-h-[300px] md:min-h-[500px]">
                        <img src="Profile.jpg.jpg"
                             alt="Developer Portrait"
                             class="absolute inset-0 w-full h-full object-cover rounded-lg shadow-2xl opacity-70"
                        >
                        <div class="scroll-indicator hidden md:flex">
                            <div class="scroll-indicator-dot"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact" class="contact-bar py-12 md:py-16">
            <div class="container mx-auto px-6 lg:px-8">
                <div class="grid md:grid-cols-3 gap-8 text-center md:text-left">
                    <div class="contact-item p-4 rounded-lg hover:bg-gray-700/50 transition-colors">
                        <h3 class="text-sm font-semibold text-gray-400 uppercase tracking-wider mb-1">Email</h3>
                        <a href="mailto:contact@example.com" class="text-lg text-green-400 hover:text-green-300 transition-colors">nickotelan3@gmail.com</a>
                    </div>
                    <div class="contact-item p-4 rounded-lg hover:bg-gray-700/50 transition-colors">
                        <h3 class="text-sm font-semibold text-gray-400 uppercase tracking-wider mb-1">Phone</h3>
                        <a href="tel:+12235008000" class="text-lg text-green-400 hover:text-green-300 transition-colors">+639123924549</a>
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
        <p class="text-gray-500">&copy; <span id="currentYear"></span> THEPRO. All rights reserved.</p>
    </footer>

    <script>
        // Blinking cursor effect (already handled by CSS animation)
        // JavaScript for current year in footer
        document.getElementById('currentYear').textContent = new Date().getFullYear();
    </script>

</body>
</html>
