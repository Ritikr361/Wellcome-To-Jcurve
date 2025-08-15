<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jcurvelabs - Digital Marketing Agency</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Lucide Icons -->
    <script src="https://unpkg.com/lucide@latest"></script>

    <!-- Custom Styles -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;800;900&display=swap');

        .gradient-text {
            background: linear-gradient(90deg, #a855f7, #ec4899);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
        }
        .gradient-border {
            border: 2px solid;
            border-image-slice: 1;
            border-image-source: linear-gradient(to right, #a855f7, #ec4899);
        }
        .card-bg {
            background-color: rgba(255, 255, 255, 0.03);
        }
        .card-bg:hover {
            background-color: rgba(255, 255, 255, 0.05);
        }
        .animate-fade-in-up {
            animation: fadeInUp 0.8s ease-out forwards;
            opacity: 0;
        }
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body class="bg-black text-gray-200">

    <!-- Main Home Page Container -->
    <div id="home-page">
        <!-- Header -->
        <header class="bg-black/80 backdrop-blur-sm sticky top-0 z-50">
            <div class="container mx-auto px-6 py-4 flex justify-between items-center">
                <h1 class="text-2xl font-bold tracking-wider gradient-text">Jcurvelabs</h1>
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="#home" class="hover:text-purple-400 transition-colors duration-300">Home</a>
                    <a href="#services" class="hover:text-purple-400 transition-colors duration-300">Services</a>
                    <a href="#about" class="hover:text-purple-400 transition-colors duration-300">About</a>
                    <button onclick="navigateTo('contact')" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-5 py-2 rounded-full hover:scale-105 transform transition-transform duration-300">
                        Let's Work Together
                    </button>
                </nav>
                <div class="md:hidden">
                    <button id="menu-open-btn">
                        <i data-lucide="menu" class="w-7 h-7"></i>
                    </button>
                </div>
            </div>
        </header>

        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden fixed top-0 left-0 w-full h-screen bg-black/95 md:hidden flex-col items-center justify-center space-y-8 z-50 animate-fade-in-up">
            <button id="menu-close-btn" class="absolute top-6 right-6">
                <i data-lucide="x" class="w-8 h-8"></i>
            </button>
            <a href="#home" class="text-2xl hover:text-purple-400 mobile-menu-link">Home</a>
            <a href="#services" class="text-2xl hover:text-purple-400 mobile-menu-link">Services</a>
            <a href="#about" class="text-2xl hover:text-purple-400 mobile-menu-link">About</a>
            <button onclick="navigateTo('contact')" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-6 py-3 rounded-full text-lg mobile-menu-link">
                Let's Work Together
            </button>
        </div>

        <main>
            <!-- Hero Section -->
            <section id="home" class="min-h-screen flex items-center justify-center text-center relative overflow-hidden">
                <div class="absolute w-72 h-72 bg-purple-600 rounded-full -left-20 -top-20 filter blur-3xl opacity-20 animate-pulse"></div>
                <div class="absolute w-72 h-72 bg-pink-600 rounded-full -right-20 -bottom-20 filter blur-3xl opacity-20 animate-pulse animation-delay-4000"></div>
                <div class="container mx-auto px-6 z-10 animate-fade-in-up">
                    <h2 class="text-4xl md:text-7xl font-extrabold leading-tight mb-4">
                        We Don't Just Follow The Curve.<br />
                        <span class="gradient-text">We Create It.</span>
                    </h2>
                    <p class="text-lg md:text-xl text-gray-400 max-w-3xl mx-auto mb-8">
                        Jcurvelabs is your partner in navigating the digital landscape. We craft bespoke strategies and deliver results that matter.
                    </p>
                    <button onclick="navigateTo('contact')" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold text-lg px-8 py-4 rounded-full hover:scale-105 transform transition-transform duration-300 inline-block shadow-lg shadow-purple-500/20">
                        Get Your Free Proposal
                    </button>
                </div>
            </section>

            <!-- Services Section -->
            <section id="services" class="py-20">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h3 class="text-4xl font-bold gradient-text mb-2">Our Services</h3>
                        <p class="text-gray-400">Everything you need to conquer the digital world.</p>
                    </div>
                    <div id="services-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                        <!-- Service cards will be injected by JavaScript -->
                    </div>
                </div>
            </section>

            <!-- About Section -->
            <section id="about" class="py-20 bg-gray-900/30">
                 <div class="container mx-auto px-6 flex flex-col md:flex-row items-center gap-12">
                    <div class="md:w-1/2 animate-fade-in-up">
                        <h3 class="text-4xl font-bold mb-4">
                            The <span class="gradient-text">Agency</span> For The <span class="gradient-text">Bold</span>.
                        </h3>
                        <p class="text-gray-400 mb-4 leading-relaxed">
                            At Jcurvelabs, we're a team of passionate creators, strategists, and tech enthusiasts dedicated to pushing boundaries. We believe in the power of data-driven creativity to build brands that not only succeed but also inspire.
                        </p>
                         <p class="text-gray-400 leading-relaxed">
                            Our mission is simple: to be the catalyst for your growth. We combine cutting-edge technology with innovative marketing to create a curve of success that's uniquely yours.
                        </p>
                    </div>
                     <div class="md:w-1/2 animate-fade-in-up" style="animation-delay: 200ms;">
                        <div class="p-8 rounded-2xl card-bg border border-gray-800">
                            <img 
                                src="https://placehold.co/600x400/000000/a855f7?text=Jcurvelabs+Team" 
                                alt="Jcurvelabs Team" 
                                class="rounded-lg w-full h-auto"
                                onerror="this.onerror=null;this.src='https://placehold.co/600x400/000000/FFFFFF?text=Image+Not+Found';"
                            />
                        </div>
                    </div>
                </div>
            </section>

            <!-- CTA Section -->
            <section id="contact-cta" class="py-24 text-center">
                <div class="container mx-auto px-6 animate-fade-in-up">
                    <h3 class="text-4xl md:text-5xl font-extrabold mb-4">
                        Ready to redefine your <span class="gradient-text">digital presence?</span>
                    </h3>
                    <p class="text-gray-400 max-w-2xl mx-auto mb-8 text-lg">
                        Don't wait for the future, let's build it together. Reach out to us and let's discuss how we can elevate your brand to the next level.
                    </p>
                    <button onclick="navigateTo('contact')" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold text-xl px-10 py-5 rounded-full hover:scale-105 transform transition-transform duration-300 inline-block shadow-lg shadow-pink-500/30 animate-pulse">
                        Get in Touch
                    </button>
                </div>
            </section>
        </main>

        <!-- Footer -->
        <footer class="bg-gray-900/50 border-t border-gray-800 py-8">
            <div class="container mx-auto px-6 text-center text-gray-500">
                <div class="flex justify-center space-x-6 mb-4">
                    <a href="#" class="hover:text-purple-400 transition-colors"><i data-lucide="twitter"></i></a>
                    <a href="#" class="hover:text-purple-400 transition-colors"><i data-lucide="instagram"></i></a>
                    <a href="#" class="hover:text-purple-400 transition-colors"><i data-lucide="linkedin"></i></a>
                </div>
                <p>&copy; <span id="current-year"></span> Jcurvelabs. All Rights Reserved.</p>
                <p class="text-sm mt-2">Crafted with passion and code.</p>
            </div>
        </footer>
    </div>

    <!-- Contact Form Page Container -->
    <div id="contact-page" class="hidden">
        <div class="min-h-screen bg-black p-4 sm:p-8 animate-fade-in-up">
            <div class="max-w-4xl mx-auto">
                <button onclick="navigateTo('home')" class="mb-8 text-gray-300 hover:text-white transition-colors flex items-center gap-2">
                    <i data-lucide="arrow-left" class="w-5 h-5"></i> Back to Home
                </button>

                <div id="form-container">
                    <div class="text-center mb-10">
                        <h1 class="text-4xl md:text-5xl font-bold gradient-text">Let's Build Something Great</h1>
                        <p class="text-gray-400 mt-2">Please fill out this form, and we'll get back to you shortly.</p>
                    </div>

                    <form id="inquiry-form" class="card-bg border border-gray-800 rounded-2xl p-6 sm:p-10 space-y-8">
                        <!-- Form Fields -->
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="fullName" class="block text-sm font-medium text-gray-300 mb-2">Full Name (आपका नाम)</label>
                                <input type="text" name="fullName" id="fullName" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"/>
                            </div>
                            <div>
                                <label for="mobileNumber" class="block text-sm font-medium text-gray-300 mb-2">Mobile Number (मोबाइल नंबर) <span class="text-red-500">*</span></label>
                                <input type="tel" name="mobileNumber" id="mobileNumber" required class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"/>
                            </div>
                            <div>
                                <label for="email" class="block text-sm font-medium text-gray-300 mb-2">Email Address (ईमेल, optional)</label>
                                <input type="email" name="email" id="email" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"/>
                            </div>
                            <div>
                                <label for="businessName" class="block text-sm font-medium text-gray-300 mb-2">Business Name (व्यवसाय का नाम)</label>
                                <input type="text" name="businessName" id="businessName" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"/>
                            </div>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="businessType" class="block text-sm font-medium text-gray-300 mb-2">Business Type (व्यवसाय का प्रकार)</label>
                                <select name="businessType" id="businessType" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition">
                                    <option value="">Select Type</option><option>Service-based</option><option>E-commerce / Product</option><option>Local Business</option><option>Startup</option><option>Other</option>
                                </select>
                            </div>
                            <div>
                                <label for="location" class="block text-sm font-medium text-gray-300 mb-2">Business Location (City/Area)</label>
                                <input type="text" name="location" id="location" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"/>
                            </div>
                        </div>
                        <div>
                            <label for="duration" class="block text-sm font-medium text-gray-300 mb-2">Business Duration (कितने समय से चल रहा है)</label>
                            <select name="duration" id="duration" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition">
                                <option value="">Select Duration</option><option>Just Starting</option><option>Less than 1 year</option><option>1-3 years</option><option>3-5 years</option><option>More than 5 years</option>
                            </select>
                        </div>
                        <div>
                            <label for="challenge" class="block text-sm font-medium text-gray-300 mb-2">Biggest Business Challenge (सबसे बड़ी चुनौती)</label>
                            <textarea name="challenge" id="challenge" rows="4" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition"></textarea>
                        </div>
                        <div>
                            <label class="block text-sm font-medium text-gray-300 mb-2">Support Required (क्या सहायता चाहिए?)</label>
                            <div id="support-options-container" class="grid grid-cols-2 sm:grid-cols-3 gap-4 mt-2">
                                <!-- Checkboxes injected by JS -->
                            </div>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div>
                                <label for="revenue" class="block text-sm font-medium text-gray-300 mb-2">Monthly Revenue Range (मासिक आय)</label>
                                <select name="revenue" id="revenue" class="w-full bg-gray-900/50 border border-gray-700 rounded-lg px-4 py-2 focus:ring-purple-500 focus:border-purple-500 transition">
                                    <option value="">Select Range</option><option>Below ₹50,000</option><option>₹50,000 - ₹2 Lakh</option><option>₹2 Lakh - ₹10 Lakh</option><option>Above ₹10 Lakh</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-300 mb-2">Consultation Call Request? (हाँ/नहीं)</label>
                                <div class="flex items-center space-x-6 mt-2">
                                    <div class="flex items-center">
                                        <input id="consultation-yes" name="consultation" type="radio" value="Yes" class="h-4 w-4 border-gray-600 bg-gray-800 text-purple-600 focus:ring-purple-500"/>
                                        <label for="consultation-yes" class="ml-3 block text-sm font-medium text-gray-300">Yes (हाँ)</label>
                                    </div>
                                    <div class="flex items-center">
                                        <input id="consultation-no" name="consultation" type="radio" value="No" class="h-4 w-4 border-gray-600 bg-gray-800 text-purple-600 focus:ring-purple-500"/>
                                        <label for="consultation-no" class="ml-3 block text-sm font-medium text-gray-300">No (नहीं)</label>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="text-center pt-4">
                            <button type="submit" id="submit-btn" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-bold text-lg px-10 py-4 rounded-full hover:scale-105 transform transition-transform duration-300 inline-block shadow-lg shadow-purple-500/30">
                                Submit Inquiry
                            </button>
                        </div>
                    </form>
                </div>

                <!-- Thank You Message -->
                <div id="thank-you-message" class="hidden min-h-screen flex-col items-center justify-center text-center p-6 animate-fade-in-up">
                    <h2 class="text-4xl font-bold gradient-text mb-4">Thank You!</h2>
                    <p class="text-gray-300 text-lg max-w-md mx-auto mb-8">Aapki inquiry humein mil gayi hai. Hum jald hi aapse sampark karenge. Agar WhatsApp open nahi hua hai, to aap humein direct message kar sakte hain.</p>
                    <button onclick="navigateTo('home')" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white font-semibold px-6 py-3 rounded-full hover:scale-105 transform transition-transform duration-300 flex items-center gap-2">
                        <i data-lucide="arrow-left" class="w-5 h-5"></i> Back to Home
                    </button>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Scroll to Top Button -->
    <button id="scroll-to-top" class="hidden fixed bottom-8 right-8 bg-gradient-to-r from-purple-500 to-pink-500 text-white p-3 rounded-full shadow-lg hover:scale-110 transition-transform duration-300 z-50">
        <i data-lucide="arrow-up" class="w-6 h-6"></i>
    </button>

    <script>
        // --- DATA ---
        const services = [
            { icon: 'megaphone', color: 'text-purple-400', title: "Meta Ads Marketing", description: "Targeted campaigns on Meta platforms to maximize your reach and ROI." },
            { icon: 'globe', color: 'text-blue-400', title: "Google Ads", description: "Drive high-intent traffic to your site with powerful Google Ads strategies." },
            { icon: 'facebook', color: 'text-sky-500', title: "Facebook Ads", description: "Engage with your audience through creative and effective Facebook advertising." },
            { icon: 'phone', color: 'text-green-400', title: "Truecaller Ads", description: "Reach millions of verified users with impactful Truecaller Ad solutions." },
            { icon: 'palette', color: 'text-rose-400', title: "Website Designing", description: "Stunning, user-centric website designs that captivate and convert." },
            { icon: 'smartphone', color: 'text-amber-400', title: "Application Development", description: "Custom mobile applications for iOS and Android to elevate your business." },
            { icon: 'code', color: 'text-teal-400', title: "Web Development", description: "Robust and scalable web solutions tailored to your specific needs." },
            { icon: 'pen-tool', color: 'text-indigo-400', title: "Graphic Designing", description: "Creative visuals and branding that tell your story and build recognition." },
            { icon: 'users', color: 'text-pink-400', title: "Social Media Management", description: "Comprehensive management of your social channels to grow your community." },
            { icon: 'image-plus', color: 'text-cyan-400', title: "Social Media Post Creation", description: "Engaging and high-quality content creation for your social media presence." },
            { icon: 'camera', color: 'text-red-400', title: "Product Shoot", description: "Professional photography and videography to showcase your products." },
            { icon: 'clapperboard', color: 'text-yellow-400', title: "Ad Creation", description: "Compelling ad creatives that grab attention and drive action." },
            { icon: 'laptop', color: 'text-lime-400', title: "Product Mockups", description: "Realistic product mockups to visualize and present your designs." },
        ];
        const supportOptions = [
            "Meta/Google Ads", "Website/App Development", "Graphic Designing", "Social Media Management", "Product Shoot/Ad Creation"
        ];

        // --- ELEMENTS ---
        const homePage = document.getElementById('home-page');
        const contactPage = document.getElementById('contact-page');
        const mobileMenu = document.getElementById('mobile-menu');
        const menuOpenBtn = document.getElementById('menu-open-btn');
        const menuCloseBtn = document.getElementById('menu-close-btn');
        const mobileMenuLinks = document.querySelectorAll('.mobile-menu-link');
        const scrollToTopBtn = document.getElementById('scroll-to-top');
        const inquiryForm = document.getElementById('inquiry-form');
        const submitBtn = document.getElementById('submit-btn');
        const formContainer = document.getElementById('form-container');
        const thankYouMessage = document.getElementById('thank-you-message');

        // --- FUNCTIONS ---

        // Page Navigation
        function navigateTo(page) {
            if (page === 'home') {
                homePage.style.display = 'block';
                contactPage.style.display = 'none';
                // Reset form page for next visit
                formContainer.style.display = 'block';
                thankYouMessage.style.display = 'none';
                inquiryForm.reset();
            } else if (page === 'contact') {
                homePage.style.display = 'none';
                contactPage.style.display = 'block';
            }
            window.scrollTo(0, 0);
            if (!mobileMenu.classList.contains('hidden')) {
                mobileMenu.classList.add('hidden');
                mobileMenu.classList.remove('flex');
            }
        }

        // Mobile Menu Toggle
        function toggleMenu() {
            mobileMenu.classList.toggle('hidden');
            mobileMenu.classList.toggle('flex');
        }

        // Populate Dynamic Content
        function populateContent() {
            // Services
            const servicesGrid = document.getElementById('services-grid');
            services.forEach((service, index) => {
                const card = document.createElement('div');
                card.className = `card-bg border border-gray-800 rounded-2xl p-8 flex flex-col items-center text-center transform hover:-translate-y-2 transition-transform duration-300 gradient-border animate-fade-in-up`;
                card.style.animationDelay = `${index * 100}ms`;
                card.innerHTML = `
                    <div class="mb-4 ${service.color}">
                        <i data-lucide="${service.icon}" class="w-10 h-10"></i>
                    </div>
                    <h4 class="text-xl font-bold mb-2 text-white">${service.title}</h4>
                    <p class="text-gray-400">${service.description}</p>
                `;
                servicesGrid.appendChild(card);
            });

            // Form Checkboxes
            const supportContainer = document.getElementById('support-options-container');
            supportOptions.forEach(option => {
                const checkboxDiv = document.createElement('div');
                checkboxDiv.className = 'flex items-center';
                checkboxDiv.innerHTML = `
                    <input id="${option.replace(/\s/g, '')}" name="support" type="checkbox" value="${option}" class="h-4 w-4 rounded border-gray-600 bg-gray-800 text-purple-600 focus:ring-purple-500">
                    <label for="${option.replace(/\s/g, '')}" class="ml-3 text-sm text-gray-300">${option}</label>
                `;
                supportContainer.appendChild(checkboxDiv);
            });

            // Year
            document.getElementById('current-year').textContent = new Date().getFullYear();
        }

        // --- EVENT LISTENERS ---
        
        // On Load
        document.addEventListener('DOMContentLoaded', () => {
            populateContent();
            lucide.createIcons(); // Initialize all icons
        });

        // Mobile Menu
        menuOpenBtn.addEventListener('click', toggleMenu);
        menuCloseBtn.addEventListener('click', toggleMenu);
        mobileMenuLinks.forEach(link => link.addEventListener('click', toggleMenu));

        // Scroll to Top
        window.addEventListener('scroll', () => {
            if (window.pageYOffset > 300) {
                scrollToTopBtn.classList.remove('hidden');
            } else {
                scrollToTopBtn.classList.add('hidden');
            }
        });
        scrollToTopBtn.addEventListener('click', () => {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });

        // Form Submission
        inquiryForm.addEventListener('submit', (e) => {
            e.preventDefault();
            submitBtn.textContent = 'Submitting...';
            submitBtn.disabled = true;

            const formData = new FormData(inquiryForm);
            const data = Object.fromEntries(formData.entries());
            data.support = formData.getAll('support'); // Get all checkbox values

            const message = `
*New Inquiry from Jcurvelabs Website*
---------------------------------
*Full Name:* ${data.fullName || 'N/A'}
*Mobile Number:* ${data.mobileNumber}
*Email:* ${data.email || 'N/A'}
*Business Name:* ${data.businessName || 'N/A'}
*Business Type:* ${data.businessType || 'N/A'}
*Location:* ${data.location || 'N/A'}
*Business Duration:* ${data.duration || 'N/A'}
*Biggest Challenge:* ${data.challenge || 'N/A'}
*Support Required:* ${data.support.join(', ') || 'N/A'}
*Monthly Revenue:* ${data.revenue || 'N/A'}
*Consultation Request:* ${data.consultation || 'N/A'}
            `;

            const encodedMessage = encodeURIComponent(message.trim());
            const whatsappNumber = '918959384509';
            const whatsappUrl = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;

            window.open(whatsappUrl, '_blank');

            // Show thank you message
            formContainer.style.display = 'none';
            thankYouMessage.classList.remove('hidden');
            thankYouMessage.classList.add('flex');
            
            submitBtn.textContent = 'Submit Inquiry';
            submitBtn.disabled = false;
        });

    </script>
</body>
</html>
