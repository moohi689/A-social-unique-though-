<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Social Unique Thought - Spreading Greenery</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0fdf4; /* Light green background */
        }
        /* Custom scrollbar for a nicer look */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #e0ffe0;
        }
        ::-webkit-scrollbar-thumb {
            background: #34d399; /* Emerald 400 */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #10b981; /* Emerald 500 */
        }
        /* Keyframes for fade-in-up animation */
        @keyframes fade-in-up {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .animate-fade-in-up {
            animation: fade-in-up 0.6s ease-out forwards;
        }
        .animate-fade-in-up.delay-200 {
            animation-delay: 0.2s;
        }
        .animate-fade-in-up.delay-400 {
            animation-delay: 0.4s;
        }

        /* Custom modal styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: #fefefe;
            margin: auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 500px;
            text-align: center;
            position: relative;
        }

        .close-button {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            position: absolute;
            top: 10px;
            right: 15px;
        }

        .close-button:hover,
        .close-button:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header Section -->
    <header class="bg-white shadow-md py-4 px-6 md:px-12 lg:px-24 flex justify-between items-center rounded-b-xl">
        <div class="flex items-center space-x-3">
            <img src="https://placehold.co/40x40/10b981/ffffff?text=🌱" alt="Leaf Logo" class="rounded-full">
            <h1 class="text-2xl font-bold text-emerald-700">A Social Unique Thought</h1>
        </div>
        <nav class="hidden md:flex space-x-8">
            <a href="#home" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Home</a>
            <a href="#about" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">About Us</a>
            <a href="#donate" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Donate</a>
            <a href="#join" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Join Us</a>
            <a href="#green-thumb-assistant" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Green Assistant</a>
            <a href="#contact" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Contact</a>
        </nav>
        <!-- Mobile Menu Button (Hamburger) -->
        <button id="mobile-menu-button" class="md:hidden text-gray-600 hover:text-emerald-600 focus:outline-none">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
            </svg>
        </button>
    </header>

    <!-- Mobile Menu Overlay -->
    <div id="mobile-menu" class="hidden md:hidden fixed inset-0 bg-white bg-opacity-95 z-50 flex flex-col items-center justify-center space-y-6">
        <button id="close-mobile-menu" class="absolute top-4 right-4 text-gray-600 hover:text-emerald-600 focus:outline-none">
            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
        </button>
        <a href="#home" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Home</a>
        <a href="#about" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">About Us</a>
        <a href="#donate" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Donate</a>
        <a href="#join" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Join Us</a>
        <a href="#green-thumb-assistant" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Green Assistant</a>
        <a href="#contact" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Contact</a>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-r from-emerald-500 to-green-600 text-white py-20 md:py-32 text-center overflow-hidden rounded-b-xl mx-4 mt-4 shadow-lg">
        <div class="absolute inset-0 opacity-20">
            <!-- Background pattern for visual appeal -->
            <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="xMidYMid slice">
                <defs>
                    <pattern id="pattern-circles" x="0" y="0" width="10" height="10" patternUnits="userSpaceOnUse">
                        <circle cx="5" cy="5" r="1" fill="rgba(255,255,255,0.1)"></circle>
                    </pattern>
                </defs>
                <rect x="0" y="0" width="100%" height="100%" fill="url(#pattern-circles)"></rect>
            </svg>
        </div>
        <div class="relative z-10 max-w-4xl mx-auto px-6">
            <h2 class="text-4xl md:text-6xl font-extrabold leading-tight mb-6 animate-fade-in-up">
                Nurturing Nature, Growing Communities
            </h2>
            <p class="text-lg md:text-xl mb-10 opacity-90 animate-fade-in-up delay-200">
                Join 'A Social Unique Thought' in our mission to make Muzaffarnagar greener and healthier.
            </p>
            <a href="#donate" class="bg-white text-emerald-700 hover:bg-emerald-100 px-8 py-4 rounded-full text-lg font-semibold shadow-lg transition duration-300 transform hover:scale-105 animate-fade-in-up delay-400">
                Support Our Green Mission
            </a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto">
            <h3 class="text-4xl font-bold text-center text-emerald-700 mb-12">About 'A Social Unique Thought'</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="text-lg leading-relaxed space-y-6">
                    <p>
                        Founded by Akshay Kumar in Muzaffarnagar, 'A Social Unique Thought' is a dedicated social group committed to enhancing the natural beauty and ecological balance of our localities. We believe that a greener environment contributes to healthier communities and a better future for everyone.
                    </p>
                    <p>
                        Our core activities revolve around planting grass in public spaces, nurturing existing trees, and actively promoting greenery wherever possible. We are passionate about hands-on work and regularly organize planting drives and maintenance efforts.
                    </p>
                    <p>
                        Beyond our direct actions, we actively engage with the community, appreciating and encouraging individuals, families, and businesses to plant trees near their homes and workplaces. We aim to foster a collective sense of responsibility towards our environment.
                    </p>
                </div>
                <div class="relative rounded-xl overflow-hidden shadow-xl">
                    <img src="https://placehold.co/600x400/34d399/ffffff?text=Community+Planting" alt="Community Planting" class="w-full h-auto object-cover">
                    <div class="absolute inset-0 bg-gradient-to-t from-emerald-700 to-transparent opacity-50"></div>
                    <p class="absolute bottom-4 left-4 text-white text-sm md:text-base font-semibold">Our community, growing together.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Our Impact/Mission Section -->
    <section class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Our Mission & Impact</h3>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌳" alt="Tree Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Planting & Nurturing</h4>
                    <p class="text-gray-700">We actively plant new trees and grass, and ensure existing greenery is well-maintained, contributing to local biodiversity.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🤝" alt="Community Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Community Engagement</h4>
                    <p class="text-gray-700">We inspire and educate residents and businesses to participate in making our surroundings greener.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌍" alt="Earth Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Environmental Awareness</h4>
                    <p class="text-gray-700">Through our efforts, we aim to raise awareness about the critical importance of environmental conservation.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Donate Section -->
    <section id="donate" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Support Our Green Initiatives</h3>
            <p class="text-lg text-gray-700 mb-10">Your contribution, no matter how big or small, helps us continue our vital work.</p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                <!-- Donate Money -->
                <div class="bg-emerald-50 p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=💰" alt="Money Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Donate Money</h4>
                    <p class="text-gray-700 mb-6">
                        Financial contributions help us purchase saplings, gardening tools, protective gear, and support our awareness campaigns.
                    </p>
                    <p class="text-gray-600 text-sm mb-4">
                        Please contact us directly for bank transfer details or online payment options.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact for Money Donation
                    </button>
                </div>

                <!-- Donate Plants -->
                <div class="bg-emerald-50 p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌿" alt="Plant Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Donate Plants</h4>
                    <p class="text-gray-700 mb-6">
                        We welcome healthy saplings and seeds of local, indigenous trees and plants suitable for our climate.
                    </p>
                    <p class="text-gray-600 text-sm mb-4">
                        Please reach out to us to coordinate plant donations and ensure they meet our requirements.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact for Plant Donation
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Join Us Section -->
    <section id="join" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Join Our Green Movement!</h3>
            <p class="text-lg text-gray-700 mb-10">
                Become a part of 'A Social Unique Thought' and contribute your time and passion to a greener Muzaffarnagar.
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                <div class="bg-white p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🤝" alt="Volunteer Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Volunteer with Us</h4>
                    <p class="text-gray-700 mb-6">
                        Join our planting drives, help with plant care, or assist in community awareness programs. No prior experience needed, just enthusiasm!
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Become a Volunteer
                    </button>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=📢" alt="Spread Word Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Spread the Word</h4>
                    <p class="text-gray-700 mb-6">
                        Even if you can't volunteer physically, you can help by sharing our mission with your friends, family, and colleagues.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact to Collaborate
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Green Thumb Assistant Section (New LLM Feature) -->
    <section id="green-thumb-assistant" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-4xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">✨ Green Thumb Assistant ✨</h3>
            <p class="text-lg text-gray-700 mb-8">
                Need advice on how to care for your plants? Our AI assistant can provide quick tips!
            </p>
            <div class="flex flex-col items-center space-y-6">
                <input type="text" id="plant-name-input" placeholder="e.g., Rose, Basil, Ficus"
                       class="w-full md:w-2/3 p-4 border border-emerald-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500 text-lg">
                <button id="get-tips-button"
                        class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105 flex items-center justify-center space-x-2">
                    <span>Get Plant Care Tips</span>
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                </button>
                <div id="loading-indicator" class="hidden text-emerald-600 font-semibold mt-4">
                    <div class="animate-spin inline-block w-6 h-6 border-4 border-emerald-500 border-t-transparent rounded-full"></div>
                    <span class="ml-2">Generating tips...</span>
                </div>
                <div id="plant-tips-output" class="mt-8 p-6 bg-emerald-50 border border-emerald-200 rounded-xl text-left text-gray-800 leading-relaxed w-full md:w-2/3 min-h-[150px] overflow-auto shadow-inner">
                    Enter a plant name above and click "Get Plant Care Tips" to see advice here.
                </div>
            </div>
        </div>
    </section>


    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-4xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Get in Touch</h3>
            <p class="text-lg text-gray-700 mb-8">
                We'd love to hear from you! Whether you have questions, want to donate, or wish to join our team, feel free to reach out.
            </p>
            <div class="flex flex-col md:flex-row justify-center items-center space-y-6 md:space-y-0 md:space-x-8">
                <div class="flex items-center space-x-4">
                    <img src="https://placehold.co/40x40/10b981/ffffff?text=📞" alt="Phone Icon" class="rounded-full">
                    <span class="text-xl font-medium text-gray-700">+91 98765 43210</span> <!-- Placeholder number -->
                </div>
                <div class="flex items-center space-x-4">
                    <img src="https://placehold.co/40x40/10b981/ffffff?text=📧" alt="Email Icon" class="rounded-full">
                    <a href="mailto:info@asocialuniquethought.org" class="text-xl font-medium text-gray-700 hover:text-emerald-600 transition duration-300">info@asocialuniquethought.org</a> <!-- Placeholder email -->
                </div>
            </div>
            <p class="text-gray-600 text-sm mt-8">
                (Please note: The phone number and email above are placeholders. Replace them with your actual contact details.)
            </p>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-emerald-800 text-white py-8 px-6 md:px-12 lg:px-24 mt-8 rounded-t-xl">
        <div class="max-w-6xl mx-auto text-center md:flex md:justify-between md:items-center">
            <p class="text-sm mb-4 md:mb-0">&copy; 2025 A Social Unique Thought. All rights reserved.</p>
            <div class="flex justify-center space-x-6">
                <!-- Placeholder Social Media Links -->
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=F" alt="Facebook" class="rounded-full">
                </a>
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=X" alt="Twitter" class="rounded-full">
                </a>
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=I" alt="Instagram" class="rounded-full">
                </a>
            </div>
        </div>
    </footer>

    <!-- Custom Modal for Messages -->
    <div id="messageModal" class="modal">
        <div class="modal-content">
            <span class="close-button" id="closeMessageModal">&times;</span>
            <p id="modalMessage" class="text-lg text-gray-700"></p>
        </div>
    </div>


    <script>
        // Function to show custom modal messages
        function showMessageModal(message) {
            const modal = document.getElementById('messageModal');
            const modalMessage = document.getElementById('modalMessage');
            modalMessage.textContent = message;
            modal.style.display = 'flex'; // Use flex to center content
        }

        // Close modal when close button is clicked
        document.getElementById('closeMessageModal').addEventListener('click', function() {
            document.getElementById('messageModal').style.display = 'none';
        });

        // Close modal when clicking outside of the modal content
        window.addEventListener('click', function(event) {
            const modal = document.getElementById('messageModal');
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle functionality
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        const closeMobileMenuButton = document.getElementById('close-mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.remove('hidden');
        });

        closeMobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
        });

        // Close mobile menu when a link is clicked inside it
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Gemini API Integration for Plant Care Tips
        const getTipsButton = document.getElementById('get-tips-button');
        const plantNameInput = document.getElementById('plant-name-input');
        const plantTipsOutput = document.getElementById('plant-tips-output');
        const loadingIndicator = document.getElementById('loading-indicator');

        getTipsButton.addEventListener('click', async () => {
            const plantName = plantNameInput.value.trim();
            if (!plantName) {
                showMessageModal("Please enter a plant name to get tips.");
                return;
            }

            plantTipsOutput.innerHTML = ''; // Clear previous output
            loadingIndicator.classList.remove('hidden'); // Show loading indicator

            try {
                let chatHistory = [];
                const prompt = `Provide concise and helpful care tips for the plant: "${plantName}". Include details on sunlight, watering, soil, and common issues. Format the response as a clear, easy-to-read list or short paragraphs.`;
                chatHistory.push({ role: "user", parts: [{ text: prompt }] });
                const payload = { contents: chatHistory };
                const apiKey = ""; // Canvas will automatically provide the API key
                const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;

                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (!response.ok) {
                    const errorData = await response.json();
                    console.error('API Error:', errorData);
                    throw new Error(`API request failed with status ${response.status}: ${errorData.error.message || 'Unknown error'}`);
                }

                const result = await response.json();

                if (result.candidates && result.candidates.length > 0 &&
                    result.candidates[0].content && result.candidates[0].content.parts &&
                    result.candidates[0].content.parts.length > 0) {
                    const text = result.candidates[0].content.parts[0].text;
                    plantTipsOutput.innerHTML = text.replace(/\n/g, '<br>'); // Display the response, convert newlines to <br> for HTML
                } else {
                    plantTipsOutput.textContent = "Could not generate tips. Please try a different plant name.";
                    console.warn("Unexpected API response structure:", result);
                }
            } catch (error) {
                console.error("Error fetching plant care tips:", error);
                plantTipsOutput.textContent = "Failed to fetch plant care tips. Please try again later.";
                showMessageModal("An error occurred while getting plant tips. Please check the console for details.");
            } finally {
                loadingIndicator.classList.add('hidden'); // Hide loading indicator
            }
        });
    </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A Social Unique Thought - Spreading Greenery</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts - Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0fdf4; /* Light green background */
        }
        /* Custom scrollbar for a nicer look */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #e0ffe0;
        }
        ::-webkit-scrollbar-thumb {
            background: #34d399; /* Emerald 400 */
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #10b981; /* Emerald 500 */
        }
        /* Keyframes for fade-in-up animation */
        @keyframes fade-in-up {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .animate-fade-in-up {
            animation: fade-in-up 0.6s ease-out forwards;
        }
        .animate-fade-in-up.delay-200 {
            animation-delay: 0.2s;
        }
        .animate-fade-in-up.delay-400 {
            animation-delay: 0.4s;
        }

        /* Custom modal styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.4); /* Black w/ opacity */
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: #fefefe;
            margin: auto;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 80%;
            max-width: 500px;
            text-align: center;
            position: relative;
        }

        .close-button {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            position: absolute;
            top: 10px;
            right: 15px;
        }

        .close-button:hover,
        .close-button:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header Section -->
    <header class="bg-white shadow-md py-4 px-6 md:px-12 lg:px-24 flex justify-between items-center rounded-b-xl">
        <div class="flex items-center space-x-3">
            <img src="https://placehold.co/40x40/10b981/ffffff?text=🌱" alt="Leaf Logo" class="rounded-full">
            <h1 class="text-2xl font-bold text-emerald-700">A Social Unique Thought</h1>
        </div>
        <nav class="hidden md:flex space-x-8">
            <a href="#home" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Home</a>
            <a href="#about" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">About Us</a>
            <a href="#donate" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Donate</a>
            <a href="#join" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Join Us</a>
            <a href="#green-thumb-assistant" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Green Assistant</a>
            <a href="#contact" class="text-gray-600 hover:text-emerald-600 font-medium transition duration-300">Contact</a>
        </nav>
        <!-- Mobile Menu Button (Hamburger) -->
        <button id="mobile-menu-button" class="md:hidden text-gray-600 hover:text-emerald-600 focus:outline-none">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
            </svg>
        </button>
    </header>

    <!-- Mobile Menu Overlay -->
    <div id="mobile-menu" class="hidden md:hidden fixed inset-0 bg-white bg-opacity-95 z-50 flex flex-col items-center justify-center space-y-6">
        <button id="close-mobile-menu" class="absolute top-4 right-4 text-gray-600 hover:text-emerald-600 focus:outline-none">
            <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
            </svg>
        </button>
        <a href="#home" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Home</a>
        <a href="#about" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">About Us</a>
        <a href="#donate" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Donate</a>
        <a href="#join" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Join Us</a>
        <a href="#green-thumb-assistant" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Green Assistant</a>
        <a href="#contact" class="text-2xl text-gray-800 hover:text-emerald-600 font-medium transition duration-300" onclick="document.getElementById('mobile-menu').classList.add('hidden')">Contact</a>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-r from-emerald-500 to-green-600 text-white py-20 md:py-32 text-center overflow-hidden rounded-b-xl mx-4 mt-4 shadow-lg">
        <div class="absolute inset-0 opacity-20">
            <!-- Background pattern for visual appeal -->
            <svg class="w-full h-full" viewBox="0 0 100 100" preserveAspectRatio="xMidYMid slice">
                <defs>
                    <pattern id="pattern-circles" x="0" y="0" width="10" height="10" patternUnits="userSpaceOnUse">
                        <circle cx="5" cy="5" r="1" fill="rgba(255,255,255,0.1)"></circle>
                    </pattern>
                </defs>
                <rect x="0" y="0" width="100%" height="100%" fill="url(#pattern-circles)"></rect>
            </svg>
        </div>
        <div class="relative z-10 max-w-4xl mx-auto px-6">
            <h2 class="text-4xl md:text-6xl font-extrabold leading-tight mb-6 animate-fade-in-up">
                Nurturing Nature, Growing Communities
            </h2>
            <p class="text-lg md:text-xl mb-10 opacity-90 animate-fade-in-up delay-200">
                Join 'A Social Unique Thought' in our mission to make Muzaffarnagar greener and healthier.
            </p>
            <a href="#donate" class="bg-white text-emerald-700 hover:bg-emerald-100 px-8 py-4 rounded-full text-lg font-semibold shadow-lg transition duration-300 transform hover:scale-105 animate-fade-in-up delay-400">
                Support Our Green Mission
            </a>
        </div>
    </section>

    <!-- About Us Section -->
    <section id="about" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto">
            <h3 class="text-4xl font-bold text-center text-emerald-700 mb-12">About 'A Social Unique Thought'</h3>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
                <div class="text-lg leading-relaxed space-y-6">
                    <p>
                        Founded by Akshay Kumar in Muzaffarnagar, 'A Social Unique Thought' is a dedicated social group committed to enhancing the natural beauty and ecological balance of our localities. We believe that a greener environment contributes to healthier communities and a better future for everyone.
                    </p>
                    <p>
                        Our core activities revolve around planting grass in public spaces, nurturing existing trees, and actively promoting greenery wherever possible. We are passionate about hands-on work and regularly organize planting drives and maintenance efforts.
                    </p>
                    <p>
                        Beyond our direct actions, we actively engage with the community, appreciating and encouraging individuals, families, and businesses to plant trees near their homes and workplaces. We aim to foster a collective sense of responsibility towards our environment.
                    </p>
                </div>
                <div class="relative rounded-xl overflow-hidden shadow-xl">
                    <img src="https://placehold.co/600x400/34d399/ffffff?text=Community+Planting" alt="Community Planting" class="w-full h-auto object-cover">
                    <div class="absolute inset-0 bg-gradient-to-t from-emerald-700 to-transparent opacity-50"></div>
                    <p class="absolute bottom-4 left-4 text-white text-sm md:text-base font-semibold">Our community, growing together.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Our Impact/Mission Section -->
    <section class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Our Mission & Impact</h3>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌳" alt="Tree Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Planting & Nurturing</h4>
                    <p class="text-gray-700">We actively plant new trees and grass, and ensure existing greenery is well-maintained, contributing to local biodiversity.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🤝" alt="Community Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Community Engagement</h4>
                    <p class="text-gray-700">We inspire and educate residents and businesses to participate in making our surroundings greener.</p>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌍" alt="Earth Icon" class="mx-auto mb-6">
                    <h4 class="text-2xl font-semibold text-emerald-600 mb-4">Environmental Awareness</h4>
                    <p class="text-gray-700">Through our efforts, we aim to raise awareness about the critical importance of environmental conservation.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Donate Section -->
    <section id="donate" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Support Our Green Initiatives</h3>
            <p class="text-lg text-gray-700 mb-10">Your contribution, no matter how big or small, helps us continue our vital work.</p>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                <!-- Donate Money -->
                <div class="bg-emerald-50 p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=💰" alt="Money Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Donate Money</h4>
                    <p class="text-gray-700 mb-6">
                        Financial contributions help us purchase saplings, gardening tools, protective gear, and support our awareness campaigns.
                    </p>
                    <p class="text-gray-600 text-sm mb-4">
                        Please contact us directly for bank transfer details or online payment options.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact for Money Donation
                    </button>
                </div>

                <!-- Donate Plants -->
                <div class="bg-emerald-50 p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🌿" alt="Plant Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Donate Plants</h4>
                    <p class="text-gray-700 mb-6">
                        We welcome healthy saplings and seeds of local, indigenous trees and plants suitable for our climate.
                    </p>
                    <p class="text-gray-600 text-sm mb-4">
                        Please reach out to us to coordinate plant donations and ensure they meet our requirements.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact for Plant Donation
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Join Us Section -->
    <section id="join" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-6xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Join Our Green Movement!</h3>
            <p class="text-lg text-gray-700 mb-10">
                Become a part of 'A Social Unique Thought' and contribute your time and passion to a greener Muzaffarnagar.
            </p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
                <div class="bg-white p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=🤝" alt="Volunteer Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Volunteer with Us</h4>
                    <p class="text-gray-700 mb-6">
                        Join our planting drives, help with plant care, or assist in community awareness programs. No prior experience needed, just enthusiasm!
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Become a Volunteer
                    </button>
                </div>
                <div class="bg-white p-8 rounded-xl shadow-md border border-emerald-200">
                    <img src="https://placehold.co/80x80/10b981/ffffff?text=📢" alt="Spread Word Icon" class="mx-auto mb-6">
                    <h4 class="text-3xl font-semibold text-emerald-600 mb-4">Spread the Word</h4>
                    <p class="text-gray-700 mb-6">
                        Even if you can't volunteer physically, you can help by sharing our mission with your friends, family, and colleagues.
                    </p>
                    <button class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105"
                            onclick="document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });">
                        Contact to Collaborate
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- Green Thumb Assistant Section (New LLM Feature) -->
    <section id="green-thumb-assistant" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-white rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-4xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">✨ Green Thumb Assistant ✨</h3>
            <p class="text-lg text-gray-700 mb-8">
                Need advice on how to care for your plants? Our AI assistant can provide quick tips!
            </p>
            <div class="flex flex-col items-center space-y-6">
                <input type="text" id="plant-name-input" placeholder="e.g., Rose, Basil, Ficus"
                       class="w-full md:w-2/3 p-4 border border-emerald-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500 text-lg">
                <button id="get-tips-button"
                        class="bg-emerald-600 text-white hover:bg-emerald-700 px-8 py-4 rounded-full text-lg font-semibold shadow-md transition duration-300 transform hover:scale-105 flex items-center justify-center space-x-2">
                    <span>Get Plant Care Tips</span>
                    <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>
                </button>
                <div id="loading-indicator" class="hidden text-emerald-600 font-semibold mt-4">
                    <div class="animate-spin inline-block w-6 h-6 border-4 border-emerald-500 border-t-transparent rounded-full"></div>
                    <span class="ml-2">Generating tips...</span>
                </div>
                <div id="plant-tips-output" class="mt-8 p-6 bg-emerald-50 border border-emerald-200 rounded-xl text-left text-gray-800 leading-relaxed w-full md:w-2/3 min-h-[150px] overflow-auto shadow-inner">
                    Enter a plant name above and click "Get Plant Care Tips" to see advice here.
                </div>
            </div>
        </div>
    </section>


    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24 px-6 md:px-12 lg:px-24 bg-emerald-50 rounded-xl mx-4 mt-8 shadow-lg">
        <div class="max-w-4xl mx-auto text-center">
            <h3 class="text-4xl font-bold text-emerald-700 mb-12">Get in Touch</h3>
            <p class="text-lg text-gray-700 mb-8">
                We'd love to hear from you! Whether you have questions, want to donate, or wish to join our team, feel free to reach out.
            </p>
            <div class="flex flex-col md:flex-row justify-center items-center space-y-6 md:space-y-0 md:space-x-8">
                <div class="flex items-center space-x-4">
                    <img src="https://placehold.co/40x40/10b981/ffffff?text=📞" alt="Phone Icon" class="rounded-full">
                    <span class="text-xl font-medium text-gray-700">+91 98765 43210</span> <!-- Placeholder number -->
                </div>
                <div class="flex items-center space-x-4">
                    <img src="https://placehold.co/40x40/10b981/ffffff?text=📧" alt="Email Icon" class="rounded-full">
                    <a href="mailto:info@asocialuniquethought.org" class="text-xl font-medium text-gray-700 hover:text-emerald-600 transition duration-300">info@asocialuniquethought.org</a> <!-- Placeholder email -->
                </div>
            </div>
            <p class="text-gray-600 text-sm mt-8">
                (Please note: The phone number and email above are placeholders. Replace them with your actual contact details.)
            </p>
        </div>
    </section>

    <!-- Footer Section -->
    <footer class="bg-emerald-800 text-white py-8 px-6 md:px-12 lg:px-24 mt-8 rounded-t-xl">
        <div class="max-w-6xl mx-auto text-center md:flex md:justify-between md:items-center">
            <p class="text-sm mb-4 md:mb-0">&copy; 2025 A Social Unique Thought. All rights reserved.</p>
            <div class="flex justify-center space-x-6">
                <!-- Placeholder Social Media Links -->
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=F" alt="Facebook" class="rounded-full">
                </a>
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=X" alt="Twitter" class="rounded-full">
                </a>
                <a href="#" class="text-white hover:text-emerald-300 transition duration-300">
                    <img src="https://placehold.co/24x24/10b981/ffffff?text=I" alt="Instagram" class="rounded-full">
                </a>
            </div>
        </div>
    </footer>

    <!-- Custom Modal for Messages -->
    <div id="messageModal" class="modal">
        <div class="modal-content">
            <span class="close-button" id="closeMessageModal">&times;</span>
            <p id="modalMessage" class="text-lg text-gray-700"></p>
        </div>
    </div>


    <script>
        // Function to show custom modal messages
        function showMessageModal(message) {
            const modal = document.getElementById('messageModal');
            const modalMessage = document.getElementById('modalMessage');
            modalMessage.textContent = message;
            modal.style.display = 'flex'; // Use flex to center content
        }

        // Close modal when close button is clicked
        document.getElementById('closeMessageModal').addEventListener('click', function() {
            document.getElementById('messageModal').style.display = 'none';
        });

        // Close modal when clicking outside of the modal content
        window.addEventListener('click', function(event) {
            const modal = document.getElementById('messageModal');
            if (event.target == modal) {
                modal.style.display = 'none';
            }
        });

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle functionality
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        const closeMobileMenuButton = document.getElementById('close-mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.remove('hidden');
        });

        closeMobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
        });

        // Close mobile menu when a link is clicked inside it
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Gemini API Integration for Plant Care Tips
        const getTipsButton = document.getElementById('get-tips-button');
        const plantNameInput = document.getElementById('plant-name-input');
        const plantTipsOutput = document.getElementById('plant-tips-output');
        const loadingIndicator = document.getElementById('loading-indicator');

        getTipsButton.addEventListener('click', async () => {
            const plantName = plantNameInput.value.trim();
            if (!plantName) {
                showMessageModal("Please enter a plant name to get tips.");
                return;
            }

            plantTipsOutput.innerHTML = ''; // Clear previous output
            loadingIndicator.classList.remove('hidden'); // Show loading indicator

            try {
                let chatHistory = [];
                const prompt = `Provide concise and helpful care tips for the plant: "${plantName}". Include details on sunlight, watering, soil, and common issues. Format the response as a clear, easy-to-read list or short paragraphs.`;
                chatHistory.push({ role: "user", parts: [{ text: prompt }] });
                const payload = { contents: chatHistory };
                const apiKey = ""; // Canvas will automatically provide the API key
                const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;

                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (!response.ok) {
                    const errorData = await response.json();
                    console.error('API Error:', errorData);
                    throw new Error(`API request failed with status ${response.status}: ${errorData.error.message || 'Unknown error'}`);
                }

                const result = await response.json();

                if (result.candidates && result.candidates.length > 0 &&
                    result.candidates[0].content && result.candidates[0].content.parts &&
                    result.candidates[0].content.parts.length > 0) {
                    const text = result.candidates[0].content.parts[0].text;
                    plantTipsOutput.innerHTML = text.replace(/\n/g, '<br>'); // Display the response, convert newlines to <br> for HTML
                } else {
                    plantTipsOutput.textContent = "Could not generate tips. Please try a different plant name.";
                    console.warn("Unexpected API response structure:", result);
                }
            } catch (error) {
                console.error("Error fetching plant care tips:", error);
                plantTipsOutput.textContent = "Failed to fetch plant care tips. Please try again later.";
                showMessageModal("An error occurred while getting plant tips. Please check the console for details.");
            } finally {
                loadingIndicator.classList.add('hidden'); // Hide loading indicator
            }
        });
    </script>
</body>
</html>
