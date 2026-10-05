<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title id="site-title-meta">Jurnal Pramuka Indonesia | Portal Berita & Event Pramuka</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        pramuka: {
                            dark: '#3D2312',
                            primary: '#4A2E16',
                            medium: '#8C5A2B',
                            accent: '#C39B6B',
                            gold: '#D4AF37',
                            yellow: '#FFC107',
                            light: '#F8F5F0',
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #F8F5F0; }
        ::-webkit-scrollbar-thumb { background: #C39B6B; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #4A2E16; }
        .line-clamp-2 { display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden; }
        .line-clamp-3 { display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical; overflow: hidden; }
    </style>
</head>
<body class="bg-[#FDFBF7] text-gray-800 font-sans antialiased min-h-screen flex flex-col">

    <!-- HEADER & NAVBAR -->
    <header class="sticky top-0 z-40 bg-pramuka-primary text-white shadow-lg border-b-4 border-pramuka-gold">
        <!-- Top Bar Info & Social Links -->
        <div class="bg-pramuka-dark text-xs py-1.5 px-4 text-pramuka-accent flex justify-between items-center border-b border-pramuka-primary/40">
            <div class="container mx-auto flex justify-between items-center">
                <div class="flex items-center space-x-4">
                    <span><i class="fa-solid fa-calendar-day text-pramuka-yellow mr-1"></i> <span id="current-date">Senin, 5 Oktober 2026</span></span>
                    <span class="hidden md:inline"><i class="fa-solid fa-bullhorn text-pramuka-yellow mr-1"></i> <span id="top-domain-display">jurnal_pramuka.co.id</span></span>
                </div>
                <!-- Dynamic Social Media Header Links -->
                <div class="flex items-center space-x-3 text-white">
                    <span class="text-xs text-pramuka-accent">Kanal Resmi:</span>
                    <a id="hdr-link-tiktok" href="#" target="_blank" class="hover:text-pramuka-yellow transition"><i class="fa-brands fa-tiktok"></i></a>
                    <a id="hdr-link-youtube" href="#" target="_blank" class="hover:text-pramuka-yellow transition"><i class="fa-brands fa-youtube"></i></a>
                    <a id="hdr-link-instagram" href="#" target="_blank" class="hover:text-pramuka-yellow transition"><i class="fa-brands fa-instagram"></i></a>
                    <a id="hdr-link-facebook" href="#" target="_blank" class="hover:text-pramuka-yellow transition"><i class="fa-brands fa-facebook"></i></a>
                    <a id="hdr-link-whatsapp" href="#" target="_blank" class="hover:text-pramuka-yellow transition"><i class="fa-brands fa-whatsapp"></i></a>
                </div>
            </div>
        </div>

        <!-- Main Navigation Bar -->
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <!-- Dynamic Logo -->
            <a href="#" onclick="filterCategory('all')" class="flex items-center space-x-3 group">
                <div id="site-logo-container" class="w-10 h-10 rounded-full bg-pramuka-yellow text-pramuka-dark flex items-center justify-center font-bold text-xl shadow-md overflow-hidden group-hover:rotate-6 transition transform">
                    <i class="fa-solid fa-compass" id="default-logo-icon"></i>
                    <img id="site-logo-img" src="" class="w-full h-full object-cover hidden" alt="Logo">
                </div>
                <div>
                    <span id="site-name-display" class="text-xl font-extrabold tracking-tight text-white block leading-none">Jurnal<span class="text-pramuka-yellow">Pramuka</span></span>
                    <span id="site-sub-display" class="text-[10px] text-pramuka-accent tracking-widest font-semibold uppercase block mt-0.5">Media Informasi Terkini</span>
                </div>
            </a>

            <!-- Search Bar -->
            <div class="hidden md:flex items-center flex-1 max-w-xs mx-8 relative">
                <input type="text" id="search-input" onkeyup="handleSearch()" placeholder="Cari berita atau event..." class="w-full bg-pramuka-dark/60 text-white placeholder-pramuka-accent/70 text-sm rounded-full py-2 pl-4 pr-10 border border-pramuka-accent/30 focus:outline-none focus:border-pramuka-yellow">
                <i class="fa-solid fa-magnifying-glass absolute right-3 text-pramuka-accent"></i>
            </div>

            <!-- Dynamic User Authentication State Actions -->
            <div id="auth-actions" class="flex items-center space-x-2 sm:space-x-3">
                <!-- Injected via JS based on session role: Guest, Journalist, or Admin -->
            </div>
        </div>

        <!-- Filter Categories Bar -->
        <nav class="bg-pramuka-dark/90 border-t border-pramuka-primary/60 hidden md:block">
            <div class="container mx-auto px-4 flex space-x-1 text-sm font-medium overflow-x-auto">
                <button onclick="filterCategory('all')" class="cat-btn active px-4 py-2.5 text-pramuka-yellow border-b-2 border-pramuka-yellow transition flex items-center space-x-2 whitespace-nowrap">
                    <i class="fa-solid fa-layer-group text-xs"></i> <span>Semua Terbitan</span>
                </button>
                <button onclick="filterCategory('Berita')" class="cat-btn px-4 py-2.5 text-gray-300 hover:text-white transition flex items-center space-x-2 whitespace-nowrap">
                    <i class="fa-solid fa-newspaper text-xs"></i> <span>Berita Pramuka</span>
                </button>
                <button onclick="filterCategory('Artikel')" class="cat-btn px-4 py-2.5 text-gray-300 hover:text-white transition flex items-center space-x-2 whitespace-nowrap">
                    <i class="fa-solid fa-book-open text-xs"></i> <span>Artikel & Edukasi</span>
                </button>
                <button onclick="filterCategory('Info Event')" class="cat-btn px-4 py-2.5 text-gray-300 hover:text-white transition flex items-center space-x-2 whitespace-nowrap">
                    <i class="fa-solid fa-calendar-star text-xs"></i> <span>Info Event & Kegiatan</span>
                </button>
                <button onclick="filterCategory('Pengumuman')" class="cat-btn px-4 py-2.5 text-gray-300 hover:text-white transition flex items-center space-x-2 whitespace-nowrap">
                    <i class="fa-solid fa-bullhorn text-xs"></i> <span>Pengumuman Kwartir</span>
                </button>
            </div>
        </nav>

        <!-- Mobile Menu Navigation -->
        <div id="mobile-menu" class="hidden md:hidden bg-pramuka-dark border-t border-pramuka-primary px-4 py-3 space-y-2">
            <div class="relative mb-3">
                <input type="text" id="search-input-mobile" onkeyup="handleSearchMobile()" placeholder="Cari berita atau event..." class="w-full bg-pramuka-primary text-white placeholder-pramuka-accent/70 text-sm rounded-lg py-2 pl-4 pr-10 border border-pramuka-accent/30 focus:outline-none">
                <i class="fa-solid fa-magnifying-glass absolute right-3 top-2.5 text-pramuka-accent"></i>
            </div>
            <a href="#" onclick="filterCategory('all'); toggleMobileMenu();" class="block py-2 text-pramuka-yellow font-medium">Semua Terbitan</a>
            <a href="#" onclick="filterCategory('Berita'); toggleMobileMenu();" class="block py-2 text-gray-200 hover:text-pramuka-yellow">Berita Pramuka</a>
            <a href="#" onclick="filterCategory('Artikel'); toggleMobileMenu();" class="block py-2 text-gray-200 hover:text-pramuka-yellow">Artikel & Edukasi</a>
            <a href="#" onclick="filterCategory('Info Event'); toggleMobileMenu();" class="block py-2 text-gray-200 hover:text-pramuka-yellow">Info Event & Kegiatan</a>
            <a href="#" onclick="filterCategory('Pengumuman'); toggleMobileMenu();" class="block py-2 text-gray-200 hover:text-pramuka-yellow">Pengumuman Kwartir</a>
        </div>
    </header>

    <!-- HERO / FEATURED SECTION -->
    <section class="bg-gradient-to-b from-pramuka-primary to-pramuka-dark text-white py-8 px-4 border-b border-pramuka-accent/20">
        <div class="container mx-auto">
            <div id="hero-banner" class="relative rounded-2xl overflow-hidden shadow-2xl bg-pramuka-dark border border-pramuka-accent/30 min-h-[320px] md:min-h-[400px] flex items-end">
                <img id="hero-img" src="https://images.unsplash.com/photo-1526772662000-3f88f10405ff?auto=format&fit=crop&w=1200&q=80" class="absolute inset-0 w-full h-full object-cover opacity-50 mix-blend-overlay" alt="Hero Banner">
                <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/40 to-transparent"></div>
                <div class="relative p-6 md:p-10 max-w-3xl z-10 space-y-3">
                    <span id="hero-category" class="bg-pramuka-yellow text-pramuka-dark font-extrabold text-xs uppercase px-3 py-1 rounded-full inline-block shadow">
                        Utama & Terhangat
                    </span>
                    <h1 id="hero-title" class="text-2xl md:text-4xl font-black leading-tight tracking-tight text-white drop-shadow">
                        Persiapan Raimuna Nasional 2026: Ribuan Pramuka Penegak Siap Mengabdi untuk Negeri
                    </h1>
                    <p id="hero-desc" class="text-sm md:text-base text-gray-200 line-clamp-2 font-normal">
                        Kwartir Nasional Gerakan Pramuka merilis petunjuk teknis pelaksanaan kegiatan perkemahan akbar yang mengedepankan inovasi teknologi dan kepedulian lingkungan.
                    </p>
                    <div class="flex items-center space-x-4 text-xs text-gray-300 pt-2">
                        <span id="hero-author"><i class="fa-solid fa-user-pen text-pramuka-yellow mr-1"></i> Tim Redaksi Kwarnas</span>
                        <span id="hero-date"><i class="fa-solid fa-clock text-pramuka-yellow mr-1"></i> 5 Oktober 2026</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- MAIN CONTENT CONTAINER -->
    <div class="container mx-auto px-4 py-8 flex-1">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- LEFT COLUMN: POSTS FEED -->
            <div class="lg:col-span-2 space-y-6">
                <div class="flex justify-between items-center border-b-2 border-pramuka-accent/30 pb-3">
                    <h2 id="section-title" class="text-xl md:text-2xl font-bold text-pramuka-primary flex items-center">
                        <i class="fa-solid fa-newspaper text-pramuka-gold mr-2.5"></i>
                        Semua Terbitan Terbaru
                    </h2>
                    <span id="post-count-badge" class="bg-pramuka-light text-pramuka-primary border border-pramuka-accent text-xs font-semibold px-2.5 py-1 rounded-full">
                        0 Artikel
                    </span>
                </div>

                <!-- Feed Posts Grid -->
                <div id="posts-container" class="space-y-6"></div>

                <!-- Empty State Notice -->
                <div id="empty-state" class="hidden text-center py-16 bg-white rounded-2xl border border-dashed border-gray-300 p-6">
                    <i class="fa-solid fa-folder-open text-5xl text-gray-300 mb-3 block"></i>
                    <h3 class="text-lg font-bold text-gray-600">Belum ada berita atau artikel</h3>
                    <p class="text-sm text-gray-400 mt-1">Daftar sebagai Jurnalis untuk menerbitkan berita pertama di kategori ini!</p>
                    <button onclick="openRegisterModal()" class="mt-4 bg-pramuka-primary text-white text-xs font-bold px-4 py-2 rounded-lg hover:bg-pramuka-dark transition">
                        Daftar Jurnalis Sekarang
                    </button>
                </div>
            </div>

            <!-- RIGHT COLUMN: SIDEBAR -->
            <div class="space-y-6">
                
                <!-- DYNAMIC SIDEBAR JOURNALIST / ADMIN CTA CARD -->
                <div id="sidebar-cta-card" class="bg-gradient-to-br from-pramuka-primary to-pramuka-dark text-white rounded-2xl p-6 shadow-xl border border-pramuka-gold/30 relative overflow-hidden">
                    <!-- Dynamic CTA content rendered by JS based on user role -->
                </div>

                <!-- EVENT HIGHLIGHT WIDGET -->
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-gray-200">
                    <div class="flex justify-between items-center mb-4 pb-2 border-b border-gray-100">
                        <h3 class="font-bold text-pramuka-primary text-base flex items-center">
                            <i class="fa-solid fa-calendar-days text-pramuka-gold mr-2"></i> Agenda Event Terdekat
                        </h3>
                        <a href="#" onclick="filterCategory('Info Event')" class="text-xs text-pramuka-medium font-semibold hover:underline">Lihat Semua</a>
                    </div>
                    <div id="sidebar-events" class="space-y-3"></div>
                </div>

                <!-- SOCIAL MEDIA CHANNELS SIDEBAR WIDGET -->
                <div class="bg-white rounded-2xl p-5 shadow-sm border border-gray-200">
                    <h3 class="font-bold text-pramuka-primary text-base mb-2 flex items-center">
                        <i class="fa-solid fa-share-nodes text-pramuka-gold mr-2"></i> Media Sosial Resmi
                    </h3>
                    <p class="text-xs text-gray-500 mb-4">Akses langsung kanal resmi komunikasi kepramukaan:</p>
                    <div class="grid grid-cols-2 gap-2.5">
                        <a id="sdb-link-tiktok" href="#" target="_blank" class="flex items-center space-x-2.5 p-2.5 rounded-xl bg-gray-900 text-white hover:bg-black transition text-xs font-semibold">
                            <i class="fa-brands fa-tiktok text-base text-pink-500"></i>
                            <span>TikTok Official</span>
                        </a>
                        <a id="sdb-link-youtube" href="#" target="_blank" class="flex items-center space-x-2.5 p-2.5 rounded-xl bg-red-50 text-red-700 border border-red-200 hover:bg-red-100 transition text-xs font-semibold">
                            <i class="fa-brands fa-youtube text-base text-red-600"></i>
                            <span>YouTube Kwarnas</span>
                        </a>
                        <a id="sdb-link-instagram" href="#" target="_blank" class="flex items-center space-x-2.5 p-2.5 rounded-xl bg-pink-50 text-pink-700 border border-pink-200 hover:bg-pink-100 transition text-xs font-semibold">
                            <i class="fa-brands fa-instagram text-base text-pink-600"></i>
                            <span>Instagram</span>
                        </a>
                        <a id="sdb-link-facebook" href="#" target="_blank" class="flex items-center space-x-2.5 p-2.5 rounded-xl bg-blue-50 text-blue-700 border border-blue-200 hover:bg-blue-100 transition text-xs font-semibold">
                            <i class="fa-brands fa-facebook text-base text-blue-600"></i>
                            <span>Facebook</span>
                        </a>
                        <a id="sdb-link-whatsapp" href="#" target="_blank" class="col-span-2 flex items-center justify-center space-x-2 p-2.5 rounded-xl bg-emerald-50 text-emerald-800 border border-emerald-200 hover:bg-emerald-100 transition text-xs font-bold">
                            <i class="fa-brands fa-whatsapp text-base text-emerald-600"></i>
                            <span>Saluran WhatsApp Resmi</span>
                        </a>
                    </div>
                </div>

                <!-- TENTANG JURNAL PRAMUKA -->
                <div class="bg-pramuka-light/60 rounded-2xl p-5 border border-pramuka-accent/20">
                    <h4 class="font-bold text-pramuka-primary text-sm mb-1.5">Tentang Portal Jurnal Pramuka</h4>
                    <p class="text-xs text-gray-600 leading-relaxed" id="about-text-sidebar">
                        jurnal_pramuka.co.id adalah portal independen & resmi pers kepramukaan Indonesia untuk publikasi warta, karya jurnalis, dan event Kwartir seluruh Nusantara.
                    </p>
                </div>

            </div>
        </div>
    </div>

    
    <!-- MODAL 1: REGISTER AS JOURNALIST -->
    <div id="register-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-2xl max-w-md w-full shadow-2xl border border-pramuka-accent overflow-hidden my-8">
            <div class="bg-pramuka-primary text-white p-5 flex justify-between items-center border-b-4 border-pramuka-gold">
                <div class="flex items-center space-x-3">
                    <div class="w-9 h-9 rounded-lg bg-pramuka-yellow text-pramuka-dark flex items-center justify-center font-bold">
                        <i class="fa-solid fa-id-card"></i>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg leading-tight">Pendaftaran Jurnalis</h3>
                        <p class="text-xs text-pramuka-accent">Bergabung jadi kontributor jurnal_pramuka.co.id</p>
                    </div>
                </div>
                <button onclick="closeModal('register-modal')" class="text-gray-300 hover:text-white text-xl font-bold">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form onsubmit="handleJournalistRegister(event)" class="p-6 space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Nama Lengkap *</label>
                    <input type="text" id="reg-fullname" required placeholder="Contoh: Kak Dedi Supriadi" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Gugus Depan / Kwartir *</label>
                    <input type="text" id="reg-kwartir" required placeholder="Contoh: Kwarcab Jakarta Selatan / Gudep 02.101" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Email *</label>
                    <input type="email" id="reg-email" required placeholder="nama@email.com" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Password *</label>
                    <input type="password" id="reg-password" required placeholder="••••••••" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Bio / Alasan Bergabung</label>
                    <textarea id="reg-bio" rows="2" placeholder="Tuliskan pengalaman singkat atau motivasi jurnalistik Anda..." class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none"></textarea>
                </div>
                
                <div class="pt-2">
                    <button type="submit" class="w-full py-3 text-xs font-extrabold text-pramuka-dark bg-pramuka-yellow hover:bg-amber-400 rounded-xl shadow-lg transition transform active:scale-95 flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-user-plus"></i>
                        <span>Daftar Akun Jurnalis</span>
                    </button>
                </div>
                <p class="text-center text-xs text-gray-500 mt-2">Sudah punya akun? <a href="#" onclick="closeModal('register-modal'); openLoginModal();" class="text-pramuka-primary font-bold hover:underline">Login disini</a></p>
            </form>
        </div>
    </div>

    <!-- MODAL 2: LOGIN MODAL (JURNALIS & ADMIN) -->
    <div id="login-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-2xl max-w-sm w-full shadow-2xl border border-pramuka-accent overflow-hidden my-8">
            <div class="bg-pramuka-primary text-white p-5 flex justify-between items-center border-b-4 border-pramuka-gold">
                <div class="flex items-center space-x-3">
                    <div class="w-9 h-9 rounded-lg bg-pramuka-yellow text-pramuka-dark flex items-center justify-center font-bold">
                        <i class="fa-solid fa-right-to-bracket"></i>
                    </div>
                    <div>
                        <h3 class="font-bold text-lg leading-tight">Masuk Portal</h3>
                        <p class="text-xs text-pramuka-accent">Login Jurnalis atau Super Admin</p>
                    </div>
                </div>
                <button onclick="closeModal('login-modal')" class="text-gray-300 hover:text-white text-xl font-bold">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form onsubmit="handleLogin(event)" class="p-6 space-y-4">
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Email / Username</label>
                    <input type="text" id="login-email" required placeholder="admin / email jurnalis" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>
                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Password</label>
                    <input type="password" id="login-password" required placeholder="••••••••" class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>

                <div class="bg-pramuka-light p-3 rounded-xl text-[11px] text-gray-600 space-y-1">
                    <p class="font-bold text-pramuka-primary"><i class="fa-solid fa-key mr-1"></i> Akun Pengujian Demo:</p>
                    <p>• <strong>Super Admin:</strong> admin / admin123</p>
                    <p>• <strong>Jurnalis:</strong> jurnalis@pramuka.id / jurnalis123</p>
                </div>

                <div class="pt-2">
                    <button type="submit" class="w-full py-3 text-xs font-extrabold text-white bg-pramuka-primary hover:bg-pramuka-dark rounded-xl shadow-lg transition transform active:scale-95 flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-right-to-bracket"></i>
                        <span>Masuk Sekarang</span>
                    </button>
                </div>
                <p class="text-center text-xs text-gray-500 mt-2">Belum jadi Jurnalis? <a href="#" onclick="closeModal('login-modal'); openRegisterModal();" class="text-pramuka-primary font-bold hover:underline">Daftar Jurnalis</a></p>
            </form>
        </div>
    </div>

    <!-- MODAL 3: JOURNALIST WRITE & EDIT POST -->
    <div id="journalist-modal" class="fixed inset-0 bg-black/75 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-2xl max-w-2xl w-full shadow-2xl border border-pramuka-accent overflow-hidden my-8">
            <div class="bg-pramuka-primary text-white p-5 flex justify-between items-center border-b-4 border-pramuka-gold">
                <div class="flex items-center space-x-3">
                    <div class="w-9 h-9 rounded-lg bg-pramuka-yellow text-pramuka-dark flex items-center justify-center font-bold">
                        <i class="fa-solid fa-feather-pointed"></i>
                    </div>
                    <div>
                        <h3 id="journalist-modal-title" class="font-bold text-lg leading-tight">Panel Tulis Berita Jurnalis</h3>
                        <p class="text-xs text-pramuka-accent">Buat artikel, berita, atau event baru untuk publikasi</p>
                    </div>
                </div>
                <button onclick="closeModal('journalist-modal')" class="text-gray-300 hover:text-white text-xl font-bold">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <form id="post-form" onsubmit="savePost(event)" class="p-6 space-y-4">
                <input type="hidden" id="post-edit-id" value="">
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Penulis (Jurnalis)</label>
                        <input type="text" id="post-author" readonly class="w-full bg-gray-100 border border-gray-300 text-gray-600 text-sm rounded-xl p-2.5 font-semibold">
                    </div>
                    <div>
                        <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Kategori Tulisan *</label>
                        <select id="post-category" required class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                            <option value="Berita">Berita Pramuka</option>
                            <option value="Artikel">Artikel & Edukasi</option>
                            <option value="Info Event">Info Event & Kegiatan</option>
                            <option value="Pengumuman">Pengumuman Kwartir</option>
                        </select>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Judul Tulisan *</label>
                    <input type="text" id="post-title" required placeholder="Masukkan judul artikel yang informatif..." class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                </div>

                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">URL Foto / Banner Berita</label>
                    <div class="flex space-x-2">
                        <input type="url" id="post-image" placeholder="https://images.unsplash.com/photo-..." class="flex-1 bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5 focus:ring-2 focus:ring-pramuka-primary focus:outline-none">
                        <button type="button" onclick="setRandomPresetImage()" class="bg-pramuka-light border border-pramuka-accent text-pramuka-primary text-xs font-semibold px-3 py-2 rounded-xl hover:bg-pramuka-accent/20 transition whitespace-nowrap">
                            <i class="fa-solid fa-dice mr-1"></i> Gambar Acak
                        </button>
                    </div>
                </div>

                <div>
                    <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Isi Berita / Artikel *</label>
                    <textarea id="post-content" rows="6" required placeholder="Tuliskan isi artikel atau perincian berita secara lengkap..." class="w-full bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-xl p-3 focus:ring-2 focus:ring-pramuka-primary focus:outline-none"></textarea>
                </div>

                <div class="flex justify-end space-x-3 pt-3 border-t border-gray-100">
                    <button type="button" onclick="closeModal('journalist-modal')" class="px-5 py-2.5 text-xs font-bold text-gray-600 bg-gray-100 hover:bg-gray-200 rounded-xl transition">
                        Batal
                    </button>
                    <button type="submit" class="px-6 py-2.5 text-xs font-extrabold text-pramuka-dark bg-pramuka-yellow hover:bg-amber-400 rounded-xl shadow-lg transition transform active:scale-95 flex items-center space-x-2">
                        <i class="fa-solid fa-paper-plane"></i>
                        <span>Terbitkan Berita</span>
                    </button>
                </div>
            </form>
        </div>
    </div>

    <!-- MODAL 4: SUPER ADMIN DASHBOARD -->
    <div id="admin-modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-2xl max-w-4xl w-full shadow-2xl border border-pramuka-gold overflow-hidden my-8 max-h-[90vh] flex flex-col">
            <!-- Admin Header -->
            <div class="bg-pramuka-dark text-white p-5 flex justify-between items-center border-b-4 border-pramuka-gold flex-shrink-0">
                <div class="flex items-center space-x-3">
                    <div class="w-10 h-10 rounded-xl bg-pramuka-gold text-pramuka-dark flex items-center justify-center font-extrabold text-xl shadow">
                        <i class="fa-solid fa-user-shield"></i>
                    </div>
                    <div>
                        <h3 class="font-extrabold text-lg leading-tight text-pramuka-yellow">Panel Super Admin Portal</h3>
                        <p class="text-xs text-pramuka-accent">Kelola Pengaturan Web, Media Sosial, Jurnalis & Berita</p>
                    </div>
                </div>
                <button onclick="closeModal('admin-modal')" class="text-gray-300 hover:text-white text-xl font-bold p-1">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <!-- Admin Tabs Navigation -->
            <div class="bg-pramuka-primary text-white border-b border-pramuka-accent/30 flex space-x-1 px-4 text-xs font-bold flex-shrink-0">
                <button onclick="switchAdminTab('settings')" id="tab-btn-settings" class="admin-tab-btn active px-4 py-3 border-b-2 border-pramuka-yellow text-pramuka-yellow transition flex items-center space-x-2">
                    <i class="fa-solid fa-sliders"></i> <span>Pengaturan Web & URL</span>
                </button>
                <button onclick="switchAdminTab('socials')" id="tab-btn-socials" class="admin-tab-btn px-4 py-3 text-gray-300 hover:text-white transition flex items-center space-x-2">
                    <i class="fa-solid fa-share-nodes"></i> <span>Akses Media Sosial</span>
                </button>
                <button onclick="switchAdminTab('journalists')" id="tab-btn-journalists" class="admin-tab-btn px-4 py-3 text-gray-300 hover:text-white transition flex items-center space-x-2">
                    <i class="fa-solid fa-users-gear"></i> <span>Kelola Jurnalis</span>
                </button>
                <button onclick="switchAdminTab('posts')" id="tab-btn-posts" class="admin-tab-btn px-4 py-3 text-gray-300 hover:text-white transition flex items-center space-x-2">
                    <i class="fa-solid fa-newspaper"></i> <span>Moderasi Berita</span>
                </button>
            </div>

            <!-- Admin Tab Contents Body -->
            <div class="p-6 overflow-y-auto space-y-6 flex-1 bg-gray-50 text-sm">
                
                <!-- TAB 1: WEBSITE SETTINGS -->
                <div id="admin-tab-settings" class="admin-tab-content space-y-4">
                    <h4 class="font-bold text-pramuka-primary text-base border-b pb-2 flex items-center">
                        <i class="fa-solid fa-globe text-pramuka-gold mr-2"></i> Identitas & Banner Web
                    </h4>
                    <form onsubmit="saveSiteSettings(event)" class="space-y-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Nama Portal Utama</label>
                                <input type="text" id="adm-site-name" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Sub-Judul / Tagline</label>
                                <input type="text" id="adm-site-tagline" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                        </div>

                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1">Domain Web / Akses Meta URL</label>
                                <input type="text" id="adm-site-domain" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1">URL Foto Logo Web (Kosongkan utk default icon)</label>
                                <input type="url" id="adm-site-logo" placeholder="https://..." class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-bold text-gray-700 uppercase mb-1">URL Foto Sampul / Hero Banner Utama Web</label>
                            <input type="url" id="adm-site-banner" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                        </div>

                        <button type="submit" class="px-5 py-2.5 bg-pramuka-primary text-white text-xs font-extrabold rounded-xl hover:bg-pramuka-dark transition flex items-center space-x-2">
                            <i class="fa-solid fa-floppy-disk"></i> <span>Simpan Pengaturan Web</span>
                        </button>
                    </form>
                </div>

                <!-- TAB 2: SOCIAL MEDIA SETTINGS -->
                <div id="admin-tab-socials" class="admin-tab-content space-y-4 hidden">
                    <h4 class="font-bold text-pramuka-primary text-base border-b pb-2 flex items-center">
                        <i class="fa-solid fa-share-nodes text-pramuka-gold mr-2"></i> Akses Link Media Sosial Resmi
                    </h4>
                    <form onsubmit="saveSocialSettings(event)" class="space-y-4">
                        <div class="space-y-3">
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1"><i class="fa-brands fa-whatsapp text-emerald-600 mr-1"></i> WhatsApp Channel / Nomor Admin</label>
                                <input type="url" id="adm-soc-wa" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1"><i class="fa-brands fa-facebook text-blue-600 mr-1"></i> Facebook Page URL</label>
                                <input type="url" id="adm-soc-fb" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1"><i class="fa-brands fa-instagram text-pink-600 mr-1"></i> Instagram Account URL</label>
                                <input type="url" id="adm-soc-ig" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1"><i class="fa-brands fa-youtube text-red-600 mr-1"></i> YouTube Channel URL</label>
                                <input type="url" id="adm-soc-yt" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                            <div>
                                <label class="block text-xs font-bold text-gray-700 uppercase mb-1"><i class="fa-brands fa-tiktok text-black mr-1"></i> TikTok Account URL</label>
                                <input type="url" id="adm-soc-tiktok" required class="w-full bg-white border border-gray-300 text-gray-900 text-sm rounded-xl p-2.5">
                            </div>
                        </div>

                        <button type="submit" class="px-5 py-2.5 bg-pramuka-primary text-white text-xs font-extrabold rounded-xl hover:bg-pramuka-dark transition flex items-center space-x-2">
                            <i class="fa-solid fa-floppy-disk"></i> <span>Simpan Akses Medsos</span>
                        </button>
                    </form>
                </div>

                <!-- TAB 3: JOURNALISTS MANAGEMENT -->
                <div id="admin-tab-journalists" class="admin-tab-content space-y-4 hidden">
                    <h4 class="font-bold text-pramuka-primary text-base border-b pb-2 flex items-center">
                        <i class="fa-solid fa-users text-pramuka-gold mr-2"></i> Daftar Jurnalis Terdaftar
                    </h4>
                    <div class="overflow-x-auto bg-white rounded-xl border border-gray-200">
                        <table class="w-full text-left border-collapse text-xs">
                            <thead>
                                <tr class="bg-pramuka-primary text-white">
                                    <th class="p-3">Nama Jurnalis</th>
                                    <th class="p-3">Gugus Depan / Kwartir</th>
                                    <th class="p-3">Email</th>
                                    <th class="p-3">Status</th>
                                    <th class="p-3 text-right">Aksi</th>
                                </tr>
                            </thead>
                            <tbody id="adm-journalist-table">
                                <!-- Rendered dynamically -->
                            </tbody>
                        </table>
                    </div>
                </div>

                <!-- TAB 4: MODERATE ALL POSTS -->
                <div id="admin-tab-posts" class="admin-tab-content space-y-4 hidden">
                    <h4 class="font-bold text-pramuka-primary text-base border-b pb-2 flex items-center">
                        <i class="fa-solid fa-newspaper text-pramuka-gold mr-2"></i> Moderasi Seluruh Artikel & Berita
                    </h4>
                    <div class="overflow-x-auto bg-white rounded-xl border border-gray-200">
                        <table class="w-full text-left border-collapse text-xs">
                            <thead>
                                <tr class="bg-pramuka-primary text-white">
                                    <th class="p-3">Judul Berita</th>
                                    <th class="p-3">Kategori</th>
                                    <th class="p-3">Penulis</th>
                                    <th class="p-3">Tanggal</th>
                                    <th class="p-3 text-right">Aksi Moderasi</th>
                                </tr>
                            </thead>
                            <tbody id="adm-posts-table">
                                <!-- Rendered dynamically -->
                            </tbody>
                        </table>
                    </div>
                </div>

            </div>
        </div>
    </div>

    <!-- MODAL 5: FULL ARTICLE READER -->
    <div id="read-modal" class="fixed inset-0 bg-black/80 backdrop-blur-sm z-50 hidden flex items-center justify-center p-4 overflow-y-auto">
        <div class="bg-white rounded-2xl max-w-3xl w-full shadow-2xl overflow-hidden my-8 max-h-[90vh] flex flex-col">
            <div class="relative h-64 md:h-80 bg-pramuka-dark flex-shrink-0">
                <img id="read-img" src="" class="w-full h-full object-cover opacity-80" alt="Detail Image">
                <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/30 to-transparent"></div>
                <button onclick="closeModal('read-modal')" class="absolute top-4 right-4 bg-black/50 text-white hover:bg-black rounded-full w-9 h-9 flex items-center justify-center transition">
                    <i class="fa-solid fa-xmark text-lg"></i>
                </button>
                <div class="absolute bottom-4 left-6 right-6 text-white space-y-2">
                    <span id="read-category" class="bg-pramuka-yellow text-pramuka-dark font-extrabold text-[10px] uppercase px-2.5 py-1 rounded-md inline-block">
                        Category
                    </span>
                    <h2 id="read-title" class="text-xl md:text-2xl font-bold leading-snug drop-shadow-md">
                        Title
                    </h2>
                </div>
            </div>

            <div class="p-6 overflow-y-auto space-y-4 text-gray-700 text-sm md:text-base leading-relaxed flex-1">
                <div class="flex items-center justify-between text-xs text-gray-500 border-b border-gray-100 pb-3">
                    <span id="read-author"><i class="fa-solid fa-pen-nib text-pramuka-medium mr-1"></i> Oleh: Author</span>
                    <span id="read-date"><i class="fa-solid fa-clock text-pramuka-medium mr-1"></i> Tanggal</span>
                </div>
                <div id="read-content" class="space-y-3 whitespace-pre-line text-gray-800"></div>

                <!-- Social Share Buttons inside Reader -->
                <div class="mt-8 pt-4 border-t border-gray-200 bg-pramuka-light/50 p-4 rounded-xl">
                    <p class="text-xs font-bold text-pramuka-primary mb-2 uppercase tracking-wide">Bagikan Berita Ini ke Media Sosial:</p>
                    <div id="modal-social-share" class="flex flex-wrap gap-2"></div>
                </div>
            </div>

            <div class="p-4 bg-gray-50 border-t border-gray-100 flex justify-end">
                <button onclick="closeModal('read-modal')" class="px-5 py-2 text-xs font-bold text-white bg-pramuka-primary hover:bg-pramuka-dark rounded-xl transition">
                    Tutup Bacaan
                </button>
            </div>
        </div>
    </div>

    <!-- TOAST NOTIFICATION CONTAINER -->
    <div id="toast-container" class="fixed bottom-5 right-5 z-50 space-y-2 pointer-events-none"></div>

    <!-- FOOTER -->
    <footer class="bg-pramuka-dark text-white border-t-4 border-pramuka-gold mt-12">
        <div class="container mx-auto px-4 py-10">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Branding -->
                <div class="space-y-3">
                    <div class="flex items-center space-x-3">
                        <div class="w-9 h-9 rounded-full bg-pramuka-yellow text-pramuka-dark flex items-center justify-center font-bold text-lg">
                            <i class="fa-solid fa-compass"></i>
                        </div>
                        <span id="ftr-site-name" class="text-xl font-bold tracking-tight text-white">Jurnal<span class="text-pramuka-yellow">Pramuka</span></span>
                    </div>
                    <p class="text-xs text-pramuka-accent leading-relaxed">
                        Satu Nusa, Satu Bangsa, Satu Bahasa, dan Satu Pramuka. Portal jurnalisme warga dan warta resmi kepramukaan Indonesia.
                    </p>
                </div>

                <!-- Navigation Links -->
                <div>
                    <h4 class="text-sm font-bold text-pramuka-yellow uppercase tracking-wider mb-3">Navigasi Utama</h4>
                    <ul class="space-y-2 text-xs text-gray-300">
                        <li><a href="#" onclick="filterCategory('all')" class="hover:text-pramuka-yellow transition"><i class="fa-solid fa-chevron-right text-[10px] mr-1 text-pramuka-accent"></i> Beranda Utama</a></li>
                        <li><a href="#" onclick="filterCategory('Berita')" class="hover:text-pramuka-yellow transition"><i class="fa-solid fa-chevron-right text-[10px] mr-1 text-pramuka-accent"></i> Berita Kepramukaan</a></li>
                        <li><a href="#" onclick="filterCategory('Artikel')" class="hover:text-pramuka-yellow transition"><i class="fa-solid fa-chevron-right text-[10px] mr-1 text-pramuka-accent"></i> Artikel & Teknik Kepramukaan</a></li>
                        <li><a href="#" onclick="filterCategory('Info Event')" class="hover:text-pramuka-yellow transition"><i class="fa-solid fa-chevron-right text-[10px] mr-1 text-pramuka-accent"></i> Calendar Event & Lomba</a></li>
                    </ul>
                </div>

                <!-- Contact & Social -->
                <div class="space-y-3">
                    <h4 class="text-sm font-bold text-pramuka-yellow uppercase tracking-wider mb-3">Hubungi Redaksi</h4>
                    <p class="text-xs text-gray-300"><i class="fa-solid fa-envelope text-pramuka-yellow mr-1.5"></i> redaksi@<span id="ftr-domain">jurnal_pramuka.co.id</span></p>
                    <p class="text-xs text-gray-300"><i class="fa-solid fa-phone text-pramuka-yellow mr-1.5"></i> (021) 79191928 - Layanan Redaksi</p>
                    <div class="pt-2">
                        <span class="text-xs text-pramuka-accent block mb-2">Akses Media Sosial Resmi:</span>
                        <div class="flex space-x-2">
                            <a id="ftr-link-tiktok" href="#" target="_blank" class="w-8 h-8 rounded-lg bg-pramuka-primary hover:bg-pramuka-yellow hover:text-pramuka-dark text-white flex items-center justify-center transition text-sm"><i class="fa-brands fa-tiktok"></i></a>
                            <a id="ftr-link-youtube" href="#" target="_blank" class="w-8 h-8 rounded-lg bg-pramuka-primary hover:bg-pramuka-yellow hover:text-pramuka-dark text-white flex items-center justify-center transition text-sm"><i class="fa-brands fa-youtube"></i></a>
                            <a id="ftr-link-instagram" href="#" target="_blank" class="w-8 h-8 rounded-lg bg-pramuka-primary hover:bg-pramuka-yellow hover:text-pramuka-dark text-white flex items-center justify-center transition text-sm"><i class="fa-brands fa-instagram"></i></a>
                            <a id="ftr-link-facebook" href="#" target="_blank" class="w-8 h-8 rounded-lg bg-pramuka-primary hover:bg-pramuka-yellow hover:text-pramuka-dark text-white flex items-center justify-center transition text-sm"><i class="fa-brands fa-facebook-f"></i></a>
                            <a id="ftr-link-whatsapp" href="#" target="_blank" class="w-8 h-8 rounded-lg bg-pramuka-primary hover:bg-pramuka-yellow hover:text-pramuka-dark text-white flex items-center justify-center transition text-sm"><i class="fa-brands fa-whatsapp"></i></a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="border-t border-pramuka-primary/60 mt-8 pt-6 text-center text-xs text-pramuka-accent">
                <p>&copy; 2026 <span id="ftr-domain-copy">jurnal_pramuka.co.id</span> — Hak Cipta Dilindungi. Dibuat untuk Kemajuan Gerakan Pramuka Indonesia.</p>
            </div>
        </div>
    </footer>

    <!-- JAVASCRIPT APP STATE & LOGIC -->
    <script>
        // --- INITIAL DEFAULT DATA ---
        const DEFAULT_SETTINGS = {
            siteName: "Jurnal Pramuka",
            tagline: "Media Informasi Terkini",
            domain: "jurnal_pramuka.co.id",
            logoUrl: "",
            bannerUrl: "https://images.unsplash.com/photo-1526772662000-3f88f10405ff?auto=format&fit=crop&w=1200&q=80",
            socials: {
                whatsapp: "https://wa.me/628123456789",
                facebook: "https://facebook.com/jurnalpramuka",
                instagram: "https://instagram.com/jurnalpramuka",
                youtube: "https://youtube.com/@jurnalpramuka",
                tiktok: "https://tiktok.com/@jurnalpramuka"
            }
        };

        const INITIAL_POSTS = [
            {
                id: 101,
                title: "Persiapan Raimuna Nasional 2026: Ribuan Pramuka Penegak Siap Mengabdi untuk Negeri",
                category: "Berita",
                author: "Kak Rizky (Redaksi Kwarnas)",
                authorEmail: "jurnalis@pramuka.id",
                date: "5 Oktober 2026",
                image: "https://images.unsplash.com/photo-1526772662000-3f88f10405ff?auto=format&fit=crop&w=800&q=80",
                content: `Kwartir Nasional Gerakan Pramuka resmi membuka pendaftaran akhir untuk kontingen Raimuna Nasional 2026. Kegiatan lima tahunan bagi Pramuka Penegak dan Pandega ini diperkirakan akan dihadiri lebih dari 15.000 peserta dari 34 Kwartir Daerah serta kontingen luar negeri.\n\nTema yang diusung tahun ini berfokus pada digitalisasi gerakan kepramukaan, pemanfaatan energi terbarukan di perkemahan, serta aksi tanggap bencana berbasis komunitas.`
            },
            {
                id: 102,
                title: "Pendaftaran Lomba Tingkat V (LT-V) Penggalang Resmi Dibuka Bulan Ini",
                category: "Info Event",
                author: "Kak Siti Aisyah (Kwarda)",
                authorEmail: "siti@pramuka.id",
                date: "4 Oktober 2026",
                image: "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?auto=format&fit=crop&w=800&q=80",
                content: `Ajang bereprestasi tertinggi bagi Pramuka Penggalang, Lomba Tingkat V (LT-V), akan kembali digelar di Bumi Perkemahan Cibubur, Jakarta.\n\nMateri yang akan dilombakan meliputi pioneering bertingkat, orientering malam, navigasi kompas digital, semaphore speed battle, hingga pertunjukan seni budaya daerah.`
            },
            {
                id: 103,
                title: "Panduan Membuat Simpul & Ikatan Dasar Bagi Pramuka Siaga dan Penggalang",
                category: "Artikel",
                author: "Kak Budi Santoso (Pembina)",
                authorEmail: "budi@pramuka.id",
                date: "3 Oktober 2026",
                image: "https://images.unsplash.com/photo-1517649763962-0c623266ddc0?auto=format&fit=crop&w=800&q=80",
                content: `Tali temali merupakan salah satu keterampilan dasar (Scoutcraft) wajib dalam Gerakan Pramuka. Artikel ini membahas perbedaan mendasar antara simpul (knot) dan ikatan (lashing) serta penerapan praktisnya dalam membangun menara pandang.`
            }
        ];

        const INITIAL_JOURNALISTS = [
            {
                fullname: "Kak Rizky Pratama",
                kwartir: "Kwarcab Jakarta Selatan",
                email: "jurnalis@pramuka.id",
                password: "jurnalis123",
                bio: "Kontributor aktif berita kepramukaan wilayah DKI Jakarta.",
                status: "Approved"
            }
        ];

        // --- APP STATE VARIABLES ---
        let appSettings = JSON.parse(localStorage.getItem('jp_settings')) || DEFAULT_SETTINGS;
        let postsData = JSON.parse(localStorage.getItem('jp_posts')) || INITIAL_POSTS;
        let journalistsData = JSON.parse(localStorage.getItem('jp_journalists')) || INITIAL_JOURNALISTS;
        let currentUser = JSON.parse(localStorage.getItem('jp_user')) || null; // null, {role: 'journalist'|'admin', email, fullname}

        let activeCategory = 'all';
        let searchQuery = '';

        // --- DOM INITIALIZATION ---
        document.addEventListener("DOMContentLoaded", function() {
            applySiteSettings();
            updateAuthUI();
            renderPosts();
            renderSidebarEvents();
        });

        // Apply Settings to UI Elements
        function applySiteSettings() {
            document.getElementById('site-name-display').innerHTML = `Jurnal<span class="text-pramuka-yellow">${appSettings.siteName.replace('Jurnal', '') || 'Pramuka'}</span>`;
            document.getElementById('site-sub-display').innerText = appSettings.tagline;
            document.getElementById('top-domain-display').innerText = appSettings.domain;
            document.getElementById('ftr-domain').innerText = appSettings.domain;
            document.getElementById('ftr-domain-copy').innerText = appSettings.domain;
            document.getElementById('ftr-site-name').innerHTML = `Jurnal<span class="text-pramuka-yellow">${appSettings.siteName.replace('Jurnal', '') || 'Pramuka'}</span>`;
            
            // Meta & Logo
            document.title = `${appSettings.siteName} | Portal Berita & Event Pramuka`;
            if (appSettings.logoUrl) {
                document.getElementById('site-logo-img').src = appSettings.logoUrl;
                document.getElementById('site-logo-img').classList.remove('hidden');
                document.getElementById('default-logo-icon').classList.add('hidden');
            } else {
                document.getElementById('site-logo-img').classList.add('hidden');
                document.getElementById('default-logo-icon').classList.remove('hidden');
            }

            // Banner Image
            document.getElementById('hero-img').src = appSettings.bannerUrl;

            // Update All Social Links in DOM
            const socs = appSettings.socials;
            document.getElementById('hdr-link-whatsapp').href = socs.whatsapp;
            document.getElementById('hdr-link-facebook').href = socs.facebook;
            document.getElementById('hdr-link-instagram').href = socs.instagram;
            document.getElementById('hdr-link-youtube').href = socs.youtube;
            document.getElementById('hdr-link-tiktok').href = socs.tiktok;

            document.getElementById('sdb-link-whatsapp').href = socs.whatsapp;
            document.getElementById('sdb-link-facebook').href = socs.facebook;
            document.getElementById('sdb-link-instagram').href = socs.instagram;
            document.getElementById('sdb-link-youtube').href = socs.youtube;
            document.getElementById('sdb-link-tiktok').href = socs.tiktok;

            document.getElementById('ftr-link-whatsapp').href = socs.whatsapp;
            document.getElementById('ftr-link-facebook').href = socs.facebook;
            document.getElementById('ftr-link-instagram').href = socs.instagram;
            document.getElementById('ftr-link-youtube').href = socs.youtube;
            document.getElementById('ftr-link-tiktok').href = socs.tiktok;
        }

        // Save State
        function saveToStorage() {
            localStorage.setItem('jp_settings', JSON.stringify(appSettings));
            localStorage.setItem('jp_posts', JSON.stringify(postsData));
            localStorage.setItem('jp_journalists', JSON.stringify(journalistsData));
            localStorage.setItem('jp_user', JSON.stringify(currentUser));
        }

        // Update Authentication Header & Sidebar UI based on Role
        function updateAuthUI() {
            const authContainer = document.getElementById('auth-actions');
            const sidebarCta = document.getElementById('sidebar-cta-card');

            if (!currentUser) {
                // GUEST USER STATE
                authContainer.innerHTML = `
                    <button onclick="openLoginModal()" class="text-xs font-bold text-white hover:text-pramuka-yellow px-3 py-2 transition">
                        <i class="fa-solid fa-right-to-bracket mr-1"></i> Login
                    </button>
                    <button onclick="openRegisterModal()" class="bg-gradient-to-r from-pramuka-gold to-pramuka-yellow hover:from-pramuka-yellow hover:to-amber-400 text-pramuka-dark font-extrabold text-xs px-3.5 py-2 rounded-lg shadow transition transform hover:-translate-y-0.5 flex items-center space-x-1.5">
                        <i class="fa-solid fa-id-card"></i>
                        <span>Daftar Jurnalis</span>
                    </button>
                `;

                sidebarCta.innerHTML = `
                    <div class="flex items-center space-x-3 mb-3">
                        <div class="w-10 h-10 rounded-xl bg-pramuka-yellow/20 text-pramuka-yellow flex items-center justify-center font-bold text-lg">
                            <i class="fa-solid fa-id-card"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-base text-white">Ingin Menulis Berita?</h3>
                            <p class="text-xs text-pramuka-accent">Daftar Akun Jurnalis</p>
                        </div>
                    </div>
                    <p class="text-xs text-gray-200 mb-4 leading-relaxed">
                        Hanya jurnalis terdaftar yang dapat mempublikasikan warta kegiatan gudep atau event Kwartir ke portal ini.
                    </p>
                    <button onclick="openRegisterModal()" class="w-full bg-pramuka-yellow hover:bg-amber-400 text-pramuka-dark font-extrabold text-xs py-2.5 px-4 rounded-xl shadow transition flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-user-plus"></i>
                        <span>Daftar Jadi Jurnalis Sekarang</span>
                    </button>
                `;
            } else if (currentUser.role === 'journalist') {
                // JOURNALIST LOGGED IN STATE
                authContainer.innerHTML = `
                    <div class="hidden sm:flex items-center space-x-2 text-xs text-pramuka-accent font-semibold mr-2">
                        <i class="fa-solid fa-user-pen text-pramuka-yellow"></i>
                        <span>${currentUser.fullname}</span>
                    </div>
                    <button onclick="openJournalistModal()" class="bg-pramuka-yellow hover:bg-amber-400 text-pramuka-dark font-extrabold text-xs px-3.5 py-2 rounded-lg shadow transition flex items-center space-x-1.5">
                        <i class="fa-solid fa-pen-nib"></i>
                        <span>+ Tulis Berita</span>
                    </button>
                    <button onclick="handleLogout()" title="Keluar Akun" class="text-xs font-bold bg-red-900/60 hover:bg-red-800 text-white p-2 rounded-lg transition">
                        <i class="fa-solid fa-right-from-bracket"></i>
                    </button>
                `;

                sidebarCta.innerHTML = `
                    <div class="flex items-center space-x-3 mb-3">
                        <div class="w-10 h-10 rounded-xl bg-pramuka-yellow/20 text-pramuka-yellow flex items-center justify-center font-bold text-lg">
                            <i class="fa-solid fa-feather-pointed"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-base text-white">Halo, ${currentUser.fullname}</h3>
                            <p class="text-xs text-pramuka-accent">Status: Jurnalis Aktif</p>
                        </div>
                    </div>
                    <p class="text-xs text-gray-200 mb-4 leading-relaxed">
                        Siapkan liputan atau warta kegiatan terbaru dari kwartir atau gudep Anda dan publikasikan langsung.
                    </p>
                    <button onclick="openJournalistModal()" class="w-full bg-pramuka-yellow hover:bg-amber-400 text-pramuka-dark font-extrabold text-xs py-2.5 px-4 rounded-xl shadow transition flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-plus-circle"></i>
                        <span>Buat Artikel / Berita Baru</span>
                    </button>
                `;
            } else if (currentUser.role === 'admin') {
                // ADMIN LOGGED IN STATE
                authContainer.innerHTML = `
                    <div class="hidden sm:flex items-center space-x-2 text-xs text-pramuka-yellow font-bold mr-2">
                        <i class="fa-solid fa-user-shield"></i>
                        <span>Super Admin</span>
                    </div>
                    <button onclick="openAdminModal()" class="bg-pramuka-gold hover:bg-amber-400 text-pramuka-dark font-extrabold text-xs px-3.5 py-2 rounded-lg shadow transition flex items-center space-x-1.5">
                        <i class="fa-solid fa-sliders"></i>
                        <span>Dashboard Admin</span>
                    </button>
                    <button onclick="handleLogout()" title="Keluar Akun Admin" class="text-xs font-bold bg-red-900/60 hover:bg-red-800 text-white p-2 rounded-lg transition">
                        <i class="fa-solid fa-right-from-bracket"></i>
                    </button>
                `;

                sidebarCta.innerHTML = `
                    <div class="flex items-center space-x-3 mb-3">
                        <div class="w-10 h-10 rounded-xl bg-pramuka-gold/30 text-pramuka-yellow flex items-center justify-center font-bold text-lg">
                            <i class="fa-solid fa-user-shield"></i>
                        </div>
                        <div>
                            <h3 class="font-bold text-base text-white">Panel Super Admin</h3>
                            <p class="text-xs text-pramuka-accent">Kontrol Penuh Portal</p>
                        </div>
                    </div>
                    <p class="text-xs text-gray-200 mb-4 leading-relaxed">
                        Kelola URL, logo web, media sosial, persetujuan jurnalis, serta moderasi seluruh konten terbitan.
                    </p>
                    <button onclick="openAdminModal()" class="w-full bg-pramuka-gold hover:bg-amber-400 text-pramuka-dark font-extrabold text-xs py-2.5 px-4 rounded-xl shadow transition flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-sliders"></i>
                        <span>Buka Dashboard Admin</span>
                    </button>
                `;
            }
        }

        // Register Journalist
        function handleJournalistRegister(e) {
            e.preventDefault();
            const fullname = document.getElementById('reg-fullname').value.trim();
            const kwartir = document.getElementById('reg-kwartir').value.trim();
            const email = document.getElementById('reg-email').value.trim().toLowerCase();
            const password = document.getElementById('reg-password').value;
            const bio = document.getElementById('reg-bio').value.trim();

            if (journalistsData.some(j => j.email === email)) {
                showToast("Email tersebut sudah terdaftar!", "warning");
                return;
            }

            const newJournalist = {
                fullname, kwartir, email, password, bio, status: "Approved"
            };

            journalistsData.push(newJournalist);
            
            // Auto Login newly registered journalist
            currentUser = {
                role: 'journalist',
                fullname: newJournalist.fullname,
                email: newJournalist.email,
                kwartir: newJournalist.kwartir
            };

            saveToStorage();
            updateAuthUI();
            closeModal('register-modal');
            showToast("Pendaftaran Jurnalis berhasil! Anda sekarang bisa menulis berita.", "success");
        }

        // Login Handler (Admin or Journalist)
        function handleLogin(e) {
            e.preventDefault();
            const emailInput = document.getElementById('login-email').value.trim().toLowerCase();
            const passwordInput = document.getElementById('login-password').value;

            // Check Super Admin Credentials
            if ((emailInput === 'admin' || emailInput === 'admin@pramuka.id') && passwordInput === 'admin123') {
                currentUser = {
                    role: 'admin',
                    fullname: 'Super Admin',
                    email: 'admin@jurnal_pramuka.co.id'
                };
                saveToStorage();
                updateAuthUI();
                closeModal('login-modal');
                showToast("Selamat datang Kembali, Super Admin!", "success");
                return;
            }

            // Check Registered Journalists
            const foundJurnalis = journalistsData.find(j => j.email === emailInput && j.password === passwordInput);
            if (foundJurnalis) {
                currentUser = {
                    role: 'journalist',
                    fullname: foundJurnalis.fullname,
                    email: foundJurnalis.email,
                    kwartir: foundJurnalis.kwartir
                };
                saveToStorage();
                updateAuthUI();
                closeModal('login-modal');
                showToast(`Login berhasil! Selamat bertugas, ${foundJurnalis.fullname}.`, "success");
                return;
            }

            showToast("Email / Password salah! Periksa kembali akun Anda.", "warning");
        }

        // Logout Handler
        function handleLogout() {
            currentUser = null;
            saveToStorage();
            updateAuthUI();
            showToast("Anda telah keluar akun.", "info");
        }

        // Render Feed Posts
        function renderPosts() {
            const container = document.getElementById('posts-container');
            const emptyState = document.getElementById('empty-state');
            const badge = document.getElementById('post-count-badge');

            let filtered = postsData.filter(post => {
                const matchCategory = activeCategory === 'all' || post.category === activeCategory;
                const matchSearch = post.title.toLowerCase().includes(searchQuery.toLowerCase()) || 
                                    post.content.toLowerCase().includes(searchQuery.toLowerCase()) ||
                                    post.author.toLowerCase().includes(searchQuery.toLowerCase());
                return matchCategory && matchSearch;
            });

            badge.innerText = `${filtered.length} Artikel`;

            if (filtered.length === 0) {
                container.innerHTML = '';
                emptyState.classList.remove('hidden');
                return;
            }

            emptyState.classList.add('hidden');
            container.innerHTML = filtered.map(post => createPostCardHTML(post)).join('');
        }

        // Single Post Card HTML Component
        function createPostCardHTML(post) {
            let catBadgeColor = 'bg-pramuka-primary text-white';
            if (post.category === 'Info Event') catBadgeColor = 'bg-red-600 text-white';
            if (post.category === 'Artikel') catBadgeColor = 'bg-emerald-700 text-white';
            if (post.category === 'Pengumuman') catBadgeColor = 'bg-amber-600 text-white';

            const encodedTitle = encodeURIComponent(post.title);
            const currentUrl = encodeURIComponent(window.location.href);

            // Is the current user the author of this post or Admin?
            const isOwner = currentUser && (
                currentUser.role === 'admin' || 
                (currentUser.role === 'journalist' && currentUser.email === post.authorEmail)
            );

            return `
                <article class="bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-md transition border border-gray-200 flex flex-col md:flex-row group">
                    <div class="md:w-2/5 h-48 md:h-auto relative overflow-hidden bg-pramuka-dark flex-shrink-0">
                        <img src="${post.image}" alt="${post.title}" class="w-full h-full object-cover group-hover:scale-105 transition duration-500">
                        <span class="absolute top-3 left-3 ${catBadgeColor} font-extrabold text-[10px] uppercase px-2.5 py-1 rounded-md shadow">
                            ${post.category}
                        </span>
                    </div>

                    <div class="p-5 md:w-3/5 flex flex-col justify-between">
                        <div class="space-y-2">
                            <div class="flex items-center justify-between text-xs text-gray-400">
                                <span><i class="fa-solid fa-user-pen text-pramuka-gold mr-1"></i> ${post.author}</span>
                                <span><i class="fa-solid fa-clock text-pramuka-gold mr-1"></i> ${post.date}</span>
                            </div>

                            <h3 onclick="openReadModal(${post.id})" class="text-base md:text-lg font-bold text-gray-900 group-hover:text-pramuka-primary transition cursor-pointer line-clamp-2 leading-snug">
                                ${post.title}
                            </h3>

                            <p class="text-xs md:text-sm text-gray-600 line-clamp-2 leading-relaxed">
                                ${post.content}
                            </p>
                        </div>

                        <div class="mt-4 pt-3 border-t border-gray-100 flex items-center justify-between">
                            <div class="flex items-center space-x-3">
                                <button onclick="openReadModal(${post.id})" class="text-xs font-bold text-pramuka-primary hover:text-pramuka-medium flex items-center space-x-1">
                                    <span>Baca</span> <i class="fa-solid fa-arrow-right text-[10px]"></i>
                                </button>
                                ${isOwner ? `
                                    <button onclick="editPost(${post.id})" class="text-xs font-bold text-blue-600 hover:underline">
                                        <i class="fa-solid fa-pen-to-square"></i> Edit
                                    </button>
                                    <button onclick="deletePost(${post.id})" class="text-xs font-bold text-red-600 hover:underline">
                                        <i class="fa-solid fa-trash"></i> Hapus
                                    </button>
                                ` : ''}
                            </div>

                            <!-- Social Media Share -->
                            <div class="flex items-center space-x-1.5 text-gray-400">
                                <a href="https://api.whatsapp.com/send?text=${encodedTitle}%20${currentUrl}" target="_blank" title="WhatsApp" class="w-7 h-7 rounded-full bg-emerald-50 text-emerald-600 hover:bg-emerald-600 hover:text-white flex items-center justify-center transition text-xs">
                                    <i class="fa-brands fa-whatsapp"></i>
                                </a>
                                <a href="https://www.facebook.com/sharer/sharer.php?u=${currentUrl}" target="_blank" title="Facebook" class="w-7 h-7 rounded-full bg-blue-50 text-blue-600 hover:bg-blue-600 hover:text-white flex items-center justify-center transition text-xs">
                                    <i class="fa-brands fa-facebook-f"></i>
                                </a>
                                <button onclick="copyToClipboard('${post.title}')" title="TikTok Link" class="w-7 h-7 rounded-full bg-gray-100 text-gray-700 hover:bg-black hover:text-white flex items-center justify-center transition text-xs">
                                    <i class="fa-brands fa-tiktok"></i>
                                </button>
                                <a href="${appSettings.socials.instagram}" target="_blank" title="Instagram" class="w-7 h-7 rounded-full bg-pink-50 text-pink-600 hover:bg-pink-600 hover:text-white flex items-center justify-center transition text-xs">
                                    <i class="fa-brands fa-instagram"></i>
                                </a>
                                <a href="${appSettings.socials.youtube}" target="_blank" title="YouTube" class="w-7 h-7 rounded-full bg-red-50 text-red-600 hover:bg-red-600 hover:text-white flex items-center justify-center transition text-xs">
                                    <i class="fa-brands fa-youtube"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </article>
            `;
        }

        // Save Journalist / Admin Post (Create or Update)
        function savePost(e) {
            e.preventDefault();
            if (!currentUser) return;

            const editId = document.getElementById('post-edit-id').value;
            const category = document.getElementById('post-category').value;
            const title = document.getElementById('post-title').value.trim();
            let image = document.getElementById('post-image').value.trim();
            const content = document.getElementById('post-content').value.trim();

            if (!image) {
                image = "https://images.unsplash.com/photo-1526772662000-3f88f10405ff?auto=format&fit=crop&w=800&q=80";
            }

            if (editId) {
                // Update Existing Post
                const index = postsData.findIndex(p => p.id == editId);
                if (index !== -1) {
                    postsData[index].category = category;
                    postsData[index].title = title;
                    postsData[index].image = image;
                    postsData[index].content = content;
                    showToast("Artikel berhasil diperbarui!", "success");
                }
            } else {
                // Create New Post
                const newPost = {
                    id: Date.now(),
                    title: title,
                    category: category,
                    author: `${currentUser.fullname} (${currentUser.kwartir || 'Redaksi'})`,
                    authorEmail: currentUser.email,
                    date: "Baru Saja",
                    image: image,
                    content: content
                };
                postsData.unshift(newPost);
                showToast("Berita baru berhasil diterbitkan!", "success");
            }

            saveToStorage();
            renderPosts();
            renderSidebarEvents();
            closeModal('journalist-modal');
        }

        // Edit Post
        function editPost(id) {
            const post = postsData.find(p => p.id === id);
            if (!post) return;

            document.getElementById('post-edit-id').value = post.id;
            document.getElementById('post-author').value = post.author;
            document.getElementById('post-category').value = post.category;
            document.getElementById('post-title').value = post.title;
            document.getElementById('post-image').value = post.image;
            document.getElementById('post-content').value = post.content;

            document.getElementById('journalist-modal-title').innerText = "Edit Artikel / Berita";
            openModal('journalist-modal');
        }

        // Delete Post
        function deletePost(id) {
            if (confirm("Apakah Anda yakin ingin menghapus artikel berita ini?")) {
                postsData = postsData.filter(p => p.id !== id);
                saveToStorage();
                renderPosts();
                renderSidebarEvents();
                showToast("Artikel berita berhasil dihapus.", "info");
            }
        }

        // Open Super Admin Dashboard
        function openAdminModal() {
            // Populate Admin Settings Forms
            document.getElementById('adm-site-name').value = appSettings.siteName;
            document.getElementById('adm-site-tagline').value = appSettings.tagline;
            document.getElementById('adm-site-domain').value = appSettings.domain;
            document.getElementById('adm-site-logo').value = appSettings.logoUrl;
            document.getElementById('adm-site-banner').value = appSettings.bannerUrl;

            // Populate Social Forms
            document.getElementById('adm-soc-wa').value = appSettings.socials.whatsapp;
            document.getElementById('adm-soc-fb').value = appSettings.socials.facebook;
            document.getElementById('adm-soc-ig').value = appSettings.socials.instagram;
            document.getElementById('adm-soc-yt').value = appSettings.socials.youtube;
            document.getElementById('adm-soc-tiktok').value = appSettings.socials.tiktok;

            renderAdminJournalistsTable();
            renderAdminPostsTable();
            openModal('admin-modal');
        }

        // Save Web Settings (Admin)
        function saveSiteSettings(e) {
            e.preventDefault();
            appSettings.siteName = document.getElementById('adm-site-name').value.trim();
            appSettings.tagline = document.getElementById('adm-site-tagline').value.trim();
            appSettings.domain = document.getElementById('adm-site-domain').value.trim();
            appSettings.logoUrl = document.getElementById('adm-site-logo').value.trim();
            appSettings.bannerUrl = document.getElementById('adm-site-banner').value.trim();

            saveToStorage();
            applySiteSettings();
            showToast("Pengaturan Web berhasil diperbarui!", "success");
        }

        // Save Social Settings (Admin)
        function saveSocialSettings(e) {
            e.preventDefault();
            appSettings.socials.whatsapp = document.getElementById('adm-soc-wa').value.trim();
            appSettings.socials.facebook = document.getElementById('adm-soc-fb').value.trim();
            appSettings.socials.instagram = document.getElementById('adm-soc-ig').value.trim();
            appSettings.socials.youtube = document.getElementById('adm-soc-yt').value.trim();
            appSettings.socials.tiktok = document.getElementById('adm-soc-tiktok').value.trim();

            saveToStorage();
            applySiteSettings();
            showToast("Akses Media Sosial berhasil disimpan!", "success");
        }

        // Render Admin Journalist Management Table
        function renderAdminJournalistsTable() {
            const tbody = document.getElementById('adm-journalist-table');
            if (journalistsData.length === 0) {
                tbody.innerHTML = `<tr><td colspan="5" class="p-4 text-center text-gray-400">Belum ada jurnalis terdaftar.</td></tr>`;
                return;
            }

            tbody.innerHTML = journalistsData.map((j, idx) => `
                <tr class="border-b border-gray-100 hover:bg-gray-50">
                    <td class="p-3 font-bold">${j.fullname}</td>
                    <td class="p-3">${j.kwartir}</td>
                    <td class="p-3">${j.email}</td>
                    <td class="p-3"><span class="bg-emerald-100 text-emerald-800 text-[10px] px-2 py-0.5 rounded font-bold">${j.status}</span></td>
                    <td class="p-3 text-right">
                        <button onclick="deleteJournalist(${idx})" class="text-red-600 font-bold hover:underline text-xs">Hapus Akun</button>
                    </td>
                </tr>
            `).join('');
        }

        function deleteJournalist(index) {
            if (confirm("Hapus jurnalis ini dari sistem?")) {
                journalistsData.splice(index, 1);
                saveToStorage();
                renderAdminJournalistsTable();
                showToast("Akun Jurnalis dihapus.", "info");
            }
        }

        // Render Admin Posts Moderation Table
        function renderAdminPostsTable() {
            const tbody = document.getElementById('adm-posts-table');
            if (postsData.length === 0) {
                tbody.innerHTML = `<tr><td colspan="5" class="p-4 text-center text-gray-400">Belum ada postingan terbit.</td></tr>`;
                return;
            }

            tbody.innerHTML = postsData.map(p => `
                <tr class="border-b border-gray-100 hover:bg-gray-50">
                    <td class="p-3 font-bold text-gray-800">${p.title}</td>
                    <td class="p-3">${p.category}</td>
                    <td class="p-3">${p.author}</td>
                    <td class="p-3">${p.date}</td>
                    <td class="p-3 text-right space-x-2">
                        <button onclick="closeModal('admin-modal'); editPost(${p.id});" class="text-blue-600 font-bold hover:underline">Edit</button>
                        <button onclick="deletePost(${p.id}); renderAdminPostsTable();" class="text-red-600 font-bold hover:underline">Hapus</button>
                    </td>
                </tr>
            `).join('');
        }

        // Switch Tabs in Admin Dashboard
        function switchAdminTab(tabName) {
            document.querySelectorAll('.admin-tab-content').forEach(el => el.classList.add('hidden'));
            document.querySelectorAll('.admin-tab-btn').forEach(btn => {
                btn.classList.remove('active', 'border-b-2', 'border-pramuka-yellow', 'text-pramuka-yellow');
                btn.classList.add('text-gray-300');
            });

            document.getElementById(`admin-tab-${tabName}`).classList.remove('hidden');
            const activeBtn = document.getElementById(`tab-btn-${tabName}`);
            activeBtn.classList.add('active', 'border-b-2', 'border-pramuka-yellow', 'text-pramuka-yellow');
            activeBtn.classList.remove('text-gray-300');
        }

        // Render Sidebar Upcoming Events
        function renderSidebarEvents() {
            const container = document.getElementById('sidebar-events');
            const events = postsData.filter(p => p.category === 'Info Event').slice(0, 3);

            if(events.length === 0) {
                container.innerHTML = `<p class="text-xs text-gray-400">Belum ada agenda event terdekat.</p>`;
                return;
            }

            container.innerHTML = events.map(ev => `
                <div onclick="openReadModal(${ev.id})" class="flex space-x-3 p-2 rounded-xl hover:bg-pramuka-light/80 transition cursor-pointer border border-transparent hover:border-pramuka-accent/30">
                    <div class="w-12 h-12 rounded-lg bg-pramuka-dark overflow-hidden flex-shrink-0">
                        <img src="${ev.image}" class="w-full h-full object-cover" alt="Event">
                    </div>
                    <div class="flex-1 min-w-0">
                        <h4 class="text-xs font-bold text-gray-800 truncate hover:text-pramuka-primary">${ev.title}</h4>
                        <p class="text-[10px] text-gray-500 mt-0.5"><i class="fa-solid fa-calendar text-pramuka-gold mr-1"></i> ${ev.date}</p>
                    </div>
                </div>
            `).join('');
        }

        // Read Article Full Modal
        function openReadModal(id) {
            const post = postsData.find(p => p.id === id);
            if (!post) return;

            document.getElementById('read-title').innerText = post.title;
            document.getElementById('read-category').innerText = post.category;
            document.getElementById('read-author').innerHTML = `<i class="fa-solid fa-user-pen text-pramuka-medium mr-1"></i> Penulis: ${post.author}`;
            document.getElementById('read-date').innerHTML = `<i class="fa-solid fa-clock text-pramuka-medium mr-1"></i> ${post.date}`;
            document.getElementById('read-content').innerText = post.content;
            document.getElementById('read-img').src = post.image;

            const encodedTitle = encodeURIComponent(post.title);
            const currentUrl = encodeURIComponent(window.location.href);

            document.getElementById('modal-social-share').innerHTML = `
                <a href="https://api.whatsapp.com/send?text=${encodedTitle}%20${currentUrl}" target="_blank" class="px-3 py-1.5 rounded-lg bg-emerald-600 text-white text-xs font-bold flex items-center space-x-1.5 hover:bg-emerald-700 transition">
                    <i class="fa-brands fa-whatsapp text-sm"></i> <span>WhatsApp</span>
                </a>
                <a href="https://www.facebook.com/sharer/sharer.php?u=${currentUrl}" target="_blank" class="px-3 py-1.5 rounded-lg bg-blue-600 text-white text-xs font-bold flex items-center space-x-1.5 hover:bg-blue-700 transition">
                    <i class="fa-brands fa-facebook-f text-sm"></i> <span>Facebook</span>
                </a>
                <button onclick="copyToClipboard('${post.title}')" class="px-3 py-1.5 rounded-lg bg-black text-white text-xs font-bold flex items-center space-x-1.5 hover:bg-gray-800 transition">
                    <i class="fa-brands fa-tiktok text-sm"></i> <span>Salin Tautan TikTok</span>
                </button>
                <a href="${appSettings.socials.instagram}" target="_blank" class="px-3 py-1.5 rounded-lg bg-pink-600 text-white text-xs font-bold flex items-center space-x-1.5 hover:bg-pink-700 transition">
                    <i class="fa-brands fa-instagram text-sm"></i> <span>Instagram</span>
                </a>
                <a href="${appSettings.socials.youtube}" target="_blank" class="px-3 py-1.5 rounded-lg bg-red-600 text-white text-xs font-bold flex items-center space-x-1.5 hover:bg-red-700 transition">
                    <i class="fa-brands fa-youtube text-sm"></i> <span>YouTube</span>
                </a>
            `;

            openModal('read-modal');
        }

        // Open Journalist Write Modal
        function openJournalistModal() {
            if (!currentUser) {
                openLoginModal();
                return;
            }

            document.getElementById('post-form').reset();
            document.getElementById('post-edit-id').value = "";
            document.getElementById('post-author').value = `${currentUser.fullname} (${currentUser.kwartir || 'Redaksi'})`;
            document.getElementById('journalist-modal-title').innerText = "Panel Tulis Berita Jurnalis";
            openModal('journalist-modal');
        }

        // Modal Utilities
        function openModal(id) {
            document.getElementById(id).classList.remove('hidden');
        }

        function closeModal(id) {
            document.getElementById(id).classList.add('hidden');
        }

        function openRegisterModal() { openModal('register-modal'); }
        function openLoginModal() { openModal('login-modal'); }

        // Category Filter & Search
        function filterCategory(cat) {
            activeCategory = cat;
            const buttons = document.querySelectorAll('.cat-btn');
            buttons.forEach(btn => {
                if (btn.innerText.includes(cat) || (cat === 'all' && btn.innerText.includes('Semua'))) {
                    btn.classList.add('text-pramuka-yellow', 'border-b-2', 'border-pramuka-yellow');
                    btn.classList.remove('text-gray-300');
                } else {
                    btn.classList.remove('text-pramuka-yellow', 'border-b-2', 'border-pramuka-yellow');
                    btn.classList.add('text-gray-300');
                }
            });

            const titleEl = document.getElementById('section-title');
            if (cat === 'all') titleEl.innerHTML = `<i class="fa-solid fa-layer-group text-pramuka-gold mr-2"></i> Semua Terbitan Terbaru`;
            else titleEl.innerHTML = `<i class="fa-solid fa-filter text-pramuka-gold mr-2"></i> Kategori: ${cat}`;

            renderPosts();
        }

        function handleSearch() {
            searchQuery = document.getElementById('search-input').value;
            renderPosts();
        }

        function handleSearchMobile() {
            searchQuery = document.getElementById('search-input-mobile').value;
            renderPosts();
        }

        function toggleMobileMenu() {
            document.getElementById('mobile-menu').classList.toggle('hidden');
        }

        function setRandomPresetImage() {
            const presets = [
                "https://images.unsplash.com/photo-1504280390367-361c6d9f38f4?auto=format&fit=crop&w=800&q=80",
                "https://images.unsplash.com/photo-1517649763962-0c623266ddc0?auto=format&fit=crop&w=800&q=80",
                "https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?auto=format&fit=crop&w=800&q=80",
                "https://images.unsplash.com/photo-1542601906990-b4d3fb778b09?auto=format&fit=crop&w=800&q=80"
            ];
            const random = presets[Math.floor(Math.random() * presets.length)];
            document.getElementById('post-image').value = random;
            showToast("Gambar sampel terpilih!", "info");
        }

        function copyToClipboard(text) {
            const dummy = document.createElement('textarea');
            document.body.appendChild(dummy);
            dummy.value = `[${appSettings.siteName}] ${text} - Baca selengkapnya di ${appSettings.domain}`;
            dummy.select();
            document.execCommand('copy');
            document.body.removeChild(dummy);
            showToast("Tautan berita berhasil disalin ke clipboard!", "success");
        }

        // Toast System
        function showToast(message, type = "info") {
            const container = document.getElementById('toast-container');
            const toast = document.createElement('div');

            let bgColor = "bg-pramuka-primary text-white";
            if (type === "success") bgColor = "bg-emerald-700 text-white";
            if (type === "warning") bgColor = "bg-amber-600 text-white";

            toast.className = `${bgColor} px-4 py-3 rounded-xl shadow-2xl text-xs font-bold flex items-center space-x-2 border border-white/20 transform transition-all duration-300 translate-y-5 opacity-0`;
            toast.innerHTML = `<i class="fa-solid fa-circle-check text-pramuka-yellow"></i> <span>${message}</span>`;

            container.appendChild(toast);
            setTimeout(() => toast.classList.remove('translate-y-5', 'opacity-0'), 50);
            setTimeout(() => {
                toast.classList.add('translate-y-5', 'opacity-0');
                setTimeout(() => toast.remove(), 300);
            }, 3500);
        }
    </script>
</body>
</html>
