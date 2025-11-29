# Delhi-Explorer
 The website Delhi Explorer helps tourists discover the best food spots, hidden gems, and must-visit places across Delhi. It offers curated guides, budget-friendly recommendations, and easy navigation to make exploring the city simple, enjoyable, and hassle-free.
#codes
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incredible Delhi - Discover the Capital</title>
    <!-- Load Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Use Inter font -->
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f7f7f7;
            color: #1a1a1a;
        }
        .nav-link.active {
            border-bottom: 2px solid #D97706; /* Amber-600 */
            color: #D97706;
        }
        .card-shadow {
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .main-container {
            min-height: calc(100vh - 80px); /* Adjust for header height */
        }
        /* Smooth fade in animation */
        .fade-in {
            animation: fadeIn 0.5s ease-in;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        /* Custom Checkbox Style */
        .pref-checkbox:checked + div {
            background-color: #D97706;
            color: white;
            border-color: #D97706;
        }
    </style>
</head>
<body>

    <!-- Navigation Header -->
    <header class="sticky top-0 z-50 bg-white shadow-lg">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <h1 class="text-2xl font-extrabold text-[#991b1b] tracking-wider mb-4 md:mb-0 cursor-pointer" onclick="showSection('home')">
                    DELHI <span class="text-[#D97706]">EXPLORER</span>
                </h1>
                <!-- Mobile-friendly overflow scrolling for nav -->
                <div class="flex overflow-x-auto w-full md:w-auto space-x-6 text-sm md:text-lg font-medium pb-2 md:pb-0 whitespace-nowrap">
                    <a href="#home" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="home">Home</a>
                    <a href="#attractions" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="attractions">Attractions</a>
                    <a href="#culture" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="culture">Culture</a>
                    <a href="#food" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="food">Food Finder</a>
                    <a href="#planner" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="planner">Trip Planner</a>
                    <a href="#profile" class="nav-link p-2 transition duration-150 ease-in-out hover:text-[#D97706]" data-section="profile">Profile</a>
                </div>
            </div>
        </nav>
    </header>

    <!-- Main Content Area -->
    <main class="main-container max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">

        <!-- 1. HOME Section -->
        <section id="home" class="content-section fade-in">
            <div class="relative bg-gray-900 rounded-2xl overflow-hidden shadow-2xl mb-12">
                <!-- Hero Image Placeholder -->
                <img src="https://placehold.co/1200x500/991b1b/ffffff?text=Welcome+to+Dilwalon+Ki+Dilli" alt="Delhi Panorama" class="w-full h-64 md:h-96 object-cover opacity-60">
                <div class="absolute inset-0 flex flex-col justify-center items-center text-center px-6">
                    <h2 class="text-4xl md:text-6xl font-bold text-white mb-4 drop-shadow-lg">The Heart of India</h2>
                    <p class="text-xl md:text-2xl text-gray-100 max-w-3xl drop-shadow-md">
                        Where ancient history breathes through modern streets. Experience the chaos, the calm, and the culture of a city that has lived a thousand lives.
                    </p>
                    <button onclick="document.querySelector('[data-section=attractions]').click()" class="mt-8 bg-[#D97706] hover:bg-[#B45309] text-white font-bold py-3 px-8 rounded-full transition duration-300 transform hover:scale-105 shadow-lg">
                        Start Exploring
                    </button>
                </div>
            </div>

            <div class="grid md:grid-cols-2 gap-8 mb-12">
                <div class="bg-white p-8 rounded-xl card-shadow border-l-4 border-[#991b1b]">
                    <h3 class="text-2xl font-bold text-[#991b1b] mb-3">A City of Contrasts</h3>
                    <p class="text-gray-600 leading-relaxed">
                        Delhi is a unique blend of two cities: **Old Delhi**, the historic capital of the Mughals with its labyrinthine alleys, bustling bazaars, and grand mosques; and **New Delhi**, the imperial city built by the British with wide tree-lined avenues and colonial architecture. It is the political and cultural soul of the nation.
                    </p>
                </div>
                <div class="bg-white p-8 rounded-xl card-shadow border-l-4 border-[#D97706]">
                    <h3 class="text-2xl font-bold text-[#D97706] mb-3">Why Visit?</h3>
                    <p class="text-gray-600 leading-relaxed">
                        From the world's tallest brick minaret to Asia's largest spice market, Delhi offers sensory overload in the best way possible. Whether you are a history buff, a foodie, or a shopaholic, the capital welcomes you with open arms. As the saying goes, *"Dilli hai dilwalon ki"* (Delhi belongs to the large-hearted).
                    </p>
                </div>
            </div>
        </section>

        <!-- 2. Attractions Section -->
        <section id="attractions" class="content-section hidden fade-in">
            <h2 class="text-4xl font-bold mb-8 text-[#991b1b] border-b-4 border-[#D97706] pb-2 inline-block">Historic & Cultural Wonders</h2>
            <p class="text-gray-600 mb-10 text-xl">Explore the monuments that tell the story of Delhi, spanning centuries from the Mughals to modern India.</p>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Old Delhi Highlights -->
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/a52a2a/ffffff?text=Red+Fort" alt="Red Fort" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Red Fort (Lal Qila)</h3>
                    <p class="text-gray-700">A massive 17th-century fort built by Shah Jahan, symbolizing Mughal grandeur and Indian independence.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/d4af37/ffffff?text=Jama+Masjid" alt="Jama Masjid" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Jama Masjid</h3>
                    <p class="text-gray-700">One of the largest mosques in India, an architectural masterpiece located in the heart of Old Delhi.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/8b4513/ffffff?text=Qutub+Minar" alt="Qutub Minar" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Qutub Minar Complex</h3>
                    <p class="text-gray-700">A UNESCO World Heritage Site featuring the tallest brick minaret in the world and the ancient Iron Pillar.</p>
                </div>

                <!-- New Delhi Highlights -->
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/bc8f8f/ffffff?text=Humayun's+Tomb" alt="Humayun's Tomb" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Humayun's Tomb</h3>
                    <p class="text-gray-700">The first garden-tomb on the Indian subcontinent, and the inspiration for the Taj Mahal.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/708090/ffffff?text=India+Gate" alt="India Gate" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">India Gate</h3>
                    <p class="text-gray-700">A majestic war memorial located on the Rajpath, best visited in the evening when it's illuminated.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/4682b4/ffffff?text=Lotus+Temple" alt="Lotus Temple" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Lotus Temple</h3>
                    <p class="text-gray-700">A stunning Baha'i House of Worship, famous for its distinctive, flower-like architecture.</p>
                </div>

                <!-- Previous Additions -->
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/FF8C00/ffffff?text=Akshardham" alt="Akshardham Temple" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Akshardham Temple</h3>
                    <p class="text-gray-700">The world's largest comprehensive Hindu temple, showcasing millennia of traditional Indian culture.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/556B2F/ffffff?text=Agrasen+Ki+Baoli" alt="Agrasen Ki Baoli" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Agrasen Ki Baoli</h3>
                    <p class="text-gray-700">A protected archaeological site and an ancient stepwell (baoli) with 108 steps, famous for its haunting beauty.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/FFD700/ffffff?text=Bangla+Sahib" alt="Gurudwara Bangla Sahib" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Gurudwara Bangla Sahib</h3>
                    <p class="text-gray-700">One of the most prominent Sikh gurudwaras, known for its association with the eighth Sikh Guru and the holy pond.</p>
                </div>

                <!-- NEW 5 MONUMENTS -->
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/008080/ffffff?text=National+Rail+Museum" alt="National Rail Museum" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">National Rail Museum</h3>
                    <p class="text-gray-700">A fascinating museum in Chanakyapuri celebrating the history of rail transport in India with vintage locomotives.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/C71585/ffffff?text=Dilli+Haat" alt="Dilli Haat INA" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Dilli Haat (INA)</h3>
                    <p class="text-gray-700">An open-air food plaza and craft bazaar simulating a traditional village market. Great for shopping and regional food.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/2F4F4F/ffffff?text=Nizamuddin+Dargah" alt="Nizamuddin Dargah" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Nizamuddin Dargah</h3>
                    <p class="text-gray-700">The mausoleum of Sufi saint Nizamuddin Auliya. Famous for its evening Qawwali sessions filled with spiritual energy.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/800000/ffffff?text=National+Museum" alt="National Museum" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">National Museum</h3>
                    <p class="text-gray-700">One of the largest museums in India, holding over 200,000 works of art, covering 5,000 years of Indian heritage.</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow hover:shadow-xl transition duration-300 group">
                    <div class="overflow-hidden rounded-lg mb-4 h-48">
                        <img src="https://placehold.co/600x400/228B22/ffffff?text=Waste+to+Wonder" alt="Waste to Wonder Park" class="w-full h-full object-cover transform group-hover:scale-110 transition duration-500">
                    </div>
                    <h3 class="text-2xl font-semibold text-[#991b1b] mb-2">Waste to Wonder Park</h3>
                    <p class="text-gray-700">A unique theme park featuring replicas of the Seven Wonders of the World created entirely from industrial waste.</p>
                </div>
            </div>
        </section>

        <!-- 3. CULTURE Section -->
        <section id="culture" class="content-section hidden fade-in">
            <h2 class="text-4xl font-bold mb-8 text-[#991b1b] border-b-4 border-[#D97706] pb-2 inline-block">The Soul of Delhi</h2>
            <p class="text-gray-600 mb-10 text-xl">Delhi's culture is a mosaic of history, art, and festivities. It is where the old world charm meets the contemporary pace.</p>

            <div class="flex flex-col lg:flex-row gap-12">
                <div class="lg:w-1/2">
                    <img src="https://placehold.co/800x600/D97706/ffffff?text=Festivals+of+Delhi" alt="Culture of Delhi" class="rounded-xl shadow-lg w-full h-auto object-cover mb-6">
                    
                    <div class="bg-gray-900 text-white p-6 rounded-xl shadow-lg">
                        <h4 class="text-xl font-bold text-[#D97706] mb-2">Language & Literature</h4>
                        <p class="text-sm leading-relaxed">
                            Delhi has been the muse for poets like Mirza Ghalib and Amir Khusro. The city speaks a mix of Hindi, Punjabi, Urdu, and English. You can still find traditional <span class="italic text-gray-300">Mushairas</span> (poetic symposiums) in Old Delhi, keeping the legacy of Urdu poetry alive.
                        </p>
                    </div>
                </div>
                <div class="lg:w-1/2 space-y-6">
                    <div class="bg-white p-6 rounded-lg card-shadow border-l-4 border-[#991b1b]">
                        <h3 class="text-2xl font-bold text-[#991b1b] mb-2">Ganga-Jamuni Tehzeeb</h3>
                        <p class="text-gray-700">
                            This phrase describes the syncretic fusion of Hindu and Muslim elements in the culture of central North India. In Delhi, this is visible in the shared celebrations of festivals like Diwali, Eid, and Holi, and the harmonious existence of temples, mosques, and gurudwaras side by side.
                        </p>
                    </div>
                    <div class="bg-white p-6 rounded-lg card-shadow border-l-4 border-[#D97706]">
                        <h3 class="text-2xl font-bold text-[#991b1b] mb-2">Music & Performing Arts</h3>
                        <p class="text-gray-700">
                            Delhi is the cultural capital for performing arts. The **Mandi House** circle is famous for its theaters like Kamani and Sri Ram Centre. The annual **Qutub Festival** sets classical music against the backdrop of the Qutub Minar, while Nizamuddin Dargah offers soul-stirring Qawwalis every Thursday.
                        </p>
                    </div>
                    <div class="bg-white p-6 rounded-lg card-shadow border-l-4 border-[#991b1b]">
                        <h3 class="text-2xl font-bold text-[#991b1b] mb-2">Shopping & Bazars</h3>
                        <p class="text-gray-700">
                            Shopping is a ritual here. **Chandni Chowk** offers wedding gear and spices, **Sarojini Nagar** is famous for export surplus fashion, **Dilli Haat** showcases rural handicrafts, and **Khan Market** offers high-end retail. Every market has its own unique cultural vibe.
                        </p>
                    </div>
                    <div class="bg-white p-6 rounded-lg card-shadow border-l-4 border-[#D97706]">
                        <h3 class="text-2xl font-bold text-[#991b1b] mb-2">Modern Art Scene</h3>
                        <p class="text-gray-700">
                            The **National Gallery of Modern Art (NGMA)** and the **Lodhi Art District**—India's first open-air art district with massive murals on building facades—showcase Delhi's evolving contemporary identity.
                        </p>
                    </div>
                </div>
            </div>
        </section>

        <!-- 4. Food Finder Section -->
        <section id="food" class="content-section hidden fade-in">
            <div class="text-center mb-10">
                <h2 class="text-4xl font-bold mb-4 text-[#991b1b] border-b-4 border-[#D97706] inline-block pb-2">Delhi's Food Guide</h2>
                <p class="text-gray-600 text-xl max-w-2xl mx-auto">
                    Confused about what to eat? Use our <strong>Food Finder</strong> below! Select a dish from our massive list of <strong>50+ iconic items</strong>, and we'll tell you exactly where to find the legendary version of it.
                </p>
            </div>

            <!-- Interactive Food Finder Tool -->
            <div class="bg-white p-8 rounded-2xl card-shadow max-w-4xl mx-auto mb-12 border border-gray-100">
                <h3 class="text-2xl font-bold text-gray-800 mb-6 flex items-center justify-center">
                    <span class="bg-[#D97706] text-white rounded-full w-8 h-8 flex items-center justify-center mr-3 text-sm">1</span>
                    What are you in the mood for?
                </h3>
                
                <div class="relative max-w-md mx-auto mb-8">
                    <select id="food-select" onchange="findBestFood()" class="block w-full pl-4 pr-10 py-4 text-lg border-2 border-gray-300 focus:outline-none focus:ring-2 focus:ring-[#991b1b] focus:border-[#991b1b] rounded-xl appearance-none bg-gray-50 cursor-pointer">
                        <option value="" disabled selected>Select a dish (50+ Options)...</option>
                        <!-- Options are populated via JS -->
                    </select>
                    <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-4 text-gray-700">
                        <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path></svg>
                    </div>
                </div>

                <!-- Result Container (UPDATED STRUCTURE) -->
                <div id="food-result" class="hidden transition-all duration-500 ease-in-out">
                    <div class="border-t-2 border-dashed border-gray-200 pt-6">
                        <div class="bg-[#fff7ed] border-l-4 border-[#D97706] p-6 rounded-r-lg shadow-sm">
                            
                            <!-- Main Dish Info -->
                            <h3 id="res-dish" class="text-3xl font-extrabold text-[#991b1b] mb-3">Dish Name</h3>
                            <p id="res-desc" class="text-gray-700 mb-6 text-lg italic">Description goes here...</p>
                            
                            <!-- Top 3 Places List -->
                            <h4 class="text-sm uppercase tracking-wide text-gray-500 font-bold mb-3">⭐ Top 3 Best Places to Try:</h4>
                            <ul id="res-places-list" class="space-y-4">
                                <!-- Dynamic Content will be injected here -->
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Static Info Cards (Secondary) -->
            <div class="grid lg:grid-cols-2 gap-10 opacity-80">
                <div class="bg-white p-6 rounded-xl card-shadow">
                    <h4 class="font-bold text-gray-700 mb-2">Street Food Hubs</h4>
                    <p class="text-sm text-gray-600">Chandni Chowk (Old Delhi), Bengali Market, Amar Colony, CR Park, and Hudson Lane (GTB Nagar).</p>
                </div>
                <div class="bg-white p-6 rounded-xl card-shadow">
                    <h4 class="font-bold text-gray-700 mb-2">Fine Dining Hubs</h4>
                    <p class="text-sm text-gray-600">Khan Market, Pandara Road, Cyber Hub (Gurgaon), and Connaught Place (Outer Circle).</p>
                </div>
            </div>
        </section>

        <!-- 5. Trip Planner Section (User Friendly Update) -->
        <section id="planner" class="content-section hidden fade-in">
            <h2 class="text-4xl font-bold mb-8 text-[#991b1b] border-b-4 border-[#D97706] pb-2 inline-block">Your Personalized Delhi Trip</h2>
            <p class="text-gray-600 mb-6 text-xl">Tell us your preferences, and we will build a perfect day-by-day blueprint for you.</p>

            <div class="grid lg:grid-cols-3 gap-8">
                <!-- Planner Column 1: Inputs -->
                <div class="lg:col-span-1 bg-white p-6 rounded-xl card-shadow overflow-y-auto">
                    <h3 class="text-2xl font-bold text-[#991b1b] mb-6">Trip Details</h3>
                    
                    <!-- Days Input -->
                    <div class="mb-6">
                        <label for="trip-days" class="block text-sm font-bold text-gray-700 mb-2">How many days?</label>
                        <input type="number" id="trip-days" min="1" max="7" value="2" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#D97706] focus:border-[#D97706] outline-none text-lg" onchange="validateDays(this)">
                        <p class="text-xs text-gray-500 mt-1">Enter between 1 and 7 days</p>
                    </div>

                    <!-- Interests Input -->
                    <div class="mb-6">
                        <label class="block text-sm font-bold text-gray-700 mb-3">What are your interests?</label>
                        <div class="grid grid-cols-1 gap-3">
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="History" checked>
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🏛️ History & Heritage</div>
                            </label>
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="Faith">
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🙏 Faith & Spirituality</div>
                            </label>
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="Food" checked>
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🥘 Food & Dining</div>
                            </label>
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="Shopping">
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🛍️ Markets & Shopping</div>
                            </label>
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="Nature">
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🌳 Parks & Nature</div>
                            </label>
                            <label class="cursor-pointer relative">
                                <input type="checkbox" class="pref-checkbox hidden" value="Museum">
                                <div class="p-3 border border-gray-300 rounded-lg text-gray-600 font-medium transition hover:bg-gray-50">🎨 Museums & Culture</div>
                            </label>
                        </div>
                    </div>

                    <button onclick="generateSmartItinerary()" class="mt-2 w-full bg-[#D97706] hover:bg-[#B45309] text-white font-bold py-3 px-4 rounded-lg transition duration-300 transform hover:scale-105 shadow-md">
                        Generate Blueprint
                    </button>
                </div>

                <!-- Planner Column 2: Generated Itinerary -->
                <div class="lg:col-span-2">
                    <div class="bg-white p-6 rounded-xl card-shadow min-h-[400px]">
                        <div id="itinerary-header" class="flex justify-between items-center border-b pb-4 mb-4">
                            <h3 class="text-2xl font-bold text-[#991b1b]">Your Blueprint</h3>
                            <span class="bg-green-100 text-green-800 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded dark:bg-green-200 dark:text-green-900">Auto-Optimized</span>
                        </div>
                        
                        <div id="itinerary-output" class="space-y-6">
                            <div class="text-gray-500 italic text-center py-10">
                                <svg class="w-16 h-16 mx-auto mb-4 text-gray-300" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01"></path></svg>
                                Set your preferences on the left and click 'Generate Blueprint' to see your custom plan!
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 6. USER PROFILE Section -->
        <section id="profile" class="content-section hidden fade-in">
            <div class="max-w-2xl mx-auto bg-white p-8 rounded-2xl card-shadow">
                <div class="text-center mb-8">
                    <div class="bg-gray-100 w-24 h-24 rounded-full flex items-center justify-center mx-auto mb-4">
                        <svg class="w-12 h-12 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
                    </div>
                    <h2 class="text-3xl font-bold text-[#991b1b]">Traveler Profile</h2>
                    <p class="text-gray-600">Save your details for personalized recommendations and booking inquiries.</p>
                </div>

                <form onsubmit="saveProfile(event)" class="space-y-6">
                    <div>
                        <label for="name" class="block text-sm font-medium text-gray-700 mb-1">Full Name</label>
                        <input type="text" id="name" name="name" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#D97706] focus:border-[#D97706] outline-none transition" placeholder="Enter your name">
                    </div>
                    
                    <div>
                        <label for="email" class="block text-sm font-medium text-gray-700 mb-1">Email Address</label>
                        <input type="email" id="email" name="email" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#D97706] focus:border-[#D97706] outline-none transition" placeholder="you@example.com">
                    </div>

                    <div>
                        <label for="phone" class="block text-sm font-medium text-gray-700 mb-1">Phone Number</label>
                        <input type="tel" id="phone" name="phone" class="w-full p-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-[#D97706] focus:border-[#D97706] outline-none transition" placeholder="+91 98765 43210">
                    </div>

                    <div class="flex space-x-4">
                        <button type="submit" class="w-full bg-[#991b1b] hover:bg-[#7f1d1d] text-white font-bold py-3 px-4 rounded-lg transition duration-300 shadow-md">
                            Save Profile
                        </button>
                    </div>
                    <div id="save-msg" class="text-green-600 font-medium text-center hidden">Details saved successfully!</div>
                </form>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="bg-[#991b1b] text-white py-6 mt-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p>&copy; 2025 Delhi Explorer. Designed for the Incredible Capital.</p>
        </div>
    </footer>

    <script>
        // --- Core Data: Delhi Places to Visit with ZONES ---
        const DELHIPLACES = [
            // Zone 1: Old Delhi
            { id: 'red_fort', name: 'Red Fort (Lal Qila)', type: 'History', zone: 'Old Delhi', duration: '2-3 hrs' },
            { id: 'jama_masjid', name: 'Jama Masjid', type: 'Faith', zone: 'Old Delhi', duration: '1-2 hrs' },
            { id: 'chandni_chowk', name: 'Chandni Chowk Market', type: 'Shopping', zone: 'Old Delhi', duration: '2-4 hrs' },
            { id: 'food_old_delhi', name: 'Old Delhi Street Food Hub', type: 'Food', zone: 'Old Delhi', duration: '2 hrs' },

            // Zone 2: Central / Lutyens Delhi
            { id: 'india_gate', name: 'India Gate & War Memorial', type: 'History', zone: 'Central Delhi', duration: '1 hr' },
            { id: 'rashtrapati_bhavan', name: 'Rashtrapati Bhavan', type: 'History', zone: 'Central Delhi', duration: '1-2 hrs' },
            { id: 'bangla_sahib', name: 'Gurdwara Bangla Sahib', type: 'Faith', zone: 'Central Delhi', duration: '1-2 hrs' },
            { id: 'connaught_place', name: 'Connaught Place (CP)', type: 'Shopping', zone: 'Central Delhi', duration: '2 hrs' },
            { id: 'agrasen_baoli', name: 'Agrasen Ki Baoli', type: 'History', zone: 'Central Delhi', duration: '1 hr' },
            { id: 'national_museum', name: 'National Museum', type: 'Museum', zone: 'Central Delhi', duration: '3 hrs' },
            { id: 'jantar_mantar', name: 'Jantar Mantar', type: 'History', zone: 'Central Delhi', duration: '1 hr' },
            { id: 'food_cp', name: 'CP Food Hub', type: 'Food', zone: 'Central Delhi', duration: '1.5 hrs' },
            { id: 'food_khan_market', name: 'Khan Market Cafes', type: 'Food', zone: 'Central Delhi', duration: '2 hrs' },

            // Zone 3: South Delhi Heritage (Mehrauli/Hauz Khas)
            { id: 'qutub_minar', name: 'Qutub Minar Complex', type: 'History', zone: 'South Heritage', duration: '2 hrs' },
            { id: 'hauz_khas', name: 'Hauz Khas Fort & Village', type: 'History', zone: 'South Heritage', duration: '2-3 hrs' },
            { id: 'chattarpur', name: 'Chattarpur Temple', type: 'Faith', zone: 'South Heritage', duration: '1 hr' },

            // Zone 4: South Delhi Modern/Parks (Nizamuddin/Lotus/Dilli Haat)
            { id: 'humayuns_tomb', name: 'Humayun\'s Tomb', type: 'History', zone: 'South Modern', duration: '2 hrs' },
            { id: 'lotus_temple', name: 'Lotus Temple', type: 'Faith', zone: 'South Modern', duration: '1-2 hrs' },
            { id: 'nizamuddin', name: 'Nizamuddin Dargah', type: 'Faith', zone: 'South Modern', duration: '1.5 hrs' },
            { id: 'lodhi_garden', name: 'Lodhi Garden', type: 'Nature', zone: 'South Modern', duration: '1.5 hrs' },
            { id: 'dilli_haat', name: 'Dilli Haat (INA)', type: 'Shopping', zone: 'South Modern', duration: '2-3 hrs' },
            { id: 'iskcon', name: 'ISKCON Temple', type: 'Faith', zone: 'South Modern', duration: '1.5 hrs' },
            { id: 'waste_to_wonder', name: 'Waste to Wonder Park', type: 'Nature', zone: 'South Modern', duration: '1.5 hrs' },
            { id: 'safdarjung_tomb', name: 'Safdarjung Tomb', type: 'History', zone: 'South Modern', duration: '1 hr' },

            // Zone 5: East / Other
            { id: 'akshardham', name: 'Swaminarayan Akshardham', type: 'Faith', zone: 'East Delhi', duration: '3-4 hrs' },
            { id: 'rail_museum', name: 'National Rail Museum', type: 'Museum', zone: 'Central Delhi', duration: '2-3 hrs' },
            { id: 'raj_ghat', name: 'Raj Ghat', type: 'History', zone: 'Central Delhi', duration: '1 hr' }
        ];

        // --- EXPANDED FOOD GUIDE (3 Recommendations per item) ---
        const FOOD_GUIDE = {
            'butter_chicken': { 
                name: 'Butter Chicken (Murg Makhani)', 
                desc: 'The birthplace of Butter Chicken! Creamy, tomato-based gravy with tandoori chicken.',
                places: [
                    { name: 'Moti Mahal', loc: 'Daryaganj (Original)' },
                    { name: 'Gulati', loc: 'Pandara Road' },
                    { name: 'Havemore', loc: 'Pandara Road' }
                ]
            },
            'chole_bhature': { 
                name: 'Chole Bhature', 
                desc: 'Spicy chickpeas with fluffy fried bread. The ultimate Delhi breakfast.',
                places: [
                    { name: 'Sitaram Diwan Chand', loc: 'Paharganj' },
                    { name: 'Chache Di Hatti', loc: 'Kamla Nagar (North Campus)' },
                    { name: 'Sita Ram', loc: 'Pitampura' }
                ]
            },
            'paratha': { 
                name: 'Stuffed Parathas', 
                desc: 'Deep-fried flatbreads with fillings like potato, paneer, and even almond!',
                places: [
                    { name: 'Pt. Gaya Prasad Shiv Charan', loc: 'Parathe Wali Gali' },
                    { name: 'Moolchand Paratha', loc: 'Near Moolchand Metro' },
                    { name: 'Not Just Parathas', loc: 'GK-2' }
                ]
            },
            'dahi_bhalla': { 
                name: 'Dahi Bhalla', 
                desc: 'Soft lentil dumplings in yogurt with tamarind chutney.',
                places: [
                    { name: 'Natraj Dahi Bhalle Wala', loc: 'Chandni Chowk' },
                    { name: 'Atul Chaat', loc: 'Rajouri Garden' },
                    { name: 'Shyam Sweets', loc: 'Chawri Bazar' }
                ]
            },
            'aloo_tikki': { 
                name: 'Aloo Tikki Chaat', 
                desc: 'Crispy potato patties topped with yogurt and chutneys.',
                places: [
                    { name: 'Bittoo Tikki Wala (BTW)', loc: 'Pitampura/Multiple Outlets' },
                    { name: 'Natraj', loc: 'Chandni Chowk' },
                    { name: 'Sindhi Corner', loc: 'Karol Bagh' }
                ]
            },
            'gol_gappe': { 
                name: 'Gol Gappe (Pani Puri)', 
                desc: 'Crispy hollow shells filled with spicy water and potatoes.',
                places: [
                    { name: 'Prince Chaat', loc: 'GK-1 M Block' },
                    { name: 'Vaishno Chaat Bhandar', loc: 'Kamla Nagar' },
                    { name: 'Bengali Sweet House', loc: 'Connaught Place' }
                ]
            },
            'ram_ladoo': { 
                name: 'Ram Ladoo', 
                desc: 'Deep-fried moong dal fritters topped with radish and green chutney.',
                places: [
                    { name: 'Lajpat Nagar Central Market', loc: 'Street Vendors' },
                    { name: 'Sarojini Nagar Market', loc: 'Entry Gate' },
                    { name: 'Janpath', loc: 'Street Vendors' }
                ]
            },
            'kachori_aloo': { 
                name: 'Kachori with Aloo Sabzi', 
                desc: 'Crispy kachoris served with spicy potato curry.',
                places: [
                    { name: 'Jung Bahadur Kachori Wala', loc: 'Chandni Chowk' },
                    { name: 'Fateh Chand Kachori', loc: 'Civil Lines' },
                    { name: 'Narayan Das', loc: 'Khari Baoli' }
                ]
            },
            'bedmi_puri': { 
                name: 'Bedmi Puri Aloo', 
                desc: 'Coarse wheat puris with spicy aloo sabzi, a classic Old Delhi breakfast.',
                places: [
                    { name: 'Shyam Sweets', loc: 'Chawri Bazar' },
                    { name: 'Ram Swaroop Halwai', loc: 'Sitaram Bazar' },
                    { name: 'Mahalaxmi', loc: 'Fatehpuri' }
                ]
            },
            'chole_kulche': { 
                name: 'Chole Kulche', 
                desc: 'Soft bread (kulcha) served with spicy boiled chickpeas.',
                places: [
                    { name: 'Lotan Chole Kulche', loc: 'Chawri Bazar' },
                    { name: 'Bhogal Chole Kulche', loc: 'Scindia House, CP' },
                    { name: 'Mayapuri Chole Kulche', loc: 'Mayapuri Junk Market' }
                ]
            },
            'seekh_kebab': { 
                name: 'Seekh Kebabs', 
                desc: 'Minced meat grilled on skewers over charcoal.',
                places: [
                    { name: 'Qureshi Kebab Corner', loc: 'Jama Masjid' },
                    { name: 'Babu Bhai Kabab Wale', loc: 'Jama Masjid' },
                    { name: 'Ghalib Kabab Corner', loc: 'Nizamuddin' }
                ]
            },
            'galouti_kebab': { 
                name: 'Galouti Kebab', 
                desc: 'Melt-in-your-mouth minced meat kebabs.',
                places: [
                    { name: 'Rajinder Da Dhaba', loc: 'Safdarjung Enclave' },
                    { name: 'Tunday Kababi', loc: 'Multiple Locations' },
                    { name: 'Alkauser', loc: 'Chanakyapuri' }
                ]
            },
            'shami_kebab': { 
                name: 'Shami Kebab', 
                desc: 'Patty-style meat kebabs, soft and silky.',
                places: [
                    { name: 'Ustad Moinuddin', loc: 'Lal Kuan, Old Delhi' },
                    { name: 'Karim\'s', loc: 'Jama Masjid' },
                    { name: 'Al Jawahar', loc: 'Jama Masjid' }
                ]
            },
            'nihari': { 
                name: 'Nihari', 
                desc: 'Slow-cooked meat stew, spicy and rich. Best for breakfast.',
                places: [
                    { name: 'Kallu Nihari', loc: 'Daryaganj' },
                    { name: 'Haji Shabrati Nihari Wale', loc: 'Jama Masjid' },
                    { name: 'Javed Famous Nihari', loc: 'Zakir Nagar' }
                ]
            },
            'mutton_korma': { 
                name: 'Mutton Korma', 
                desc: 'Meat cooked in a rich yogurt and spice gravy.',
                places: [
                    { name: 'Karim\'s', loc: 'Jama Masjid' },
                    { name: 'Al Jawahar', loc: 'Jama Masjid' },
                    { name: 'Ashok & Ashok', loc: 'Sadar Bazar' }
                ]
            },
            'changezi_chicken': { 
                name: 'Chicken Changezi', 
                desc: 'Roasted chicken in a tangy, spicy, tomato-rich gravy.',
                places: [
                    { name: 'Changezi Chicken', loc: 'Daryaganj' },
                    { name: 'Al-Jawahar', loc: 'Jama Masjid' },
                    { name: 'Karim\'s', loc: 'Jama Masjid' }
                ]
            },
            'fried_chicken': { 
                name: 'Fried Chicken', 
                desc: 'Delhi\'s answer to KFC. Spicy, marinated fried chicken.',
                places: [
                    { name: 'Haji Mohd. Hussain', loc: 'Jama Masjid' },
                    { name: 'Rajinder Da Dhaba', loc: 'Safdarjung' },
                    { name: 'MI Food Center', loc: 'Lodhi Colony' }
                ]
            },
            'biryani': { 
                name: 'Biryani', 
                desc: 'Spicy Chicken Biryani (Andhra style) or Mughlai style.',
                places: [
                    { name: 'Andhra Bhavan', loc: 'Ashoka Road' },
                    { name: 'Matka Peer', loc: 'Pragati Maidan' },
                    { name: 'Dil Pasand Biryani', loc: 'Jama Masjid' }
                ]
            },
            'tandoori_chicken': { 
                name: 'Tandoori Chicken', 
                desc: 'Chicken marinated in yogurt and spices, roasted in a clay oven.',
                places: [
                    { name: 'Moti Mahal Delux', loc: 'Daryaganj/GK' },
                    { name: 'Rajinder Da Dhaba', loc: 'Safdarjung' },
                    { name: 'Kake Da Hotel', loc: 'Connaught Place' }
                ]
            },
            'momos': { 
                name: 'Momos (Steam/Fried)', 
                desc: 'Tibetan dumplings served with fiery red chutney.',
                places: [
                    { name: 'Dolma Aunty Momos', loc: 'Lajpat Nagar' },
                    { name: 'Yeti - The Himalayan Kitchen', loc: 'CP/Hauz Khas' },
                    { name: 'Depaul\'s', loc: 'Janpath' }
                ]
            },
            'tandoori_momos': { 
                name: 'Tandoori Momos', 
                desc: 'Momos marinated and roasted in a tandoor. A Delhi invention!',
                places: [
                    { name: 'Hunger Strike', loc: 'Amar Colony' },
                    { name: 'QD\'s', loc: 'Satya Niketan' },
                    { name: 'Chalak Vyapari', loc: 'Kamla Nagar' }
                ]
            },
            'laphing': { 
                name: 'Laphing', 
                desc: 'Spicy cold mung bean noodle roll.',
                places: [
                    { name: 'Majnu Ka Tila (MKT)', loc: 'Tibetan Colony' },
                    { name: 'Lajpat Nagar', loc: 'Dolma Aunty Stall' },
                    { name: 'Humayunpur', loc: 'Safdarjung' }
                ]
            },
            'chur_chur_naan': { 
                name: 'Chur Chur Naan', 
                desc: 'Crushed naan stuffed with paneer/aloo, served with dal.',
                places: [
                    { name: 'Raju Chur Chur Naan', loc: 'Dwarka/Rohini' },
                    { name: 'Sanjay Chur Chur Naan', loc: 'Moolchand' },
                    { name: 'Chawla De Mashoor', loc: 'Paharganj' }
                ]
            },
            'rajma_chawal': { 
                name: 'Rajma Chawal', 
                desc: 'Kidney beans curry with rice. Comfort food.',
                places: [
                    { name: 'Jain Chawal Wale', loc: 'Connaught Place' },
                    { name: 'Parashar Foods', loc: 'Shankar Market' },
                    { name: 'Baba Nagpal Corner', loc: 'Lajpat Nagar' }
                ]
            },
            'kadhi_chawal': { 
                name: 'Kadhi Chawal', 
                desc: 'Yogurt-based curry with fritters served with rice.',
                places: [
                    { name: 'Baba Nagpal Corner', loc: 'Lajpat Nagar' },
                    { name: 'Jain Chawal Wale', loc: 'CP' },
                    { name: 'Rajma Chawal Point', loc: 'Nehru Place' }
                ]
            },
            'dal_makhani': { 
                name: 'Dal Makhani', 
                desc: 'Black lentils cooked overnight with butter and cream.',
                places: [
                    { name: 'Bukhara', loc: 'ITC Maurya (Expensive)' },
                    { name: 'Gulati', loc: 'Pandara Road' },
                    { name: 'Minar', loc: 'Connaught Place' }
                ]
            },
            'shahi_paneer': { 
                name: 'Shahi Paneer', 
                desc: 'Cottage cheese in a rich, creamy tomato gravy.',
                places: [
                    { name: 'Kake Da Hotel', loc: 'Connaught Place' },
                    { name: 'Sitaram Diwan Chand', loc: 'Paharganj' },
                    { name: 'Bikanervala', loc: 'Multiple Outlets' }
                ]
            },
            'soya_chaap': { 
                name: 'Soya Chaap', 
                desc: 'Soybean chunks marinated and grilled (Veg meat).',
                places: [
                    { name: 'Sardarji Malai Chaap', loc: 'Subhash Nagar' },
                    { name: 'Wah Ji Wah', loc: 'Multiple Outlets' },
                    { name: 'Kulcha King', loc: 'Sarojini Nagar' }
                ]
            },
            'pav_bhaji': { 
                name: 'Pav Bhaji', 
                desc: 'Spicy vegetable mash served with buttered buns.',
                places: [
                    { name: 'Arjun Bombay Pav Bhaji', loc: 'Model Town' },
                    { name: 'Kumar Pav Bhaji', loc: 'Krishna Nagar' },
                    { name: 'Jhakkas Pav Bhaji', loc: 'Rohini' }
                ]
            },
            'kulfi_faluda': { 
                name: 'Kulfi Faluda', 
                desc: 'Traditional dense ice cream with noodles and rose syrup.',
                places: [
                    { name: 'Roshan Di Kulfi', loc: 'Karol Bagh' },
                    { name: 'Kuremal Mohan Lal', loc: 'Chawri Bazar' },
                    { name: 'Krishna Di Kulfi', loc: 'Pandara Road' }
                ]
            },
            'rabri_faluda': { 
                name: 'Rabri Faluda', 
                desc: 'Thick sweetened milk with vermicelli.',
                places: [
                    { name: 'Giani\'s di Hatti', loc: 'Chandni Chowk' },
                    { name: 'Mahavir Rabri', loc: 'Chandni Chowk' },
                    { name: 'Hira Lal Chaat', loc: 'Chawri Bazar' }
                ]
            },
            'jalebi': { 
                name: 'Jalebi', 
                desc: 'Thick, syrup-soaked fried batter spirals.',
                places: [
                    { name: 'Old Famous Jalebi Wala', loc: 'Chandni Chowk' },
                    { name: 'Bangla Sweets', loc: 'CP' },
                    { name: 'Gohana Jalebi', loc: 'Sonepat Stand' }
                ]
            },
            'daulat_ki_chaat': { 
                name: 'Daulat Ki Chaat', 
                desc: 'Frothy, airy milk dessert available only in winters.',
                places: [
                    { name: 'Khemchand Daulat Ki Chaat', loc: 'Kinari Bazar' },
                    { name: 'Ajit Daulat Ki Chaat', loc: 'Chandni Chowk' },
                    { name: 'Hemchand', loc: 'Chawri Bazar' }
                ]
            },
            'shahi_tukda': { 
                name: 'Shahi Tukda', 
                desc: 'Fried bread soaked in sugar syrup and topped with rabri.',
                places: [
                    { name: 'Cool Point', loc: 'Jama Masjid' },
                    { name: 'Shahi Tukda Stall', loc: 'Matia Mahal' },
                    { name: 'Karim\'s', loc: 'Jama Masjid' }
                ]
            },
            'moong_dal_halwa': { 
                name: 'Moong Dal Halwa', 
                desc: 'Rich lentil pudding cooked in ghee.',
                places: [
                    { name: 'Chaina Ram Sindhi Confectioners', loc: 'Chandni Chowk' },
                    { name: 'Bikanervala', loc: 'Multiple Outlets' },
                    { name: 'Kaleva', loc: 'Gole Market' }
                ]
            },
            'gajar_halwa': { 
                name: 'Gajar Ka Halwa', 
                desc: 'Carrot pudding, a winter staple.',
                places: [
                    { name: 'Giani\'s', loc: 'Fatehpuri' },
                    { name: 'Chaina Ram', loc: 'Chandni Chowk' },
                    { name: 'Kanwarji\'s', loc: 'Chandni Chowk' }
                ]
            },
            'fruit_sandwich': { 
                name: 'Fruit Sandwich', 
                desc: 'Bread layered with fresh fruits, paneer, and marmalade.',
                places: [
                    { name: 'Jain Coffee House', loc: 'Chawri Bazar' },
                    { name: 'Novelty Dairy', loc: 'Jangpura' },
                    { name: 'Guptaji', loc: 'Old Delhi' }
                ]
            },
            'banta': { 
                name: 'Banta (Lemon Soda)', 
                desc: 'Lemon soda spiced with masala in a marble-stopper bottle.',
                places: [
                    { name: 'Ved Prakash Lemon Wale', loc: 'Chandni Chowk' },
                    { name: 'North Campus', loc: 'University Area' },
                    { name: 'Pandit Ved Prakash', loc: 'Town Hall' }
                ]
            },
            'mohabbat_sharbat': { 
                name: 'Mohabbat Ka Sharbat', 
                desc: 'Watermelon and rose milk shake.',
                places: [
                    { name: 'Nawab Qureshi', loc: 'Jama Masjid' },
                    { name: 'Old Delhi Streets', loc: 'Matia Mahal' },
                    { name: 'Sharbat Wala', loc: 'Daryaganj' }
                ]
            },
            'lassi': { 
                name: 'Lassi', 
                desc: 'Thick, creamy yogurt drink topped with malai.',
                places: [
                    { name: 'Amritsari Lassi Wala', loc: 'Chandni Chowk' },
                    { name: 'Bille Di Hatti', loc: 'Kamla Nagar' },
                    { name: 'Aggarwal Lassi', loc: 'Sadar Bazar' }
                ]
            },
            'hot_chocolate': { 
                name: 'Hot Chocolate', 
                desc: 'Rich, thick hot chocolate.',
                places: [
                    { name: 'The Big Chill', loc: 'Khan Market' },
                    { name: 'Colocal', loc: 'Dhan Mill/Khan Market' },
                    { name: 'Choko la', loc: 'Multiple Outlets' }
                ]
            },
            'waffles': { 
                name: 'Waffles', 
                desc: 'Classic bakery waffles.',
                places: [
                    { name: 'Wengers', loc: 'Connaught Place' },
                    { name: 'Depaul\'s', loc: 'Janpath' },
                    { name: 'Ricos', loc: 'Hudson Lane' }
                ]
            },
            'coffee': { 
                name: 'Cold Coffee', 
                desc: 'Iconic hazelnut cold coffee in a plastic bottle.',
                places: [
                    { name: 'Depaul\'s', loc: 'Janpath' },
                    { name: 'United Coffee House', loc: 'Connaught Place' },
                    { name: 'Blue Tokai', loc: 'Multiple Outlets' }
                ]
            },
            'mutton_ghotala': { 
                name: 'Mutton Ghotala', 
                desc: 'Mutton cooked with eggs.',
                places: [
                    { name: 'Parsi Anjuman', loc: 'Daryaganj' },
                    { name: 'Rustom\'s', loc: 'ITO' },
                    { name: 'SodaBottleOpenerWala', loc: 'Khan Market' }
                ]
            },
            'japani_samosa': { 
                name: 'Japani Samosa', 
                desc: 'Layered puff pastry samosa.',
                places: [
                    { name: 'Manohar Dhaba', loc: 'Chandni Chowk' },
                    { name: 'Umesh Samosa', loc: 'Chandni Chowk' },
                    { name: 'Local Sweet Shops', loc: 'Old Delhi' }
                ]
            },
            'fruit_chaat': { 
                name: 'Fruit Chaat', 
                desc: 'Spicy mixed fruit salad.',
                places: [
                    { name: 'Bishan Swaroop', loc: 'Chandni Chowk' },
                    { name: 'Hira Lal', loc: 'Chawri Bazar' },
                    { name: 'Jai Mata Di', loc: 'UPSC Lane' }
                ]
            },
            'omelette': { 
                name: 'Omelette', 
                desc: 'Cheese laden buttery omelettes.',
                places: [
                    { name: 'Khan Omelette Corner', loc: 'Chandni Chowk' },
                    { name: 'Rahul Eggs', loc: 'Keshav Puram' },
                    { name: 'Dwarka Omelette', loc: 'Dwarka' }
                ]
            }
        };

        // --- Navigation Logic ---
        function showSection(targetId) {
             document.querySelectorAll('.content-section').forEach(section => {
                section.classList.add('hidden');
            });
            document.getElementById(targetId).classList.remove('hidden');
            document.querySelectorAll('.nav-link').forEach(nav => nav.classList.remove('active'));
            const activeLink = document.querySelector(`.nav-link[data-section="${targetId}"]`);
            if(activeLink) activeLink.classList.add('active');
            window.scrollTo({top: 0, behavior: 'smooth'});
        }

        document.querySelectorAll('.nav-link').forEach(link => {
            link.addEventListener('click', function(e) {
                e.preventDefault();
                const targetId = this.getAttribute('data-section');
                showSection(targetId);
            });
        });

        // --- Food Finder Logic ---
        function populateFoodDropdown() {
            const select = document.getElementById('food-select');
            select.innerHTML = '<option value="" disabled selected>Select a dish (50+ Options)...</option>';
            const sortedKeys = Object.keys(FOOD_GUIDE).sort();
            sortedKeys.forEach(key => {
                const option = document.createElement('option');
                option.value = key;
                option.textContent = FOOD_GUIDE[key].name;
                select.appendChild(option);
            });
        }

        function findBestFood() {
            const select = document.getElementById('food-select');
            const resultDiv = document.getElementById('food-result');
            const dishKey = select.value;

            if (dishKey && FOOD_GUIDE[dishKey]) {
                const info = FOOD_GUIDE[dishKey];
                
                // 1. Set Dish Details
                document.getElementById('res-dish').innerText = info.name;
                document.getElementById('res-desc').innerText = info.desc;

                // 2. Build Recommendations List
                const placesList = document.getElementById('res-places-list');
                placesList.innerHTML = ''; // Clear previous

                info.places.forEach((spot, index) => {
                    const li = document.createElement('li');
                    li.className = 'flex items-center justify-between p-3 bg-white rounded border border-gray-200 hover:shadow-sm transition';
                    li.innerHTML = `
                        <div class="flex items-center">
                            <div class="bg-[#D97706] text-white rounded-full w-6 h-6 flex items-center justify-center mr-3 text-xs font-bold">${index + 1}</div>
                            <span class="font-bold text-gray-800">${spot.name}</span>
                        </div>
                        <span class="text-sm text-gray-500 flex items-center">
                            <svg class="w-4 h-4 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.828 0l-4.243-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                            ${spot.loc}
                        </span>
                    `;
                    placesList.appendChild(li);
                });

                resultDiv.classList.remove('hidden');
            }
        }

        // --- Profile Logic ---
        function saveProfile(e) {
            e.preventDefault();
            const msg = document.getElementById('save-msg');
            msg.classList.remove('hidden');
            setTimeout(() => msg.classList.add('hidden'), 3000);
        }

        // --- NEW SMART ITINERARY LOGIC ---

        function validateDays(input) {
            if (input.value < 1) input.value = 1;
            if (input.value > 7) input.value = 7;
        }

        function generateSmartItinerary() {
            const days = parseInt(document.getElementById('trip-days').value) || 2;
            const selectedPrefs = Array.from(document.querySelectorAll('.pref-checkbox:checked')).map(cb => cb.value);
            const output = document.getElementById('itinerary-output');

            // 1. Mapping UI preferences to internal Data Types
            // Preferences: History, Faith, Food, Shopping, Nature, Museum
            const prefMap = {
                'History': ['History'],
                'Faith': ['Faith'],
                'Food': ['Food'],
                'Shopping': ['Shopping'],
                'Nature': ['Nature'],
                'Museum': ['Museum']
            };

            // 2. Filter Places based on Preferences
            let activeTypes = [];
            if (selectedPrefs.length === 0) {
                // Default if nothing selected: History + Food
                activeTypes = ['History', 'Food'];
            } else {
                selectedPrefs.forEach(pref => {
                    if(prefMap[pref]) activeTypes = [...activeTypes, ...prefMap[pref]];
                });
            }

            const filteredPlaces = DELHIPLACES.filter(place => activeTypes.includes(place.type));

            // 3. Group by Zone
            const zoneGroups = filteredPlaces.reduce((acc, place) => {
                if (!acc[place.zone]) acc[place.zone] = [];
                acc[place.zone].push(place);
                return acc;
            }, {});

            // 4. Sort Zones by "Richness" (how many preferred spots are there)
            const sortedZones = Object.keys(zoneGroups).sort((a, b) => zoneGroups[b].length - zoneGroups[a].length);

            // 5. Select Zones for the trip
            // Logic: Assign top zones to available days.
            // If days > zones, we might need to split big zones or add generic days.
            // If zones > days, we take the best ones.
            
            let finalPlan = [];
            
            // Define Zone Priority manually to ensure logical flow if counts are equal
            const zonePriority = { 'Old Delhi': 1, 'Central Delhi': 2, 'South Heritage': 3, 'South Modern': 4, 'East Delhi': 5 };

            // Re-sort based on count AND priority
            sortedZones.sort((a, b) => {
                const countDiff = zoneGroups[b].length - zoneGroups[a].length;
                if (countDiff !== 0) return countDiff;
                return (zonePriority[a] || 99) - (zonePriority[b] || 99);
            });

            // Build the days
            let usedZones = 0;
            for (let i = 1; i <= days; i++) {
                let dayZone = sortedZones[usedZones];
                
                if (!dayZone) {
                    // Ran out of zones with specific matches, suggest a leisure day
                    finalPlan.push({
                        day: i,
                        title: "Relax & Explore Local Markets",
                        places: [{name: "Local Markets or Revisiting Favorites", type: "Leisure", duration: "Flexible"}]
                    });
                } else {
                    finalPlan.push({
                        day: i,
                        title: `${dayZone} Highlights`,
                        places: zoneGroups[dayZone]
                    });
                    usedZones++;
                }
            }

            // 6. Render HTML
            let html = '';
            
            finalPlan.forEach(dayPlan => {
                let dayPlacesHtml = '';
                dayPlan.places.forEach(place => {
                    const color = place.type === 'Food' ? 'text-green-600' : 'text-blue-600';
                    dayPlacesHtml += `
                        <li class="pl-2 flex justify-between items-center border-l-4 border-[#D97706] py-1">
                            <div>
                                <span class="font-semibold block text-gray-800">${place.name}</span>
                                <span class="text-xs text-gray-500">${place.type}</span>
                            </div>
                            <span class="text-sm font-medium text-gray-600 bg-gray-100 px-2 py-1 rounded whitespace-nowrap">${place.duration}</span>
                        </li>
                    `;
                });

                html += `
                    <div class="border border-gray-200 rounded-lg p-5 hover:shadow-md transition bg-white">
                        <div class="flex items-center justify-between mb-3">
                            <h4 class="text-xl font-bold text-[#991b1b]">Day ${dayPlan.day}: ${dayPlan.title}</h4>
                            <span class="text-sm text-gray-500 bg-gray-100 px-2 py-1 rounded-full">Zone Based</span>
                        </div>
                        <ul class="space-y-3 mt-2">
                            ${dayPlacesHtml}
                        </ul>
                    </div>
                `;
            });

            output.innerHTML = html;
        }

        window.onload = function() {
            populateFoodDropdown();
            showSection('home');
        };
    </script>
</body>
</html>
