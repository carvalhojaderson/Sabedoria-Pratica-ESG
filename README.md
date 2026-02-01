<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fundo Sabedoria Prática ESG | O Legado da Virtude</title>
    
    <!-- Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    
    <!-- Tailwind -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- GSAP -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    
    <!-- Three.js -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    
    <!-- Lucide -->
    <script src="https://unpkg.com/lucide@latest"></script>
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                        display: ['Cinzel', 'serif'],
                    },
                    colors: {
                        'ruby': '#9f1239',
                        'ruby-dark': '#4c0519',
                        'ruby-light': '#e11d48',
                        'gold': '#d4af37',
                        'gold-light': '#f4d03f',
                        'obsidian': '#0a0a0f',
                        'crimson': '#dc2626',
                    },
                    animation: {
                        'pulse-slow': 'pulse 4s cubic-bezier(0.4, 0, 0.6, 1) infinite',
                        'float': 'float 6s ease-in-out infinite',
                        'glow': 'glow 2s ease-in-out infinite alternate',
                        'shimmer': 'shimmer 2s linear infinite',
                    },
                    keyframes: {
                        float: {
                            '0%, 100%': { transform: 'translateY(0)' },
                            '50%': { transform: 'translateY(-20px)' },
                        },
                        glow: {
                            '0%': { boxShadow: '0 0 20px rgba(220, 38, 38, 0.5)' },
                            '100%': { boxShadow: '0 0 40px rgba(220, 38, 38, 0.8), 0 0 60px rgba(212, 175, 55, 0.4)' },
                        },
                        shimmer: {
                            '0%': { backgroundPosition: '-200% 0' },
                            '100%': { backgroundPosition: '200% 0' },
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            background: #0a0a0f;
            color: #e2e8f0;
            overflow-x: hidden;
            cursor: none;
        }
        
        /* Custom Cursor */
        .cursor-dot,
        .cursor-outline {
            position: fixed;
            top: 0;
            left: 0;
            transform: translate(-50%, -50%);
            border-radius: 50%;
            z-index: 9999;
            pointer-events: none;
        }
        
        .cursor-dot {
            width: 5px;
            height: 5px;
            background: #dc2626;
        }
        
        .cursor-outline {
            width: 30px;
            height: 30px;
            border: 2px solid rgba(220, 38, 38, 0.5);
            transition: all 0.2s ease;
        }
        
        .cursor-outline.hover {
            width: 60px;
            height: 60px;
            background: rgba(220, 38, 38, 0.1);
            border-color: #d4af37;
        }
        
        /* Grain */
        .grain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 9998;
            opacity: 0.04;
            background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)'/%3E%3C/svg%3E");
        }
        
        /* Glass */
        .glass-ruby {
            background: rgba(159, 18, 57, 0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(220, 38, 38, 0.2);
        }
        
        .glass-ruby:hover {
            border-color: rgba(212, 175, 55, 0.5);
            background: rgba(159, 18, 57, 0.15);
        }
        
        /* Text Effects */
        .text-glow {
            text-shadow: 0 0 20px rgba(220, 38, 38, 0.5), 0 0 40px rgba(212, 175, 55, 0.3);
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #d4af37 0%, #dc2626 50%, #9f1239 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            background-size: 200% 200%;
            animation: gradient-shift 8s ease infinite;
        }
        
        @keyframes gradient-shift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Video Container */
        .video-container {
            position: relative;
            overflow: hidden;
            border-radius: 24px;
            box-shadow: 0 25px 50px -12px rgba(220, 38, 38, 0.5);
        }
        
        .video-container::before {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(45deg, rgba(220, 38, 38, 0.3), rgba(212, 175, 55, 0.2));
            z-index: 1;
            pointer-events: none;
        }
        
        /* Lion/Bull Symbolism */
        .beast-frame {
            position: relative;
            border: 2px solid rgba(212, 175, 55, 0.3);
            border-radius: 50%;
            padding: 20px;
            background: radial-gradient(circle, rgba(220, 38, 38, 0.2) 0%, transparent 70%);
        }
        
        /* Territory Cards */
        .territory-card {
            background: linear-gradient(135deg, rgba(159, 18, 57, 0.1) 0%, rgba(10, 10, 15, 0.9) 100%);
            border: 1px solid rgba(220, 38, 38, 0.3);
            transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .territory-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: #d4af37;
            box-shadow: 0 20px 40px rgba(220, 38, 38, 0.3);
        }
        
        /* Hub Grid */
        .hub-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 1.5rem;
        }
        
        /* Animated Border */
        .animated-border {
            position: relative;
            background: linear-gradient(60deg, #0a0a0f, #1a1a2e, #0a0a0f);
            background-size: 300% 300%;
            animation: animatedgradient 3s ease alternate infinite;
        }
        
        @keyframes animatedgradient {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }
        
        /* Scrollbar */
        ::-webkit-scrollbar {
            width: 10px;
        }
        
        ::-webkit-scrollbar-track {
            background: #0a0a0f;
        }
        
        ::-webkit-scrollbar-thumb {
            background: linear-gradient(180deg, #dc2626, #d4af37);
            border-radius: 5px;
        }
        
        /* Mobile Menu */
        .menu-mobile {
            clip-path: circle(0% at calc(100% - 40px) 40px);
            transition: clip-path 0.6s ease-in-out;
        }
        
        .menu-mobile.active {
            clip-path: circle(150% at calc(100% - 40px) 40px);
        }
        
        /* Sacred Geometry Background */
        .sacred-geometry {
            position: absolute;
            width: 100%;
            height: 100%;
            opacity: 0.1;
            background-image: 
                repeating-linear-gradient(60deg, transparent, transparent 50px, rgba(220, 38, 38, 0.1) 50px, rgba(220, 38, 38, 0.1) 51px),
                repeating-linear-gradient(-60deg, transparent, transparent 50px, rgba(212, 175, 55, 0.1) 50px, rgba(212, 175, 55, 0.1) 51px);
        }
    </style>
</head>
<body class="font-sans antialiased selection:bg-crimson selection:text-white">

    <!-- Grain Overlay -->
    <div class="grain"></div>
    
    <!-- Custom Cursor -->
    <div class="cursor-dot hidden md:block"></div>
    <div class="cursor-outline hidden md:block"></div>

    <!-- Navigation -->
    <nav class="fixed w-full z-50 top-0 transition-all duration-500" id="navbar">
        <div class="max-w-7xl mx-auto px-6 py-6">
            <div class="flex justify-between items-center">
                <a href="#" class="group flex items-center space-x-3 magnetic-btn">
                    <div class="beast-frame w-14 h-14 flex items-center justify-center">
                        <i data-lucide="gem" class="text-gold w-8 h-8"></i>
                    </div>
                    <div>
                        <span class="text-xl font-display font-bold text-white block leading-none tracking-wider">SABEDORIA</span>
                        <span class="text-xs text-crimson font-bold tracking-[0.3em] uppercase">Prática ESG</span>
                    </div>
                </a>
                
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#visao" class="text-sm text-gray-400 hover:text-gold transition-colors magnetic-btn">A Visão</a>
                    <a href="#territorios" class="text-sm text-gray-400 hover:text-gold transition-colors magnetic-btn">Territórios</a>
                    <a href="#pilares" class="text-sm text-gray-400 hover:text-gold transition-colors magnetic-btn">3 Pilares</a>
                    <a href="#mulheres" class="text-sm text-crimson hover:text-red-400 transition-colors magnetic-btn font-medium">Liderança Feminina</a>
                    <a href="#hub" class="text-sm text-gray-400 hover:text-gold transition-colors magnetic-btn">Hub</a>
                    <a href="#contato" class="magnetic-btn bg-gradient-to-r from-crimson to-ruby hover:from-red-600 hover:to-red-800 text-white px-6 py-3 rounded-full text-sm font-bold transition-all transform hover:scale-105 shadow-lg shadow-crimson/30">
                        Investir
                    </a>
                </div>
                
                <button class="md:hidden text-white" id="menuToggle">
                    <i data-lucide="menu" class="w-8 h-8"></i>
                </button>
            </div>
        </div>
        
        <!-- Mobile Menu -->
        <div class="menu-mobile fixed inset-0 bg-obsidian z-40 flex items-center justify-center md:hidden">
            <div class="text-center space-y-8">
                <a href="#visao" class="block text-3xl font-display text-white hover:text-gold transition-colors">A Visão</a>
                <a href="#territorios" class="block text-3xl font-display text-white hover:text-gold transition-colors">Territórios</a>
                <a href="#pilares" class="block text-3xl font-display text-white hover:text-gold transition-colors">3 Pilares</a>
                <a href="#mulheres" class="block text-3xl font-display text-crimson transition-colors">Liderança Feminina</a>
                <a href="#hub" class="block text-3xl font-display text-white hover:text-gold transition-colors">Hub</a>
                <a href="#contato" class="inline-block bg-crimson text-white px-8 py-4 rounded-full text-xl font-bold">Investir Agora</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section with Video -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
        <!-- Background Elements -->
        <div class="absolute inset-0">
            <div class="absolute top-1/4 left-1/4 w-[500px] h-[500px] bg-crimson/20 rounded-full blur-[150px] animate-pulse-slow"></div>
            <div class="absolute bottom-1/4 right-1/4 w-[600px] h-[600px] bg-ruby/20 rounded-full blur-[150px] animate-pulse-slow" style="animation-delay: 2s;"></div>
            <div class="sacred-geometry"></div>
        </div>

        <div class="relative z-10 max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-12 items-center">
            <!-- Left: Content -->
            <div class="order-2 lg:order-1 text-center lg:text-left">
                <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full glass-ruby border border-crimson/30 mb-6">
                    <span class="w-2 h-2 bg-crimson rounded-full animate-pulse"></span>
                    <span class="text-crimson text-xs font-bold tracking-widest uppercase">O Legado da Virtude</span>
                </div>
                
                <h1 class="font-display text-5xl md:text-7xl font-bold text-white mb-6 leading-tight">
                    <span class="block">Sabedoria</span>
                    <span class="gradient-text">Prática ESG</span>
                </h1>
                
                <p class="text-xl text-gray-300 mb-8 leading-relaxed font-serif italic">
                    "Mais preciosa que os rubis, a sabedoria guia a gestão virtuosa que transforma tributos em restauração de vidas e comunidades."
                </p>
                
                <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                    <a href="#territorios" class="magnetic-btn group relative px-8 py-4 bg-gradient-to-r from-crimson to-ruby text-white rounded-full font-bold text-lg overflow-hidden transition-all hover:scale-105 shadow-xl shadow-crimson/30">
                        <span class="relative z-10 flex items-center space-x-2">
                            <span>Descobrir Territórios</span>
                            <i data-lucide="arrow-down-right" class="w-5 h-5"></i>
                        </span>
                    </a>
                    
                    <a href="#visao" class="magnetic-btn px-8 py-4 glass-ruby text-white rounded-full font-medium text-lg hover:bg-white/5 transition-all border border-crimson/30">
                        Nossa Estratégia
                    </a>
                </div>
                
                <div class="mt-12 flex items-center justify-center lg:justify-start space-x-8">
                    <div class="text-center">
                        <div class="text-3xl font-display font-bold text-gold">R$25M</div>
                        <div class="text-xs text-gray-500 uppercase tracking-wider">Meta de Captação</div>
                    </div>
                    <div class="h-12 w-px bg-gradient-to-b from-crimson to-gold"></div>
                    <div class="text-center">
                        <div class="text-3xl font-display font-bold text-crimson">100%</div>
                        <div class="text-xs text-gray-500 uppercase tracking-wider">Equity-Free</div>
                    </div>
                    <div class="h-12 w-px bg-gradient-to-b from-crimson to-gold"></div>
                    <div class="text-center">
                        <div class="text-3xl font-display font-bold text-gold">3</div>
                        <div class="text-xs text-gray-500 uppercase tracking-wider">Pilares ESG</div>
                    </div>
                </div>
            </div>
            
            <!-- Right: Video -->
            <div class="order-1 lg:order-2">
                <div class="video-container aspect-[9/16] max-w-md mx-auto relative group cursor-pointer" onclick="document.getElementById('heroVideo').play()">
                    <video id="heroVideo" class="w-full h-full object-cover" loop muted playsinline poster="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1080 1920'%3E%3Crect fill='%239f1239' width='1080' height='1920'/%3E%3C/svg%3E">
                        <source src="https://cdn.discordapp.com/attachments/123456789/123456789/sabedoria_pratica_esg.mp4" type="video/mp4">
                    </video>
                    
                    <!-- Play Overlay -->
                    <div class="absolute inset-0 flex items-center justify-center z-10 group-hover:opacity-0 transition-opacity duration-300">
                        <div class="w-20 h-20 rounded-full bg-crimson/80 flex items-center justify-center backdrop-blur-sm border-2 border-gold animate-glow">
                            <i data-lucide="play" class="w-8 h-8 text-white ml-1"></i>
                        </div>
                    </div>
                    
                    <!-- Decorative Elements -->
                    <div class="absolute -inset-4 border border-crimson/20 rounded-3xl -z-10"></div>
                    <div class="absolute -inset-8 border border-gold/10 rounded-3xl -z-10"></div>
                </div>
                
                <p class="text-center text-xs text-gray-500 mt-4 italic">Toque para ativar o vídeo</p>
            </div>
        </div>
        
        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <i data-lucide="chevron-down" class="w-6 h-6 text-crimson"></i>
        </div>
    </section>

    <!-- Visão Section -->
    <section id="visao" class="py-32 relative overflow-hidden">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-20">
                <span class="text-crimson text-sm font-bold tracking-[0.3em] uppercase mb-4 block">A Estratégia</span>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">
                    O <span class="gradient-text">Valor</span> Invisível
                </h2>
                <p class="text-gray-400 text-xl max-w-3xl mx-auto leading-relaxed">
                    No mercado financeiro, o valor é medido pelo visível. No Fundo Sabedoria Prática ESG, medimos pela <strong class="text-gold">Sabedoria Prática</strong> — um ativo que transcende o ouro fino.
                </p>
            </div>

            <div class="grid md:grid-cols-3 gap-8">
                <!-- Card 1 -->
                <div class="territory-card rounded-3xl p-8 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-crimson/20 rounded-full blur-3xl"></div>
                    <div class="relative z-10">
                        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-crimson to-ruby flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                            <i data-lucide="gem" class="w-8 h-8 text-gold"></i>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">A Sabedoria como Ativo</h3>
                        <p class="text-gray-400 leading-relaxed mb-6">
                            "Mais preciosa é do que os rubis, e tudo o que mais possas desejar não se pode comparar a ela." Transformamos capital em <strong class="text-gold">riqueza verdadeira</strong>.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500">
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Restauração Ambiental</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Inclusão Social</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Honra na Governança</li>
                        </ul>
                    </div>
                </div>

                <!-- Card 2 -->
                <div class="territory-card rounded-3xl p-8 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-gold/20 rounded-full blur-3xl"></div>
                    <div class="relative z-10">
                        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-gold to-yellow-600 flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                            <i data-lucide="eye" class="w-8 h-8 text-obsidian"></i>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">Liderança de Olhos Abertos</h3>
                        <p class="text-gray-400 leading-relaxed mb-6">
                            Governança com <strong class="text-gold">integridade absoluta</strong>. Alianças acadêmicas com UNICAMP, PUC e ESPM garantem rigor técnico e inovação.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500">
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>Transparência máxima</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>Pesquisa científica</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>Excelência em gestão</li>
                        </ul>
                    </div>
                </div>

                <!-- Card 3 -->
                <div class="territory-card rounded-3xl p-8 relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-crimson/20 rounded-full blur-3xl"></div>
                    <div class="relative z-10">
                        <div class="w-16 h-16 rounded-2xl bg-gradient-to-br from-ruby to-crimson flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                            <i data-lucide="shield" class="w-8 h-8 text-gold"></i>
                        </div>
                        <h3 class="font-display text-2xl font-bold text-white mb-4">O Vigor da Proteção</h3>
                        <p class="text-gray-400 leading-relaxed mb-6">
                            "As suas forças são como as do boi selvagem." Nossa rede <strong class="text-gold">Disruptivos</strong> protege o que é valioso com inovação e estratégia.
                        </p>
                        <ul class="space-y-2 text-sm text-gray-500">
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Blindagem social</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Tecnologia de ponta</li>
                            <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Governança ativa</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Territórios Culturais Permanentes -->
    <section id="territorios" class="py-32 relative bg-gradient-to-b from-obsidian via-ruby-dark/20 to-obsidian">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid lg:grid-cols-2 gap-16 items-center mb-20">
                <div>
                    <span class="text-crimson text-sm font-bold tracking-[0.3em] uppercase mb-4 block">A Casa que Voa</span>
                    <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6 leading-tight">
                        Territórios <span class="gradient-text">Culturais</span><br>Permanentes
                    </h2>
                    <p class="text-gray-400 text-lg leading-relaxed mb-8">
                        Não são eventos. São <strong class="text-gold">faróis na favela</strong>: pontos fixos de transformação social, cultura e geração de renda. Rodas de conversa toda terça, oficinas pra quebrar vício, atendimento pra quem precisa.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-crimson/20 flex items-center justify-center flex-shrink-0">
                                <i data-lucide="sprout" class="w-6 h-6 text-crimson"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-bold mb-1">Horta Hidropônica Resiliente</h4>
                                <p class="text-gray-400 text-sm">Alimento grátis pra quem chega sem dinheiro. Tecnologia que nem chuva mata.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-gold/20 flex items-center justify-center flex-shrink-0">
                                <i data-lucide="graduation-cap" class="w-6 h-6 text-gold"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-bold mb-1">Sala de Formação Cultural</h4>
                                <p class="text-gray-400 text-sm">Teatro que denuncia, música que grava o grito virando rap, cultura que educa.</p>
                            </div>
                        </div>
                        
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-crimson/20 flex items-center justify-center flex-shrink-0">
                                <i data-lucide="rocket" class="w-6 h-6 text-crimson"></i>
                            </div>
                            <div>
                                <h4 class="text-white font-bold mb-1">Incubadora Dupla</h4>
                                <p class="text-gray-400 text-sm">Negócio cultural (quem canta vira produtor) e tradicional (quem costura vira marca).</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="relative">
                    <div class="absolute inset-0 bg-gradient-to-r from-crimson to-gold rounded-3xl blur-3xl opacity-20"></div>
                    <div class="relative glass-ruby rounded-3xl p-8 border border-crimson/30">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?w=800&auto=format&fit=crop&q=80" alt="Território Cultural" class="w-full h-64 object-cover rounded-2xl mb-6">
                        
                        <div class="grid grid-cols-2 gap-4">
                            <div class="glass-ruby rounded-xl p-4 text-center">
                                <i data-lucide="users" class="w-6 h-6 text-crimson mx-auto mb-2"></i>
                                <div class="text-white font-bold">Rodas de Conversa</div>
                                <div class="text-xs text-gray-400">Toda terça-feira</div>
                            </div>
                            <div class="glass-ruby rounded-xl p-4 text-center">
                                <i data-lucide="heart-handshake" class="w-6 h-6 text-crimson mx-auto mb-2"></i>
                                <div class="text-white font-bold">Atendimento Social</div>
                                <div class="text-xs text-gray-400">Mulheres, LGBTQIA+, negros</div>
                            </div>
                            <div class="glass-ruby rounded-xl p-4 text-center">
                                <i data-lucide="palette" class="w-6 h-6 text-gold mx-auto mb-2"></i>
                                <div class="text-white font-bold">Oficinas Terapêuticas</div>
                                <div class="text-xs text-gray-400">Quebra de vícios</div>
                            </div>
                            <div class="glass-ruby rounded-xl p-4 text-center">
                                <i data-lucide="building-2" class="w-6 h-6 text-gold mx-auto mb-2"></i>
                                <div class="text-white font-bold">Estrutura Fixa</div>
                                <div class="text-xs text-gray-400">Domo, biblioteca, som</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Domos Geodésicos -->
            <div class="glass-ruby rounded-3xl p-8 md:p-12 border border-crimson/20 relative overflow-hidden">
                <div class="absolute top-0 right-0 w-64 h-64 bg-crimson/10 rounded-full blur-3xl"></div>
                
                <div class="relative z-10 grid md:grid-cols-2 gap-12 items-center">
                    <div>
                        <h3 class="font-display text-3xl font-bold text-white mb-4">Domos Geodésicos Sustentáveis</h3>
                        <p class="text-gray-400 mb-6 leading-relaxed">
                            Construção rápida, econômica e ecológica para comunidades rurais e urbanas. Parceria com empresas especializadas e integração com o <strong class="text-gold">Minha Casa Minha Vida</strong>.
                        </p>
                        
                        <div class="space-y-3">
                            <div class="flex items-center text-gray-300">
                                <i data-lucide="check-circle" class="w-5 h-5 text-crimson mr-3"></i>
                                <span>Reforma Agrária Produtiva</span>
                            </div>
                            <div class="flex items-center text-gray-300">
                                <i data-lucide="check-circle" class="w-5 h-5 text-crimson mr-3"></i>
                                <span>Assentamentos Autossuficientes</span>
                            </div>
                            <div class="flex items-center text-gray-300">
                                <i data-lucide="check-circle" class="w-5 h-5 text-crimson mr-3"></i>
                                <span>Agroecologia e Preservação</span>
                            </div>
                            <div class="flex items-center text-gray-300">
                                <i data-lucide="check-circle" class="w-5 h-5 text-crimson mr-3"></i>
                                <span>Captação via Caixa Econômica</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="grid grid-cols-2 gap-4">
                        <img src="https://images.unsplash.com/photo-1518780664697-55e3ad937233?w=400&auto=format&fit=crop&q=80" alt="Domo" class="rounded-2xl w-full h-48 object-cover">
                        <img src="https://images.unsplash.com/photo-1449156493391-d2cfa28e468b?w=400&auto=format&fit=crop&q=80" alt="Horta" class="rounded-2xl w-full h-48 object-cover">
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Liderança Feminina - NOVA SEÇÃO DESTAQUE -->
    <section id="mulheres" class="py-32 relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-ruby-dark/30 via-obsidian to-ruby-dark/30"></div>
        
        <div class="max-w-7xl mx-auto px-6 relative z-10">
            <div class="text-center mb-16">
                <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full glass-ruby border border-gold/30 mb-6">
                    <i data-lucide="crown" class="w-4 h-4 text-gold"></i>
                    <span class="text-gold text-xs font-bold tracking-widest uppercase">Nova Estrutura</span>
                </div>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">
                    Gerido por <span class="gradient-text">Mulheres</span> que Voam
                </h2>
                <p class="text-gray-400 text-xl max-w-3xl mx-auto leading-relaxed">
                    O território só dá estrutura — elas já têm a visão. <strong class="text-gold">Mulheres líderes de comunidades e ONGs</strong> que sabem onde pousar, quem puxar e quando soltar.
                </p>
            </div>

            <div class="grid md:grid-cols-3 gap-8 mb-16">
                <!-- Card 1 -->
                <div class="territory-card rounded-3xl p-8 text-center group">
                    <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-crimson to-ruby flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="crown" class="w-10 h-10 text-gold"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-3">Liderança Comunitária</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Mulheres que já voam nas comunidades. Elas conhecem o território, sabem quem precisa de ajuda e como chegar.
                    </p>
                </div>

                <!-- Card 2 -->
                <div class="territory-card rounded-3xl p-8 text-center group">
                    <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-gold to-yellow-600 flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="network" class="w-10 h-10 text-obsidian"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-3">Replicação Via Rouanet</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Territórios Culturais Permanentes replicados em escala via Lei Rouanet, Fundo Municipal e imposto direcionado.
                    </p>
                </div>

                <!-- Card 3 -->
                <div class="territory-card rounded-3xl p-8 text-center group">
                    <div class="w-24 h-24 mx-auto mb-6 rounded-full bg-gradient-to-br from-ruby to-crimson flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="scale" class="w-10 h-10 text-gold"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-3">Autonomia Real</h3>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Estrutura física (domo, biblioteca, som, advogado) + autonomia de gestão. Elas comandam, nós apoiamos.
                    </p>
                </div>
            </div>

            <!-- Estrutura do Território Águia -->
            <div class="glass-ruby rounded-3xl p-8 md:p-12 border border-gold/20 relative overflow-hidden">
                <div class="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-crimson via-gold to-crimson"></div>
                
                <div class="grid lg:grid-cols-2 gap-12 items-center">
                    <div>
                        <h3 class="font-display text-3xl font-bold text-white mb-6 flex items-center">
                            <span class="w-10 h-10 rounded-full bg-crimson flex items-center justify-center mr-4">
                                <i data-lucide="bird" class="w-5 h-5 text-gold"></i>
                            </span>
                            Território Águia
                        </h3>
                        <p class="text-gray-400 mb-8 leading-relaxed">
                            Um novo modelo de Território Cultural gerido exclusivamente por mulheres líderes. <strong class="text-gold">Casa que voa</strong> — estrutura fixa com alma nômade, adaptando-se às necessidades da comunidade.
                        </p>
                        
                        <div class="space-y-4">
                            <div class="flex items-center justify-between p-4 bg-white/5 rounded-xl border border-white/10">
                                <div class="flex items-center space-x-3">
                                    <i data-lucide="shield" class="w-5 h-5 text-crimson"></i>
                                    <span class="text-white">Atendimento à mulher que apanhou</span>
                                </div>
                                <span class="text-xs text-gold px-2 py-1 bg-gold/10 rounded">Proteção</span>
                            </div>
                            
                            <div class="flex items-center justify-between p-4 bg-white/5 rounded-xl border border-white/10">
                                <div class="flex items-center space-x-3">
                                    <i data-lucide="heart" class="w-5 h-5 text-crimson"></i>
                                    <span class="text-white">Apoio ao gay que ouviu 'anormal'</span>
                                </div>
                                <span class="text-xs text-gold px-2 py-1 bg-gold/10 rounded">Acolhimento</span>
                            </div>
                            
                            <div class="flex items-center justify-between p-4 bg-white/5 rounded-xl border border-white/10">
                                <div class="flex items-center space-x-3">
                                    <i data-lucide="fist" class="w-5 h-5 text-crimson"></i>
                                    <span class="text-white">Defesa do preto que levou injúria</span>
                                </div>
                                <span class="text-xs text-gold px-2 py-1 bg-gold/10 rounded">Justiça</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="relative">
                        <div class="absolute -inset-4 bg-gradient-to-r from-crimson to-gold rounded-3xl blur-2xl opacity-20"></div>
                        <div class="relative glass-ruby rounded-2xl p-6 border border-crimson/30">
                            <div class="aspect-video rounded-xl overflow-hidden mb-6">
                                <img src="https://images.unsplash.com/photo-1591848478625-de43268e6fb8?w=800&auto=format&fit=crop&q=80" alt="Mulheres líderes" class="w-full h-full object-cover hover:scale-110 transition-transform duration-700">
                            </div>
                            
                            <div class="grid grid-cols-2 gap-4 text-center">
                                <div class="p-4 bg-crimson/10 rounded-xl">
                                    <div class="text-2xl font-display font-bold text-gold">Via Rouanet</div>
                                    <div class="text-xs text-gray-400">Captação principal</div>
                                </div>
                                <div class="p-4 bg-crimson/10 rounded-xl">
                                    <div class="text-2xl font-display font-bold text-gold">Via Município</div>
                                    <div class="text-xs text-gray-400">Fundo Municipal</div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- 3 Pilares ESG -->
    <section id="pilares" class="py-32 relative bg-gradient-to-b from-obsidian to-ruby-dark/20">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-20">
                <span class="text-crimson text-sm font-bold tracking-[0.3em] uppercase mb-4 block">ESG Integrado</span>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">
                    Os Três <span class="gradient-text">Pilares</span>
                </h2>
            </div>

            <div class="space-y-12">
                <!-- Governança -->
                <div class="glass-ruby rounded-3xl p-8 md:p-12 border border-crimson/20 relative overflow-hidden group hover:border-gold/50 transition-colors">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-gold/5 rounded-full blur-3xl"></div>
                    <div class="grid md:grid-cols-2 gap-12 items-center">
                        <div>
                            <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-gold/10 text-gold text-xs font-bold mb-4">
                                <span>01</span>
                                <span>GOVERNANÇA</span>
                            </div>
                            <h3 class="font-display text-3xl font-bold text-white mb-4">Liderança de "Olhos Abertos"</h3>
                            <p class="text-gray-400 leading-relaxed mb-6">
                                Inspirados na visão de Olhos Abertos, garantimos a integridade do banco de projetos e transparência máxima. Alianças acadêmicas fortalecem o rigor técnico.
                            </p>
                            <ul class="space-y-2 text-sm text-gray-500">
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>UNICAMP, PUC, ESPM</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>Disruptivos Culturais</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-gold mr-2"></i>Captadores Especializados</li>
                            </ul>
                        </div>
                        <div class="relative">
                            <img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&auto=format&fit=crop&q=80" alt="Governança" class="rounded-2xl w-full h-64 object-cover">
                        </div>
                    </div>
                </div>

                <!-- Social -->
                <div class="glass-ruby rounded-3xl p-8 md:p-12 border border-crimson/20 relative overflow-hidden group hover:border-crimson/50 transition-colors">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-crimson/5 rounded-full blur-3xl"></div>
                    <div class="grid md:grid-cols-2 gap-12 items-center">
                        <div class="order-2 md:order-1 relative">
                            <img src="https://images.unsplash.com/photo-1469571486292-0ba58a3f068b?w=600&auto=format&fit=crop&q=80" alt="Social" class="rounded-2xl w-full h-64 object-cover">
                        </div>
                        <div class="order-1 md:order-2">
                            <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-crimson/10 text-crimson text-xs font-bold mb-4">
                                <span>02</span>
                                <span>SOCIAL</span>
                            </div>
                            <h3 class="font-display text-3xl font-bold text-white mb-4">A Mão Estendida</h3>
                            <p class="text-gray-400 leading-relaxed mb-6">
                                O tributo torna-se semente que restaura a dignidade. Moradia social, esporte, neurociência e práticas circenses em parceria com a UNICAMP.
                            </p>
                            <ul class="space-y-2 text-sm text-gray-500">
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Domos Geodésicos & Steel Frame</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Biomecânica + Artes Circenses</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-crimson mr-2"></i>Parkour, Hip-Hop, Pa Kua</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Ambiental -->
                <div class="glass-ruby rounded-3xl p-8 md:p-12 border border-crimson/20 relative overflow-hidden group hover:border-emerald-500/50 transition-colors">
                    <div class="absolute top-0 right-0 w-64 h-64 bg-emerald-500/5 rounded-full blur-3xl"></div>
                    <div class="grid md:grid-cols-2 gap-12 items-center">
                        <div>
                            <div class="inline-flex items-center space-x-2 px-3 py-1 rounded-full bg-emerald-500/10 text-emerald-400 text-xs font-bold mb-4">
                                <span>03</span>
                                <span>AMBIENTAL</span>
                            </div>
                            <h3 class="font-display text-3xl font-bold text-white mb-4">Urbanismo Sustentável</h3>
                            <p class="text-gray-400 leading-relaxed mb-6">
                                Transformamos praças degradadas em ambientes de vida. Formato CEUs com bibliotecas, hortas hidropônicas e tokens sociais de reciclagem.
                            </p>
                            <ul class="space-y-2 text-sm text-gray-500">
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-emerald-400 mr-2"></i>Revitalização de Ambientes</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-emerald-400 mr-2"></i>Hortas Hidropônicas</li>
                                <li class="flex items-center"><i data-lucide="check" class="w-4 h-4 text-emerald-400 mr-2"></i>Tokens de Reciclagem</li>
                            </ul>
                        </div>
                        <div class="relative">
                            <img src="https://images.unsplash.com/photo-1518531933037-91b2f5f229cc?w=600&auto=format&fit=crop&q=80" alt="Ambiental" class="rounded-2xl w-full h-64 object-cover">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Hub Aberto -->
    <section id="hub" class="py-32 relative">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <span class="text-crimson text-sm font-bold tracking-[0.3em] uppercase mb-4 block">Participe</span>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">
                    Hub <span class="gradient-text">Aberto</span>
                </h2>
                <p class="text-gray-400 text-xl max-w-2xl mx-auto">
                    Conecte-se ao ecossistema. Cadastre seu território, sua ONG ou descubra incentivos disponíveis.
                </p>
            </div>

            <div class="hub-grid max-w-5xl mx-auto">
                <a href="#" class="glass-ruby rounded-2xl p-8 text-center hover:bg-crimson/20 transition-all group border border-crimson/20 hover:border-gold/50">
                    <div class="w-16 h-16 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-crimson to-ruby flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="map-pin" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-2">Cadastrar Território Águia</h3>
                    <p class="text-gray-400 text-sm">Seja um ponto fixo de transformação na sua comunidade</p>
                </a>

                <a href="#" class="glass-ruby rounded-2xl p-8 text-center hover:bg-crimson/20 transition-all group border border-crimson/20 hover:border-gold/50">
                    <div class="w-16 h-16 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-gold to-yellow-600 flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="heart-handshake" class="w-8 h-8 text-obsidian"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-2">Cadastrar ONG Parceira</h3>
                    <p class="text-gray-400 text-sm">Junte-se à rede de implementadores</p>
                </a>

                <a href="#" class="glass-ruby rounded-2xl p-8 text-center hover:bg-crimson/20 transition-all group border border-crimson/20 hover:border-gold/50">
                    <div class="w-16 h-16 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-ruby to-crimson flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="search" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-2">Ver Incentivos</h3>
                    <p class="text-gray-400 text-sm">Descubra as leis de incentivo disponíveis</p>
                </a>

                <a href="#" class="glass-ruby rounded-2xl p-8 text-center hover:bg-crimson/20 transition-all group border border-crimson/20 hover:border-gold/50">
                    <div class="w-16 h-16 mx-auto mb-4 rounded-2xl bg-gradient-to-br from-crimson to-ruby flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i data-lucide="users" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="font-display text-xl font-bold text-white mb-2">Seja Investidor</h3>
                    <p class="text-gray-400 text-sm">Transforme tributos em legado</p>
                </a>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contato" class="py-32 relative bg-gradient-to-t from-ruby-dark/40 to-obsidian">
        <div class="max-w-4xl mx-auto px-6 text-center">
            <h2 class="font-display text-5xl md:text-7xl font-bold text-white mb-8 leading-tight">
                Restaurando lares,<br>
                <span class="gradient-text">revitalizando cidades</span>
            </h2>
            
            <p class="text-xl text-gray-400 mb-12 leading-relaxed">
                Transformando tributos num legado de sabedoria e ciência. Entre em contato para parcerias, investimentos ou para cadastrar seu território.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-6 justify-center mb-16">
                <a href="mailto:carvalhojaderson@gmail.com" class="magnetic-btn px-10 py-5 bg-gradient-to-r from-crimson to-ruby text-white rounded-full font-bold text-lg hover:shadow-2xl hover:shadow-crimson/50 transition-all flex items-center justify-center space-x-3">
                    <i data-lucide="mail" class="w-5 h-5"></i>
                    <span>carvalhojaderson@gmail.com</span>
                </a>
                
                <a href="https://wa.me/5531982510633" class="magnetic-btn px-10 py-5 glass-ruby text-white rounded-full font-bold text-lg hover:bg-white/5 transition-all flex items-center justify-center space-x-3 border border-crimson/30">
                    <i data-lucide="phone" class="w-5 h-5"></i>
                    <span>(31) 98251-0633</span>
                </a>
            </div>
            
            <div class="glass-ruby rounded-2xl p-8 inline-block border border-gold/20">
                <p class="text-gold font-serif italic text-lg mb-4">"Sabedoria Prática ESG"</p>
                <div class="flex items-center justify-center space-x-6 text-sm text-gray-400">
                    <span>Belo Horizonte, MG</span>
                    <span class="w-1 h-1 bg-crimson rounded-full"></span>
                    <span>Brasil</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="border-t border-crimson/20 bg-obsidian py-16">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid md:grid-cols-4 gap-12 mb-12">
                <div class="md:col-span-2">
                    <div class="flex items-center space-x-3 mb-6">
                        <div class="beast-frame w-12 h-12 flex items-center justify-center">
                            <i data-lucide="gem" class="text-gold w-6 h-6"></i>
                        </div>
                        <div>
                            <span class="text-xl font-display font-bold text-white block tracking-wider">SABEDORIA</span>
                            <span class="text-xs text-crimson font-bold tracking-widest">PRÁTICA ESG</span>
                        </div>
                    </div>
                    <p class="text-gray-500 mb-6 max-w-md">
                        Transformando obrigações tributárias em legado cultural e desenvolvimento humano através de Territórios Culturais Permanentes.
                    </p>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 rounded-full glass-ruby flex items-center justify-center text-gray-400 hover:text-gold hover:border-gold/50 transition-all">
                            <i data-lucide="linkedin" class="w-5 h-5"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full glass-ruby flex items-center justify-center text-gray-400 hover:text-gold hover:border-gold/50 transition-all">
                            <i data-lucide="instagram" class="w-5 h-5"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full glass-ruby flex items-center justify-center text-gray-400 hover:text-gold hover:border-gold/50 transition-all">
                            <i data-lucide="youtube" class="w-5 h-5"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-6 font-display">Navegação</h4>
                    <ul class="space-y-3 text-gray-500">
                        <li><a href="#visao" class="hover:text-gold transition-colors">A Visão</a></li>
                        <li><a href="#territorios" class="hover:text-gold transition-colors">Territórios</a></li>
                        <li><a href="#mulheres" class="hover:text-gold transition-colors">Liderança Feminina</a></li>
                        <li><a href="#pilares" class="hover:text-gold transition-colors">3 Pilares</a></li>
                        <li><a href="#hub" class="hover:text-gold transition-colors">Hub Aberto</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-6 font-display">Parceiros</h4>
                    <ul class="space-y-3 text-gray-500 text-sm">
                        <li>Ministério da Cultura</li>
                        <li>UNICAMP</li>
                        <li>PUC</li>
                        <li>ESPM</li>
                        <li>Incentiv.me</li>
                        <li>Ecossistema Disruptivos</li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-crimson/10 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-gray-600 text-sm">© 2025 Fundo Sabedoria Prática ESG. Todos os direitos reservados.</p>
                <p class="text-gray-600 text-sm mt-4 md:mt-0 font-display">O Legado da Virtude</p>
            </div>
        </div>
    </footer>

    <script>
        // Initialize Lucide
        lucide.createIcons();

        // Custom Cursor
        const cursorDot = document.querySelector('.cursor-dot');
        const cursorOutline = document.querySelector('.cursor-outline');
        
        window.addEventListener('mousemove', (e) => {
            const posX = e.clientX;
            const posY = e.clientY;
            
            cursorDot.style.left = `${posX}px`;
            cursorDot.style.top = `${posY}px`;
            
            cursorOutline.animate({
                left: `${posX}px`,
                top: `${posY}px`
            }, { duration: 500, fill: "forwards" });
        });
        
        document.querySelectorAll('a, button, .territory-card').forEach(el => {
            el.addEventListener('mouseenter', () => cursorOutline.classList.add('hover'));
            el.addEventListener('mouseleave', () => cursorOutline.classList.remove('hover'));
        });

        // GSAP Animations
        gsap.registerPlugin(ScrollTrigger);

        // Hero Animation
        gsap.from('.reveal-text', {
            y: 100,
            opacity: 0,
            duration: 1.2,
            stagger: 0.2,
            ease: "power4.out"
        });

        // Counter Animation
        document.querySelectorAll('.counter').forEach(counter => {
            const target = parseFloat(counter.dataset.target);
            const isDecimal = counter.dataset.decimal === 'true';
            
            ScrollTrigger.create({
                trigger: counter,
                start: "top 85%",
                once: true,
                onEnter: () => {
                    gsap.to(counter, {
                        innerHTML: target,
                        duration: 2,
                        snap: { innerHTML: isDecimal ? 0.1 : 1 },
                        ease: "power2.out",
                        onUpdate: function() {
                            counter.innerHTML = isDecimal ? 
                                parseFloat(this.targets()[0].innerHTML).toFixed(1) : 
                                Math.ceil(this.targets()[0].innerHTML);
                        }
                    });
                }
            });
        });

        // Scroll Reveal
        gsap.utils.toArray('.territory-card').forEach((card, i) => {
            gsap.from(card, {
                scrollTrigger: {
                    trigger: card,
                    start: "top 85%",
                    toggleActions: "play none none reverse"
                },
                y: 60,
                opacity: 0,
                duration: 1,
                delay: i * 0.1,
                ease: "power3.out"
            });
        });

        // Mobile Menu
        const menuToggle = document.getElementById('menuToggle');
        const menuMobile = document.querySelector('.menu-mobile');
        
        menuToggle.addEventListener('click', () => {
            menuMobile.classList.toggle('active');
        });

        // Navbar Scroll Effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.classList.add('bg-obsidian/90', 'backdrop-blur-md');
            } else {
                navbar.classList.remove('bg-obsidian/90', 'backdrop-blur-md');
            }
        });

        // Smooth Scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                    menuMobile.classList.remove('active');
                }
            });
        });

        // Magnetic Buttons
        document.querySelectorAll('.magnetic-btn').forEach(btn => {
            btn.addEventListener('mousemove', (e) => {
                const rect = btn.getBoundingClientRect();
                const x = e.clientX - rect.left - rect.width / 2;
                const y = e.clientY - rect.top - rect.height / 2;
                
                btn.style.transform = `translate(${x * 0.2}px, ${y * 0.2}px)`;
            });
            
            btn.addEventListener('mouseleave', () => {
                btn.style.transform = 'translate(0, 0)';
            });
        });
    </script>
</body>
</html>
