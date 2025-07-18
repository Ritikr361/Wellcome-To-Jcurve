<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JCurve Labs - Helping Businesses Achieve J-Curve Growth</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
    
    <!-- Custom Styles & Animations -->
    <style>
        /* Set the default font for the entire page */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0A0A0A;
            color: #E5E7EB; /* A light gray for better readability than pure white */
        }

        /* Glassmorphism Card Style */
        .glass-card {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.3s ease;
        }

        .glass-card:hover {
            background: rgba(255, 255, 255, 0.08);
            border: 1px solid rgba(59, 130, 246, 0.5); /* Accent color border on hover */
            transform: translateY(-5px);
        }

        /* Animated Gradient Text */
        .animated-gradient-text {
            background: linear-gradient(90deg, #3B82F6, #8B5CF6, #EC4899, #3B82F6);
            background-size: 200% 200%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient-animation 5s ease infinite;
        }

        @keyframes gradient-animation {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Scroll-triggered Fade-in Animation */
        .fade-in-section {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }

        .fade-in-section.is-visible {
            opacity: 1;
            transform: translateY(0);
        }

        /* Blinking Cursor for Hero Section */
        .blinking-cursor {
            font-weight: 300;
            color: #3B82F6;
            animation: blink 1s step-end infinite;
        }

        @keyframes blink {
            from, to { opacity: 1; }
            50% { opacity: 0; }
        }

        /* Custom styling for sticky nav on scroll */
        .scrolled-nav {
            background-color: rgba(10, 10, 10, 0.8);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header & Navigation -->
    <header id="navbar" class="fixed top-0 left-0 w-full z-50 transition-all duration-300">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#home" class="text-2xl font-bold text-white">JCurve<span class="text-blue-500">Labs</span></a>
            <div class="hidden md:flex space-x-8 items-center">
                <a href="#about" class="text-gray-300 hover:text-blue-400 transition-colors">About</a>
                <a href="#services" class="text-gray-300 hover:text-blue-400 transition-colors">Services</a>
                <a href="#portfolio" class="text-gray-300 hover:text-blue-400 transition-colors">Case Studies</a>
                <a href="#contact" class="text-gray-300 hover:text-blue-400 transition-colors">Contact</a>
            </div>
            <a href="#contact" class="hidden md:block bg-blue-600 hover:bg-blue-700 text-white font-semibold py-2 px-5 rounded-lg transition-all duration-300 transform hover:scale-105">
                Book a Call
            </a>
            <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden text-white focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </nav>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-gray-900/90 backdrop-blur-sm">
            <a href="#about" class="block text-center py-3 text-gray-300 hover:bg-blue-600 hover:text-white">About</a>
            <a href="#services" class="block text-center py-3 text-gray-300 hover:bg-blue-600 hover:text-white">Services</a>
            <a href="#portfolio" class="block text-center py-3 text-gray-300 hover:bg-blue-600 hover:text-white">Case Studies</a>
            <a href="#contact" class="block text-center py-3 text-gray-300 hover:bg-blue-600 hover:text-white">Contact</a>
        </div>
    </header>

    <main>
        <!-- Hero Section -->
        <section id="home" class="min-h-screen flex items-center justify-center text-center relative overflow-hidden">
            <!-- Background Glow Effect -->
            <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-96 h-96 md:w-[600px] md:h-[600px] bg-blue-700 rounded-full filter blur-[150px] opacity-20"></div>
            <div class="absolute top-1/4 left-1/4 -translate-x-1/2 -translate-y-1/2 w-72 h-72 bg-purple-700 rounded-full filter blur-[120px] opacity-10"></div>
            
            <div class="container mx-auto px-6 z-10">
                <h1 class="text-4xl md:text-6xl lg:text-7xl font-extrabold text-white leading-tight mb-4">
                    Achieve J-Curve Growth With
                    <br>
                    <span id="dynamic-text" class="animated-gradient-text"></span><span class="blinking-cursor">|</span>
                </h1>
                <p class="text-lg md:text-xl text-gray-300 max-w-3xl mx-auto mb-8">
                    We combine data-driven strategies with cutting-edge automation to propel your business forward.
                </p>
                <a href="#contact" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 px-8 rounded-lg text-lg transition-all duration-300 transform hover:scale-105 inline-block shadow-lg shadow-blue-500/20">
                    Book Free Consultation
                </a>
            </div>
        </section>

        <!-- About Us Section -->
        <section id="about" class="py-20 md:py-32 fade-in-section">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">We Are JCurve Labs</h2>
                <div class="w-24 h-1 bg-blue-500 mx-auto mb-8"></div>
                <p class="text-lg text-gray-400 max-w-3xl mx-auto">
                    JCurve Labs was founded on a simple principle: to help ambitious businesses navigate the complexities of digital growth. Our mission is to be your dedicated partner, implementing strategies that don't just increase numbers, but build sustainable, long-term success, mirroring the exponential trajectory of the J-Curve.
                </p>
            </div>
        </section>

        <!-- Services Section -->
        <section id="services" class="py-20 md:py-32 bg-black fade-in-section">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">Our Core Services</h2>
                    <p class="text-lg text-gray-400">Tailored solutions for exponential growth.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
                    <!-- Service Card 1 -->
                    <div class="glass-card rounded-xl p-8 text-center">
                        <div class="mb-6">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 mx-auto text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-3">Digital Marketing</h3>
                        <p class="text-gray-400">Comprehensive strategies including SEO, PPC, and content marketing to dominate your niche.</p>
                    </div>
                    <!-- Service Card 2 -->
                    <div class="glass-card rounded-xl p-8 text-center">
                        <div class="mb-6">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 mx-auto text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-3">Branding & Identity</h3>
                        <p class="text-gray-400">Crafting memorable brands that resonate with your audience and stand out from the competition.</p>
                    </div>
                    <!-- Service Card 3 -->
                    <div class="glass-card rounded-xl p-8 text-center">
                        <div class="mb-6">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 mx-auto text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v.01M12 6v-1m0-1V4m0 2.01M12 18v-2m0-2v-2m0-2v-2m0-2V8m0 10V8m0 0h.01M12 8H8m4 0h4m-4 10v.01M12 18h.01M12 18h-4m4 0h4" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-3">Meta Ads</h3>
                        <p class="text-gray-400">Precision-targeted Facebook & Instagram ad campaigns that deliver measurable ROI.</p>
                    </div>
                    <!-- Service Card 4 -->
                    <div class="glass-card rounded-xl p-8 text-center">
                        <div class="mb-6">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-16 w-16 mx-auto text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z" />
                                <path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                            </svg>
                        </div>
                        <h3 class="text-xl font-bold text-white mb-3">Business Automation</h3>
                        <p class="text-gray-400">Streamlining your operations with custom workflows and AI-powered solutions to save time and money.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Why Choose Us Section -->
        <section id="why-us" class="py-20 md:py-32 fade-in-section">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">The JCurve Advantage</h2>
                    <p class="text-lg text-gray-400">We're more than an agency; we're your growth partner.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-12 text-center">
                    <div class="flex flex-col items-center">
                        <div class="p-4 bg-blue-500/10 rounded-full mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M17 9V7a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2m2 4h10a2 2 0 002-2v-6a2 2 0 00-2-2H9a2 2 0 00-2 2v6a2 2 0 002 2zm7-5a2 2 0 11-4 0 2 2 0 014 0z" /></svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">ROI-Focused</h3>
                        <p class="text-gray-400">Every action we take is aimed at maximizing your return on investment.</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="p-4 bg-purple-500/10 rounded-full mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-purple-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M9 3v2m6-2v2M9 19v2m6-2v2M5 9H3m2 6H3m18-6h-2m2 6h-2M12 6V3m0 18v-3" /></svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">Data-Driven</h3>
                        <p class="text-gray-400">We leverage analytics to make informed decisions and pivot strategies effectively.</p>
                    </div>
                    <div class="flex flex-col items-center">
                        <div class="p-4 bg-green-500/10 rounded-full mb-4">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-green-400" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path stroke-linecap="round" stroke-linejoin="round" d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2 1M4 7l2-1M4 7v2.5M12 21l-2-1m2 1l2-1m-2 1v-2.5M6 18l-2-1m2 1l-2 1m2-1V15" /></svg>
                        </div>
                        <h3 class="text-xl font-semibold text-white mb-2">Transparent & Collaborative</h3>
                        <p class="text-gray-400">You're always in the loop with clear communication and detailed reporting.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- Portfolio/Case Studies Section -->
        <section id="portfolio" class="py-20 md:py-32 bg-black fade-in-section">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">Our Track Record</h2>
                    <p class="text-lg text-gray-400">Proven success stories from our clients.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Case Study Card 1 -->
                    <div class="glass-card rounded-xl overflow-hidden">
                        <img src="https://placehold.co/600x400/0A0A0A/3B82F6?text=E-commerce+Giant" alt="E-commerce project" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-white mb-2">E-commerce Giant</h3>
                            <p class="text-gray-400 mb-4">Increased online sales by 300% in 6 months through targeted Meta Ads and SEO.</p>
                            <span class="text-blue-400 font-semibold">Meta Ads & SEO</span>
                        </div>
                    </div>
                    <!-- Case Study Card 2 -->
                    <div class="glass-card rounded-xl overflow-hidden">
                        <img src="https://placehold.co/600x400/0A0A0A/8B5CF6?text=SaaS+Unicorn" alt="SaaS project" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-white mb-2">SaaS Unicorn</h3>
                            <p class="text-gray-400 mb-4">Built a powerful brand identity and automated lead nurturing, boosting MQLs by 150%.</p>
                            <span class="text-purple-400 font-semibold">Branding & Automation</span>
                        </div>
                    </div>
                    <!-- Case Study Card 3 -->
                    <div class="glass-card rounded-xl overflow-hidden">
                        <img src="https://placehold.co/600x400/0A0A0A/10B981?text=Local+Service+Pro" alt="Local service project" class="w-full h-48 object-cover">
                        <div class="p-6">
                            <h3 class="text-xl font-bold text-white mb-2">Local Service Pro</h3>
                            <p class="text-gray-400 mb-4">Dominated local search results and generated a 5x ROAS with a hyperlocal marketing strategy.</p>
                            <span class="text-green-400 font-semibold">Digital Marketing</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Testimonials Section -->
        <section id="testimonials" class="py-20 md:py-32 fade-in-section">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">What Our Clients Say</h2>
                </div>
                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
                    <!-- Testimonial Card 1 -->
                    <div class="glass-card rounded-xl p-8">
                        <p class="text-gray-300 italic mb-6">"JCurve Labs transformed our digital presence. Their automation strategies saved us 20+ hours a week. Incredible team, incredible results."</p>
                        <div class="flex items-center">
                            <img src="https://i.pravatar.cc/48?u=1" alt="Client 1" class="w-12 h-12 rounded-full mr-4">
                            <div>
                                <p class="font-bold text-white">Sarah Johnson</p>
                                <p class="text-gray-400">CEO, Tech Innovators</p>
                            </div>
                        </div>
                    </div>
                    <!-- Testimonial Card 2 -->
                    <div class="glass-card rounded-xl p-8">
                        <p class="text-gray-300 italic mb-6">"The ROI on our Meta Ad campaigns has been phenomenal. They understand our market better than anyone. Highly recommended."</p>
                        <div class="flex items-center">
                            <img src="https://i.pravatar.cc/48?u=2" alt="Client 2" class="w-12 h-12 rounded-full mr-4">
                            <div>
                                <p class="font-bold text-white">Mike Chen</p>
                                <p class="text-gray-400">Founder, StyleHub</p>
                            </div>
                        </div>
                    </div>
                    <!-- Testimonial Card 3 -->
                    <div class="glass-card rounded-xl p-8">
                        <p class="text-gray-300 italic mb-6">"From a vague idea to a powerful brand, JCurve Labs guided us every step of the way. Their branding work was a game-changer for us."</p>
                        <div class="flex items-center">
                            <img src="https://i.pravatar.cc/48?u=3" alt="Client 3" class="w-12 h-12 rounded-full mr-4">
                            <div>
                                <p class="font-bold text-white">Emily Rodriguez</p>
                                <p class="text-gray-400">Co-Founder, NutriLife</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Contact Section -->
        <section id="contact" class="py-20 md:py-32 bg-black fade-in-section">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-white mb-4">Ready to Start Your Growth Curve?</h2>
                    <p class="text-lg text-gray-400">Let's talk. Fill out the form below or reach out directly.</p>
                </div>
                <div class="max-w-3xl mx-auto">
                    <form action="#" method="POST" class="space-y-6">
                        <div>
                            <label for="name" class="sr-only">Name</label>
                            <input type="text" name="name" id="name" placeholder="Your Name" class="w-full bg-gray-800/50 border border-gray-700 rounded-lg py-3 px-4 text-white focus:outline-none focus:ring-2 focus:ring-blue-500 transition-all" required>
                        </div>
                        <div>
                            <label for="email" class="sr-only">Email</label>
                            <input type="email" name="email" id="email" placeholder="Your Email" class="w-full bg-gray-800/50 border border-gray-700 rounded-lg py-3 px-4 text-white focus:outline-none focus:ring-2 focus:ring-blue-500 transition-all" required>
                        </div>
                        <div>
                            <label for="message" class="sr-only">Message</label>
                            <textarea name="message" id="message" rows="5" placeholder="Tell us about your project..." class="w-full bg-gray-800/50 border border-gray-700 rounded-lg py-3 px-4 text-white focus:outline-none focus:ring-2 focus:ring-blue-500 transition-all" required></textarea>
                        </div>
                        <div class="text-center">
                            <button type="submit" class="bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 px-12 rounded-lg text-lg transition-all duration-300 transform hover:scale-105 shadow-lg shadow-blue-500/20">
                                Send Message
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900/50 border-t border-gray-800 py-12">
        <div class="container mx-auto px-6 text-center text-gray-400">
            <div class="flex justify-center space-x-6 mb-6">
                <a href="#" class="hover:text-blue-400 transition-colors">
                    <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" /></svg>
                </a>
                <a href="#" class="hover:text-blue-400 transition-colors">
                     <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.71v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" /></svg>
                </a>
                <a href="#" class="hover:text-blue-400 transition-colors">
                    <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12.011c0 4.434 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.009-.868-.014-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.031-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.203 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.338 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.001 10.001 0 0022 12.011C22 6.477 17.523 2 12 2z" clip-rule="evenodd" /></svg>
                </a>
            </div>
            <p>&copy; 2024 JCurve Labs. All Rights Reserved.</p>
            <div class="mt-2 text-sm">
                <a href="#" class="hover:text-white">Privacy Policy</a>
                <span class="mx-2">|</span>
                <a href="#" class="hover:text-white">Terms of Service</a>
            </div>
        </div>
    </footer>

    <script>
        // --- Dynamic Text Typing Animation ---
        const dynamicText = document.getElementById('dynamic-text');
        const phrases = ["Digital Marketing", "Branding", "Meta Ads", "Business Automation"];
        let phraseIndex = 0;
        let charIndex = 0;
        let isDeleting = false;

        function type() {
            const currentPhrase = phrases[phraseIndex];
            if (isDeleting) {
                dynamicText.textContent = currentPhrase.substring(0, charIndex - 1);
                charIndex--;
            } else {
                dynamicText.textContent = currentPhrase.substring(0, charIndex + 1);
                charIndex++;
            }

            let typeSpeed = isDeleting ? 75 : 150;

            if (!isDeleting && charIndex === currentPhrase.length) {
                typeSpeed = 2000; // Pause at end of word
                isDeleting = true;
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                phraseIndex = (phraseIndex + 1) % phrases.length;
                typeSpeed = 500; // Pause before starting new word
            }

            setTimeout(type, typeSpeed);
        }

        document.addEventListener('DOMContentLoaded', type);


        // --- Scroll-triggered Fade-in Animation ---
        const sections = document.querySelectorAll('.fade-in-section');
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('is-visible');
                    observer.unobserve(entry.target); // Optional: stop observing once visible
                }
            });
        }, {
            threshold: 0.1 // Trigger when 10% of the section is visible
        });

        sections.forEach(section => {
            observer.observe(section);
        });

        // --- Sticky Navigation Background on Scroll ---
        const navbar = document.getElementById('navbar');
        window.addEventListener('scroll', () => {
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled-nav');
            } else {
                navbar.classList.remove('scrolled-nav');
            }
        });

        // --- Mobile Menu Toggle ---
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu when a link is clicked
        const mobileMenuLinks = mobileMenu.querySelectorAll('a');
        mobileMenuLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

    </script>
</body>
</html>
