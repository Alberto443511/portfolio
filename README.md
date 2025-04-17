 <!DOCTYPE html>
// ...existing code...
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Himal Subedi -WELCOME TO MY PORTFOLIO </title>
    <meta name="description" content="Personal portfolio of Himal Himal_Subedi_Resume">

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- Typed.js CDN -->
    <script src="https://unpkg.com/typed.js@2.1.0/dist/typed.umd.js"></script>
    <!-- AOS.js CDN (for scroll animations) -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>

    <!-- Google Fonts (Poppins) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

    <!-- Embedded Tailwind Configuration -->
    <script>
        tailwind.config = {
          darkMode: 'class',
          theme: {
            extend: {
              colors: {
                primary: '#2563eb', // Blue-600
                primarydark: '#3b82f6', // Blue-500
                secondary: '#64748b', // Slate-500
                secondarydark: '#94a3b8', // Slate-400
                accent: '#f97316', // Orange-500
                lightbg: '#f8fafc', // Slate-50
                darkbg: '#020617', // Slate-950
                lighttext: '#1e293b', // Slate-800
                darktext: '#e2e8f0', // Slate-200
                cardlight: '#ffffff',
                carddark: '#1e293b', // Slate-800
                cardborderlight: '#e5e7eb', // Gray-200
                cardborderdark: '#334155' // Slate-700
              },
              fontFamily: {
                sans: ['Poppins', 'sans-serif'],
              }
            }
          }
        }
      </script>

    <!-- Embedded Custom CSS -->
    <style type="text/tailwindcss">
        /* Base styles are handled by Tailwind config + body classes */
        body {
          @apply bg-lightbg text-lighttext dark:bg-darkbg dark:text-darktext font-sans transition-colors duration-300 text-base antialiased;
        }

        /* Timeline line style */
        #timeline-container::before {
            content: '';
            position: absolute;
            left: -1px;
            top: 0;
            bottom: 0;
            width: 4px;
            background-color: theme('colors.blue.200');
            border-radius: 2px;
            transform: translateX(1.5rem); /* Match left padding of the items container */
            z-index: -1; /* Ensure line is behind dots */
        }

        html.dark #timeline-container::before {
            background-color: theme('colors.slate.600');
        }

        /* Center timeline line on medium screens and up */
        @media (min-width: 768px) {
            #timeline-container::before {
                left: 50%;
                transform: translateX(-50%);
            }
        }

         /* Ensure smooth scrolling */
         html {
            scroll-behavior: smooth;
         }

         /* Style for Typed.js cursor */
        .typed-cursor {
            opacity: 1;
            animation: typedjsBlink 0.7s infinite;
        }
        @keyframes typedjsBlink {
            50% { opacity: 0.0; }
        }
    </style>

