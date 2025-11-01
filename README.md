<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmed Academy - Your Gateway to World-Class Online Education</title>
    <!-- Load Tailwind CSS from CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Inter font from Google Fonts -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap">

    <!-- Tailwind CSS configuration for dark mode and custom animations -->
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    fontFamily: {
                        inter: ['Inter', 'sans-serif'],
                    },
                    keyframes: {
                        fadeIn: {
                            '0%': { opacity: '0', transform: 'translateY(20px)' },
                            '100%': { opacity: '1', transform: 'translateY(0)' },
                        },
                    },
                    animation: {
                        'fade-in': 'fadeIn 0.7s ease-out forwards',
                    },
                },
            },
        };
    </script>
    <style>
        /* Custom CSS to ensure smooth transitions and full-height body */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* Default light mode background */
            transition: background-color 0.5s ease;
        }
        .dark body {
            background-color: #111827; /* Dark mode background */
        }
        /* Ensure pages are initially hidden by default, and only shown by JS */
        main.content-page {
            display: none;
        }
        main#home-page {
            display: block; /* Home page is visible by default */
        }
    </style>
</head>

<body class="bg-gray-100 dark:bg-gray-900 text-gray-900 dark:text-white">

    <!-- Notice Banner -->
    <div id="notice-banner" class="fixed bottom-0 left-0 w-full bg-yellow-400 text-gray-900 p-4 text-center shadow-xl flex flex-col md:flex-row items-center justify-center space-y-2 md:space-y-0 md:space-x-4 z-50 transition-all duration-500 ease-in-out transform translate-y-0">
        <span class="font-bold text-lg">
            Important Notice: <span class="text-red-700 animate-pulse">!!!BIG DEAL!!!</span>
        </span>
        <span class="text-md">
            Pre-book* one class in each subject to get one class free**
        </span>
        <div class="text-sm mt-1 md:mt-0">
            <p class="opacity-80">*Prebooked classes are accepted at least two days in advance of the class date.</p>
            <p class="opacity-80">**One of the four pre-booked classes will be free.</p>
        </div>
        <button id="close-notice" class="ml-0 md:ml-4 text-2xl font-bold text-gray-700 hover:text-red-600 focus:outline-none focus:ring-2 focus:ring-gray-700 rounded-full p-1 transition-all duration-300 ease-in-out transform hover:rotate-90" aria-label="Close Notice">
            &times;
        </button>
    </div>

    <!-- Header Section -->
    <header class="bg-gradient-to-r from-blue-800 to-blue-900 text-white p-10 text-center shadow-2xl rounded-b-3xl flex flex-col items-center justify-center space-y-4">
        <img src="https://placehold.co/120x120/1f3a93/ffffff?text=AA+Logo" alt="Ahmed Academy Logo - A symbol of excellence in education" class="rounded-full border-4 border-white shadow-lg transition-all duration-500 ease-in-out hover:scale-110 hover:shadow-xl" width="120" height="120">
        <h1 class="text-4xl md:text-5xl font-extrabold tracking-tight drop-shadow-lg">Welcome to Ahmed Academy</h1>
        <h2 class="text-xl md:text-2xl font-light text-blue-100 drop-shadow-md">Your Gateway to World-Class Online Education</h2>
    </header>

    <!-- Navigation Bar -->
    <nav class="bg-blue-900 shadow-xl py-4 sticky top-0 z-50">
        <ul class="flex flex-wrap justify-center space-x-4 md:space-x-8 text-lg font-medium">
            <li>
                <button onclick="navigateTo('home-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    Home
                </button>
            </li>
            <li>
                <button onclick="navigateTo('math-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    Math
                </button>
            </li>
            <li>
                <button onclick="navigateTo('science-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    Science
                </button>
            </li>
            <li>
                <button onclick="navigateTo('english-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    English
                </button>
            </li>
            <li>
                <button onclick="navigateTo('computer-science-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    Comp. Science
                </button>
            </li>
            <li>
                <button onclick="navigateTo('about-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50">
                    About Us
                </button>
            </li>
            <li>
                <button onclick="navigateTo('settings-page')" class="nav-button px-4 py-2 rounded-lg transition-all duration-300 ease-in-out text-white hover:bg-blue-700 hover:text-white hover:scale-105 focus:outline-none focus:ring-2 focus:ring-white focus:ring-opacity-50 text-2xl" aria-label="Settings">
                    ⚙️
                </button>
            </li>
        </ul>
    </nav>

    <!-- Page Content Containers -->
    <div id="content-container" class="animate-fade-in">
        <!-- Home Page -->
        <main id="home-page" class="container mx-auto p-4 md:p-8 content-page">
            <div id="home-notice-banner" class="bg-yellow-100 border-l-4 border-yellow-500 text-yellow-700 p-4 mb-8 rounded-lg shadow-md flex justify-between items-center" role="alert">
                <div>
                    <p class="font-bold">Important Notice</p>
                    <p>Enrollment for the new academic year in **September** is now open, insha'Allah! Secure your child's spot today!</p>
                </div>
                <button id="close-home-notice" class="text-yellow-700 hover:text-yellow-900 font-bold text-xl ml-4 focus:outline-none" aria-label="Close notice">
                    &times;
                </button>
            </div>

            <section id="hero" class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl p-6 md:p-10 mb-12 text-center transform transition-all duration-500 hover:scale-[1.01] hover:shadow-2xl">
                <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 mb-4">Empowering Minds, Shaping Futures</h2>
                <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed mb-6">
                    Ahmed Academy offers comprehensive online courses designed to help students excel in Math, Science, English, and Computer Science. Our expert instructors and interactive learning environment ensure a rewarding educational experience.
                </p>
                <div class="flex flex-col sm:flex-row justify-center items-center space-y-4 sm:space-y-0 sm:space-x-6">
                    <button onclick="navigateTo('computer-science-page')" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-8 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-75 w-full sm:w-auto">
                        Explore Courses
                    </button>
                </div>
            </section>

            <section id="features" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-12">
                <!-- Feature Card 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 text-center transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <div class="text-blue-600 dark:text-blue-400 mb-4">
                        <svg class="w-12 h-12 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Flexible Learning</h3>
                    <p class="text-gray-600 dark:text-gray-400">Learn at your own pace, anytime, anywhere, with our flexible online platform.</p>
                </div>
                <!-- Feature Card 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 text-center transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <div class="text-blue-600 dark:text-blue-400 mb-4">
                        <svg class="w-12 h-12 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H2v-2a3 3 0 015.356-1.857M17 20v-2c0-.134-.01-.267-.03-.4H22m-4.356-1.857A3 3 0 0114 15c-1.428 0-2.76-.476-3.856-1.857M7 20v-2a3 3 0 00-5.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.134-.01-.267-.03-.4H22m-4.356-1.857A3 3 0 0114 15c-1.428 0-2.76-.476-3.856-1.857M12 12a4 4 0 100-8 4 4 0 000 8zm-2 2h4"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Expert Instructors</h3>
                    <p class="text-gray-600 dark:text-gray-400">Learn from highly qualified and experienced educators passionate about teaching.</p>
                </div>
                <!-- Feature Card 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 text-center transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <div class="text-blue-600 dark:text-blue-400 mb-4">
                        <svg class="w-12 h-12 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.001 12.001 0 002 12c0 2.75 1.11 5.268 2.944 7.071L12 22l7.056-2.929A12.001 12.001 0 0022 12c0-2.75-1.11-5.268-2.944-7.071z"></path></svg>
                    </div>
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Interactive Content</h3>
                    <p class="text-gray-600 dark:text-gray-400">Engage with dynamic lessons, quizzes, and projects to reinforce learning.</p>
                </div>
            </section>

            <section id="testimonials" class="bg-blue-50 dark:bg-gray-900 rounded-2xl shadow-xl p-6 md:p-10 mb-12">
                <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">What Our Students Say</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                    <!-- Testimonial Card 1 -->
                    <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md border border-blue-100 dark:border-blue-700">
                        <p class="text-gray-700 dark:text-gray-300 italic mb-4">"Ahmed Academy transformed my understanding of mathematics. The lessons are clear, concise, and incredibly helpful!"</p>
                        <p class="font-semibold text-blue-700 dark:text-blue-300">- Ahsan F., Primary School Student</p>
                    </div>
                    <!-- Testimonial Card 2 -->
                    <div class="bg-white dark:bg-gray-800 p-6 rounded-lg shadow-md border border-blue-100 dark:border-blue-700">
                        <p class="text-gray-700 dark:text-gray-300 italic mb-4">"I never thought I could grasp computer science concepts so easily. Thank you, Ahmed Academy, for making learning fun!"</p>
                        <p class="font-semibold text-blue-700 dark:text-blue-300">- Ahsan F., Young Coder</p>
                    </div>
                </div>
            </section>
        </main>

        <!-- Math Page -->
        <main id="math-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">Primary Math Adventures!</h2>
            <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed text-center mb-8">
                Our fun and interactive math lessons help young learners build a strong foundation in numbers, counting, and basic arithmetic. We make math exciting!
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Math Course Card 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Counting & Number Sense</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn to count, recognize numbers, and understand their value through engaging activities.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- Math Course Card 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Addition & Subtraction Fun</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Master adding and subtracting with playful games and real-world examples.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- Math Course Card 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Shapes & Patterns</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Discover different shapes, create patterns, and understand basic geometry.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- New Math Course Card 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Time & Money Skills</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn to tell time, count money, and solve simple word problems.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
            </div>
        </main>

        <!-- Science Page -->
        <main id="science-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">Discovering Science!</h2>
            <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed text-center mb-8">
                Our science courses introduce young minds to the wonders of the natural world through exciting experiments and engaging observations.
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Science Course Card 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Amazing Animals</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Explore different animal habitats, their life cycles, and what makes them unique.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- Science Course Card 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Plants & Nature</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn about plants, how they grow, and the importance of nature around us.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- Science Course Card 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Weather Wonders</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Understand different types of weather, seasons, and basic weather phenomena.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- New Science Course Card 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">My Body & Health</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">A fun introduction to how our bodies work and how to stay healthy.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
            </div>
        </main>

        <!-- English Page -->
        <main id="english-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">English for Young Readers!</h2>
            <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed text-center mb-8">
                Our English program focuses on building strong literacy skills, from phonics and reading to creative writing and storytelling.
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- English Course Card 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Phonics & Reading Readiness</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn letter sounds, blend words, and develop early reading skills with engaging activities.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- English Course Card 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Storytelling & Comprehension</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Read exciting stories, understand characters, and answer questions about what you've read.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- English Course Card 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Creative Writing & Grammar</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn to write simple sentences, paragraphs, and express your ideas creatively.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- New English Course Card 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Spelling & Vocabulary Builders</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Fun ways to learn new words and improve your spelling for better writing.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
            </div>
        </main>

        <!-- Computer Science Page -->
        <main id="computer-science-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">Tech Fun for Kids!</h2>
            <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed text-center mb-8">
                Our Computer Science courses introduce young learners to the exciting world of technology, coding, and digital safety in a fun and age-appropriate way.
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- CS Course Card 1 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Introduction to Coding (Block-Based)</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Learn to code by dragging and dropping blocks to create games and stories.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- CS Course Card 2 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Digital Citizenship & Safety</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Understand how to be safe and responsible when using computers and the internet.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- CS Course Card 3 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Creative Computing with Art</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Use computers to draw, create animations, and express your artistic ideas.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
                <!-- New CS Course Card 4 -->
                <div class="bg-white dark:bg-gray-800 rounded-2xl shadow-lg p-6 transform transition-all duration-300 hover:scale-105 hover:shadow-xl border border-blue-100 dark:border-blue-700">
                    <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-2">Keyboarding & Mouse Skills</h3>
                    <p class="text-gray-600 dark:text-gray-400 mb-4">Develop essential computer skills like typing and using a mouse effectively.</p>
                    <button class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full">Explore</button>
                </div>
            </div>
        </main>

        <!-- About Us Page -->
        <main id="about-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">About Ahmed Academy</h2>
            <section class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl p-6 md:p-10 mb-8">
                <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Our Mission</h3>
                <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed mb-6">
                    At Ahmed Academy, our mission is to provide high-quality, accessible online education to students worldwide. We believe that everyone deserves the opportunity to learn and grow, regardless of their location or circumstances.
                </p>
                <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Our Vision</h3>
                <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed mb-6">
                    We envision a future where learning is engaging, personalized, and empowers students to achieve their full potential. We are committed to continuously innovating our teaching methods and course content to meet the evolving needs of our learners.
                </p>
                <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Our Team</h3>
                <p class="text-lg text-gray-700 dark:text-gray-300 leading-relaxed">
                    Our team comprises passionate educators, subject matter experts, and technology enthusiasts dedicated to creating an exceptional learning environment. We are here to support you every step of the way on your educational journey.
                </p>
            </section>
        </main>

        <!-- Settings Page -->
        <main id="settings-page" class="container mx-auto p-4 md:p-8 content-page">
            <h2 class="text-3xl md:text-4xl font-bold text-blue-800 dark:text-blue-400 text-center mb-8">Settings</h2>
            <section class="bg-white dark:bg-gray-800 rounded-2xl shadow-xl p-6 md:p-10 mb-8">
                <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Display Options</h3>
                <div class="flex items-center justify-between mb-8 p-4 bg-gray-50 dark:bg-gray-700 rounded-lg shadow-sm">
                    <span class="text-lg font-medium text-gray-800 dark:text-gray-200">Dark Mode:</span>
                    <button id="dark-mode-toggle" class="relative inline-flex items-center h-6 rounded-full w-11 transition-colors duration-300 ease-in-out focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-opacity-50 bg-gray-200 dark:bg-gray-600">
                        <span class="inline-block w-5 h-5 transform transition-transform duration-300 ease-in-out rounded-full bg-white shadow-md dark:translate-x-5"></span>
                    </button>
                </div>
                
                <hr class="my-6 border-t border-gray-200 dark:border-gray-700" />
                
                <h3 class="text-2xl font-semibold text-gray-900 dark:text-white mb-4">Quick Navigation</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                    <button onclick="navigateTo('home-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">Home</button>
                    <button onclick="navigateTo('math-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">Math</button>
                    <button onclick="navigateTo('science-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">Science</button>
                    <button onclick="navigateTo('english-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">English</button>
                    <button onclick="navigateTo('computer-science-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">Comp. Science</button>
                    <button onclick="navigateTo('about-page')" class="nav-button bg-blue-600 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full shadow-lg transform transition-all duration-300 ease-in-out hover:scale-105">About Us</button>
                </div>
            </section>
        </main>
    </div>

    <!-- Footer Section -->
    <footer class="bg-gradient-to-r from-blue-800 to-blue-900 text-white p-6 text-center mt-16 rounded-t-3xl shadow-inner">
        <p class="text-lg mb-2">&copy; 2024 Ahmed Academy. All rights reserved.</p>
        <div class="flex justify-center space-x-4">
            <!-- Simple text placeholders for social media icons -->
            <a href="#" aria-label="Facebook" class="text-white hover:text-blue-200 transition-colors duration-300">
                Facebook
            </a>
            <a href="#" aria-label="Twitter" class="text-white hover:text-blue-200 transition-colors duration-300">
                Twitter
            </a>
            <a href="#" aria-label="Instagram" class="text-white hover:text-blue-200 transition-colors duration-300">
                Instagram
            </a>
        </div>
    </footer>

    <script>
        // Store all page IDs
        const pageIds = ['home-page', 'math-page', 'science-page', 'english-page', 'computer-science-page', 'about-page', 'settings-page'];
        const navButtons = document.querySelectorAll('.nav-button');

        // Function to show the selected page and hide others
        function navigateTo(pageId) {
            pageIds.forEach(id => {
                const page = document.getElementById(id);
                if (page) {
                    page.style.display = 'none'; // Explicitly hide the page
                }
            });

            const targetPage = document.getElementById(pageId);
            if (targetPage) {
                targetPage.style.display = 'block'; // Explicitly show the target page
            } else {
                console.error('Target page not found:', pageId);
            }

            // Update active class on nav buttons
            navButtons.forEach(button => {
                const onClickAttribute = button.getAttribute('onclick');
                if (onClickAttribute && onClickAttribute.includes(`'${pageId}'`)) {
                    button.classList.add('bg-blue-700', 'shadow-inner', 'scale-105');
                } else {
                    button.classList.remove('bg-blue-700', 'shadow-inner', 'scale-105');
                }
            });

            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // --- Notice Banner and Dark Mode Logic ---

        // Get elements for dark mode toggle
        const darkModeToggle = document.getElementById('dark-mode-toggle');
        const noticeBanner = document.getElementById('notice-banner');
        const closeNoticeButton = document.getElementById('close-notice');
        const homeNoticeBanner = document.getElementById('home-notice-banner');
        const closeHomeNoticeButton = document.getElementById('close-home-notice');

        // Initial setup for dark mode and notice banner on page load
        document.addEventListener('DOMContentLoaded', () => {
            // Load dark mode preference from localStorage
            if (localStorage.getItem('theme') === 'dark') {
                document.documentElement.classList.add('dark');
                // The toggle button has a dark mode state, so let's update it
                if (darkModeToggle) {
                    darkModeToggle.classList.remove('bg-gray-200');
                    darkModeToggle.classList.add('bg-gray-600');
                    darkModeToggle.querySelector('span').classList.add('translate-x-5');
                }
            }
            
            // Set initial active nav button and show home page
            navigateTo('home-page'); // Ensure home page is visible on load

            // Hide the home page notice banner if it was closed before
            if (localStorage.getItem('homeNoticeClosed') === 'true' && homeNoticeBanner) {
                homeNoticeBanner.style.display = 'none'; // Use style.display for consistency
            }
        });

        // Toggle dark mode function
        function toggleDarkMode() {
            const isDarkMode = document.documentElement.classList.toggle('dark');
            if (isDarkMode) {
                localStorage.setItem('theme', 'dark');
            } else {
                localStorage.setItem('theme', 'light');
            }
            // Animate the toggle button
            const toggleSpan = darkModeToggle.querySelector('span');
            if (isDarkMode) {
                darkModeToggle.classList.remove('bg-gray-200');
                darkModeToggle.classList.add('bg-gray-600');
                toggleSpan.classList.add('translate-x-5');
            } else {
                darkModeToggle.classList.remove('bg-gray-600');
                darkModeToggle.classList.add('bg-gray-200');
                toggleSpan.classList.remove('translate-x-5');
            }
        }

        // Event listener for dark mode toggle button
        if (darkModeToggle) {
            darkModeToggle.addEventListener('click', toggleDarkMode);
        }

        // Event listeners to close notice banners
        if (closeNoticeButton) {
            closeNoticeButton.addEventListener('click', () => {
                noticeBanner.style.display = 'none'; // Use style.display for consistency
            });
        }
        if (closeHomeNoticeButton) {
            closeHomeNoticeButton.addEventListener('click', () => {
                homeNoticeBanner.style.display = 'none'; // Use style.display for consistency
                localStorage.setItem('homeNoticeClosed', 'true');
            });
        }
    </script>
</body>
</html>
