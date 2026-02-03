<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fundo Sabedoria Prática ESG - Transforme Imposto em Legado</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --ruby-primary: #DC143C;
            --ruby-dark: #8B0000;
            --ruby-light: #FF6B6B;
            --ruby-pulse: rgba(220, 20, 60, 0.4);
            --gold: #D4AF37;
            --dark-bg: #0a0a0a;
            --darker-bg: #050505;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--darker-bg);
            color: #f5f5f5;
            overflow-x: hidden;
        }
        
        h1, h2, h3, h4, .serif {
            font-family: 'Cormorant Garamond', serif;
        }
        
        .ruby-glow {
            box-shadow: 0 0 60px rgba(220, 20, 60, 0.6), 0 0 100px rgba(220, 20, 60, 0.3);
        }
        
        .ruby-text-glow {
            text-shadow: 0 0 20px rgba(220, 20, 60, 0.8), 0 0 40px rgba(220, 20, 60, 0.4);
        }
        
        .ruby-gradient {
            background: linear-gradient(135deg, #DC143C 0%, #8B0000 50%, #4a0404 100%);
        }
        
        .ruby-shine {
            background: linear-gradient(45deg, transparent 30%, rgba(255,255,255,0.3) 50%, transparent 70%);
            background-size: 200% 200%;
            animation: shine 3s infinite;
        }
        
        @keyframes shine {
            0% { background-position: 200% 0; }
            100% { background-position: -200% 0; }
        }
        
        @keyframes pulse-ruby {
            0%, 100% { box-shadow: 0 0 20px rgba(220, 20, 60, 0.4); }
            50% { box-shadow: 0 0 60px rgba(220, 20, 60, 0.8), 0 0 100px rgba(220, 20, 60, 0.4); }
        }
        
        .animate-pulse-ruby {
            animation: pulse-ruby 2s infinite;
        }
        
        .glass-panel {
            background: rgba(20, 20, 20, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(220, 20, 60, 0.2);
        }
        
        .input-field {
            background: rgba(10, 10, 10, 0.8);
            border: 1px solid rgba(220, 20, 60, 0.3);
            transition: all 0.3s ease;
        }
        
        .input-field:focus {
            border-color: var(--ruby-primary);
            box-shadow: 0 0 20px rgba(220, 20, 60, 0.3);
            outline: none;
        }
        
        .territory-card {
            background: linear-gradient(145deg, rgba(20,20,20,0.9) 0%, rgba(10,10,10,0.9) 100%);
            border: 1px solid rgba(220, 20, 60, 0.2);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .territory-card:hover {
            border-color: var(--ruby-primary);
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(220, 20, 60, 0.2);
        }
        
        .scroll-reveal {
            opacity: 0;
            transform: translateY(30px);
        }
        
        .ruby-particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: var(--ruby-primary);
            border-radius: 50%;
            pointer-events: none;
            opacity: 0.6;
        }
        
        .nav-link {
            position: relative;
            overflow: hidden;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -2px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--ruby-primary);
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .btn-primary {
            background: linear-gradient(135deg, #DC143C 0%, #8B0000 100%);
            position: relative;
            overflow: hidden;
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 40px rgba(220, 20, 60, 0.5);
        }
        
        .btn-primary::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            transition: left 0.5s ease;
        }
        
        .btn-primary:hover::before {
            left: 100%;
        }
        
        .geometric-bg {
            background-image: 
                radial-gradient(circle at 20% 50%, rgba(220, 20, 60, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(139, 0, 0, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 20%, rgba(220, 20, 60, 0.05) 0%, transparent 50%);
        }
        
        .quote-mark {
            font-size: 6rem;
            line-height: 1;
            opacity: 0.2;
            color: var(--ruby-primary);
        }
        
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.9);
            z-index: 1000;
            backdrop-filter: blur(10px);
        }
        
        .modal.active {
            display: flex;
            animation: fadeIn 0.3s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        .floating-ruby {
            animation: float 6s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px) rotate(0deg); }
            50% { transform: translateY(-20px) rotate(5deg); }
        }
        
        .tab-active {
            border-bottom: 3px solid var(--ruby-primary);
            color: var(--ruby-primary);
        }
        
        .progress-bar {
            background: linear-gradient(90deg, var(--ruby-dark) 0%, var(--ruby-primary) 100%);
            height: 4px;
            border-radius: 2px;
            transition: width 1s ease;
        }
    </style>
</head>
<body class="geometric-bg">

    <!-- Navigation -->
    <nav class="fixed w-full z-50 glass-panel border-b border-red-900/20 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center space-x-3 cursor-pointer" onclick="window.scrollTo(0,0)">
                    <div class="w-10 h-10 ruby-gradient rounded-lg flex items-center justify-center animate-pulse-ruby">
                        <svg class="w-6 h-6 text-white" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M12 2L2 12l10 10 10-10L12 2zm0 3.5L18.5 12 12 18.5 5.5 12 12 5.5z"/>
                        </svg>
                    </div>
                    <span class="serif text-2xl font-bold text-white tracking-wide">Sabedoria<span class="text-red-500">Prática</span>ESG</span>
                </div>
                
                <div class="hidden md:flex space-x-8">
                    <a href="#sobre" class="nav-link text-gray-300 hover:text-white transition-colors">Sobre</a>
                    <a href="#territorios" class="nav-link text-gray-300 hover:text-white transition-colors">Territórios</a>
                    <a href="#cadastro" class="nav-link text-gray-300 hover:text-white transition-colors">Cadastrar Projeto</a>
                    <a href="#apoiar" class="nav-link text-gray-300 hover:text-white transition-colors">Apoiar</a>
                    <button onclick="openModal('loginModal')" class="px-6 py-2 border border-red-600 text-red-500 hover:bg-red-600 hover:text-white transition-all rounded-full">Área Restrita</button>
                </div>
                
                <button class="md:hidden text-white" onclick="toggleMobileMenu()">
                    <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/></svg>
                </button>
            </div>
        </div>
    </nav>

    <!-- Mobile Menu -->
    <div id="mobileMenu" class="fixed inset-0 z-40 bg-black/95 transform translate-x-full transition-transform duration-300 md:hidden">
        <div class="flex flex-col items-center justify-center h-full space-y-8">
            <a href="#sobre" onclick="toggleMobileMenu()" class="text-2xl text-white hover:text-red-500">Sobre</a>
            <a href="#territorios" onclick="toggleMobileMenu()" class="text-2xl text-white hover:text-red-500">Territórios</a>
            <a href="#cadastro" onclick="toggleMobileMenu()" class="text-2xl text-white hover:text-red-500">Cadastrar Projeto</a>
            <a href="#apoiar" onclick="toggleMobileMenu()" class="text-2xl text-white hover:text-red-500">Apoiar</a>
        </div>
    </div>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
        <div class="absolute inset-0 z-0">
            <div class="absolute top-20 left-10 w-72 h-72 bg-red-600/20 rounded-full blur-3xl animate-pulse"></div>
            <div class="absolute bottom-20 right-10 w-96 h-96 bg-red-800/20 rounded-full blur-3xl animate-pulse delay-1000"></div>
        </div>
        
        <div class="container mx-auto px-4 z-10 text-center">
            <div class="floating-ruby mb-8 inline-block">
                <svg class="w-24 h-24 mx-auto text-red-600 drop-shadow-2xl" fill="currentColor" viewBox="0 0 24 24">
                    <path d="M12 2L4 9l8 13 8-13-8-7zm0 2.5L17.5 9 12 17.5 6.5 9 12 4.5z"/>
                </svg>
            </div>
            
            <h1 class="serif text-5xl md:text-7xl lg:text-8xl font-bold mb-6 leading-tight">
                <span class="block text-transparent bg-clip-text bg-gradient-to-r from-red-400 via-red-600 to-red-800 ruby-text-glow">Mais valioso que rubis</span>
                <span class="block text-2xl md:text-4xl mt-4 text-gray-300 font-light">Transforme imposto em legado sustentável</span>
            </h1>
            
            <p class="max-w-3xl mx-auto text-lg md:text-xl text-gray-400 mb-12 leading-relaxed">
                Plataforma de facilitação para empresas, bancos e fundos tributários redirecionarem IRPJ devido 
                <span class="text-red-400 font-semibold">(sem custo extra)</span> para projetos de restauração social, 
                territórios culturais permanentes e inovação com universidades.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                <button onclick="scrollToSection('cadastro')" class="btn-primary px-8 py-4 rounded-full text-white font-semibold text-lg flex items-center gap-2 group">
                    Cadastrar Projeto
                    <svg class="w-5 h-5 transform group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/></svg>
                </button>
                <button onclick="scrollToSection('apoiar')" class="px-8 py-4 rounded-full border-2 border-red-600 text-red-500 hover:bg-red-600 hover:text-white transition-all font-semibold text-lg">
                    Quero Apoiar
                </button>
            </div>
            
            <div class="mt-16 grid grid-cols-1 md:grid-cols-3 gap-8 max-w-4xl mx-auto">
                <div class="glass-panel p-6 rounded-2xl scroll-reveal">
                    <div class="text-3xl font-bold text-red-500 mb-2">60-100%</div>
                    <div class="text-sm text-gray-400">PD&I com parcerias acadêmicas</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl scroll-reveal">
                    <div class="text-3xl font-bold text-red-500 mb-2">0%</div>
                    <div class="text-sm text-gray-400">Custo extra para empresa</div>
                </div>
                <div class="glass-panel p-6 rounded-2xl scroll-reveal">
                    <div class="text-3xl font-bold text-red-500 mb-2">100%</div>
                    <div class="text-sm text-gray-400">Destinação legal do IRPJ</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Mechanism Section -->
    <section id="sobre" class="py-24 relative">
        <div class="container mx-auto px-4">
            <div class="max-w-4xl mx-auto text-center mb-16 scroll-reveal">
                <h2 class="serif text-4xl md:text-5xl font-bold mb-6 text-white">Mecanismo de Transformação</h2>
                <p class="text-xl text-gray-400">Imposto em Impacto</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-6xl mx-auto">
                <div class="glass-panel p-8 rounded-2xl scroll-reveal relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-red-600/10 rounded-full blur-2xl group-hover:bg-red-600/20 transition-all"></div>
                    <div class="w-16 h-16 ruby-gradient rounded-2xl flex items-center justify-center mb-6 text-2xl font-bold text-white">01</div>
                    <h3 class="serif text-2xl font-bold mb-4 text-white">Lei de Incentivo ao Esporte</h3>
                    <p class="text-gray-400 leading-relaxed">Destinação direta via legislação vigente, transformando obrigação tributária em investimento social.</p>
                </div>
                
                <div class="glass-panel p-8 rounded-2xl scroll-reveal relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-red-600/10 rounded-full blur-2xl group-hover:bg-red-600/20 transition-all"></div>
                    <div class="w-16 h-16 ruby-gradient rounded-2xl flex items-center justify-center mb-6 text-2xl font-bold text-white">02</div>
                    <h3 class="serif text-2xl font-bold mb-4 text-white">FIA (Criança/Adolescente)</h3>
                    <p class="text-gray-400 leading-relaxed">Fundo da Infância e Adolescência para projetos de proteção e desenvolvimento de jovens em vulnerabilidade.</p>
                </div>
                
                <div class="glass-panel p-8 rounded-2xl scroll-reveal relative overflow-hidden group">
                    <div class="absolute top-0 right-0 w-32 h-32 bg-red-600/10 rounded-full blur-2xl group-hover:bg-red-600/20 transition-all"></div>
                    <div class="w-16 h-16 ruby-gradient rounded-2xl flex items-center justify-center mb-6 text-2xl font-bold text-white">03</div>
                    <h3 class="serif text-2xl font-bold mb-4 text-white">Incentivo à Cultura</h3>
                    <p class="text-gray-400 leading-relaxed">Rouanet e outras leis de incentivo para territórios culturais permanentes e produção artística.</p>
                </div>
            </div>
            
            <div class="mt-16 max-w-4xl mx-auto glass-panel p-8 rounded-2xl scroll-reveal border-l-4 border-red-600">
                <div class="flex items-start gap-6">
                    <div class="quote-mark serif">"</div>
                    <div>
                        <p class="text-lg md:text-xl text-gray-300 italic mb-4">Mais preciosa é do que os rubis, e tudo o que mais possas desejar não se pode comparar a ela.</p>
                        <p class="text-red-400 font-semibold">Provérbios 31</p>
                        <p class="text-sm text-gray-500 mt-2">Inspirados por essa verdade atemporal, transformamos capital financeiro em riqueza inestimável e verdadeira.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Territories Section -->
    <section id="territorios" class="py-24 bg-black/50">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 scroll-reveal">
                <h2 class="serif text-4xl md:text-5xl font-bold mb-6">Territórios Culturais Permanentes</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">Espaços físicos de transformação social, combinando estrutura fixa com alma nômade</p>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-7xl mx-auto">
                <!-- Territory 1 -->
                <div class="territory-card rounded-2xl overflow-hidden scroll-reveal group">
                    <div class="h-48 bg-gradient-to-br from-purple-900 to-red-900 relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center">
                            <svg class="w-20 h-20 text-white/20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 3c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm0 14.2c-2.5 0-4.71-1.28-6-3.22.03-1.99 4-3.08 6-3.08 1.99 0 5.97 1.09 6 3.08-1.29 1.94-3.5 3.22-6 3.22z"/></svg>
                        </div>
                        <div class="absolute top-4 right-4 bg-red-600 text-white px-3 py-1 rounded-full text-xs font-bold">ATIVO</div>
                    </div>
                    <div class="p-6">
                        <h3 class="serif text-2xl font-bold mb-2 text-white">Território Águia</h3>
                        <p class="text-red-400 text-sm mb-4">Mulheres que Voam</p>
                        <p class="text-gray-400 text-sm mb-4">Espaço gerido por mulheres líderes de comunidades, oferecendo rodas de conversa terapêuticas, atendimento a vítimas de violência e formação profissional.</p>
                        <div class="flex gap-2 flex-wrap">
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Horta Hidropônica</span>
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Empreendedorismo</span>
                        </div>
                    </div>
                </div>
                
                <!-- Territory 2 -->
                <div class="territory-card rounded-2xl overflow-hidden scroll-reveal group">
                    <div class="h-48 bg-gradient-to-br from-blue-900 to-red-900 relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center">
                            <svg class="w-20 h-20 text-white/20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
                        </div>
                        <div class="absolute top-4 right-4 bg-red-600 text-white px-3 py-1 rounded-full text-xs font-bold">ATIVO</div>
                    </div>
                    <div class="p-6">
                        <h3 class="serif text-2xl font-bold mb-2 text-white">Guardião Corpo</h3>
                        <p class="text-red-400 text-sm mb-4">Homens Guardiões</p>
                        <p class="text-gray-400 text-sm mb-4">Três domos geodésicos: parkour/Krav Maga/arqueria, biblioteca viva e incubadora cultural. Parceria com IA da Unicamp para análise biomecânica.</p>
                        <div class="flex gap-2 flex-wrap">
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Parkour</span>
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Krav Maga</span>
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Empreendedorismo</span>
                        </div>
                    </div>
                </div>
                
                <!-- Territory 3 -->
                <div class="territory-card rounded-2xl overflow-hidden scroll-reveal group">
                    <div class="h-48 bg-gradient-to-br from-yellow-900 to-red-900 relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center">
                            <svg class="w-20 h-20 text-white/20" fill="currentColor" viewBox="0 0 24 24"><path d="M12 3v10.55c-.59-.34-1.27-.55-2-.55-2.21 0-4 1.79-4 4s1.79 4 4 4 4-1.79 4-4V7h4V3h-6z"/></svg>
                        </div>
                        <div class="absolute top-4 right-4 bg-yellow-600 text-white px-3 py-1 rounded-full text-xs font-bold">EXPANSÃO</div>
                    </div>
                    <div class="p-6">
                        <h3 class="serif text-2xl font-bold mb-2 text-white">Território Sonoro</h3>
                        <p class="text-red-400 text-sm mb-4">Música e Produção</p>
                        <p class="text-gray-400 text-sm mb-4">Estúdios de produção profissional, aulas de instrumentos diversos e plataforma para eventos comunitários. Transformando talento em renda.</p>
                        <div class="flex gap-2 flex-wrap">
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Estúdio</span>
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Eventos</span>
                        </div>
                    </div>
                </div>
                
                <!-- Territory 4 -->
                <div class="territory-card rounded-2xl overflow-hidden scroll-reveal group">
                    <div class="h-48 bg-gradient-to-br from-green-900 to-red-900 relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center">
                            <svg class="w-20 h-20 text-white/20" fill="currentColor" viewBox="0 0 24 24"><path d="M21 3H3c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h18c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm0 13H3V5h18v11z"/></svg>
                        </div>
                        <div class="absolute top-4 right-4 bg-yellow-600 text-white px-3 py-1 rounded-full text-xs font-bold">EXPANSÃO</div>
                    </div>
                    <div class="p-6">
                        <h3 class="serif text-2xl font-bold mb-2 text-white">Território Digital</h3>
                        <p class="text-red-400 text-sm mb-4">Games e Audiovisual</p>
                        <p class="text-gray-400 text-sm mb-4">Laboratório de desenvolvimento de games, estúdios de gravação 4K e programa de residência artística para criadores emergentes.</p>
                        <div class="flex gap-2 flex-wrap">
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Games</span>
                            <span class="px-3 py-1 bg-red-900/30 text-red-400 rounded-full text-xs">Audiovisual</span>
                        </div>
                    </div>
                </div>
                
                <!-- Territory 5 -->
                <div class="territory-card rounded-2xl overflow-hidden scroll-reveal group md:col-span-2 lg:col-span-2">
                    <div class="h-48 bg-gradient-to-r from-red-900 via-purple-900 to-red-900 relative overflow-hidden">
                        <div class="absolute inset-0 flex items-center justify-center">
                            <h3 class="serif text-3xl text-white/30 font-bold">ZONA LESTE SP</h3>
                        </div>
                        <div class="absolute top-4 right-4 bg-red-600 text-white px-3 py-1 rounded-full text-xs font-bold">NOVO</div>
                    </div>
                    <div class="p-6">
                        <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                            <div>
                                <h3 class="serif text-2xl font-bold text-white">Centro Cultural Zona Leste</h3>
                                <p class="text-red-400 text-sm">São Paulo</p>
                            </div>
                            <div class="mt-4 md:mt-0 text-right">
                                <div class="text-2xl font-bold text-white">400m²</div>
                                <div class="text-xs text-gray-500">Estrutura padronizada</div>
                            </div>
                        </div>
                        <p class="text-gray-400 mb-4">Centro cultural permanente estrategicamente localizado na Zona Leste de São Paulo. Infraestrutura completa com 3 domos geodésicos, horta hidropônica, sistema de energia solar e bicicletas geradoras.</p>
                        <div class="grid grid-cols-3 gap-4 mt-4">
                            <div class="text-center p-3 bg-white/5 rounded-lg">
                                <div class="text-red-500 font-bold">3</div>
                                <div class="text-xs text-gray-500">Domos</div>
                            </div>
                            <div class="text-center p-3 bg-white/5 rounded-lg">
                                <div class="text-red-500 font-bold">100%</div>
                                <div class="text-xs text-gray-500">Sustentável</div>
                            </div>
                            <div class="text-center p-3 bg-white/5 rounded-lg">
                                <div class="text-red-500 font-bold">24/7</div>
                                <div class="text-xs text-gray-500">Comunidade</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Registration Section -->
    <section id="cadastro" class="py-24 relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-b from-red-900/10 to-transparent"></div>
        <div class="container mx-auto px-4 relative z-10">
            <div class="max-w-4xl mx-auto">
                <div class="text-center mb-12 scroll-reveal">
                    <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-red-900/30 border border-red-600/30 mb-6">
                        <span class="w-2 h-2 rounded-full bg-red-500 animate-pulse"></span>
                        <span class="text-red-400 text-sm font-semibold">NOVOS PROJETOS</span>
                    </div>
                    <h2 class="serif text-4xl md:text-5xl font-bold mb-6">Cadastre seu Projeto</h2>
                    <p class="text-gray-400 text-lg">Tem uma iniciativa de impacto social? Junte-se ao ecossistema Sabedoria Prática.</p>
                </div>
                
                <div class="glass-panel rounded-3xl p-8 md:p-12 scroll-reveal">
                    <form id="projectForm" class="space-y-8" onsubmit="handleProjectSubmit(event)">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Nome do Projeto</label>
                                <input type="text" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="Ex: Território Cultural Norte">
                            </div>
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Tipo de Projeto</label>
                                <select class="input-field w-full px-4 py-3 rounded-xl text-white bg-transparent">
                                    <option value="" class="bg-gray-900">Selecione...</option>
                                    <option value="cultural" class="bg-gray-900">Território Cultural</option>
                                    <option value="esporte" class="bg-gray-900">Projeto Esportivo</option>
                                    <option value="educacao" class="bg-gray-900">Educação</option>
                                    <option value="saude" class="bg-gray-900">Saúde/Mulher</option>
                                    <option value="tecnologia" class="bg-gray-900">Tecnologia/Inovação</option>
                                </select>
                            </div>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Responsável</label>
                                <input type="text" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="Nome completo">
                            </div>
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Email</label>
                                <input type="email" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="contato@projeto.org">
                            </div>
                        </div>
                        
                        <div class="space-y-2">
                            <label class="text-sm font-medium text-gray-300">Descrição do Impacto</label>
                            <textarea rows="4" class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600 resize-none" placeholder="Descreva como seu projeto transforma vidas e comunidades..."></textarea>
                        </div>
                        
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Público Beneficiado</label>
                                <input type="number" class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="Número estimado">
                            </div>
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">Cidade/Estado</label>
                                <input type="text" class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="São Paulo/SP">
                            </div>
                            <div class="space-y-2">
                                <label class="text-sm font-medium text-gray-300">CNPJ (se houver)</label>
                                <input type="text" class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600" placeholder="00.000.000/0000-00">
                            </div>
                        </div>
                        
                        <div class="pt-6 border-t border-gray-800">
                            <div class="flex items-start gap-3 mb-6">
                                <input type="checkbox" required class="mt-1 w-5 h-5 rounded border-gray-600 text-red-600 focus:ring-red-600 bg-gray-800">
                                <label class="text-sm text-gray-400">Declaro que as informações são verdadeiras e autorizo o contato para análise de viabilidade de parceria.</label>
                            </div>
                            
                            <button type="submit" class="w-full btn-primary py-4 rounded-xl text-white font-bold text-lg flex items-center justify-center gap-2">
                                <span>Enviar Cadastro</span>
                                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/></svg>
                            </button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Support Section -->
    <section id="apoiar" class="py-24 bg-black/50">
        <div class="container mx-auto px-4">
            <div class="max-w-6xl mx-auto">
                <div class="text-center mb-16 scroll-reveal">
                    <h2 class="serif text-4xl md:text-5xl font-bold mb-6">Seja um Apoiador</h2>
                    <p class="text-gray-400 text-lg max-w-2xl mx-auto">Empresas e bancos podem destinar IRPJ devido para projetos certificados sem custo operacional adicional.</p>
                </div>
                
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
                    <div class="space-y-8 scroll-reveal">
                        <div class="glass-panel p-6 rounded-2xl border-l-4 border-red-600">
                            <h3 class="serif text-2xl font-bold mb-3 text-white">Para Empresas</h3>
                            <ul class="space-y-3 text-gray-400">
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-red-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Assessoria exclusiva de destinação fiscal</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-red-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Relatórios de impacto ESG mensuráveis</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-red-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Posicionamento como líder em sustentabilidade</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-red-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Fidelização de clientes PJ</span>
                                </li>
                            </ul>
                        </div>
                        
                        <div class="glass-panel p-6 rounded-2xl border-l-4 border-yellow-600">
                            <h3 class="serif text-2xl font-bold mb-3 text-white">Para Bancos</h3>
                            <ul class="space-y-3 text-gray-400">
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-yellow-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Produto de valor agregado para carteira PJ</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-yellow-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Receita indireta via facilitação</span>
                                </li>
                                <li class="flex items-start gap-3">
                                    <svg class="w-6 h-6 text-yellow-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
                                    <span>Cumprimento de metas sociais do Banco Central</span>
                                </li>
                            </ul>
                        </div>
                    </div>
                    
                    <div class="glass-panel rounded-3xl p-8 scroll-reveal">
                        <h3 class="serif text-2xl font-bold mb-6 text-center">Simule sua Destinação</h3>
                        
                        <div class="space-y-6">
                            <div>
                                <label class="text-sm text-gray-400 mb-2 block">Valor do IRPJ Devido (R$)</label>
                                <input type="range" min="100000" max="10000000" step="100000" value="1000000" class="w-full h-2 bg-gray-700 rounded-lg appearance-none cursor-pointer accent-red-600" id="irpjRange" oninput="updateSimulation(this.value)">
                                <div class="flex justify-between text-xs text-gray-500 mt-1">
                                    <span>R$ 100k</span>
                                    <span class="text-red-400 font-bold text-lg" id="irpjValue">R$ 1.000.000</span>
                                    <span>R$ 10M</span>
                                </div>
                            </div>
                            
                            <div class="space-y-4">
                                <div class="flex justify-between items-center p-4 bg-white/5 rounded-xl">
                                    <span class="text-gray-400">Destinação máxima (6%)</span>
                                    <span class="text-2xl font-bold text-red-500" id="destinacaoValor">R$ 60.000</span>
                                </div>
                                <div class="flex justify-between items-center p-4 bg-white/5 rounded-xl">
                                    <span class="text-gray-400">Vidas impactadas (est.)</span>
                                    <span class="text-2xl font-bold text-green-500" id="vidasImpactadas">120</span>
                                </div>
                                <div class="flex justify-between items-center p-4 bg-white/5 rounded-xl">
                                    <span class="text-gray-400">Retorno ESG Score</span>
                                    <span class="text-2xl font-bold text-yellow-500">A+</span>
                                </div>
                            </div>
                            
                            <button onclick="openModal('contactModal')" class="w-full btn-primary py-4 rounded-xl text-white font-bold text-lg mt-6">
                                Falar com Consultor
                            </button>
                            
                            <p class="text-xs text-gray-500 text-center mt-4">*Valores estimados. Consulte nossa equipe para análise detalhada.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Partners & Universities -->
    <section class="py-24">
        <div class="container mx-auto px-4">
            <div class="text-center mb-16 scroll-reveal">
                <h2 class="serif text-3xl md:text-4xl font-bold mb-4">Parcerias Acadêmicas</h2>
                <p class="text-gray-400">Excelência técnica e inovação contínua</p>
            </div>
            
            <div class="flex flex-wrap justify-center gap-8 md:gap-16 opacity-60 grayscale hover:grayscale-0 transition-all duration-500">
                <div class="flex flex-col items-center gap-2 scroll-reveal">
                    <div class="w-24 h-24 rounded-full bg-white/10 flex items-center justify-center text-2xl font-bold text-white">UNICAMP</div>
                    <span class="text-sm text-gray-500">IA & Biomecânica</span>
                </div>
                <div class="flex flex-col items-center gap-2 scroll-reveal">
                    <div class="w-24 h-24 rounded-full bg-white/10 flex items-center justify-center text-2xl font-bold text-white">PUC</div>
                    <span class="text-sm text-gray-500">Gestão Social</span>
                </div>
                <div class="flex flex-col items-center gap-2 scroll-reveal">
                    <div class="w-24 h-24 rounded-full bg-white/10 flex items-center justify-center text-2xl font-bold text-white">ESPM</div>
                    <span class="text-sm text-gray-500">Inovação</span>
                </div>
                <div class="flex flex-col items-center gap-2 scroll-reveal">
                    <div class="w-24 h-24 rounded-full bg-white/10 flex items-center justify-center text-2xl font-bold text-white">USP</div>
                    <span class="text-sm text-gray-500">Pesquisa Aplicada</span>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black border-t border-red-900/20 py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8 mb-8">
                <div class="col-span-1 md:col-span-2">
                    <div class="flex items-center gap-3 mb-4">
                        <div class="w-8 h-8 ruby-gradient rounded-lg flex items-center justify-center">
                            <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2L2 12l10 10 10-10L12 2z"/></svg>
                        </div>
                        <span class="serif text-xl font-bold text-white">Sabedoria Prática ESG</span>
                    </div>
                    <p class="text-gray-500 text-sm max-w-md">
                        Transformando impostos em legado sustentável. Mais precioso que rubis, 
                        construímos territórios culturais permanentes que geram impacto mensurável e duradouro.
                    </p>
                </div>
                
                <div>
                    <h4 class="text-white font-semibold mb-4">Links Rápidos</h4>
                    <ul class="space-y-2 text-sm text-gray-500">
                        <li><a href="#sobre" class="hover:text-red-500 transition-colors">Sobre nós</a></li>
                        <li><a href="#territorios" class="hover:text-red-500 transition-colors">Territórios</a></li>
                        <li><a href="#cadastro" class="hover:text-red-500 transition-colors">Cadastrar Projeto</a></li>
                        <li><a href="#apoiar" class="hover:text-red-500 transition-colors">Seja Apoiador</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-semibold mb-4">Contato</h4>
                    <ul class="space-y-2 text-sm text-gray-500">
                        <li>contato@sabedoriapratica.org</li>
                        <li>São Paulo, SP - Brasil</li>
                        <li class="pt-2">
                            <button onclick="openModal('contactModal')" class="text-red-500 hover:text-red-400 font-medium">Fale Conosco →</button>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center gap-4">
                <p class="text-gray-600 text-sm">© 2026 Fundo Sabedoria Prática ESG. Todos os direitos reservados.</p>
                <div class="flex gap-4">
                    <a href="#" class="text-gray-600 hover:text-red-500 transition-colors">Privacidade</a>
                    <a href="#" class="text-gray-600 hover:text-red-500 transition-colors">Termos</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Contact Modal -->
    <div id="contactModal" class="modal items-center justify-center p-4">
        <div class="glass-panel rounded-3xl p-8 max-w-md w-full relative transform scale-95 opacity-0 transition-all duration-300" id="contactModalContent">
            <button onclick="closeModal('contactModal')" class="absolute top-4 right-4 text-gray-500 hover:text-white">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
            
            <h3 class="serif text-2xl font-bold mb-2 text-white">Fale com um Consultor</h3>
            <p class="text-gray-400 text-sm mb-6">Preencha seus dados e nossa equipe entrará em contato em até 24h.</p>
            
            <form class="space-y-4" onsubmit="handleContactSubmit(event)">
                <input type="text" placeholder="Nome completo" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600">
                <input type="email" placeholder="Email corporativo" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600">
                <input type="text" placeholder="Empresa" class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600">
                <select class="input-field w-full px-4 py-3 rounded-xl text-white bg-transparent">
                    <option value="" class="bg-gray-900">Interesse...</option>
                    <option value="empresa" class="bg-gray-900">Destinar IRPJ (Empresa)</option>
                    <option value="banco" class="bg-gray-900">Parceria (Banco)</option>
                    <option value="projeto" class="bg-gray-900">Cadastrar Projeto</option>
                </select>
                <button type="submit" class="w-full btn-primary py-3 rounded-xl text-white font-bold">Solicitar Contato</button>
            </form>
        </div>
    </div>

    <!-- Login Modal -->
    <div id="loginModal" class="modal items-center justify-center p-4">
        <div class="glass-panel rounded-3xl p-8 max-w-md w-full relative transform scale-95 opacity-0 transition-all duration-300" id="loginModalContent">
            <button onclick="closeModal('loginModal')" class="absolute top-4 right-4 text-gray-500 hover:text-white">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
            </button>
            
            <div class="text-center mb-6">
                <div class="w-16 h-16 ruby-gradient rounded-2xl flex items-center justify-center mx-auto mb-4">
                    <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2L2 12l10 10 10-10L12 2z"/></svg>
                </div>
                <h3 class="serif text-2xl font-bold text-white">Área Restrita</h3>
                <p class="text-gray-400 text-sm">Acesso para parceiros e gestores de projetos</p>
            </div>
            
            <form class="space-y-4" onsubmit="handleLogin(event)">
                <input type="email" placeholder="Email" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600">
                <input type="password" placeholder="Senha" required class="input-field w-full px-4 py-3 rounded-xl text-white placeholder-gray-600">
                <div class="flex justify-between text-sm">
                    <label class="flex items-center gap-2 text-gray-400">
                        <input type="checkbox" class="rounded border-gray-600 text-red-600 focus:ring-red-600 bg-gray-800"> Lembrar-me
                    </label>
                    <a href="#" class="text-red-500 hover:text-red-400">Esqueci a senha</a>
                </div>
                <button type="submit" class="w-full btn-primary py-3 rounded-xl text-white font-bold">Entrar</button>
            </form>
            
            <div class="mt-6 pt-6 border-t border-gray-800 text-center">
                <p class="text-sm text-gray-500">Ainda não tem acesso? <a href="#cadastro" onclick="closeModal('loginModal')" class="text-red-500 hover:text-red-400">Cadastre-se</a></p>
            </div>
        </div>
    </div>

    <!-- Success Notification -->
    <div id="notification" class="fixed bottom-4 right-4 transform translate-y-20 opacity-0 transition-all duration-500 z-50">
        <div class="glass-panel px-6 py-4 rounded-2xl border-l-4 border-green-500 flex items-center gap-3">
            <svg class="w-6 h-6 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
            <div>
                <h4 class="text-white font-semibold" id="notificationTitle">Sucesso!</h4>
                <p class="text-gray-400 text-sm" id="notificationText">Operação realizada com sucesso.</p>
            </div>
        </div>
    </div>

    <script>
        // Initialize GSAP ScrollTrigger
        gsap.registerPlugin(ScrollTrigger);
        
        // Scroll reveal animations
        gsap.utils.toArray('.scroll-reveal').forEach((element, i) => {
            gsap.to(element, {
                scrollTrigger: {
                    trigger: element,
                    start: "top 85%",
                    toggleActions: "play none none reverse"
                },
                opacity: 1,
                y: 0,
                duration: 0.8,
                ease: "power3.out",
                delay: i * 0.1
            });
        });
        
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('bg-black/90', 'shadow-lg', 'shadow-red-900/10');
            } else {
                navbar.classList.remove('bg-black/90', 'shadow-lg', 'shadow-red-900/10');
            }
        });
        
        // Mobile menu toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('translate-x-full');
        }
        
        // Modal functions
        function openModal(modalId) {
            const modal = document.getElementById(modalId);
            const content = document.getElementById(modalId + 'Content');
            modal.classList.add('active');
            setTimeout(() => {
                content.classList.remove('scale-95', 'opacity-0');
                content.classList.add('scale-100', 'opacity-100');
            }, 10);
        }
        
        function closeModal(modalId) {
            const modal = document.getElementById(modalId);
            const content = document.getElementById(modalId + 'Content');
            content.classList.remove('scale-100', 'opacity-100');
            content.classList.add('scale-95', 'opacity-0');
            setTimeout(() => {
                modal.classList.remove('active');
            }, 300);
        }
        
        // Close modal on outside click
        window.onclick = function(event) {
            if (event.target.classList.contains('modal')) {
                closeModal(event.target.id);
            }
        }
        
        // Smooth scroll
        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
        }
        
        // Simulation calculator
        function updateSimulation(value) {
            const formatted = new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL', maximumFractionDigits: 0 }).format(value);
            document.getElementById('irpjValue').textContent = formatted;
            
            const destinacao = value * 0.06;
            document.getElementById('destinacaoValor').textContent = new Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL', maximumFractionDigits: 0 }).format(destinacao);
            
            const vidas = Math.floor(destinacao / 500);
            document.getElementById('vidasImpactadas').textContent = vidas;
        }
        
        // Form handlers
        function showNotification(title, text) {
            const notif = document.getElementById('notification');
            document.getElementById('notificationTitle').textContent = title;
            document.getElementById('notificationText').textContent = text;
            notif.classList.remove('translate-y-20', 'opacity-0');
            setTimeout(() => {
                notif.classList.add('translate-y-20', 'opacity-0');
            }, 4000);
        }
        
        function handleProjectSubmit(e) {
            e.preventDefault();
            showNotification('Projeto Cadastrado!', 'Nossa equipe analisará sua proposta e entrará em contato em até 5 dias úteis.');
            e.target.reset();
        }
        
        function handleContactSubmit(e) {
            e.preventDefault();
            closeModal('contactModal');
            showNotification('Solicitação Enviada!', 'Um consultor entrará em contato em até 24 horas.');
            e.target.reset();
        }
        
        function handleLogin(e) {
            e.preventDefault();
            closeModal('loginModal');
            showNotification('Bem-vindo!', 'Redirecionando para sua dashboard...');
        }
        
        // Create floating particles
        function createParticles() {
            const container = document.body;
            for (let i = 0; i < 20; i++) {
                const particle = document.createElement('div');
                particle.className = 'ruby-particle';
                particle.style.left = Math.random() * 100 + 'vw';
                particle.style.top = Math.random() * 100 + 'vh';
                particle.style.animationDuration = (Math.random() * 10 + 10) + 's';
                particle.style.animationDelay = Math.random() * 5 + 's';
                container.appendChild(particle);
                
                gsap.to(particle, {
                    y: -100,
                    x: Math.random() * 100 - 50,
                    opacity: 0,
                    duration: Math.random() * 10 + 10,
                    repeat: -1,
                    ease: "none",
                    delay: Math.random() * 5
                });
            }
        }
        
        createParticles();
    </script>
</body>
</html>
