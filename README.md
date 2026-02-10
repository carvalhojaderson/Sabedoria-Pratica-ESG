<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fundo Sabedoria Prática ESG | O Legado da Virtude</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
    <script src="https://unpkg.com/lucide@latest"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: { sans: ['Inter', 'sans-serif'], serif: ['Playfair Display', 'serif'], display: ['Cinzel', 'serif'] },
                    colors: { 'ruby': '#9f1239', 'ruby-dark': '#4c0519', 'gold': '#d4af37', 'obsidian': '#0a0a0f', 'crimson': '#dc2626', 'bronze': '#cd7f32' }
                }
            }
        }
    </script>
    <style>
        body { background: #0a0a0f; color: #e2e8f0; overflow-x: hidden; cursor: none; }
        .cursor-dot, .cursor-outline { position: fixed; top: 0; left: 0; transform: translate(-50%, -50%); border-radius: 50%; z-index: 9999; pointer-events: none; }
        .cursor-dot { width: 5px; height: 5px; background: #dc2626; }
        .cursor-outline { width: 30px; height: 30px; border: 2px solid rgba(220, 38, 38, 0.5); transition: all 0.2s ease; }
        .cursor-outline.hover { width: 60px; height: 60px; background: rgba(220, 38, 38, 0.1); border-color: #d4af37; }
        .glass-ruby { background: rgba(159, 18, 57, 0.1); backdrop-filter: blur(20px); border: 1px solid rgba(220, 38, 38, 0.2); }
        .glass-bronze { background: rgba(205, 127, 50, 0.1); backdrop-filter: blur(20px); border: 1px solid rgba(205, 127, 50, 0.3); }
        .gradient-text { background: linear-gradient(135deg, #d4af37 0%, #dc2626 50%, #9f1239 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
        .gradient-text-bronze { background: linear-gradient(135deg, #cd7f32 0%, #d4af37 50%, #8b4513 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
        .territory-card { background: linear-gradient(135deg, rgba(159, 18, 57, 0.1) 0%, rgba(10, 10, 15, 0.9) 100%); border: 1px solid rgba(220, 38, 38, 0.3); transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1); }
        .territory-card:hover { transform: translateY(-10px) scale(1.02); border-color: #d4af37; box-shadow: 0 20px 40px rgba(220, 38, 38, 0.3); }
        .territory-card-masculino { background: linear-gradient(135deg, rgba(205, 127, 50, 0.1) 0%, rgba(10, 10, 15, 0.9) 100%); border: 1px solid rgba(205, 127, 50, 0.3); transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1); }
        .territory-card-masculino:hover { transform: translateY(-10px) scale(1.02); border-color: #cd7f32; box-shadow: 0 20px 40px rgba(205, 127, 50, 0.3); }
        .feature-image { border-radius: 24px; overflow: hidden; box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5); }
        .feature-image img { width: 100%; height: 100%; object-fit: cover; transition: transform 0.7s ease; }
        .feature-image:hover img { transform: scale(1.05); }
        .menu-mobile { clip-path: circle(0% at calc(100% - 40px) 40px); transition: clip-path 0.6s ease-in-out; }
        .menu-mobile.active { clip-path: circle(150% at calc(100% - 40px) 40px); }
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: #0a0a0f; }
        ::-webkit-scrollbar-thumb { background: linear-gradient(180deg, #dc2626, #d4af37); border-radius: 5px; }
    </style>
</head>
<body class="font-sans antialiased selection:bg-crimson selection:text-white">
    <div class="cursor-dot hidden md:block"></div>
    <div class="cursor-outline hidden md:block"></div>

    <!-- Navigation -->
    <nav class="fixed w-full z-50 top-0 transition-all duration-500" id="navbar">
        <div class="max-w-7xl mx-auto px-6 py-6">
            <div class="flex justify-between items-center">
                <a href="#" class="flex items-center space-x-3">
                    <div class="w-14 h-14 rounded-full border-2 border-gold/30 flex items-center justify-center bg-crimson/20">
                        <i data-lucide="gem" class="text-gold w-8 h-8"></i>
                    </div>
                    <div>
                        <span class="text-xl font-display font-bold text-white block tracking-wider">SABEDORIA</span>
                        <span class="text-xs text-crimson font-bold tracking-[0.3em] uppercase">Prática ESG</span>
                    </div>
                </a>
                <div class="hidden md:flex items-center space-x-8">
                    <a href="#visao" class="text-sm text-gray-400 hover:text-gold transition-colors">A Visão</a>
                    <a href="#territorios" class="text-sm text-gray-400 hover:text-gold transition-colors">Territórios</a>
                    <a href="#mulheres" class="text-sm text-crimson hover:text-red-400 font-medium">Águia</a>
                    <a href="#homens" class="text-sm text-amber-600 hover:text-amber-400 font-medium">Guardião</a>
                    <a href="#contato" class="bg-gradient-to-r from-crimson to-ruby text-white px-6 py-3 rounded-full text-sm font-bold hover:scale-105 transition-transform">Investir</a>
                </div>
                <button class="md:hidden text-white" id="menuToggle"><i data-lucide="menu" class="w-8 h-8"></i></button>
            </div>
        </div>
        <div class="menu-mobile fixed inset-0 bg-obsidian z-40 flex items-center justify-center md:hidden">
            <div class="text-center space-y-8">
                <a href="#visao" class="block text-3xl font-display text-white menu-link">A Visão</a>
                <a href="#territorios" class="block text-3xl font-display text-white menu-link">Territórios</a>
                <a href="#mulheres" class="block text-3xl font-display text-crimson menu-link">Território Águia</a>
                <a href="#homens" class="block text-3xl font-display text-amber-600 menu-link">Guardião Corpo</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden pt-20">
        <div class="absolute inset-0">
            <div class="absolute top-1/4 left-1/4 w-[500px] h-[500px] bg-crimson/20 rounded-full blur-[150px]"></div>
            <div class="absolute bottom-1/4 right-1/4 w-[600px] h-[600px] bg-bronze/10 rounded-full blur-[150px]"></div>
        </div>
        <div class="relative z-10 max-w-7xl mx-auto px-6 grid lg:grid-cols-2 gap-12 items-center">
            <div class="text-center lg:text-left">
                <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full glass-ruby border border-crimson/30 mb-6">
                    <span class="w-2 h-2 bg-crimson rounded-full animate-pulse"></span>
                    <span class="text-crimson text-xs font-bold tracking-widest uppercase">O Legado da Virtude</span>
                </div>
                <h1 class="font-display text-5xl md:text-7xl font-bold text-white mb-6">
                    <span class="block">Sabedoria</span>
                    <span class="gradient-text">Prática ESG</span>
                </h1>
                <p class="text-xl text-gray-300 mb-8 font-serif italic">"Mais preciosa que os rubis, a sabedoria guia a gestão virtuosa que transforma tributos em restauração de vidas."</p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center lg:justify-start">
                    <a href="#territorios" class="px-8 py-4 bg-gradient-to-r from-crimson to-ruby text-white rounded-full font-bold text-lg hover:scale-105 transition-transform shadow-xl">Descobrir Territórios</a>
                    <a href="#visao" class="px-8 py-4 glass-ruby text-white rounded-full font-medium text-lg border border-crimson/30">Nossa Estratégia</a>
                </div>
                <div class="mt-12 flex items-center justify-center lg:justify-start space-x-8">
                    <div class="text-center"><div class="text-3xl font-display font-bold text-gold">R$36M</div><div class="text-xs text-gray-500 uppercase">Meta Total</div></div>
                    <div class="h-12 w-px bg-gradient-to-b from-crimson to-gold"></div>
                    <div class="text-center"><div class="text-3xl font-display font-bold text-crimson">100%</div><div class="text-xs text-gray-500 uppercase">Equity-Free</div></div>
                    <div class="h-12 w-px bg-gradient-to-b from-crimson to-gold"></div>
                    <div class="text-center"><div class="text-3xl font-display font-bold text-gold">8+</div><div class="text-xs text-gray-500 uppercase">Territórios</div></div>
                </div>
            </div>
            <div>
                <div class="feature-image aspect-[4/5] max-w-md mx-auto relative">
                    <img src="https://images.unsplash.com/photo-1529156069898-49953e39b3ac?w=800&auto=format&fit=crop&q=80" alt="Comunidade unida">
                    <div class="absolute inset-0 bg-gradient-to-t from-obsidian via-transparent to-transparent opacity-80"></div>
                    <div class="absolute bottom-0 left-0 right-0 p-8">
                        <div class="glass-ruby rounded-2xl p-6 border border-crimson/30">
                            <div class="flex items-center space-x-3 mb-3">
                                <div class="w-10 h-10 rounded-full bg-crimson flex items-center justify-center"><i data-lucide="flame" class="w-5 h-5 text-gold"></i></div>
                                <span class="text-gold font-bold text-sm">TRANSFORMAÇÃO REAL</span>
                            </div>
                            <p class="text-white text-sm">Territórios culturais permanentes que convertem imposto em impacto mensurável</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- TERRITÓRIOS PILOTO -->
    <section id="territorios" class="py-32 bg-gradient-to-b from-obsidian via-ruby-dark/20 to-obsidian">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-20">
                <span class="text-crimson text-sm font-bold tracking-[0.3em] uppercase">Os Dois Pilares</span>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">Territórios <span class="gradient-text">Piloto</span></h2>
                <p class="text-gray-400 text-xl max-w-3xl mx-auto">Dois modelos complementares: um gerido por mulheres líderes, outro por homens guardiões.</p>
            </div>

            <div class="grid lg:grid-cols-2 gap-8">
                <!-- Território Águia -->
                <div class="territory-card rounded-3xl p-8">
                    <div class="flex items-center space-x-4 mb-6">
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-crimson to-ruby flex items-center justify-center">
                            <i data-lucide="bird" class="w-8 h-8 text-gold"></i>
                        </div>
                        <div>
                            <h3 class="font-display text-2xl font-bold text-white">Território Águia</h3>
                            <p class="text-crimson text-sm font-medium">Mulheres que Voam</p>
                        </div>
                    </div>
                    <div class="feature-image aspect-video mb-6">
                        <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?w=800&auto=format&fit=crop&q=80" alt="Território Águia">
                    </div>
                    <p class="text-gray-400 mb-6">Território gerido por <strong class="text-gold">mulheres líderes</strong>, criado para acolher, fortalecer e empoderar.</p>
                    <ul class="space-y-2 text-sm text-gray-300 mb-6">
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-crimson mr-2"></i>Rodas de conversa terapêuticas</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-crimson mr-2"></i>Atendimento a vítimas de violência</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-crimson mr-2"></i>Apoio LGBTQIA+</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-crimson mr-2"></i>Horta hidropônica resiliente</li>
                    </ul>
                    <div class="flex justify-between pt-6 border-t border-crimson/20">
                        <div class="text-center"><div class="text-2xl font-display font-bold text-gold">R$5M</div><div class="text-xs text-gray-500">Meta</div></div>
                        <div class="text-center"><div class="text-2xl font-display font-bold text-crimson">Via Rouanet</div><div class="text-xs text-gray-500">Captação</div></div>
                    </div>
                </div>

                <!-- Guardião Corpo -->
                <div class="territory-card-masculino rounded-3xl p-8">
                    <div class="flex items-center space-x-4 mb-6">
                        <div class="w-16 h-16 rounded-full bg-gradient-to-br from-amber-600 to-bronze flex items-center justify-center">
                            <i data-lucide="shield" class="w-8 h-8 text-white"></i>
                        </div>
                        <div>
                            <h3 class="font-display text-2xl font-bold text-white">Guardião Corpo</h3>
                            <p class="text-amber-600 text-sm font-medium">Homens Guardiões</p>
                        </div>
                    </div>
                    <div class="feature-image aspect-video mb-6">
                        <img src="https://images.unsplash.com/photo-1571019614242-c5c5dee9f50b?w=800&auto=format&fit=crop&q=80" alt="Guardião Corpo">
                    </div>
                    <p class="text-gray-400 mb-6">Liderado por <strong class="text-amber-500">homens guardiões</strong>. Entrada vulnerável, saída fortalecido fisica, mental e emocionalmente.</p>
                    <ul class="space-y-2 text-sm text-gray-300 mb-6">
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-amber-600 mr-2"></i>Parkour, Krav Maga, arqueria</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-amber-600 mr-2"></i>Biblioteca Viva: direito popular</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-amber-600 mr-2"></i>Incubadora: talento → negócio</li>
                        <li class="flex items-center"><i data-lucide="check-circle" class="w-4 h-4 text-amber-600 mr-2"></i>IA Unicamp: biomecânica</li>
                    </ul>
                    <div class="flex justify-between pt-6 border-t border-bronze/20">
                        <div class="text-center"><div class="text-2xl font-display font-bold text-amber-500">R$5M</div><div class="text-xs text-gray-500">Meta</div></div>
                        <div class="text-center"><div class="text-2xl font-display font-bold text-amber-600">3 Domos</div><div class="text-xs text-gray-500">Corpo+Mente+Cultura</div></div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO DETALHADA: TERRITÓRIO ÁGUIA -->
    <section id="mulheres" class="py-32 bg-gradient-to-b from-ruby-dark/30 via-obsidian to-ruby-dark/30">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div>
                    <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full glass-ruby border border-gold/30 mb-6">
                        <i data-lucide="crown" class="w-4 h-4 text-gold"></i>
                        <span class="text-gold text-xs font-bold tracking-widest uppercase">Liderança Feminina</span>
                    </div>
                    <h2 class="font-display text-5xl font-bold text-white mb-6">Território <span class="gradient-text">Águia</span></h2>
                    <p class="text-gray-400 text-lg mb-8">O território só dá estrutura — elas já têm a visão. <strong class="text-gold">Mulheres líderes</strong> que sabem onde pousar, quem puxar e quando soltar.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-crimson/20 flex items-center justify-center"><i data-lucide="heart" class="w-6 h-6 text-crimson"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Acolhimento Terapêutico</h4>
                                <p class="text-gray-400 text-sm">Rodas de conversa e atendimento a mulheres vítimas de violência doméstica.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-crimson/20 flex items-center justify-center"><i data-lucide="sprout" class="w-6 h-6 text-crimson"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Horta Hidropônica</h4>
                                <p class="text-gray-400 text-sm">Sistema sustentável que gera alimento e renda.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-crimson/20 flex items-center justify-center"><i data-lucide="palette" class="w-6 h-6 text-crimson"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Incubadora Cultural</h4>
                                <p class="text-gray-400 text-sm">Empreendimentos criativos liderados por mulheres.</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="relative">
                    <div class="absolute -inset-4 bg-gradient-to-r from-crimson to-gold rounded-3xl blur-2xl opacity-20"></div>
                    <div class="relative feature-image aspect-[4/5]">
                        <img src="https://images.unsplash.com/photo-1591848478625-de43268e6fb8?w=800&auto=format&fit=crop&q=80" alt="Mulheres líderes">
                        <div class="absolute inset-0 bg-gradient-to-t from-obsidian via-transparent to-transparent opacity-60"></div>
                        <div class="absolute bottom-0 left-0 right-0 p-8">
                            <div class="glass-ruby rounded-2xl p-6 border border-crimson/30">
                                <p class="text-white font-serif italic text-lg">"Ela veste-se de força e dignidade, e ri do futuro."</p>
                                <p class="text-gold text-sm mt-2">— Provérbios 31:25</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO DETALHADA: GUARDIÃO CORPO -->
    <section id="homens" class="py-32 bg-gradient-to-b from-obsidian via-amber-900/20 to-obsidian">
        <div class="max-w-7xl mx-auto px-6">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div class="order-2 relative">
                    <div class="absolute -inset-4 bg-gradient-to-r from-amber-600 to-bronze rounded-3xl blur-2xl opacity-20"></div>
                    <div class="relative feature-image aspect-[4/5]">
                        <img src="https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=800&auto=format&fit=crop&q=80" alt="Guardião Corpo">
                        <div class="absolute inset-0 bg-gradient-to-t from-obsidian via-transparent to-transparent opacity-60"></div>
                        <div class="absolute bottom-0 left-0 right-0 p-8">
                            <div class="glass-bronze rounded-2xl p-6 border border-amber-600/30">
                                <p class="text-white font-serif italic text-lg">"As suas forças são como as do boi selvagem."</p>
                                <p class="text-amber-500 text-sm mt-2">— Números 23:22</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="order-1">
                    <div class="inline-flex items-center space-x-2 px-4 py-2 rounded-full glass-bronze border border-amber-600/30 mb-6">
                        <i data-lucide="shield" class="w-4 h-4 text-amber-500"></i>
                        <span class="text-amber-500 text-xs font-bold tracking-widest uppercase">Liderança Masculina</span>
                    </div>
                    <h2 class="font-display text-5xl font-bold text-white mb-6">Guardião <span class="gradient-text-bronze">Corpo</span></h2>
                    <p class="text-gray-400 text-lg mb-8">Responde à necessidade urgente de <strong class="text-amber-500">modelos positivos de masculinidade</strong> nas periferias.</p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-amber-600/20 flex items-center justify-center"><i data-lucide="activity" class="w-6 h-6 text-amber-500"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Domo do Corpo Inteiro</h4>
                                <p class="text-gray-400 text-sm">Parkour, Krav Maga, arqueria, hip-hop.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-amber-600/20 flex items-center justify-center"><i data-lucide="book-open" class="w-6 h-6 text-amber-500"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Biblioteca Viva</h4>
                                <p class="text-gray-400 text-sm">Direito popular, história afro-brasileira.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-amber-600/20 flex items-center justify-center"><i data-lucide="trending-up" class="w-6 h-6 text-amber-500"></i></div>
                            <div>
                                <h4 class="text-white font-bold">Incubadora Cultural</h4>
                                <p class="text-gray-400 text-sm">Malabarista vira circo, rapper vira estúdio.</p>
                            </div>
                        </div>
                        <div class="flex items-start space-x-4">
                            <div class="w-12 h-12 rounded-xl bg-amber-600/20 flex items-center justify-center"><i data-lucide="cpu" class="w-6 h-6 text-amber-500"></i></div>
                            <div>
                                <h4 class="text-white font-bold">IA Unicamp</h4>
                                <p class="text-gray-400 text-sm">Análise biomecânica avançada.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SEÇÃO A VISÃO (ADICIONADA) -->
    <section id="visao" class="py-32 bg-gradient-to-b from-ruby-dark/20 via-obsidian to-ruby-dark/20">
        <div class="max-w-7xl mx-auto px-6">
            <div class="text-center mb-16">
                <span class="text-gold text-sm font-bold tracking-[0.3em] uppercase">Nossa Estratégia</span>
                <h2 class="font-display text-5xl md:text-6xl font-bold text-white mb-6">A <span class="gradient-text">Visão</span></h2>
                <p class="text-gray-400 text-xl max-w-3xl mx-auto">Transformar tributos em ferramentas de restauração social através de territórios culturais permanentes.</p>
            </div>
            
            <div class="grid md:grid-cols-3 gap-8">
                <div class="glass-ruby rounded-2xl p-8 text-center">
                    <div class="w-16 h-16 rounded-full bg-crimson/20 flex items-center justify-center mx-auto mb-4">
                        <i data-lucide="landmark" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="text-white font-bold text-xl mb-2">Captação Fiscal</h3>
                    <p class="text-gray-400 text-sm">Rouanet, Lei do Bem, Pronon e outras leis de incentivo fiscal.</p>
                </div>
                <div class="glass-ruby rounded-2xl p-8 text-center">
                    <div class="w-16 h-16 rounded-full bg-crimson/20 flex items-center justify-center mx-auto mb-4">
                        <i data-lucide="map-pin" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="text-white font-bold text-xl mb-2">Territórios Fixos</h3>
                    <p class="text-gray-400 text-sm">Espaços físicos permanentes com gestão local e autônoma.</p>
                </div>
                <div class="glass-ruby rounded-2xl p-8 text-center">
                    <div class="w-16 h-16 rounded-full bg-crimson/20 flex items-center justify-center mx-auto mb-4">
                        <i data-lucide="bar-chart-3" class="w-8 h-8 text-gold"></i>
                    </div>
                    <h3 class="text-white font-bold text-xl mb-2">Impacto Mensurável</h3>
                    <p class="text-gray-400 text-sm">Métricas claras de transformação social e retorno para investidores.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contato" class="border-t border-crimson/20 bg-obsidian py-16">
        <div class="max-w-7xl mx-auto px-6 text-center">
            <h2 class="font-display text-4xl font-bold text-white mb-8">Restaurando lares, <span class="gradient-text">revitalizando cidades</span></h2>
            <div class="flex flex-col sm:flex-row gap-6 justify-center mb-8">
                <a href="mailto:carvalhojaderson@gmail.com" class="px-8 py-4 bg-gradient-to-r from-crimson to-ruby text-white rounded-full font-bold hover:scale-105 transition-transform">carvalhojaderson@gmail.com</a>
                <a href="https://wa.me/5531982510633" class="px-8 py-4 glass-ruby text-white rounded-full font-bold border border-crimson/30 hover:bg-crimson/20 transition-colors">(31) 98251-0633</a>
            </div>
            <p class="text-gray-600 text-sm">© 2025 Fundo Sabedoria Prática ESG. Todos os direitos reservados.</p>
        </div>
    </footer>

    <script>
        // Inicializar ícones Lucide
        lucide.createIcons();
        
        // Cursor personalizado
        const cursorDot = document.querySelector('.cursor-dot');
        const cursorOutline = document.querySelector('.cursor-outline');
        
        window.addEventListener('mousemove', (e) => {
            cursorDot.style.left = e.clientX + 'px';
            cursorDot.style.top = e.clientY + 'px';
            cursorOutline.animate({ 
                left: e.clientX + 'px', 
                top: e.clientY + 'px' 
            }, { 
                duration: 500, 
                fill: "forwards" 
            });
        });
        
        // Efeito hover no cursor
        document.querySelectorAll('a, button').forEach(el => {
            el.addEventListener('mouseenter', () => cursorOutline.classList.add('hover'));
            el.addEventListener('mouseleave', () => cursorOutline.classList.remove('hover'));
        });
        
        // Menu mobile toggle
        const menuToggle = document.getElementById('menuToggle');
        const menuMobile = document.querySelector('.menu-mobile');
        
        menuToggle.addEventListener('click', () => {
            menuMobile.classList.toggle('active');
        });
        
        // Fechar menu ao clicar em link
        document.querySelectorAll('.menu-link').forEach(link => {
            link.addEventListener('click', () => {
                menuMobile.classList.remove('active');
            });
        });
        
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 100) {
                navbar.classList.add('bg-obsidian/90', 'backdrop-blur-md');
            } else {
                navbar.classList.remove('bg-obsidian/90', 'backdrop-blur-md');
            }
        });
        
        // Animações GSAP ScrollTrigger
        gsap.registerPlugin(ScrollTrigger);
        
        // Animação dos cards de território
        gsap.from('.territory-card', {
            scrollTrigger: {
                trigger: '#territorios',
                start: 'top 80%',
            },
            y: 50,
            opacity: 0,
            duration: 0.8,
            stagger: 0.2,
            ease: 'power3.out'
        });
        
        gsap.from('.territory-card-masculino', {
            scrollTrigger: {
                trigger: '#territorios',
                start: 'top 80%',
            },
            y: 50,
            opacity: 0,
            duration: 0.8,
            delay: 0.2,
            ease: 'power3.out'
        });
        
        // Animação das seções detalhadas
        gsap.from('#mulheres .grid > div', {
            scrollTrigger: {
                trigger: '#mulheres',
                start: 'top 70%',
            },
            x: -50,
            opacity: 0,
            duration: 1,
            stagger: 0.2,
            ease: 'power3.out'
        });
        
        gsap.from('#homens .grid > div', {
            scrollTrigger: {
                trigger: '#homens',
                start: 'top 70%',
            },
            x: 50,
            opacity: 0,
            duration: 1,
            stagger: 0.2,
            ease: 'power3.out'
        });
        
        // Smooth scroll para links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
