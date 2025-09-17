# 🧩 COMPONENTES AVANÇADOS E ÚNICOS

## 🌟 HERO SECTIONS INOVADORAS

### 1. Hero com Partículas Interativas
```html
<section class="relative min-h-screen overflow-hidden bg-gradient-to-br from-gray-900 via-purple-900 to-gray-900">
    <!-- Canvas para partículas -->
    <canvas id="particles-canvas" class="absolute inset-0"></canvas>
    
    <!-- Glassmorphism overlay -->
    <div class="absolute inset-0 bg-black/30 backdrop-blur-sm"></div>
    
    <!-- Conteúdo -->
    <div class="relative z-10 flex items-center justify-center min-h-screen">
        <div class="text-center max-w-5xl mx-auto px-4">
            <!-- Texto com gradiente animado -->
            <h1 class="text-6xl md:text-8xl font-black mb-6">
                <span class="bg-clip-text text-transparent bg-gradient-to-r from-cyan-400 via-purple-500 to-pink-500 animate-gradient-x">
                    Futuro Digital
                </span>
            </h1>
            
            <!-- Subtítulo com typewriter effect -->
            <div class="text-2xl text-gray-300 mb-8 h-8">
                <span class="typewriter"></span>
            </div>
            
            <!-- CTA com efeito magnético -->
            <button class="magnetic-btn relative group">
                <div class="absolute -inset-0.5 bg-gradient-to-r from-pink-600 to-purple-600 rounded-2xl blur opacity-75 group-hover:opacity-100 transition duration-1000 group-hover:duration-200 animate-tilt"></div>
                <div class="relative bg-black px-8 py-4 rounded-2xl leading-none flex items-center">
                    <span class="text-gray-100 font-semibold">Começar Jornada</span>
                    <svg class="w-5 h-5 ml-2 text-gray-100 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
                    </svg>
                </div>
            </button>
        </div>
    </div>
    
    <!-- Indicador de scroll animado -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2">
        <div class="w-6 h-10 border-2 border-white/30 rounded-full relative">
            <div class="absolute w-1.5 h-3 bg-white rounded-full left-1/2 transform -translate-x-1/2 top-2 animate-bounce"></div>
        </div>
    </div>
</section>
```

