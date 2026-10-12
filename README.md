<!DOCTYPE html>
<html lang="vi" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc Mừng 20/10 - Tôn Vinh Tất Cả Phụ Nữ Việt Nam</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400&family=Dancing+Script:wght@600;700&family=Great+Vibes&family=Playfair+Display:ital,wght@0,400;0,600;0,700;0,800;0,900;1,400;1,600&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Canvas Confetti Library CDN -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.9.2/dist/confetti.browser.min.js"></script>

    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        gold: {
                            100: '#FFF8E1',
                            200: '#F5E3A9',
                            300: '#E6C665',
                            400: '#D4AF37', // Champagne Gold
                            500: '#B89028',
                            600: '#916E19',
                            700: '#6D500E',
                        },
                        rosegold: {
                            DEFAULT: '#B76E79',
                            light: '#E8B4B8',
                            soft: '#F4D3D5'
                        },
                        burgundy: {
                            800: '#4A0413',
                            900: '#2A0209',
                            950: '#170206' // Soft Dark Ivory-Burgundy Background
                        }
                    },
                    fontFamily: {
                        serif: ['Playfair Display', 'serif'],
                        sans: ['Be Vietnam Pro', 'sans-serif'],
                        handwriting: ['Dancing Script', 'cursive'],
                        script: ['Great Vibes', 'cursive']
                    }
                }
            }
        }
    </script>

    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #170206;
        }
        ::-webkit-scrollbar-thumb {
            background: #B89028;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #D4AF37;
        }

        /* Gold Gradient Text */
        .text-gold-gradient {
            background: linear-gradient(135deg, #FFF8E1 0%, #D4AF37 50%, #AA7C11 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .text-rose-gradient {
            background: linear-gradient(135deg, #FFFFFF 0%, #E8B4B8 50%, #D4AF37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* Glassmorphism Styles */
        .glass-card {
            background: rgba(42, 2, 9, 0.65);
            backdrop-filter: blur(18px);
            -webkit-backdrop-filter: blur(18px);
            border: 1px solid rgba(212, 175, 55, 0.25);
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.6), inset 0 0 15px rgba(212, 175, 55, 0.05);
        }

        .glass-card-hover {
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
        }
        .glass-card-hover:hover {
            transform: translateY(-6px) scale(1.01);
            border-color: rgba(212, 175, 55, 0.6);
            box-shadow: 0 20px 45px rgba(212, 175, 55, 0.22), inset 0 0 20px rgba(212, 175, 55, 0.15);
        }

        /* Gold Shimmer Button Effect */
        .btn-gold {
            background: linear-gradient(135deg, #D4AF37 0%, #B89028 50%, #8A6412 100%);
            background-size: 200% 200%;
            transition: all 0.4s ease;
            position: relative;
            overflow: hidden;
        }
        .btn-gold:hover {
            background-position: right center;
            box-shadow: 0 0 30px rgba(212, 175, 55, 0.6);
            transform: translateY(-2px);
        }
        .btn-gold::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: rgba(255, 255, 255, 0.2);
            transform: rotate(45deg) translateY(-100%);
            transition: all 0.7s ease;
        }
        .btn-gold:hover::before {
            transform: rotate(45deg) translateY(100%);
        }

        /* 3D Envelope Styles */
        .envelope-wrapper {
            perspective: 1000px;
        }
        
        .envelope {
            position: relative;
            width: 320px;
            height: 220px;
            background: #3B030E;
            border-radius: 8px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.8), 0 0 25px rgba(212, 175, 55, 0.25);
            border: 2px solid #D4AF37;
            cursor: pointer;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }
        @media (min-width: 640px) {
            .envelope {
                width: 440px;
                height: 280px;
            }
        }

        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 0;
            border-left: 160px solid transparent;
            border-right: 160px solid transparent;
            border-top: 130px solid #5C061C;
            transform-origin: top;
            transition: transform 0.6s 0.4s ease-in-out, z-index 0.2s 0.4s;
            z-index: 5;
            filter: drop-shadow(0 4px 6px rgba(0,0,0,0.5));
        }
        @media (min-width: 640px) {
            .envelope-flap {
                border-left-width: 220px;
                border-right-width: 220px;
                border-top-width: 160px;
            }
        }

        .envelope.open .envelope-flap {
            transform: rotateX(180deg);
            z-index: 1;
            transition: transform 0.6s ease-in-out, z-index 0.2s 0.3s;
        }

        .envelope-pocket {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, #4A0413 0%, #2A0209 100%);
            clip-path: polygon(0 0, 50% 50%, 100% 0, 100% 100%, 0 100%);
            z-index: 3;
            border-bottom-left-radius: 6px;
            border-bottom-right-radius: 6px;
        }

        .wax-seal {
            position: absolute;
            top: 110px;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 62px;
            height: 62px;
            background: radial-gradient(circle, #D4AF37 0%, #8A6412 100%);
            border-radius: 50%;
            box-shadow: 0 4px 12px rgba(0,0,0,0.7), inset 0 2px 4px rgba(255,255,255,0.4);
            display: flex;
            align-items: center;
            justify-content: center;
            z-index: 6;
            transition: all 0.5s ease;
            border: 2px solid #FFF8E1;
        }
        @media (min-width: 640px) {
            .wax-seal {
                top: 135px;
                width: 72px;
                height: 72px;
            }
        }

        .envelope.open .wax-seal {
            opacity: 0;
            transform: translate(-50%, -50%) scale(1.5);
            pointer-events: none;
        }

        .letter-preview {
            position: absolute;
            bottom: 15px;
            left: 5%;
            width: 90%;
            height: 82%;
            background: #FFFDF7;
            border-radius: 6px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 2;
            transition: transform 0.8s 0.6s cubic-bezier(0.34, 1.56, 0.64, 1);
            color: #2A0209;
            border: 1px solid #D4AF37;
            overflow: hidden;
        }

        .envelope.open .letter-preview {
            transform: translateY(-120px) scale(1.05);
            z-index: 4;
        }
        @media (min-width: 640px) {
            .envelope.open .letter-preview {
                transform: translateY(-155px) scale(1.08);
            }
        }

        /* Pulse glow animation */
        @keyframes subtleGlow {
            0%, 100% { box-shadow: 0 0 15px rgba(212, 175, 55, 0.3); }
            50% { box-shadow: 0 0 35px rgba(212, 175, 55, 0.75); }
        }
        .glow-pulse {
            animation: subtleGlow 3s infinite ease-in-out;
        }

        /* Custom Cursor for Desktop */
        @media (min-width: 1024px) {
            body {
                cursor: default;
            }
            .custom-cursor {
                pointer-events: none;
                position: fixed;
                width: 26px;
                height: 26px;
                border: 2px solid rgba(212, 175, 55, 0.7);
                border-radius: 50%;
                transition: transform 0.15s ease-out, opacity 0.2s ease;
                z-index: 9999;
                transform: translate(-50%, -50%);
            }
            .custom-cursor-dot {
                pointer-events: none;
                position: fixed;
                width: 6px;
                height: 6px;
                background-color: #D4AF37;
                border-radius: 50%;
                z-index: 10000;
                transform: translate(-50%, -50%);
                box-shadow: 0 0 10px #D4AF37;
            }
        }
    </style>
</head>
<body class="bg-burgundy-950 text-slate-100 font-sans antialiased selection:bg-gold-400 selection:text-burgundy-950 min-h-screen relative overflow-x-hidden">

    <!-- Background Canvas for Rose Petals & Gold Dust Particles -->
    <canvas id="particleCanvas" class="fixed inset-0 pointer-events-none z-0"></canvas>

    <!-- Custom Cursor (Desktop) -->
    <div id="cursorRing" class="custom-cursor hidden lg:block"></div>
    <div id="cursorDot" class="custom-cursor-dot hidden lg:block"></div>

    <header class="fixed top-0 left-0 w-full z-40 bg-burgundy-950/75 backdrop-blur-md border-b border-gold-400/20 py-4 px-6 transition-all duration-300">
        <div class="max-w-6xl mx-auto flex items-center justify-between">
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-gold-500 to-gold-300 flex items-center justify-center text-burgundy-950 font-serif font-bold text-lg shadow-lg group-hover:rotate-12 transition-transform">
                    20
                </div>
                <div class="flex flex-col">
                    <span class="font-serif text-base sm:text-lg font-bold text-gold-gradient tracking-wider">TÔN VINH PHỤ NỮ VIỆT NAM</span>
                    <span class="text-[10px] text-rosegold-light tracking-widest uppercase">20 Tháng 10 • Dành Cho Tất Cả Phái Đẹp</span>
                </div>
            </a>

            <!-- Nav Links -->
            <nav class="hidden md:flex items-center gap-8 text-sm font-medium">
                <a href="#hero" class="text-slate-300 hover:text-gold-300 transition-colors">Trang Chủ</a>
                <a href="#wishes" class="text-slate-300 hover:text-gold-300 transition-colors">Lời Chúc Tự Chọn</a>
                <a href="#envelope" class="text-slate-300 hover:text-gold-300 transition-colors">Bức Thư Phong Ấn</a>
                <a href="#all-women" class="text-slate-300 hover:text-gold-300 transition-colors">Tất Cả Phái Đẹp</a>
            </nav>

            <button onclick="triggerFireworks()" class="px-4 py-2 text-xs font-semibold rounded-full border border-gold-400/40 text-gold-300 hover:bg-gold-400/10 transition-all flex items-center gap-2 shadow-sm">
                <i class="fa-solid fa-wand-magic-sparkles text-gold-400"></i>
                <span>Pháo Hoa</span>
            </button>
        </div>
    </header>

    <!-- Main Content Container -->
    <main class="relative z-10 pt-20">

        <section id="hero" class="min-h-[88vh] flex items-center justify-center relative px-4 py-16">
            <div class="max-w-4xl mx-auto text-center space-y-8 relative">
                
                <!-- Badge -->
                <div class="inline-flex items-center gap-2 px-5 py-2 rounded-full bg-gold-400/10 border border-gold-400/30 text-gold-300 text-xs sm:text-sm font-medium tracking-widest uppercase shadow-inner">
                    <i class="fa-solid fa-crown text-gold-400 animate-pulse"></i>
                    <span>Ngày Phụ Nữ Việt Nam 20/10</span>
                </div>

                <!-- Main Title -->
                <h1 class="font-serif text-3xl sm:text-5xl md:text-6xl lg:text-7xl font-extrabold text-gold-gradient leading-tight tracking-tight drop-shadow-2xl">
                    Tôn Vinh Vẻ Đẹp <br class="hidden sm:inline"/>
                    <span class="font-script text-4xl sm:text-6xl md:text-7xl font-normal text-rose-gradient px-2"> & </span>
                    Bản Lĩnh Phụ Nữ Việt
                </h1>

                <!-- Subtitle -->
                <p class="text-slate-200 text-base sm:text-xl max-w-2xl mx-auto font-light leading-relaxed">
                    Dành tặng Mẹ kính yêu, Người Yêu, Vợ, Cô Giáo, Chị Em Gái, Đồng Nghiệp và <strong class="text-gold-300 font-semibold">TẤT CẢ</strong> những người phụ nữ tuyệt vời – nguồn cảm hứng dịu dàng nuôi dưỡng cuộc đời!
                </p>

                <!-- CTA Button Group -->
                <div class="pt-6 flex flex-col sm:flex-row items-center justify-center gap-4">
                    <a href="#wishes" class="btn-gold px-8 py-4 rounded-full font-bold text-burgundy-950 text-sm sm:text-base tracking-wide flex items-center gap-3 shadow-xl glow-pulse">
                        <span>Khám Phá Món Quà Yêu Thương</span>
                        <i class="fa-solid fa-arrow-down text-burgundy-950"></i>
                    </a>
                    
                    <a href="#envelope" class="px-8 py-4 rounded-full font-semibold text-gold-300 border border-gold-400/40 hover:bg-gold-400/10 transition-all text-sm sm:text-base flex items-center gap-2 backdrop-blur-sm">
                        <i class="fa-solid fa-envelope-open-text text-gold-400"></i>
                        <span>Mở Thiệp Phong Ấn</span>
                    </a>
                </div>

                <!-- Decorative Quotes -->
                <div class="pt-10 text-center">
                    <p class="font-handwriting text-2xl sm:text-3xl text-rosegold-light opacity-90">
                        "Mỗi người phụ nữ là một bông hoa độc bản, khoe sắc rực rỡ và tỏa ngát hương thơm."
                    </p>
                </div>
            </div>
        </section>


        <section id="wishes" class="py-20 px-4 max-w-5xl mx-auto">
            <div class="text-center space-y-4 mb-12">
                <h2 class="font-serif text-3xl sm:text-4xl font-bold text-gold-gradient">
                    Lời Chúc Chân Thành Dành Cho Tất Cả Phái Đẹp
                </h2>
                <p class="text-slate-300 text-sm sm:text-base max-w-xl mx-auto">
                    Chọn đối tượng trao gửi tình cảm, nhập tên riêng cá nhân hóa và tạo ngay thông điệp đong đầy yêu thương.
                </p>
            </div>

            <!-- Card Container -->
            <div class="glass-card rounded-3xl p-6 sm:p-10 relative overflow-hidden border border-gold-400/30">
                
                <!-- Recipient Selection Tabs (General & Dedicated Categories) -->
                <div class="flex flex-wrap items-center justify-center gap-2 sm:gap-3 mb-8">
                    <button onclick="selectCategory('all')" id="tab-all" class="category-btn active px-4 py-2.5 rounded-full text-xs sm:text-sm font-semibold border border-gold-400/40 transition-all flex items-center gap-2 shadow-sm">
                        <i class="fa-solid fa-rose text-pink-400"></i> Tất Cả Phái Đẹp
                    </button>
                    <button onclick="selectCategory('mom')" id="tab-mom" class="category-btn px-4 py-2.5 rounded-full text-xs sm:text-sm font-medium border border-gold-400/30 text-slate-300 hover:text-gold-300 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-crown text-amber-300"></i> Mẹ Kính Yêu
                    </button>
                    <button onclick="selectCategory('lover')" id="tab-lover" class="category-btn px-4 py-2.5 rounded-full text-xs sm:text-sm font-medium border border-gold-400/30 text-slate-300 hover:text-gold-300 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-heart text-red-400"></i> Người Yêu / Vợ
                    </button>
                    <button onclick="selectCategory('colleague')" id="tab-colleague" class="category-btn px-4 py-2.5 rounded-full text-xs sm:text-sm font-medium border border-gold-400/30 text-slate-300 hover:text-gold-300 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-sun text-yellow-400"></i> Đồng Nghiệp & Bạn Bè
                    </button>
                    <button onclick="selectCategory('teacher')" id="tab-teacher" class="category-btn px-4 py-2.5 rounded-full text-xs sm:text-sm font-medium border border-gold-400/30 text-slate-300 hover:text-gold-300 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-book-bookmark text-blue-300"></i> Cô Giáo Kính Yêu
                    </button>
                    <button onclick="selectCategory('sister')" id="tab-sister" class="category-btn px-4 py-2.5 rounded-full text-xs sm:text-sm font-medium border border-gold-400/30 text-slate-300 hover:text-gold-300 transition-all flex items-center gap-2">
                        <i class="fa-solid fa-sparkles text-rosegold-light"></i> Chị Em Gái
                    </button>
                </div>

                <!-- Input Recipient Name -->
                <div class="max-w-md mx-auto mb-8 space-y-2">
                    <label for="recipientName" class="block text-xs font-semibold text-gold-300 uppercase tracking-wider text-center">
                        <i class="fa-solid fa-pen-nib mr-1"></i> Nhập Tên Người Nhận (VD: Chị Ngọc, Mẹ Yêu, Em Trang...)
                    </label>
                    <div class="relative">
                        <input type="text" id="recipientName" value="Chị Em Phụ Nữ" 
                            class="w-full bg-burgundy-900/80 border border-gold-400/40 rounded-xl px-4 py-3 text-center font-medium text-gold-100 placeholder-slate-500 focus:outline-none focus:border-gold-300 focus:ring-2 focus:ring-gold-400/30 transition-all text-lg"
                            placeholder="Nhập tên người nhận...">
                    </div>
                </div>

                <!-- Typed Wish Display Box -->
                <div class="bg-burgundy-950/70 rounded-2xl p-6 sm:p-8 border border-gold-400/20 relative min-h-[220px] flex flex-col justify-between">
                    <div class="text-gold-400/20 text-6xl font-serif absolute top-2 left-4 select-none">“</div>
                    <div class="text-gold-400/20 text-6xl font-serif absolute bottom-2 right-4 select-none">”</div>

                    <!-- Typewriter Text Output -->
                    <div id="wishOutput" class="text-slate-100 text-base sm:text-lg leading-relaxed font-sans relative z-10 my-4 min-h-[120px]">
                        <!-- Dynamic Typewriter Text -->
                    </div>

                    <!-- Card Action Buttons -->
                    <div class="flex flex-wrap items-center justify-between gap-4 pt-4 border-t border-gold-400/10 relative z-10">
                        <div class="flex items-center gap-2 text-xs text-rosegold-light">
                            <i class="fa-solid fa-wand-magic-sparkles text-gold-400"></i>
                            <span>Tên người nhận tự động khớp vào từng dòng chúc</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <button onclick="retypeWish()" class="px-4 py-2 rounded-lg bg-burgundy-900/90 hover:bg-burgundy-800 border border-gold-400/30 text-gold-300 text-xs font-medium transition-all flex items-center gap-1.5">
                                <i class="fa-solid fa-rotate-right"></i>
                                <span>Tạo Lại</span>
                            </button>
                            <button onclick="copyWishText()" class="btn-gold px-5 py-2 rounded-lg text-burgundy-950 font-bold text-xs shadow-md flex items-center gap-1.5">
                                <i class="fa-solid fa-copy"></i>
                                <span>Sao Chép Lời Chúc</span>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </section>


        <section id="envelope" class="py-20 px-4 bg-gradient-to-b from-transparent via-burgundy-900/40 to-transparent">
            <div class="max-w-4xl mx-auto text-center space-y-6">
                
                <div class="space-y-3">
                    <span class="text-xs font-bold text-gold-400 uppercase tracking-widest px-3 py-1 rounded-full border border-gold-400/30">Món Quà Bí Mật</span>
                    <h2 class="font-serif text-3xl sm:text-4xl font-bold text-gold-gradient">
                        Bức Thư Phong Ấn Mạ Vàng
                    </h2>
                    <p class="text-slate-300 text-sm sm:text-base">
                        Chạm nhẹ vào con dấu sáp hoàng gia để mở ra thông điệp thiêng liêng gửi tới <span id="envelopeRecipientLabel" class="text-gold-300 font-semibold">Chị Em Phụ Nữ</span>.
                    </p>
                </div>

                <!-- 3D Interactive Envelope Container -->
                <div class="pt-12 pb-20 flex justify-center items-center">
                    <div class="envelope-wrapper">
                        <div id="mainEnvelope" onclick="toggleEnvelope()" class="envelope group">
                            <!-- Flap -->
                            <div class="envelope-flap"></div>
                            
                            <!-- Wax Seal -->
                            <div class="wax-seal">
                                <span class="font-serif font-extrabold text-xs text-burgundy-950 tracking-tighter">20/10</span>
                            </div>

                            <!-- Letter Inside Preview -->
                            <div class="letter-preview flex flex-col justify-center text-center">
                                <h3 class="font-serif text-base sm:text-lg font-bold text-burgundy-900 mb-2">
                                    Gửi <span id="letterNamePreview">Chị Em Phụ Nữ</span>
                                </h3>
                                <p class="font-handwriting text-lg sm:text-xl text-burgundy-800 leading-snug">
                                    "Chúc bạn một đời bình an, tỏa sáng theo cách riêng và luôn trọn vẹn hạnh phúc!"
                                </p>
                                <div class="mt-4 pt-2 border-t border-gold-400/40 text-[11px] font-serif text-gold-700 italic">
                                    Click để mở toàn thư ✨
                                </div>
                            </div>

                            <!-- Front Pocket -->
                            <div class="envelope-pocket"></div>
                        </div>
                    </div>
                </div>

                <!-- Interactive Trigger Buttons -->
                <div class="flex flex-wrap items-center justify-center gap-4">
                    <button onclick="toggleEnvelope(true)" class="btn-gold px-8 py-3.5 rounded-full font-bold text-burgundy-950 text-sm shadow-lg flex items-center gap-2">
                        <i class="fa-solid fa-envelope-open"></i>
                        <span>Mở Thiệp Ngay</span>
                    </button>
                    <button onclick="triggerFireworks()" class="px-6 py-3.5 rounded-full border border-gold-400/40 text-gold-300 hover:bg-gold-400/10 transition-all text-sm font-semibold flex items-center gap-2">
                        <i class="fa-solid fa-champagne-glasses text-gold-400"></i>
                        <span>Bắn Pháo Hoa Cánh Hoa</span>
                    </button>
                </div>
            </div>
        </section>


        <section id="all-women" class="py-20 px-4 max-w-5xl mx-auto">
            <div class="text-center space-y-4 mb-16">
                <h2 class="font-serif text-3xl sm:text-4xl font-bold text-gold-gradient">
                    Tất Cả Phụ Nữ Là Những Bông Hoa Tỏa Sáng
                </h2>
                <p class="text-slate-300 text-sm sm:text-base max-w-xl mx-auto">
                    Dù ở bất kỳ vị trí nào, phái đẹp luôn cống hiến, lan tỏa tình yêu thương và làm cho thế giới trở nên tốt đẹp hơn.
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <!-- Honor Card 1 -->
                <div class="glass-card glass-card-hover rounded-2xl p-6 text-center space-y-4 border border-gold-400/20">
                    <div class="w-16 h-16 rounded-full bg-gold-400/10 border border-gold-400/40 flex items-center justify-center text-gold-400 mx-auto text-2xl">
                        <i class="fa-solid fa-gem"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-gold-100">Sang Trọng & Tự Tin</h3>
                    <p class="text-slate-300 text-sm font-light leading-relaxed">
                        Luôn vững tin vào giá trị bản thân, làm chủ cuộc sống và gặt hái những đỉnh cao thành công rực rỡ.
                    </p>
                </div>

                <!-- Honor Card 2 -->
                <div class="glass-card glass-card-hover rounded-2xl p-6 text-center space-y-4 border border-gold-400/20">
                    <div class="w-16 h-16 rounded-full bg-gold-400/10 border border-gold-400/40 flex items-center justify-center text-gold-400 mx-auto text-2xl">
                        <i class="fa-solid fa-heart-pulse"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-gold-100">Ấm Áp & Bao Dung</h3>
                    <p class="text-slate-300 text-sm font-light leading-relaxed">
                        Trái tim dịu dàng là ngọn lửa sưởi ấm mái ấm gia đình, tiếp thêm sức mạnh cho mọi người xung quanh.
                    </p>
                </div>

                <!-- Honor Card 3 -->
                <div class="glass-card glass-card-hover rounded-2xl p-6 text-center space-y-4 border border-gold-400/20">
                    <div class="w-16 h-16 rounded-full bg-gold-400/10 border border-gold-400/40 flex items-center justify-center text-gold-400 mx-auto text-2xl">
                        <i class="fa-solid fa-sun"></i>
                    </div>
                    <h3 class="font-serif text-xl font-bold text-gold-100">Cảm Hứng Rạng Rỡ</h3>
                    <p class="text-slate-300 text-sm font-light leading-relaxed">
                        Sự cống hiến và tri thức của phái đẹp thắp sáng tương lai, lan tỏa niềm vui và hy vọng mỗi ngày.
                    </p>
                </div>
            </div>

            <div class="mt-16 glass-card rounded-3xl p-8 text-center relative overflow-hidden border border-gold-400/40 bg-gradient-to-r from-burgundy-900/80 via-burgundy-950/90 to-burgundy-900/80">
                <div class="max-w-xl mx-auto space-y-6 relative z-10">
                    <div class="inline-block p-3 rounded-full bg-rose-500/10 text-rosegold-light text-3xl">
                        <i class="fa-solid fa-hand-holding-heart animate-bounce"></i>
                    </div>
                    <h3 class="font-serif text-2xl sm:text-3xl font-bold text-gold-gradient">Gửi Một Vòng Tay Ôm Ngọt Ngào</h3>
                    <p class="text-slate-300 text-sm sm:text-base font-light">
                        Nhấn nút bên dưới để trao gửi năng lượng tích cực, hàng ngàn trái tim và lời chúc bình an đến tất cả phụ nữ!
                    </p>
                    <button onclick="sendVirtualHug()" class="btn-gold px-8 py-4 rounded-full font-bold text-burgundy-950 text-base shadow-2xl flex items-center gap-3 mx-auto">
                        <i class="fa-solid fa-heart text-burgundy-950"></i>
                        <span>Gửi Yêu Thương Ngay ❤️</span>
                    </button>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="relative z-10 border-t border-gold-400/20 py-10 bg-burgundy-950/90 text-center text-slate-400 text-xs sm:text-sm">
        <div class="max-w-4xl mx-auto px-4 space-y-4">
            <p class="font-serif text-gold-300 text-base font-semibold">Tôn Vinh Phụ Nữ Việt Nam 20/10</p>
            <p class="font-light text-slate-400">Trân trọng gửi tặng tất cả phái đẹp – Những đóa hoa rạng rỡ của cuộc đời.</p>
            <p class="text-[11px] text-slate-500">© 2026 Special Edition for All Vietnamese Women.</p>
        </div>
    </footer>


    <!-- Ambient Music Player Floating Widget -->
    <div class="fixed bottom-6 left-6 z-50">
        <div class="glass-card rounded-full p-2 border border-gold-400/30 flex items-center gap-3 pr-5 shadow-2xl backdrop-blur-md">
            <button id="musicToggleBtn" onclick="toggleAudio()" class="w-12 h-12 rounded-full bg-gradient-to-tr from-gold-500 to-gold-300 flex items-center justify-center text-burgundy-950 font-bold shadow-lg transition-transform hover:scale-105 active:scale-95">
                <i id="musicIcon" class="fa-solid fa-music"></i>
            </button>
            <div class="flex flex-col">
                <span class="text-xs font-bold text-gold-300">Nhạc Nền Thư Giãn</span>
                <span id="musicStatus" class="text-[10px] text-slate-400">Chạm để bật piano du dương</span>
            </div>
        </div>
    </div>


    <!-- Fullscreen Letter Modal -->
    <div id="letterModal" class="fixed inset-0 z-50 bg-burgundy-950/80 backdrop-blur-md flex items-center justify-center p-4 opacity-0 pointer-events-none transition-opacity duration-300">
        <div class="glass-card max-w-2xl w-full rounded-3xl p-6 sm:p-10 border border-gold-400/40 relative shadow-2xl max-h-[90vh] overflow-y-auto">
            <!-- Close Button -->
            <button onclick="closeLetterModal()" class="absolute top-4 right-4 w-10 h-10 rounded-full bg-burgundy-900/80 border border-gold-400/30 text-gold-300 hover:text-white flex items-center justify-center transition-colors">
                <i class="fa-solid fa-xmark text-lg"></i>
            </button>

            <div class="text-center space-y-6 pt-2">
                <div class="w-16 h-16 rounded-full bg-gold-400/20 border border-gold-400/40 flex items-center justify-center text-gold-300 mx-auto text-2xl">
                    <i class="fa-solid fa-envelope-open-text"></i>
                </div>

                <h3 class="font-serif text-2xl sm:text-3xl font-bold text-gold-gradient">Thư Chúc Mừng 20/10 Hoàng Gia</h3>
                
                <div class="bg-burgundy-900/40 rounded-2xl p-6 sm:p-8 border border-gold-400/20 text-left space-y-4 text-slate-100 text-sm sm:text-base leading-relaxed font-sans">
                    <p class="font-serif text-lg text-gold-300 font-semibold">
                        Gửi <span id="modalLetterRecipient" class="text-white underline decoration-gold-400">Chị Em Phụ Nữ</span>,
                    </p>
                    <p>
                        Nhân ngày Phụ nữ Việt Nam 20/10, xin gửi tới bạn – người phụ nữ tuyệt vời – những lời chúc tôn vinh trân trọng và dịu dàng nhất.
                    </p>
                    <p>
                        Cảm ơn bạn vì đã luôn cống hiến, mang đến cho thế giới những nụ cười ấm áp, sự bao dung dịu dàng và bản lĩnh kiên cường. Dù ở vai trò là người mẹ, người vợ, cô giáo, chị em hay đồng nghiệp, bạn luôn tỏa sáng theo một cách rất riêng.
                    </p>
                    <p>
                        Nguyện chúc cho chặng đường phía trước của bạn luôn ngập tràn ánh nắng ấm áp, hoa nở rực rỡ và đong đầy hạnh phúc bên những người thân yêu!
                    </p>
                    <p class="text-right font-script text-2xl text-rosegold-light pt-4">
                        Trân trọng & Yêu thương!
                    </p>
                </div>

                <div class="pt-4 flex justify-center gap-4">
                    <button onclick="triggerFireworks(); closeLetterModal();" class="btn-gold px-8 py-3.5 rounded-full font-bold text-burgundy-950 text-sm shadow-xl">
                        <i class="fa-solid fa-sparkles mr-2"></i> Bắn Pháo Hoa Chúc Mừng
                    </button>
                </div>
            </div>
        </div>
    </div>


    <!-- Toast Notification Container -->
    <div id="toast" class="fixed top-24 right-6 z-50 bg-burgundy-900 border border-gold-400/50 text-gold-200 px-5 py-3 rounded-xl shadow-2xl flex items-center gap-3 transition-all duration-300 transform translate-x-full opacity-0">
        <i class="fa-solid fa-circle-check text-gold-400 text-lg"></i>
        <span id="toastMsg" class="text-sm font-medium">Đã sao chép lời chúc!</span>
    </div>


    <!-- JavaScript Section -->
    <script>
        let audioCtx = null;
        let isAudioPlaying = false;
        let audioSequenceTimer = null;

        // Classical ambient chord progression (Cmaj7 -> Am7 -> Fmaj7 -> G7)
        const chordProgression = [
            [261.63, 329.63, 392.00, 493.88], // Cmaj7
            [220.00, 261.63, 329.63, 392.00], // Am7
            [174.61, 220.00, 261.63, 329.63], // Fmaj7
            [196.00, 246.94, 293.66, 349.23]  // G7
        ];

        function initAudioContext() {
            if (!audioCtx) {
                const AudioContext = window.AudioContext || window.webkitAudioContext;
                audioCtx = new AudioContext();
            }
            if (audioCtx.state === 'suspended') {
                audioCtx.resume();
            }
        }

        function playPianoTone(freq, timeOffset, duration = 3.5) {
            if (!audioCtx) return;
            const now = audioCtx.currentTime + timeOffset;

            const osc = audioCtx.createOscillator();
            const gain = audioCtx.createGain();
            const filter = audioCtx.createBiquadFilter();

            osc.type = 'sine';
            osc.frequency.setValueAtTime(freq, now);

            // Envelope
            gain.gain.setValueAtTime(0, now);
            gain.gain.linearRampToValueAtTime(0.12, now + 0.05);
            gain.gain.exponentialRampToValueAtTime(0.0001, now + duration);

            filter.type = 'lowpass';
            filter.frequency.setValueAtTime(1100, now);

            osc.connect(gain);
            gain.connect(filter);
            filter.connect(audioCtx.destination);

            osc.start(now);
            osc.stop(now + duration);
        }

        function playAmbientLoop() {
            let step = 0;
            function scheduleNext() {
                if (!isAudioPlaying) return;
                const currentChord = chordProgression[step % chordProgression.length];
                
                // Arpeggiate chord notes
                currentChord.forEach((noteFreq, idx) => {
                    playPianoTone(noteFreq, idx * 0.35, 3.8);
                });

                step++;
                audioSequenceTimer = setTimeout(scheduleNext, 2800);
            }
            scheduleNext();
        }

        function toggleAudio() {
            initAudioContext();
            const icon = document.getElementById('musicIcon');
            const status = document.getElementById('musicStatus');

            if (!isAudioPlaying) {
                isAudioPlaying = true;
                playAmbientLoop();
                icon.className = 'fa-solid fa-compact-disc animate-spin';
                status.innerText = 'Đang phát piano du dương...';
                showToast('Đã bật nhạc nền thư giãn!');
            } else {
                isAudioPlaying = false;
                if (audioSequenceTimer) clearTimeout(audioSequenceTimer);
                icon.className = 'fa-solid fa-music';
                status.innerText = 'Chạm để bật piano du dương';
                showToast('Đã tạm dừng nhạc.');
            }
        }


        const canvas = document.getElementById('particleCanvas');
        const ctx = canvas.getContext('2d');
        let particles = [];
        let mouseX = -100, mouseY = -100;

        function resizeCanvas() {
            canvas.width = window.innerWidth;
            canvas.height = window.innerHeight;
        }
        window.addEventListener('resize', resizeCanvas);
        resizeCanvas();

        class Particle {
            constructor() {
                this.reset();
            }

            reset() {
                this.x = Math.random() * canvas.width;
                this.y = -20;
                this.size = Math.random() * 8 + 4;
                this.speedY = Math.random() * 1.1 + 0.4;
                this.speedX = Math.random() * 0.8 - 0.4;
                this.rotation = Math.random() * Math.PI * 2;
                this.rotSpeed = (Math.random() - 0.5) * 0.02;
                this.isGoldDust = Math.random() > 0.5;
                this.opacity = Math.random() * 0.65 + 0.3;
            }

            update() {
                this.y += this.speedY;
                this.x += Math.sin(this.y * 0.01) + this.speedX;
                this.rotation += this.rotSpeed;

                // Mouse subtle push
                const dx = mouseX - this.x;
                const dy = mouseY - this.y;
                const dist = Math.sqrt(dx * dx + dy * dy);
                if (dist < 110) {
                    this.x -= (dx / dist) * 2;
                    this.y -= (dy / dist) * 2;
                }

                if (this.y > canvas.height + 20) {
                    this.reset();
                }
            }

            draw() {
                ctx.save();
                ctx.translate(this.x, this.y);
                ctx.rotate(this.rotation);
                ctx.globalAlpha = this.opacity;

                if (this.isGoldDust) {
                    // Gold Dust Particle
                    ctx.fillStyle = '#D4AF37';
                    ctx.beginPath();
                    ctx.arc(0, 0, this.size * 0.35, 0, Math.PI * 2);
                    ctx.fill();
                } else {
                    // Rose Petal Particle
                    ctx.fillStyle = '#E8B4B8';
                    ctx.beginPath();
                    ctx.moveTo(0, 0);
                    ctx.bezierCurveTo(-this.size, -this.size, -this.size * 1.5, this.size / 2, 0, this.size * 1.5);
                    ctx.bezierCurveTo(this.size * 1.5, this.size / 2, this.size, -this.size, 0, 0);
                    ctx.fill();
                }

                ctx.restore();
            }
        }

        function initParticles() {
            particles = [];
            const count = Math.min(Math.floor(window.innerWidth / 15), 65);
            for (let i = 0; i < count; i++) {
                const p = new Particle();
                p.y = Math.random() * canvas.height;
                particles.push(p);
            }
        }
        initParticles();

        function animateParticles() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            particles.forEach(p => {
                p.update();
                p.draw();
            });
            requestAnimationFrame(animateParticles);
        }
        animateParticles();


        const wishesDatabase = {
            all: "Gửi {NAME} - Bông hoa xinh đẹp giữa cuộc đời!\n\nNhân ngày Phụ nữ Việt Nam 20/10, xin gửi tới {NAME} những lời chúc tốt đẹp và trân trọng nhất. Chúc {NAME} luôn giữ vững sự tự tin, rạng rỡ và bản lĩnh. Mong rằng mỗi ngày trôi qua với {NAME} đều ngập tràn niềm vui, nụ cười và trọn vẹn hạnh phúc bên những người thân yêu!",
            mom: "Gửi {NAME} kính yêu!\n\nNhân ngày Phụ nữ Việt Nam 20/10, con xin gửi tới {NAME} lời tri ân sâu sắc nhất từ đáy lòng. Cảm ơn {NAME} đã luôn là vầng thái dương ấm áp, nuôi dưỡng con bằng tình yêu thương vô bờ bến. Chúc {NAME} luôn dồi dào sức khỏe, bình an và mãi nở nụ cười hạnh phúc!",
            lover: "Gửi {NAME} - Tình yêu ngọt ngào của anh!\n\nNgày 20/10 này, anh chỉ muốn cảm ơn {NAME} vì đã đến và làm thế giới của anh trở nên ngập tràn màu sắc và hạnh phúc. Chúc {NAME} luôn rạng rỡ như những đóa hoa xuân, thành công rực rỡ và mãi là điều tuyệt vời nhất của anh!",
            colleague: "Thân gửi {NAME}!\n\nChúc {NAME} một ngày 20/10 thật nhiều niềm vui, nhận ngập tràn hoa và quà! Cảm ơn {NAME} vì sự nhiệt huyết và năng lượng tích cực luôn lan tỏa đến mọi người. Chúc {NAME} ngày càng xinh đẹp, gặt hái nhiều thành công rực rỡ trong sự nghiệp!",
            teacher: "Kính gửi {NAME}!\n\nNhân ngày 20/10, em xin gửi tới {NAME} lời chúc sức khỏe, hạnh phúc và lòng biết ơn vô hạn. Cảm ơn {NAME} đã luôn bao dung, tận tụy truyền dạy tri thức và thắp sáng tương lai cho thế hệ học trò. Chúc {NAME} luôn giữ trọn ngọn lửa nhiệt huyết!",
            sister: "Gửi {NAME} yêu quý!\n\nChúc {NAME} một ngày 20/10 rực rỡ niềm vui! Chúc {NAME} luôn xinh đẹp, tự tin, thông minh và luôn kiên định theo đuổi mọi ước mơ của mình. Hãy luôn tỏa sáng và luôn thật hạnh phúc nhé!"
        };

        let currentCategory = 'all';
        let typingTimeout = null;

        function getRecipientName() {
            const input = document.getElementById('recipientName').value.trim();
            return input || 'Chị Em Phụ Nữ';
        }

        function syncNameAcrossUI() {
            const name = getRecipientName();
            
            // Sync envelope preview
            const envName = document.getElementById('envelopeRecipientLabel');
            const letterName = document.getElementById('letterNamePreview');
            const modalRecipient = document.getElementById('modalLetterRecipient');

            if (envName) envName.innerText = name;
            if (letterName) letterName.innerText = name;
            if (modalRecipient) modalRecipient.innerText = name;
        }

        function typeWriterEffect(text) {
            const output = document.getElementById('wishOutput');
            output.innerHTML = '';
            let index = 0;

            if (typingTimeout) clearTimeout(typingTimeout);

            function type() {
                if (index < text.length) {
                    const char = text.charAt(index);
                    if (char === '\n') {
                        output.innerHTML += '<br/>';
                    } else {
                        output.innerHTML += char;
                    }
                    index++;
                    typingTimeout = setTimeout(type, 22);
                }
            }
            type();
        }

        function updateWishDisplay() {
            syncNameAcrossUI();
            const name = getRecipientName();
            const template = wishesDatabase[currentCategory];
            const formattedText = template.replace(/{NAME}/g, name);
            typeWriterEffect(formattedText);
        }

        function selectCategory(cat) {
            currentCategory = cat;
            document.querySelectorAll('.category-btn').forEach(btn => {
                btn.classList.remove('active', 'bg-gold-400/20', 'text-gold-300', 'border-gold-400', 'font-semibold');
                btn.classList.add('text-slate-300');
            });

            const activeBtn = document.getElementById(`tab-${cat}`);
            if (activeBtn) {
                activeBtn.classList.add('active', 'bg-gold-400/20', 'text-gold-300', 'border-gold-400', 'font-semibold');
            }

            updateWishDisplay();
        }

        function retypeWish() {
            updateWishDisplay();
        }

        document.getElementById('recipientName').addEventListener('input', () => {
            updateWishDisplay();
        });

        // Init default wish setup
        selectCategory('all');


        function toggleEnvelope(forceOpen = false) {
            const env = document.getElementById('mainEnvelope');
            if (forceOpen || !env.classList.contains('open')) {
                env.classList.add('open');
                triggerFireworks();
                setTimeout(() => {
                    openLetterModal();
                }, 1200);
            } else {
                env.classList.remove('open');
            }
        }

        function openLetterModal() {
            syncNameAcrossUI();
            const modal = document.getElementById('letterModal');
            modal.classList.remove('opacity-0', 'pointer-events-none');
            modal.classList.add('opacity-100');
        }

        function closeLetterModal() {
            const modal = document.getElementById('letterModal');
            modal.classList.remove('opacity-100');
            modal.classList.add('opacity-0', 'pointer-events-none');
        }

        function triggerFireworks() {
            if (typeof confetti === 'function') {
                confetti({
                    particleCount: 90,
                    spread: 80,
                    origin: { y: 0.6 },
                    colors: ['#D4AF37', '#E8B4B8', '#FF1493', '#FFFFFF', '#8A6412']
                });

                setTimeout(() => {
                    confetti({
                        particleCount: 60,
                        angle: 60,
                        spread: 60,
                        origin: { x: 0 },
                        colors: ['#D4AF37', '#E8B4B8', '#FF1493']
                    });
                }, 250);

                setTimeout(() => {
                    confetti({
                        particleCount: 60,
                        angle: 120,
                        spread: 60,
                        origin: { x: 1 },
                        colors: ['#D4AF37', '#E8B4B8', '#FF1493']
                    });
                }, 400);
            }
        }

        function sendVirtualHug() {
            triggerFireworks();
            showToast('Đã gửi trọn yêu thương & ngàn trái tim! ❤️');
        }

        function copyWishText() {
            const text = document.getElementById('wishOutput').innerText;
            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(text).then(() => {
                    showToast('Đã sao chép lời chúc vào khay nhớ tạm!');
                }).catch(() => {
                    fallbackCopy(text);
                });
            } else {
                fallbackCopy(text);
            }
        }

        function fallbackCopy(text) {
            const textArea = document.createElement('textarea');
            textArea.value = text;
            document.body.appendChild(textArea);
            textArea.select();
            try {
                document.execCommand('copy');
                showToast('Đã sao chép lời chúc!');
            } catch (err) {
                showToast('Không thể sao chép tự động.');
            }
            document.body.removeChild(textArea);
        }

        function showToast(msg) {
            const toast = document.getElementById('toast');
            document.getElementById('toastMsg').innerText = msg;
            toast.classList.remove('translate-x-full', 'opacity-0');
            setTimeout(() => {
                toast.classList.add('translate-x-full', 'opacity-0');
            }, 3200);
        }

        // Custom Cursor Tracker
        window.addEventListener('mousemove', (e) => {
            mouseX = e.clientX;
            mouseY = e.clientY;
            
            const cursorRing = document.getElementById('cursorRing');
            const cursorDot = document.getElementById('cursorDot');
            
            if (cursorRing && cursorDot) {
                cursorRing.style.left = `${e.clientX}px`;
                cursorRing.style.top = `${e.clientY}px`;
                cursorDot.style.left = `${e.clientX}px`;
                cursorDot.style.top = `${e.clientY}px`;
            }
        });

        // Initialize Web Audio context on first user click
        window.addEventListener('click', () => {
            initAudioContext();
        }, { once: true });
    </script>
</body>
</html>
