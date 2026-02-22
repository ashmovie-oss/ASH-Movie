ASH Movies 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>ASH Movies - Download Movies Free</title>
    <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            -webkit-tap-highlight-color: transparent;
        }
        body {
            font-family: 'Inter', sans-serif;
        }
        .gradient-bg {
            background: linear-gradient(135deg, #0a0a0f 0%, #1a1a2e 50%, #0f0f1a 100%);
        }
        .card-hover:hover {
            transform: translateY(-4px);
            box-shadow: 0 15px 30px rgba(99, 102, 241, 0.3);
        }
        @media (max-width: 768px) {
            .card-hover:hover {
                transform: none;
            }
        }
        .search-glow:focus {
            box-shadow: 0 0 20px rgba(99, 102, 241, 0.5);
        }
        .loader {
            border: 4px solid rgba(255, 255, 255, 0.1);
            border-left-color: #6366f1;
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            to { transform: rotate(360deg); }
        }
        .fade-in {
            animation: fadeIn 0.5s ease-in-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .hero-gradient {
            background: linear-gradient(to right, rgba(0,0,0,0.95) 0%, rgba(0,0,0,0.7) 50%, transparent 100%);
        }
        @media (max-width: 768px) {
            .hero-gradient {
                background: linear-gradient(to top, rgba(0,0,0,0.95) 0%, rgba(0,0,0,0.5) 50%, transparent 100%);
            }
        }
        .scroll-container {
            scrollbar-width: none;
            -ms-overflow-style: none;
            -webkit-overflow-scrolling: touch;
        }
        .scroll-container::-webkit-scrollbar {
            display: none;
        }
        .telegram-btn {
            background: linear-gradient(135deg, #0088cc 0%, #00aced 100%);
        }
        .telegram-btn:hover {
            background: linear-gradient(135deg, #006699 0%, #0088cc 100%);
        }
        .category-chip.active {
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
        }
        .nav-link:hover::after {
            width: 100%;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: linear-gradient(90deg, #6366f1, #8b5cf6);
            transition: width 0.3s;
        }
        .glass-card {
            background: rgba(255,255,255,0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.1);
        }
        .pulse-dot {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }
        /* Mobile Bottom Navigation */
        .mobile-nav {
            display: none;
        }
        @media (max-width: 768px) {
            .mobile-nav {
                display: flex;
            }
            .desktop-nav {
                display: none;
            }
        }
        /* Mobile optimizations */
        .mobile-card {
            min-width: 140px;
            width: 140px;
        }
        @media (min-width: 640px) {
            .mobile-card {
                min-width: 160px;
                width: 160px;
            }
        }
        @media (min-width: 768px) {
            .mobile-card {
                min-width: 180px;
                width: 180px;
            }
        }
        /* Anticipation badge */
        .anticipation-badge {
            background: linear-gradient(135deg, #f59e0b 0%, #ef4444 100%);
        }
        /* Section divider */
        .section-divider {
            background: linear-gradient(90deg, transparent, rgba(99, 102, 241, 0.3), transparent);
            height: 1px;
        }
        /* Anime chip active */
        .anime-chip.active {
            background: linear-gradient(135deg, #ec4899 0%, #a855f7 100%) !important;
        }
        /* Anime section gradient */
        .anime-gradient {
            background: linear-gradient(135deg, rgba(236, 72, 153, 0.1) 0%, rgba(168, 85, 247, 0.1) 100%);
        }
    </style>
</head>
<body class="gradient-bg min-h-screen text-white">
    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-black/90 backdrop-blur-md border-b border-white/10">
        <div class="max-w-7xl mx-auto px-3 md:px-4 py-3 md:py-4">
            <div class="flex items-center justify-between">
                <div class="flex items-center gap-2 cursor-pointer" onclick="showSection('home')">
                    <svg class="w-7 h-7 md:w-8 md:h-8 text-indigo-500" fill="currentColor" viewBox="0 0 24 24">
                        <path d="M18 4l2 4h-3l-2-4h-2l2 4h-3l-2-4H8l2 4H7L5 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V4h-4z"/>
                    </svg>
                    <span class="text-lg md:text-xl font-bold bg-gradient-to-r from-indigo-400 to-purple-400 bg-clip-text text-transparent">ASH Movies</span>
                </div>
                
                <div class="hidden md:flex items-center gap-8 desktop-nav">
                    <a href="#" onclick="showSection('home')" class="nav-link relative text-gray-300 hover:text-white transition-colors">Home</a>
                    <a href="#" onclick="showSection('indian')" class="nav-link relative text-gray-300 hover:text-white transition-colors">🇮🇳 Indian</a>
                    <a href="#" onclick="showSection('anime')" class="nav-link relative text-gray-300 hover:text-white transition-colors">🎌 Anime</a>
                    <a href="#" onclick="showSection('trending')" class="nav-link relative text-gray-300 hover:text-white transition-colors">Trending</a>
                    <a href="#" onclick="showSection('search')" class="nav-link relative text-gray-300 hover:text-white transition-colors">Search</a>
                </div>

                <div class="flex items-center gap-2 md:gap-4">
                    <a href="https://t.me/proSearch" target="_blank" class="telegram-btn px-3 py-1.5 md:px-4 md:py-2 rounded-full text-xs md:text-sm font-medium flex items-center gap-1.5 md:gap-2 transition-all hover:scale-105">
                        <svg class="w-4 h-4 md:w-5 md:h-5" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/>
                        </svg>
                        <span class="hidden sm:inline">@proSearch</span>
                    </a>
                    <button onclick="showSection('search')" class="md:hidden p-2 hover:bg-white/10 rounded-lg">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                        </svg>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Mobile Bottom Navigation -->
    <nav class="mobile-nav fixed bottom-0 left-0 right-0 z-50 bg-black/95 backdrop-blur-md border-t border-white/10 px-2 py-2 justify-around items-center">
        <button onclick="showSection('home')" class="flex flex-col items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition-colors" id="navHome">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg>
            <span class="text-[10px]">Home</span>
        </button>
        <button onclick="showSection('indian')" class="flex flex-col items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition-colors" id="navIndian">
            <span class="text-lg">🇮🇳</span>
            <span class="text-[10px]">Indian</span>
        </button>
        <button onclick="showSection('anime')" class="flex flex-col items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition-colors" id="navAnime">
            <span class="text-lg">🎌</span>
            <span class="text-[10px]">Anime</span>
        </button>
        <button onclick="showSection('trending')" class="flex flex-col items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition-colors" id="navTrending">
            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M16 6l2.29 2.29-4.88 4.88-4-4L2 16.59 3.41 18l6-6 4 4 6.3-6.29L22 12V6z"/></svg>
            <span class="text-[10px]">Trending</span>
        </button>
        <button onclick="showSection('search')" class="flex flex-col items-center gap-1 p-2 rounded-lg hover:bg-white/10 transition-colors" id="navSearch">
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
            <span class="text-[10px]">Search</span>
        </button>
    </nav>

    <!-- Main Content -->
    <main class="pt-16 md:pt-20 pb-20 md:pb-0">
        <!-- Home Section -->
        <section id="homeSection">
            <!-- Hero Banner -->
            <div id="heroBanner" class="relative h-[50vh] md:h-[70vh] overflow-hidden">
                <div class="absolute inset-0 bg-gradient-to-t from-[#0a0a0f] via-transparent to-transparent z-10"></div>
                <div class="absolute inset-0 hero-gradient z-10"></div>
                <img id="heroImage" src="https://image.tmdb.org/t/p/original/8Y43POKjjKDGI9MH89NW0NAzzp8.jpg" alt="Hero" class="w-full h-full object-cover">
                <div class="absolute bottom-0 left-0 right-0 p-4 md:p-16 z-20">
                    <div class="max-w-2xl">
                        <span class="inline-flex items-center gap-2 bg-red-600 px-2 py-0.5 md:px-3 md:py-1 rounded-full text-xs md:text-sm mb-2 md:mb-4">
                            <span class="w-1.5 h-1.5 md:w-2 md:h-2 bg-white rounded-full pulse-dot"></span>
                            Trending Now
                        </span>
                        <h1 id="heroTitle" class="text-2xl md:text-6xl font-bold mb-2 md:mb-4">Oppenheimer</h1>
                        <p id="heroDesc" class="text-gray-300 text-sm md:text-base mb-4 md:mb-6 line-clamp-2 md:line-clamp-3">The story of American scientist J. Robert Oppenheimer and his role in the development of the atomic bomb.</p>
                        <div class="flex flex-wrap gap-2 md:gap-4">
                            <button onclick="searchAndShowMovie('Oppenheimer')" class="bg-indigo-600 hover:bg-indigo-700 px-4 md:px-8 py-2 md:py-3 rounded-lg md:rounded-xl font-semibold text-sm md:text-base flex items-center gap-2 transition-all">
                                <svg class="w-4 h-4 md:w-5 md:h-5" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M8 5v14l11-7z"/>
                                </svg>
                                Watch Now
                            </button>
                            <a href="https://t.me/ProSearchM11Bot" target="_blank" class="telegram-btn px-3 md:px-6 py-2 md:py-3 rounded-lg md:rounded-xl font-semibold text-xs md:text-sm flex items-center gap-1.5 md:gap-2 transition-all">
                                <svg class="w-4 h-4 md:w-5 md:h-5" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106.024-1.793 1.14-5.061 3.345-.48.33-.913.49-1.302.48-.428-.008-1.252-.241-1.865-.44-.752-.245-1.349-.374-1.297-.789.027-.216.325-.437.893-.663 3.498-1.524 5.83-2.529 6.998-3.014 3.332-1.386 4.025-1.627 4.476-1.635z"/>
                                </svg>
                                @ProSearchM11Bot
                            </a>
                            <a href="https://t.me/ProSearchY11Bot" target="_blank" class="bg-gradient-to-r from-purple-600 to-pink-600 hover:from-purple-700 hover:to-pink-700 px-3 md:px-6 py-2 md:py-3 rounded-lg md:rounded-xl font-semibold text-xs md:text-sm flex items-center gap-1.5 md:gap-2 transition-all">
                                <svg class="w-4 h-4 md:w-5 md:h-5" fill="currentColor" viewBox="0 0 24 24">
                                    <path d="M11.944 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0a12 12 0 0 0-.056 0zm4.962 7.224c.1-.002.321.023.465.14a.506.506 0 0 1 .171.325c.016.093.036.306.02.472-.18 1.898-.962 6.502-1.36 8.627-.168.9-.499 1.201-.82 1.23-.696.065-1.225-.46-1.9-.902-1.056-.693-1.653-1.124-2.678-1.8-1.185-.78-.417-1.21.258-1.91.177-.184 3.247-2.977 3.307-3.23.007-.032.014-.15-.056-.212s-.174-.041-.249-.024c-.106