</head>
<body class=""> <!-- Body classes applied via @apply in style -->

    <!-- ===== Header/Navigation ===== -->
    <header class="fixed top-0 left-0 w-full bg-cardlight/80 dark:bg-carddark/80 backdrop-blur-md shadow-sm z-50 transition-colors duration-300 border-b border-cardborderlight/50 dark:border-cardborderdark/50">
        <nav class="container mx-auto px-4 sm:px-6 py-3 flex justify-between items-center">
            <a href="#home" class="text-2xl font-bold text-primary dark:text-primarydark hover:opacity-80 transition-opacity">Himal Subedi</a>
            <!-- Desktop Menu -->
            <div class="hidden md:flex space-x-5 lg:space-x-7 items-center text-sm font-medium text-lighttext dark:text-darktext">
                <a href="#about" class="hover:text-primary dark:hover:text-primarydark transition duration-200">About</a>
                <a href="#skills" class="hover:text-primary dark:hover:text-primarydark transition duration-200">Skills</a>
                <a href="#projects" class="hover:text-primary dark:hover:text-primarydark transition duration-200">Projects</a>
                <a href="#journey" class="hover:text-primary dark:hover:text-primarydark transition duration-200">Journey</a>
                <a href="#contact" class="hover:text-primary dark:hover:text-primarydark transition duration-200">Contact</a>
                <!-- !!! UPDATE RESUME PATH IF NEEDED !!! -->
                <a href="https://drive.google.com/file/d/1fzk_HZAJSoes_2bmZR8YVOzWl4jG-AVe/view?usp=sharing" download="https://drive.google.com/file/d/1fzk_HZAJSoes_2bmZR8YVOzWl4jG-AVe/view?usp=sharing" class="bg-primary text-white px-4 py-2 rounded-md hover:bg-blue-700 dark:bg-primarydark dark:hover:bg-blue-600 transition duration-300 text-xs font-semibold shadow-sm">RESUME</a>
                <button id="darkModeToggle" aria-label="Toggle Dark Mode" class="ml-2 p-2 rounded-full text-secondary dark:text-secondarydark hover:bg-gray-100 dark:hover:bg-slate-700 focus:outline-none focus:ring-2 focus:ring-primary dark:focus:ring-primarydark">
                    <svg id="sunIcon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M12 3v2.25m6.364.386l-1.591 1.591M21 12h-2.25m-.386 6.364l-1.591-1.591M12 18.75V21m-6.364-.386l1.591-1.591M3 12h2.25m.386-6.364l1.591 1.591" /></svg>
                    <svg id="moonIcon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 008.997-5.998z" /></svg>
                </button>
            </div>
            <!-- Mobile Menu Button -->
            <div class="md:hidden">
                <button id="mobileMenuButton" aria-label="Open Menu" class="text-gray-700 dark:text-gray-300 focus:outline-none p-2">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6"><path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" /></svg>
                </button>
            </div>
        </nav>
        <!-- Mobile Menu -->
        <div id="mobileMenu" class="md:hidden hidden bg-cardlight dark:bg-carddark py-2 absolute w-full shadow-lg border-t border-gray-200 dark:border-slate-700">
             <!-- Mobile links -->
            <a href="#about" class="block px-6 py-3 text-base hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200">About</a>
            <a href="#skills" class="block px-6 py-3 text-base hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200">Skills</a>
            <a href="#projects" class="block px-6 py-3 text-base hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200">Projects</a>
            <a href="#journey" class="block px-6 py-3 text-base hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200">Journey</a>
            <a href="#contact" class="block px-6 py-3 text-base hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200">Contact</a>
            <!-- !!! UPDATE RESUME PATH IF NEEDED !!! -->
            <a href="https://drive.google.com/file/d/1fzk_HZAJSoes_2bmZR8YVOzWl4jG-AVe/view?usp=sharing" download="https://drive.google.com/file/d/1fzk_HZAJSoes_2bmZR8YVOzWl4jG-AVe/view?usp=sharing" class="block px-6 py-3 text-base text-primary dark:text-primarydark hover:bg-gray-100 dark:hover:bg-slate-700 transition duration-200 font-medium"> Resume</a>
            <div class="px-6 py-3 border-t border-gray-200 dark:border-slate-700 mt-2">
                 <button id="darkModeToggleMobile" aria-label="Toggle Dark Mode" class="w-full text-left flex items-center space-x-3 text-secondary dark:text-secondarydark hover:text-primary dark:hover:text-primarydark text-base">
                    <svg id="sunIconMobile" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M12 3v2.25m6.364.386l-1.591 1.591M21 12h-2.25m-.386 6.364l-1.591-1.591M12 18.75V21m-6.364-.386l1.591-1.591M3 12h2.25m.386-6.364l1.591 1.591" /></svg>
                    <svg id="moonIconMobile" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5"><path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 008.997-5.998z" /></svg>
                     <span>Toggle Theme</span>
                 </button>
            </div>
        </div>
    </header>

    <!-- ===== Main Content Area ===== -->
    <main class="pt-16 md:pt-20"> <!-- Adjust padding-top based on final header height -->

        <!-- ===== Hero Section ===== -->
        <section id="home" class="min-h-screen flex items-center justify-center text-center bg-gradient-to-br from-blue-50 via-white to-indigo-100 dark:from-slate-950 dark:via-slate-900 dark:to-indigo-950 px-6 py-20 relative overflow-hidden">
             <!-- Optional: Subtle background shapes -->
             <div class="absolute top-0 left-0 w-64 h-64 bg-blue-200 dark:bg-indigo-800 rounded-full opacity-30 dark:opacity-20 -translate-x-1/4 -translate-y-1/4 blur-3xl animate-pulse"></div>
             <div class="absolute bottom-0 right-0 w-72 h-72 bg-indigo-200 dark:bg-blue-800 rounded-full opacity-30 dark:opacity-20 translate-x-1/4 translate-y-1/4 blur-3xl animate-pulse animation-delay-2000"></div>
            <div data-aos="fade-up" class="max-w-4xl z-10">
                <h1 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl font-bold mb-5 text-lighttext dark:text-darktext leading-tight">
                    Himal Subedi
                </h1>
                <p class="text-xl md:text-3xl text-primary dark:text-primarydark mb-10 h-10 md:h-12 font-medium">
                    <span id="typed-output"></span> <!-- Typed.js Target -->
                </p>
                <div class="space-x-4">
                    <a href="#projects" class="inline-block bg-primary text-white px-8 py-3 rounded-full text-lg font-semibold hover:bg-blue-700 dark:bg-primarydark dark:hover:bg-blue-600 transition duration-300 shadow-lg hover:shadow-xl transform hover:-translate-y-0.5">View My Work</a>
                    <a href="#contact" class="inline-block bg-transparent border-2 border-primary text-primary dark:border-primarydark dark:text-primarydark px-8 py-3 rounded-full text-lg font-semibold hover:bg-primary/10 dark:hover:bg-primarydark/10 transition duration-300">Get In Touch</a>
                </div>
            </div>
        </section>

        <!-- ===== About Me Section ===== -->
        <section id="about" class="py-24 px-6 container mx-auto">
            <h2 class="text-4xl font-bold text-center mb-16" data-aos="fade-up">About Me</h2>
            <div class="flex flex-col lg:flex-row items-center gap-12 lg:gap-16">
                <div class="lg:w-2/5 flex-shrink-0" data-aos="fade-right" data-aos-delay="100">
                    <img src="photos/WhatsApp Image 2025-03-10 at 11.24.59_f7fabf23.jpg" alt="Himal Subedi" class="rounded-xl shadow-xl w-full max-w-md mx-auto object-cover aspect-[4/5] border-4 border-white dark:border-slate-700">
                </div>
                <div class="lg:w-3/5 text-lg text-secondary dark:text-secondarydark space-y-5 leading-relaxed" data-aos="fade-left" data-aos-delay="200">
                    <h3 class="text-3xl font-semibold text-lighttext dark:text-darktext mb-4">Passionate Learner, Driven Innovator</h3>
                    <!-- ================================================== -->
                    <!-- ===== !!! EDIT THIS CONTENT BELOW !!!         ===== -->
                    <!-- ================================================== -->
                    <p>
                        Hello! My name is Himal Subedi . A high school graduate from Narayani English Public Secondary School , Bharatpur Chitwan .
                    <p>
                       I am currently living in Chitwan with my family.
                    </p>
                    <p>
                       Navigating a gap year, I'm dedicated to deepening my technical skills and contributing meaningfully while preparing for future studies in a field where I can create impactful solutions.
                    </p>
                    <!-- ================================================== -->
                    <!-- ============= END OF EDITABLE SECTION ============= -->
                    <!-- ================================================== -->
                </div>
            </div>
        </section>

        <!-- ===== Skills Section ===== -->
        <section id="skills" class="py-24 px-6 bg-slate-100 dark:bg-slate-900"> <!-- Slightly different dark bg -->
            <h2 class="text-4xl font-bold text-center mb-16" data-aos="fade-up">Core Competencies</h2>
            <div id="skills-container" class="container mx-auto grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5 gap-6 md:gap-8 text-center">
                <!-- Loading placeholders (will be replaced by JS) -->
                 <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md animate-pulse h-36"> <div class="h-12 w-12 mx-auto mb-3 bg-gray-300 dark:bg-slate-700 rounded-full"></div> <div class="h-4 w-3/4 mx-auto bg-gray-300 dark:bg-slate-700 rounded"></div> </div>
                 <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md animate-pulse h-36"> <div class="h-12 w-12 mx-auto mb-3 bg-gray-300 dark:bg-slate-700 rounded-full"></div> <div class="h-4 w-3/4 mx-auto bg-gray-300 dark:bg-slate-700 rounded"></div> </div>
                 <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md animate-pulse h-36"> <div class="h-12 w-12 mx-auto mb-3 bg-gray-300 dark:bg-slate-700 rounded-full"></div> <div class="h-4 w-3/4 mx-auto bg-gray-300 dark:bg-slate-700 rounded"></div> </div>
                 <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md animate-pulse h-36"> <div class="h-12 w-12 mx-auto mb-3 bg-gray-300 dark:bg-slate-700 rounded-full"></div> <div class="h-4 w-3/4 mx-auto bg-gray-300 dark:bg-slate-700 rounded"></div> </div>
                 <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md animate-pulse h-36"> <div class="h-12 w-12 mx-auto mb-3 bg-gray-300 dark:bg-slate-700 rounded-full"></div> <div class="h-4 w-3/4 mx-auto bg-gray-300 dark:bg-slate-700 rounded"></div> </div>
            </div>
        </section>

        <!-- ===== Experience Section ===== -->
        <section id="experience" class="py-24 px-6 container mx-auto">
             <h2 class="text-4xl font-bold text-center mb-16" data-aos="fade-up">Professional Experience</h2>
             <div class="max-w-4xl mx-auto bg-cardlight dark:bg-carddark p-8 md:p-10 rounded-xl shadow-xl border border-cardborderlight dark:border-cardborderdark" data-aos="fade-up" data-aos-delay="100">
                <h3 class="text-2xl font-semibold text-primary dark:text-primarydark mb-2">Mathematics Tutor (Senior Level)</h3>
                <p class="text-md text-gray-500 dark:text-gray-400 mb-6">Success Tuition & Training Centre / Ideal Education Hub | Chitwan, Nepal | Aug 2024 – Present</p>
                <ul class="list-disc list-outside pl-5 space-y-3 text-secondary dark:text-secondarydark text-lg marker:text-primary dark:marker:text-primarydark">
                    <li>Engineered and implemented effective teaching methodologies <strong class="font-medium text-lighttext dark:text-darktext"></li>
                </ul>
             </div>
        </section>

        <!-- ===== Projects Section ===== -->
        <section id="projects" class="py-24 px-6 bg-slate-100 dark:bg-slate-900">
            <h2 class="text-4xl font-bold text-center mb-16" data-aos="fade-up">Featured Projects</h2>
            <div id="projects-container" class="container mx-auto grid sm:grid-cols-2 xl:grid-cols-4 gap-8">
                <!-- Loading placeholders -->
                 <div class="bg-cardlight dark:bg-carddark rounded-xl shadow-lg overflow-hidden animate-pulse border border-cardborderlight dark:border-cardborderdark"> <div class="h-52 w-full bg-gray-300 dark:bg-slate-700"></div> <div class="p-6 space-y-4"> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-3 w-1/2 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-10 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-6 w-1/4 bg-gray-300 dark:bg-slate-700 rounded-full"></div> </div> </div>
                 <div class="bg-cardlight dark:bg-carddark rounded-xl shadow-lg overflow-hidden animate-pulse border border-cardborderlight dark:border-cardborderdark"> <div class="h-52 w-full bg-gray-300 dark:bg-slate-700"></div> <div class="p-6 space-y-4"> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-3 w-1/2 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-10 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-6 w-1/4 bg-gray-300 dark:bg-slate-700 rounded-full"></div> </div> </div>
                 <div class="bg-cardlight dark:bg-carddark rounded-xl shadow-lg overflow-hidden animate-pulse border border-cardborderlight dark:border-cardborderdark hidden sm:block"> <div class="h-52 w-full bg-gray-300 dark:bg-slate-700"></div> <div class="p-6 space-y-4"> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-3 w-1/2 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-10 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-6 w-1/4 bg-gray-300 dark:bg-slate-700 rounded-full"></div> </div> </div>
                 <div class="bg-cardlight dark:bg-carddark rounded-xl shadow-lg overflow-hidden animate-pulse border border-cardborderlight dark:border-cardborderdark hidden xl:block"> <div class="h-52 w-full bg-gray-300 dark:bg-slate-700"></div> <div class="p-6 space-y-4"> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-3 w-1/2 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-10 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-6 w-1/4 bg-gray-300 dark:bg-slate-700 rounded-full"></div> </div> </div>
            </div>
        </section>

        <!-- ===== Journey/Achievements Section ===== -->
        <section id="journey" class="py-24 px-6 container mx-auto">
            <h2 class="text-4xl font-bold text-center mb-20" data-aos="fade-up">Milestones & Achievements</h2>
            <!-- Timeline Container -->
            <div id="timeline-container" class="relative max-w-4xl mx-auto pl-6 md:pl-0"> <!-- Adjusted padding for mobile -->
                 <!-- Loading placeholders -->
                 <div class="relative mb-12 md:mb-8 animate-pulse"> <div class="absolute w-5 h-5 bg-gray-300 dark:bg-slate-700 rounded-full left-[-10px] top-1 border-4 border-lightbg dark:border-darkbg md:left-1/2 md:-ml-2.5 transform md:-translate-x-1/2"></div> <div class="ml-10 md:w-[calc(50%-2rem)] md:ml-auto md:pl-16"> <div class="p-6 bg-cardlight dark:bg-carddark rounded-xl shadow-lg border border-cardborderlight dark:border-cardborderdark space-y-3"> <div class="h-3 w-1/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-4 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-24 w-1/2 bg-gray-300 dark:bg-slate-700 rounded mt-3"></div> </div> </div> </div>
                 <div class="relative mb-12 md:mb-8 animate-pulse"> <div class="absolute w-5 h-5 bg-gray-300 dark:bg-slate-700 rounded-full left-[-10px] top-1 border-4 border-lightbg dark:border-darkbg md:left-1/2 md:-ml-2.5 transform md:-translate-x-1/2"></div> <div class="ml-10 md:w-[calc(50%-2rem)] md:mr-auto md:pr-16"> <div class="p-6 bg-cardlight dark:bg-carddark rounded-xl shadow-lg border border-cardborderlight dark:border-cardborderdark space-y-3"> <div class="h-3 w-1/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-5 w-3/4 bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-4 w-full bg-gray-300 dark:bg-slate-700 rounded"></div> <div class="h-24 w-1/2 bg-gray-300 dark:bg-slate-700 rounded mt-3 ml-auto"></div> </div> </div> </div>
            </div>
        </section>

         <!-- ===== Gallery Placeholder Section  ===== -->
        <section id="gallery-placeholder" class=></section>

        <!-- ===== Contact Section ===== -->
        <section id="contact" class="py-24 px-6 bg-slate-100 dark:bg-slate-900">
            <h2 class="text-4xl font-bold text-center mb-16" data-aos="fade-up">Let's Connect</h2>
            <!-- ================================================== -->
            <!-- ===== !!! REPLACE WITH YOUR FORMSPREE URL !!! ===== -->
            <!-- ================================================== -->
            <form action="YOUR_FORMSPREE_ENDPOINT" method="POST" class="max-w-xl mx-auto space-y-6 bg-cardlight dark:bg-carddark p-8 md:p-10 rounded-xl shadow-2xl border border-cardborderlight dark:border-cardborderdark" data-aos="fade-up" data-aos-delay="100">
                 <p class="text-center text-secondary dark:text-secondarydark mb-6 text-lg">Have a question, opportunity, or just want to chat? Drop me a line!</p>
                <div>
                    <label for="name" class="block mb-2 font-medium text-sm sr-only">Name</label>
                    <input type="text" id="name" name="name" required placeholder="Your Name" aria-label="Your Name" class="w-full p-4 border rounded-lg bg-gray-50 dark:bg-slate-700 border-cardborderlight dark:border-cardborderdark focus:outline-none focus:ring-2 focus:ring-primary dark:focus:ring-primarydark placeholder-gray-500 dark:placeholder-gray-400 transition duration-200">
                </div>
                <div>
                    <label for="email" class="block mb-2 font-medium text-sm sr-only">Email</label>
                    <input type="email" id="email" name="email" required placeholder="Your Email" aria-label="Your Email" class="w-full p-4 border rounded-lg bg-gray-50 dark:bg-slate-700 border-cardborderlight dark:border-cardborderdark focus:outline-none focus:ring-2 focus:ring-primary dark:focus:ring-primarydark placeholder-gray-500 dark:placeholder-gray-400 transition duration-200">
                </div>
                <div>
                    <label for="message" class="block mb-2 font-medium text-sm sr-only">Message</label>
                    <textarea id="message" name="message" rows="5" required placeholder="Your Message" aria-label="Your Message" class="w-full p-4 border rounded-lg bg-gray-50 dark:bg-slate-700 border-cardborderlight dark:border-cardborderdark focus:outline-none focus:ring-2 focus:ring-primary dark:focus:ring-primarydark placeholder-gray-500 dark:placeholder-gray-400 transition duration-200 resize-none"></textarea>
                </div>
                <div class="text-center pt-4">
                    <button type="submit" class="bg-primary text-white px-10 py-3 rounded-full font-semibold hover:bg-blue-700 dark:bg-primarydark dark:hover:bg-blue-600 transition duration-300 shadow-md hover:shadow-lg text-lg transform hover:-translate-y-0.5 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-primary dark:focus:ring-offset-darkbg">Send Message</button>
                </div>
            </form>
             <div class="text-center mt-16" data-aos="fade-up" data-aos-delay="200">
                 <p class="mb-6 text-xl font-medium">Find me on:</p>
                 <div class="flex justify-center space-x-8">
                     <a href="https://www.linkedin.com/in/himal-subedi-34a1bb342" target="_blank" rel="noopener noreferrer" aria-label="LinkedIn Profile" title="LinkedIn" class="text-gray-500 hover:text-primary dark:text-gray-400 dark:hover:text-primarydark transition duration-300 transform hover:scale-110">
                         <svg xmlns="http://www.w3.org/2000/svg" class="h-9 w-9" fill="currentColor" viewBox="0 0 24 24"><path d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.59-11.018-3.714v-2.155z"/></svg>
                     </a>
                      <!-- Add GitHub Icon/Link if you have one -->
                     <!-- <a href="https://github.com/YOUR_GITHUB_USERNAME" target="_blank" rel="noopener noreferrer" aria-label="GitHub Profile" title="GitHub" class="text-gray-500 hover:text-primary dark:text-gray-400 dark:hover:text-primarydark transition duration-300 transform hover:scale-110">
                          <svg class="h-9 w-9" fill="currentColor" viewBox="0 0 16 16" xmlns="http://www.w3.org/2000/svg"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.012 8.012 0 0 0 16 8c0-4.42-3.58-8-8-8z"></path></svg>
                     </a> -->
                      <!-- Add Facebook Icon/Link if desired -->
                     <!-- <a href="https://www.facebook.com/YOUR_FB_PROFILE" target="_blank" rel="noopener noreferrer" aria-label="Facebook Profile" title="Facebook" class="text-gray-500 hover:text-primary dark:text-gray-400 dark:hover:text-primarydark transition duration-300 transform hover:scale-110">
                         <svg class="h-9 w-9" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"/></svg>
                     </a> -->
                 </div>
             </div>
        </section>

    </main>

    <!-- ===== Footer ===== -->
    <footer class="py-8 bg-slate-100 dark:bg-slate-950 text-center text-sm text-gray-500 dark:text-gray-400 border-t border-cardborderlight dark:border-cardborderdark/50">
        <p>© <span id="currentYear"></span> Himal Subedi. All Rights Reserved.</p>
        <p class="mt-2">Built with <span title="Love!">♥</span> using HTML, Tailwind CSS, and JavaScript.</p>
    </footer>


    <!-- Embedded JavaScript -->
    <script>
        // --- Embedded JSON Data ---
        const skillsData = [
            {"name": "AI Automation"},
            {"name": "Machine Learning"},
            {"name": "Prompt Engineering"},
            {"name": "Python"},
            {"name": "SQL"},
            {"name": "Event Orchestration"},
            {"name": "Leadership"},
            {"name": "Project Management"},
            {"name": "Teaching & Mentoring"},
            {"name": "Content Creation (UGC)"},
            {"name": "Communication"},
            {"name": "Problem Solving"},
            {"name": "Canva"},
            {"name": "Photoshop (Basic)"}
        ];

        const projectsData = [

            {
                "title": "MCQ Exam Booster Class XII",
                "date": "Publication Ongoing",
                "image": "PHOTOS/Screenshot_20250217-164716.jpg", // !! Check filename !!
                "description": "Authored a comprehensive MCQ book tailored for high school entrance exams after identifying gaps in existing study materials. Designed questions and detailed answers to effectively address student needs for exam preparation.",
                "tags": ["Author", "Content Creation", "Education", "Publication"],
                "links": {}
            },
            {
                "title": "Community Health Awareness Campaign",
                "date": "Approx. 3 Months (Specify Year)", // !! Add Year !!
                "image": "PHOTOS/Screenshot 2025-04-17 111518.png", // !! Check filename !!
                "description": "Organized and led a vital campaign reaching 100+ families in a low-income area. Researched health practices, partnered with local nurses/doctors, rallied volunteers, secured donations, and conducted impactful workshops. Achieved 80% adoption of healthier practices.",
                "tags": ["Leadership", "Community", "Health", "Event Management", "Social Impact", "Teamwork"],
                "links": {}
            },
            {
                "title": "District Technology Exposition Lead",
                "date": "Specify High School Year", // !! Add Year !!
                "image": "PHOTOS/FB_IMG_1742023391479.jpg", // !! Check filename !!
                "description": "Conceptualized and executed a district-wide tech expo showcasing innovations from 30 schools. Secured NPR 35,000 in sponsorships via persuasive negotiation, coordinated diverse cross-functional teams, and implemented structured workflows, resulting in record attendance and positive feedback.",
                "tags": ["Leadership", "Event Orchestration", "Technology", "Sponsorship", "Communication", "Negotiation"],
                "links": {}
            }
        ];

        const achievementsData = [
            
            
            {
                "date": "2022 (Grade 9)",
                "title": "National Scrabble Championship - 3rd Place & International Qualification",
                "description": "Achieved 3rd place at both District and National levels (Tanahun), demonstrating consistent top performance. Qualified for the international championship in Bangladesh, which was unfortunately cancelled due to COVID.",
                "image": "PHOTOS/Screenshot 2025-04-17 093410.png" // !! Check filename !!
            },
            {
                "date": "Specify Year (+2 Level)", // !! Add Year !!
                "title": "HISSAN +2 Science Quiz - 1st Rank Holder",
                "description": "Achieved the top rank holder position in the competitive HISSAN +2 Science Quiz.",
                "image": "PHOTOS/FB_IMG_1742023402463.jpg" // !! Check filename !!
            },
            {
                "date": "2022-23",
                "title": "Mahatma Gandhi Scholarship Recipient (MGSS)",
                "description": "Honored with the prestigious scholarship by the Embassy of India, recognizing academic excellence and potential.",
                "image": "PHOTOS/FB_IMG_1679915101650.jpg" // !! Check filename !!
            },
            {
                "date": "2081 BS (2024 AD)",
                "title": "High School Graduation (NEB Result)",
                "description": "Successfully graduated from Narayani English Public Secondary School with an excellent GPA of 3.77.",
                "image": "PHOTOS/IMG_20240905_202709_113.jpg" // !! Check filename !!
            },
            {
                "date": "MECEE-BL 2024",
                "title": "MBBS Entrance Exam Achievement",
                "description": "Demonstrated strong academic capability by securing Rank 606 in the highly competitive Medical Education Common Entrance Examination (MECEE-BL).",
                "image": "PHOTOS/IMG_20240905_202723_954.jpg" // !! Check filename !!
            }
             // !! Add other achievements here !!
        ];

        // --- JavaScript Logic ---
        document.addEventListener('DOMContentLoaded', () => {

            // --- Dark Mode ---
            const darkModeToggle = document.getElementById('darkModeToggle');
            const darkModeToggleMobile = document.getElementById('darkModeToggleMobile');
            const htmlElement = document.documentElement;
            const sunIcons = Array.from(document.querySelectorAll('#sunIcon, #sunIconMobile'));
            const moonIcons = Array.from(document.querySelectorAll('#moonIcon, #moonIconMobile'));

            const applyTheme = (theme) => {
                if (theme === 'dark') {
                    htmlElement.classList.add('dark');
                    sunIcons.forEach(icon => icon?.classList.remove('hidden'));
                    moonIcons.forEach(icon => icon?.classList.add('hidden'));
                    localStorage.setItem('theme', 'dark');
                } else {
                    htmlElement.classList.remove('dark');
                    sunIcons.forEach(icon => icon?.classList.add('hidden'));
                    moonIcons.forEach(icon => icon?.classList.remove('hidden'));
                    localStorage.setItem('theme', 'light');
                }
            };
            const toggleDarkMode = () => applyTheme(htmlElement.classList.contains('dark') ? 'light' : 'dark');
            const preferredTheme = localStorage.getItem('theme') || (window.matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
            applyTheme(preferredTheme);
            darkModeToggle?.addEventListener('click', toggleDarkMode);
            darkModeToggleMobile?.addEventListener('click', toggleDarkMode);

            // --- Mobile Menu ---
            const mobileMenuButton = document.getElementById('mobileMenuButton');
            const mobileMenu = document.getElementById('mobileMenu');
            mobileMenuButton?.addEventListener('click', () => mobileMenu?.classList.toggle('hidden'));
            mobileMenu?.querySelectorAll('a').forEach(link => link.addEventListener('click', () => mobileMenu?.classList.add('hidden')));

            // --- Typed.js ---
            const typedOutput = document.getElementById('typed-output');
             if(typedOutput && typeof Typed !== 'undefined') {
                try {
                    new Typed('#typed-output', {
                        strings: ['Tech Enthusiast', 'Education Innovator', 'Community Leader', 'Lifelong Learner'],
                        typeSpeed: 65, backSpeed: 45, loop: true, backDelay: 1900, smartBackspace: true,
                    });
                } catch (e) { console.error("Typed.js error:", e); }
            } else { console.warn("Typed.js target or library not found."); }

            // --- AOS ---
            if(typeof AOS !== 'undefined'){
                AOS.init({ duration: 800, offset: 120, once: true, easing: 'ease-out-cubic' });
            } else { console.warn("AOS library not found."); }

            // --- Icon Mapping (Heroicons - Outline Style) ---
            const iconMap = {
                "AI Automation": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M15.59 14.37a6 6 0 01-5.84 7.38v-4.8m5.84-2.58a14.98 14.98 0 006.16-12.12A14.98 14.98 0 009.63 2.41a14.98 14.98 0 00-5.84 7.38m5.84 5.18v4.8m0-16.46a14.98 14.98 0 016.16 12.12 14.98 14.98 0 01-12.12 6.16M6.38 8.622a14.98 14.98 0 015.84-7.38m5.84 7.38a14.98 14.98 0 01-5.84 7.38M14.37 15.59a6 6 0 01-7.38 5.84m-1.18-1.18a14.98 14.98 0 017.38-5.84" /></svg>`,
                "Machine Learning": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M8.25 3v1.5M4.5 8.25H3m18 0h-1.5M4.5 12H3m18 0h-1.5m-15 3.75H3m18 0h-1.5M8.25 19.5V21M12 3v1.5m0 15V21m3.75-18v1.5m0 15V21m-9-1.5h10.5a2.25 2.25 0 002.25-2.25V6.75a2.25 2.25 0 00-2.25-2.25H6.75A2.25 2.25 0 004.5 6.75v10.5a2.25 2.25 0 002.25 2.25zm.75-12h9v9h-9v-9z" /></svg>`,
                "Prompt Engineering": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M10.5 6h9.75M10.5 6a1.5 1.5 0 11-3 0m3 0a1.5 1.5 0 10-3 0M3.75 6H7.5m3 12h9.75m-9.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-3.75 0H7.5m9-6h3.75m-3.75 0a1.5 1.5 0 01-3 0m3 0a1.5 1.5 0 00-3 0m-9.75 0h9.75" /></svg>`,
                "Python": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M17.25 6.75L22.5 12l-5.25 5.25m-10.5 0L1.5 12l5.25-5.25m7.5-3l-4.5 16.5" /></svg>`,
                "SQL": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M20.25 6.375c0 2.278-3.694 4.125-8.25 4.125S3.75 8.653 3.75 6.375m16.5 0c0-2.278-3.694-4.125-8.25-4.125S3.75 4.097 3.75 6.375m16.5 0v11.25c0 2.278-3.694 4.125-8.25 4.125s-8.25-1.847-8.25-4.125V6.375" /></svg>`,
                "Event Orchestration": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 012.25-2.25h13.5A2.25 2.25 0 0121 7.5v11.25m-18 0A2.25 2.25 0 005.25 21h13.5A2.25 2.25 0 0021 18.75m-18 0v-7.5A2.25 2.25 0 015.25 9h13.5A2.25 2.25 0 0121 11.25v7.5m-9-6h.008v.008H12v-.008zM12 15h.008v.008H12V15zm0 2.25h.008v.008H12v-.008zM9.75 15h.008v.008H9.75V15zm0 2.25h.008v.008H9.75v-.008zM7.5 15h.008v.008H7.5V15zm0 2.25h.008v.008H7.5v-.008zm6.75-4.5h.008v.008h-.008v-.008zm0 2.25h.008v.008h-.008V15zm0 2.25h.008v.008h-.008v-.008zm2.25-4.5h.008v.008H16.5v-.008zm0 2.25h.008v.008H16.5V15z" /></svg>`,
                "Leadership": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M15 19.128a9.38 9.38 0 002.625.372 9.337 9.337 0 004.121-.952 4.125 4.125 0 00-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 018.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0111.964-3.07M12 6.375a3.375 3.375 0 11-6.75 0 3.375 3.375 0 016.75 0zm8.25 2.25a2.625 2.625 0 11-5.25 0 2.625 2.625 0 015.25 0z" /></svg>`,
                "Project Management": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M3.75 9.776c.112-.017.227-.026.344-.026h15.812c.117 0 .232.009.344.026m-16.5 0a2.25 2.25 0 00-1.883 2.542l.857 6a2.25 2.25 0 002.227 1.932H19.05a2.25 2.25 0 002.227-1.932l.857-6a2.25 2.25 0 00-1.883-2.542m-16.5 0V6.75A2.25 2.25 0 015.25 4.5h13.5A2.25 2.25 0 0121 6.75v3.026m-16.5 0h16.5" /></svg>`,
                "Teaching & Mentoring": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5" /></svg>`,
                "Content Creation (UGC)": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M16.862 4.487l1.687-1.688a1.875 1.875 0 112.652 2.652L10.582 16.07a4.5 4.5 0 01-1.897 1.13L6 18l.8-2.685a4.5 4.5 0 011.13-1.897l8.932-8.931zm0 0L19.5 7.125M18 14v4.75A2.25 2.25 0 0115.75 21H5.25A2.25 2.25 0 013 18.75V8.25A2.25 2.25 0 015.25 6H10" /></svg>`,
                "Communication": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M8.625 12a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0H8.25m4.125 0a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0H12m4.125 0a.375.375 0 11-.75 0 .375.375 0 01.75 0zm0 0h-.375M21 12c0 4.556-3.04 8.25-6.75 8.25a8.25 8.25 0 110-16.5C17.96 3.75 21 7.444 21 12z" /></svg>`,
                "Problem Solving": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M9.813 15.904L9 18.75l-.813-2.846a4.5 4.5 0 00-3.09-3.09L1.875 12l2.846-.813a4.5 4.5 0 003.09-3.09L9 5.25l.813 2.846a4.5 4.5 0 003.09 3.09L15.125 12l-2.846.813a4.5 4.5 0 00-3.09 3.09zM18.259 8.715L18 9.75l-.259-1.035a3.375 3.375 0 00-2.455-2.456L14.25 6l1.036-.259a3.375 3.375 0 002.455-2.456L18 2.25l.259 1.035a3.375 3.375 0 002.456 2.456L21.75 6l-1.035.259a3.375 3.375 0 00-2.456 2.456zM16.894 20.567L16.5 21.75l-.394-1.183a2.25 2.25 0 00-1.423-1.423L13.5 18.75l1.183-.394a2.25 2.25 0 001.423-1.423l.394-1.183.394 1.183a2.25 2.25 0 001.423 1.423l1.183.394-1.183.394a2.25 2.25 0 00-1.423 1.423z" /></svg>`,
                "Resilience & Adaptability": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M19.5 12c0-1.232-.046-2.453-.138-3.662a4.006 4.006 0 00-3.7-3.7 48.678 48.678 0 00-7.324 0 4.006 4.006 0 00-3.7 3.7c-.092 1.21-.138 2.43-.138 3.662v4.159c0 1.232.046 2.453.138 3.662a4.006 4.006 0 003.7 3.7 48.656 48.656 0 007.324 0 4.006 4.006 0 003.7-3.7c.092-1.21.138-2.43.138-3.662v-4.159zM12 8.25a3.75 3.75 0 100 7.5 3.75 3.75 0 000-7.5z" /></svg>`,
                "Canva": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M9.53 16.122a3 3 0 00-5.78 1.128 2.25 2.25 0 01-2.4 2.245 4.5 4.5 0 008.4-2.245c0-.399-.078-.78-.22-1.128zm0 0a15.998 15.998 0 003.388-1.62m-5.043-.025a15.994 15.994 0 011.622-3.385m5.043.025a15.994 15.994 0 001.622-3.385m3.385 1.621a15.994 15.994 0 00-1.622 3.385m-5.043-.025a15.998 15.998 0 01-3.388-1.621m7.744 4.24a4.5 4.5 0 00-8.4-2.244 4.5 4.5 0 008.4 2.245zM12 12a3 3 0 11-6 0 3 3 0 016 0z" /></svg>`,
                "Photoshop (Basic)": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M6.827 6.175A2.31 2.31 0 015.186 7.23c-.38.054-.757.112-1.134.175C2.999 7.58 2.25 8.507 2.25 9.574V18a2.25 2.25 0 002.25 2.25h15A2.25 2.25 0 0021.75 18V9.574c0-1.067-.75-1.994-1.802-2.169a47.865 47.865 0 00-1.134-.175 2.31 2.31 0 01-1.64-1.055l-.822-1.316a2.192 2.192 0 00-1.736-1.039 48.774 48.774 0 00-5.232 0 2.192 2.192 0 00-1.736 1.039l-.821 1.316z" /><path stroke-linecap="round" stroke-linejoin="round" d="M16.5 12.75a4.5 4.5 0 11-9 0 4.5 4.5 0 019 0zM18.75 10.5h.008v.008h-.008V10.5z" /></svg>`,
                "Default": `<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-12 h-12 mx-auto mb-3 text-primary dark:text-primarydark"><path stroke-linecap="round" stroke-linejoin="round" d="M9.75 3.104v5.714a2.25 2.25 0 01-.659 1.591L5 14.5M9.75 3.104c-.251.038-.502.068-.75.097h-.002C7.544 3.3 6.75 4.043 6.75 4.93l-.003.026c0 .981.796 1.781 1.78 1.781H16.5a2.25 2.25 0 002.25-2.25V6.75a2.25 2.25 0 00-2.25-2.25H16.5m-6.75 0H9.75" /></svg>`
            };

            // --- Render Skills ---
            const skillsContainer = document.getElementById('skills-container');
            if (skillsContainer && skillsData) {
                skillsContainer.innerHTML = ''; // Clear placeholders
                skillsData.forEach(skill => {
                    const iconHtml = iconMap[skill.name] || iconMap["Default"];
                    const skillElement = `
                        <div class="p-6 bg-cardlight dark:bg-carddark rounded-lg shadow-md hover:shadow-xl transform hover:-translate-y-1.5 transition-all duration-300 border border-cardborderlight dark:border-cardborderdark" data-aos="zoom-in">
                            ${iconHtml}
                            <p class="font-semibold text-lg mt-1">${skill.name}</p>
                        </div>
                    `;
                    skillsContainer.insertAdjacentHTML('beforeend', skillElement);
                });
            } else { console.error("Skills container or data not found"); }

            // --- Render Projects ---
            const projectsContainer = document.getElementById('projects-container');
            if (projectsContainer && projectsData) {
                 projectsContainer.innerHTML = ''; // Clear placeholders
                projectsData.forEach(project => {
                    const linksHtml = Object.entries(project.links || {})
                                          .map(([key, url]) => url ? `<a href="${url}" target="_blank" rel="noopener noreferrer" class="text-primary dark:text-primarydark hover:underline capitalize font-medium">${key}</a>` : '')
                                          .filter(Boolean).join('<span class="mx-2 text-gray-300 dark:text-gray-600">|</span>');
                    const projectElement = `
                        <div class="bg-cardlight dark:bg-carddark rounded-xl shadow-lg overflow-hidden flex flex-col border border-cardborderlight dark:border-cardborderdark transform hover:scale-[1.03] transition-transform duration-300 group" data-aos="fade-up">
                            <div class="overflow-hidden"><img src="${project.image}" alt="${project.title}" class="w-full h-52 object-cover group-hover:scale-105 transition-transform duration-300 ease-in-out" loading="lazy"></div>
                            <div class="p-6 flex flex-col flex-grow">
                                <h3 class="text-xl font-bold mb-2 text-lighttext dark:text-darktext">${project.title}</h3>
                                <p class="text-sm text-gray-500 dark:text-gray-400 mb-4">${project.date}</p>
                                <p class="text-secondary dark:text-secondarydark mb-5 flex-grow text-base leading-relaxed">${project.description}</p>
                                <div class="mt-auto pt-4 border-t border-cardborderlight dark:border-cardborderdark space-y-4">
                                    <div class="flex flex-wrap gap-2">
                                        ${project.tags.map(tag => `<span class="bg-slate-200 dark:bg-slate-700 text-xs font-medium px-2.5 py-1 rounded-full text-secondary dark:text-secondarydark">${tag}</span>`).join('')}
                                    </div>
                                    ${linksHtml ? `<div class="flex space-x-4 text-sm">${linksHtml}</div>` : ''}
                                </div>
                            </div>
                        </div>
                    `;
                    projectsContainer.insertAdjacentHTML('beforeend', projectElement);
                });
            } else { console.error("Projects container or data not found"); }

            // --- Render Timeline ---
            const timelineContainer = document.getElementById('timeline-container');
             if (timelineContainer && achievementsData) {
                 timelineContainer.innerHTML = ''; // Clear placeholders
                achievementsData.forEach((achievement, index) => {
                    const alignmentClass = index % 2 === 0 ? 'md:ml-auto md:pl-16' : 'md:mr-auto md:pr-16 md:text-right';
                    const dotPositionClass = 'md:left-1/2 md:-translate-x-1/2'; // Center dot on larger screens
                    const aosAnimation = index % 2 === 0 ? 'fade-left' : 'fade-right';
                    const imgAlignment = index % 2 !== 0 ? 'md:ml-auto' : ''; // Align image right on odd items

                    const timelineElement = `
                        <div class="relative mb-10 md:mb-8" data-aos="${aosAnimation}" data-aos-delay="${index * 50}">
                            <div class="absolute w-5 h-5 bg-primary rounded-full left-[-10px] top-1 border-4 border-lightbg dark:border-darkbg dark:bg-primarydark ${dotPositionClass}"></div>
                            <div class="ml-10 md:w-[calc(50%-2rem)] ${alignmentClass}">
                               <div class="p-6 bg-cardlight dark:bg-carddark rounded-xl shadow-lg border border-cardborderlight dark:border-cardborderdark relative group">
                                    <span class="absolute -top-3 ${index % 2 === 0 ? 'left-4' : 'right-4 md:left-auto'} bg-primary dark:bg-primarydark text-white text-xs font-bold px-3 py-1 rounded-full shadow-md">${achievement.date.match(/\d{4}|\d{2,4} BS|\w+$/)?.[0] || achievement.date}</span>
                                    <p class="text-sm font-semibold text-primary dark:text-primarydark mb-2 pt-3">${achievement.date}</p>
                                    <h3 class="text-xl font-bold mb-3 text-lighttext dark:text-darktext">${achievement.title}</h3>
                                    ${achievement.image ? `<img src="${achievement.image}" alt="${achievement.title}" class="my-4 rounded-md max-w-full h-auto max-h-48 ${imgAlignment} object-contain shadow-sm border border-cardborderlight dark:border-cardborderdark cursor-pointer transition-transform duration-300 hover:scale-105 block" loading="lazy">` : ''}
                                    <p class="text-secondary dark:text-secondarydark text-base leading-relaxed">${achievement.description}</p>
                               </div>
                            </div>
                        </div>
                    `;
                    timelineContainer.insertAdjacentHTML('beforeend', timelineElement);
                });
            } else { console.error("Timeline container or data not found"); }

            // --- Footer Year ---
            const currentYearSpan = document.getElementById('currentYear');
            if (currentYearSpan) { currentYearSpan.textContent = new Date().getFullYear(); }

        }); // End DOMContentLoaded
    </script>

</body>
</html>