### 2. Hero Split Screen Dinâmico
```html
<section class="relative h-screen overflow-hidden">
    <!-- Lado Esquerdo - Imagem/Video -->
    <div class="absolute left-0 w-full md:w-1/2 h-full">
        <div class="relative h-full">
            <!-- Background com parallax -->
            <div class="absolute inset-0 bg-cover bg-center transform scale-110" 
                 style="background-image: url('...')"
                 data-parallax="0.5">
            </div>
            <!-- Overlay com padrão -->
            <div class="absolute inset-0 bg-gradient-to-r from-black/50 to-transparent"></div>
            <svg class="absolute inset-0 w-full h-full opacity-10">
                <pattern id="pattern" x="0" y="0" width="40" height="40" patternUnits="userSpaceOnUse">
                    <circle cx="20" cy="20" r="2" fill="white"/>
                </pattern>
                <rect width="100%" height="100%" fill="url(#pattern)"/>
            </svg>
        </div>
    </div>
    
    <!-- Lado Direito - Conteúdo -->
    <div class="relative md:absolute right-0 w-full md:w-1/2 h-full flex items-center bg-white">
        <div class="px-8 md:px-16 lg:px-24 max-w-2xl">
            <!-- Badge animado -->
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-primary-50 rounded-full mb-6">
                <span class="relative flex h-2 w-2">
                    <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-primary-400 opacity-75"></span>
                    <span class="relative inline-flex rounded-full h-2 w-2 bg-primary-500"></span>
                </span>
                <span class="text-primary-700 text-sm font-medium">Novo Lançamento</span>
            </div>
            
            <h1 class="text-5xl md:text-6xl font-bold text-gray-900 mb-6 leading-tight">
                Revolucione seu
                <span class="relative">
                    <span class="relative z-10">Negócio</span>
                    <!-- Underline animado -->
                    <svg class="absolute -bottom-2 left-0 w-full" height="8" viewBox="0 0 200 8">
                        <path d="M0 4 Q50 0 100 4 T200 4" stroke="url(#gradient)" stroke-width="3" fill="none" 
                              stroke-dasharray="200" stroke-dashoffset="200" class="animate-draw"/>
                        <defs>
                            <linearGradient id="gradient">
                                <stop offset="0%" stop-color="#3B82F6"/>
                                <stop offset="100%" stop-color="#8B5CF6"/>
                            </linearGradient>
                        </defs>
                    </svg>
                </span>
            </h1>
            
            <p class="text-xl text-gray-600 mb-8 leading-relaxed">
                Transforme ideias em resultados extraordinários com nossa plataforma revolucionária.
            </p>
            
            <!-- CTAs com hover criativo -->
            <div class="flex flex-wrap gap-4">
                <button class="group relative px-8 py-4 bg-gradient-to-r from-primary-600 to-primary-700 text-white rounded-xl font-semibold overflow-hidden transition-all hover:shadow-2xl">
                    <span class="relative z-10">Começar Agora</span>
                    <div class="absolute inset-0 bg-gradient-to-r from-purple-600 to-pink-600 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
                </button>
                
                <button class="group px-8 py-4 border-2 border-gray-300 rounded-xl font-semibold hover:border-primary-600 transition-colors">
                    <span class="flex items-center gap-2">
                        Ver Demo
                        <svg class="w-5 h-5 group-hover:translate-x-1 transition-transform" fill="none" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
                        </svg>
                    </span>
                </button>
            </div>
            
            <!-- Social Proof -->
            <div class="mt-12 flex items-center gap-6">
                <div class="flex -space-x-3">
                    <img class="w-10 h-10 rounded-full border-2 border-white" src="..." alt="">
                    <img class="w-10 h-10 rounded-full border-2 border-white" src="..." alt="">
                    <img class="w-10 h-10 rounded-full border-2 border-white" src="..." alt="">
                    <div class="w-10 h-10 rounded-full border-2 border-white bg-primary-600 flex items-center justify-center text-white text-xs font-bold">
                        +99
                    </div>
                </div>
                <div>
                    <div class="flex text-yellow-400">★★★★★</div>
                    <p class="text-sm text-gray-600">4.9/5 de 2.000+ avaliações</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

## 🎨 SEÇÕES FEATURES REVOLUCIONÁRIAS

### 1. Bento Grid Interativo
```html
<section class="py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4">
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
                Features que <span class="text-primary-600">Impressionam</span>
            </h2>
        </div>
        
        <!-- Bento Grid -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <!-- Card Grande -->
            <div class="md:col-span-2 md:row-span-2 group relative overflow-hidden rounded-3xl bg-gradient-to-br from-primary-500 to-purple-600 p-8 text-white">
                <div class="relative z-10">
                    <div class="w-16 h-16 bg-white/20 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 transition-transform">
                        <!-- Ícone SVG -->
                    </div>
                    <h3 class="text-3xl font-bold mb-4">Feature Principal</h3>
                    <p class="text-lg text-white/90 mb-6">
                        Descrição detalhada da feature mais importante do produto.
                    </p>
                    <button class="inline-flex items-center gap-2 text-white font-semibold group-hover:gap-4 transition-all">
                        Explorar
                        <svg class="w-5 h-5" fill="none" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"/>
                        </svg>
                    </button>
                </div>
                
                <!-- Decoração animada -->
                <div class="absolute -right-20 -bottom-20 w-80 h-80 bg-white/10 rounded-full group-hover:scale-110 transition-transform duration-700"></div>
                <div class="absolute -right-10 -bottom-10 w-60 h-60 bg-white/10 rounded-full group-hover:scale-125 transition-transform duration-700 delay-100"></div>
            </div>
            
            <!-- Cards Pequenos -->
            <div class="group relative overflow-hidden rounded-3xl bg-white p-6 shadow-lg hover:shadow-2xl transition-shadow">
                <div class="w-12 h-12 bg-primary-100 rounded-xl flex items-center justify-center mb-4 group-hover:rotate-12 transition-transform">
                    <!-- Ícone -->
                </div>
                <h3 class="text-xl font-bold text-gray-900 mb-2">Feature 2</h3>
                <p class="text-gray-600">Descrição concisa e impactante.</p>
            </div>
            
            <div class="group relative overflow-hidden rounded-3xl bg-gradient-to-br from-orange-400 to-pink-500 p-6 text-white">
                <div class="w-12 h-12 bg-white/20 rounded-xl flex items-center justify-center mb-4">
                    <!-- Ícone -->
                </div>
                <h3 class="text-xl font-bold mb-2">Feature 3</h3>
                <p class="text-white/90">Benefício claro e direto.</p>
                
                <!-- Badge -->
                <div class="absolute top-4 right-4 px-3 py-1 bg-white/20 backdrop-blur rounded-full text-xs font-semibold">
                    NOVO
                </div>
            </div>
            
            <!-- Card Horizontal -->
            <div class="md:col-span-2 group relative overflow-hidden rounded-3xl bg-gradient-to-r from-gray-900 to-gray-700 p-6 text-white">
                <div class="flex items-center justify-between">
                    <div>
                        <h3 class="text-2xl font-bold mb-2">Feature Especial</h3>
                        <p class="text-gray-300">Destaque para funcionalidade diferenciada.</p>
                    </div>
                    <div class="w-24 h-24 bg-white/10 rounded-2xl flex items-center justify-center group-hover:rotate-180 transition-transform duration-700">
                        <!-- Ícone Grande -->
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

### 2. Cards 3D Flip
```html
<section class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4">
        <div class="grid md:grid-cols-3 gap-8">
            <!-- Card 3D -->
            <div class="flip-card h-96">
                <div class="flip-card-inner relative w-full h-full transition-transform duration-700 transform-style-preserve-3d hover:rotate-y-180">
                    <!-- Frente -->
                    <div class="absolute w-full h-full backface-hidden rounded-2xl bg-gradient-to-br from-blue-500 to-purple-600 p-8 text-white">
                        <div class="flex flex-col h-full">
                            <div class="w-16 h-16 bg-white/20 rounded-2xl mb-6"></div>
                            <h3 class="text-2xl font-bold mb-4">Título Feature</h3>
                            <p class="text-white/90 flex-grow">Preview da feature</p>
                            <div class="text-sm font-semibold">Hover para detalhes →</div>
                        </div>
                    </div>
                    
                    <!-- Verso -->
                    <div class="absolute w-full h-full backface-hidden rounded-2xl bg-white shadow-2xl p-8 rotate-y-180">
                        <div class="flex flex-col h-full">
                            <h3 class="text-2xl font-bold text-gray-900 mb-4">Detalhes Completos</h3>
                            <ul class="space-y-3 flex-grow">
                                <li class="flex items-start gap-3">
                                    <svg class="w-5 h-5 text-green-500 mt-1 flex-shrink-0">
                                        <path fill="currentColor" d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                                    </svg>
                                    <span class="text-gray-700">Benefício detalhado 1</span>
                                </li>
                                <!-- Mais itens -->
                            </ul>
                            <button class="w-full py-3 bg-primary-600 text-white rounded-xl font-semibold hover:bg-primary-700 transition-colors">
                                Saber Mais
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```