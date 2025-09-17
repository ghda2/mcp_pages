# 🎪 SEÇÕES INOVADORAS E ÚNICAS

## 🌊 SEÇÃO TIMELINE INTERATIVA
```html
<section class="py-24 bg-gray-50 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4">
        <h2 class="text-4xl font-bold text-center mb-16">Nossa Jornada</h2>
        
        <!-- Timeline Container -->
        <div class="relative">
            <!-- Linha Central Animada -->
            <div class="absolute left-1/2 transform -translate-x-1/2 w-1 h-full bg-gray-300">
                <div class="timeline-progress absolute top-0 w-full bg-gradient-to-b from-primary-600 to-purple-600"></div>
            </div>
            
            <!-- Timeline Items -->
            <div class="space-y-24">
                <!-- Item 1 -->
                <div class="timeline-item opacity-0">
                    <div class="flex items-center">
                        <!-- Conteúdo Esquerda -->
                        <div class="w-1/2 pr-8 text-right">
                            <div class="inline-block">
                                <span class="text-sm text-primary-600 font-semibold">2020</span>
                                <h3 class="text-2xl font-bold text-gray-900 mt-2">Marco Importante</h3>
                                <p class="text-gray-600 mt-3">Descrição do evento ou conquista.</p>
                            </div>
                        </div>
                        
                        <!-- Círculo Central -->
                        <div class="relative flex items-center justify-center">
                            <div class="w-8 h-8 bg-white border-4 border-primary-600 rounded-full z-10"></div>
                            <div class="absolute w-20 h-20 bg-primary-100 rounded-full animate-ping"></div>
                        </div>
                        
                        <!-- Imagem Direita -->
                        <div class="w-1/2 pl-8">
                            <div class="relative group">
                                <img src="..." class="rounded-2xl shadow-lg group-hover:scale-105 transition-transform" alt="">
                                <div class="absolute inset-0 bg-gradient-to-t from-black/50 to-transparent rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Item 2 (Invertido) -->
                <div class="timeline-item opacity-0">
                    <div class="flex items-center">
                        <!-- Imagem Esquerda -->
                        <div class="w-1/2 pr-8">
                            <div class="relative group">
                                <img src="..." class="rounded-2xl shadow-lg group-hover:scale-105 transition-transform" alt="">
                            </div>
                        </div>
                        
                        <!-- Círculo Central -->
                        <div class="relative flex items-center justify-center">
                            <div class="w-8 h-8 bg-white border-4 border-purple-600 rounded-full z-10"></div>
                            <div class="absolute w-20 h-20 bg-purple-100 rounded-full animate-ping"></div>
                        </div>
                        
                        <!-- Conteúdo Direita -->
                        <div class="w-1/2 pl-8">
                            <span class="text-sm text-purple-600 font-semibold">2021</span>
                            <h3 class="text-2xl font-bold text-gray-900 mt-2">Evolução</h3>
                            <p class="text-gray-600 mt-3">Próximo passo na jornada.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

## 🎯 SEÇÃO COMPARAÇÃO INTERATIVA
```html
<section class="py-24 bg-white">
    <div class="max-w-6xl mx-auto px-4">
        <div class="text-center mb-16">
            <h2 class="text-4xl font-bold text-gray-900 mb-4">Escolha seu Plano</h2>
            <p class="text-xl text-gray-600">Compare e encontre a melhor opção</p>
        </div>
        
        <!-- Toggle Switch -->
        <div class="flex justify-center mb-12">
            <div class="bg-gray-100 p-1 rounded-full inline-flex">
                <button class="px-6 py-2 rounded-full bg-white shadow-sm font-medium transition-all">Mensal</button>
                <button class="px-6 py-2 rounded-full font-medium text-gray-600 transition-all">Anual</button>
            </div>
        </div>
        
        <!-- Cards de Preço -->
        <div class="grid md:grid-cols-3 gap-8">
            <!-- Plano Básico -->
            <div class="relative group">
                <div class="absolute inset-0 bg-gradient-to-r from-gray-200 to-gray-300 rounded-3xl blur-xl opacity-50 group-hover:opacity-75 transition-opacity"></div>
                <div class="relative bg-white rounded-3xl shadow-xl p-8 hover:scale-105 transition-transform">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900">Básico</h3>
                        <div class="mt-4 flex items-baseline justify-center">
                            <span class="text-5xl font-bold text-gray-900">R$29</span>
                            <span class="text-gray-600 ml-2">/mês</span>
                        </div>
                    </div>
                    
                    <ul class="mt-8 space-y-4">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 text-green-500 mr-3" fill="currentColor">
                                <path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                            </svg>
                            <span class="text-gray-700">Feature incluída</span>
                        </li>
                        <!-- Mais features -->
                    </ul>
                    
                    <button class="w-full mt-8 py-4 border-2 border-gray-300 rounded-xl font-semibold hover:border-gray-900 hover:bg-gray-900 hover:text-white transition-all">
                        Começar Agora
                    </button>
                </div>
            </div>
            
            <!-- Plano Popular (Destaque) -->
            <div class="relative group transform scale-105">
                <!-- Badge -->
                <div class="absolute -top-4 left-1/2 transform -translate-x-1/2 z-20">
                    <div class="bg-gradient-to-r from-primary-600 to-purple-600 text-white px-4 py-1 rounded-full text-sm font-semibold">
                        Mais Popular
                    </div>
                </div>
                
                <div class="absolute inset-0 bg-gradient-to-r from-primary-400 to-purple-400 rounded-3xl blur-xl opacity-75 group-hover:opacity-100 transition-opacity"></div>
                <div class="relative bg-gradient-to-br from-primary-600 to-purple-600 rounded-3xl shadow-2xl p-8 text-white">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold">Profissional</h3>
                        <div class="mt-4 flex items-baseline justify-center">
                            <span class="text-5xl font-bold">R$79</span>
                            <span class="text-white/80 ml-2">/mês</span>
                        </div>
                    </div>
                    
                    <ul class="mt-8 space-y-4">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 text-white mr-3" fill="currentColor">
                                <path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                            </svg>
                            <span>Feature Premium</span>
                        </li>
                    </ul>
                    
                    <button class="w-full mt-8 py-4 bg-white text-primary-600 rounded-xl font-bold hover:bg-gray-100 transition-colors shadow-lg">
                        Começar Teste Grátis
                    </button>
                </div>
            </div>
            
            <!-- Plano Enterprise -->
            <div class="relative group">
                <div class="absolute inset-0 bg-gradient-to-r from-gray-800 to-gray-900 rounded-3xl blur-xl opacity-50 group-hover:opacity-75 transition-opacity"></div>
                <div class="relative bg-white rounded-3xl shadow-xl p-8 hover:scale-105 transition-transform">
                    <div class="text-center">
                        <h3 class="text-2xl font-bold text-gray-900">Enterprise</h3>
                        <div class="mt-4">
                            <span class="text-3xl font-bold text-gray-900">Personalizado</span>
                        </div>
                    </div>
                    
                    <ul class="mt-8 space-y-4">
                        <li class="flex items-center">
                            <svg class="w-5 h-5 text-green-500 mr-3" fill="currentColor">
                                <path d="M9 16.17L4.83 12l-1.42 1.41L9 19 21 7l-1.41-1.41z"/>
                            </svg>
                            <span class="text-gray-700">Tudo do Pro</span>
                        </li>
                        <!-- Mais features -->
                    </ul>
                    
                    <button class="w-full mt-8 py-4 bg-gray-900 text-white rounded-xl font-semibold hover:bg-gray-800 transition-colors">
                        Falar com Vendas
                    </button>
                </div>
            </div>
        </div>
    </div>
</section>
```

## 🎮 SEÇÃO INTERATIVA COM TABS
```html
<section class="py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4">
        <div class="text-center mb-16">
            <h2 class="text-4xl font-bold text-gray-900">Como Funciona</h2>
        </div>
        
        <div class="grid md:grid-cols-2 gap-12 items-center">
            <!-- Tabs -->
            <div>
                <div class="space-y-4">
                    <!-- Tab 1 -->
                    <div class="tab-item group cursor-pointer p-6 bg-white rounded-2xl shadow-sm hover:shadow-xl transition-all border-l-4 border-transparent hover:border-primary-600" data-tab="1">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-primary-100 rounded-xl flex items-center justify-center group-hover:bg-primary-600 transition-colors">
                                <span class="text-primary-600 font-bold group-hover:text-white">1</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900">Passo 1: Configure</h3>
                                <p class="text-gray-600 mt-1">Personalize de acordo com suas necessidades</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Tab 2 -->
                    <div class="tab-item group cursor-pointer p-6 bg-white rounded-2xl shadow-sm hover:shadow-xl transition-all border-l-4 border-transparent hover:border-purple-600" data-tab="2">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center group-hover:bg-purple-600 transition-colors">
                                <span class="text-purple-600 font-bold group-hover:text-white">2</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900">Passo 2: Integre</h3>
                                <p class="text-gray-600 mt-1">Conecte com suas ferramentas favoritas</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Tab 3 -->
                    <div class="tab-item group cursor-pointer p-6 bg-white rounded-2xl shadow-sm hover:shadow-xl transition-all border-l-4 border-transparent hover:border-green-600" data-tab="3">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center group-hover:bg-green-600 transition-colors">
                                <span class="text-green-600 font-bold group-hover:text-white">3</span>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold text-gray-900">Passo 3: Cresça</h3>
                                <p class="text-gray-600 mt-1">Acompanhe resultados em tempo real</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Conteúdo Visual -->
            <div class="relative">
                <!-- Container para imagens/conteúdo que muda com tabs -->
                <div class="relative h-96 bg-gradient-to-br from-primary-100 to-purple-100 rounded-3xl overflow-hidden">
                    <!-- Conteúdo Tab 1 -->
                    <div class="tab-content absolute inset-0 p-8" data-content="1">
                        <!-- Mockup ou ilustração -->
                        <div class="w-full h-full bg-white rounded-2xl shadow-2xl p-6">
                            <!-- Conteúdo visual específico -->
                        </div>
                    </div>
                    
                    <!-- Decoração -->
                    <div class="absolute -top-10 -right-10 w-40 h-40 bg-primary-200 rounded-full opacity-50 blur-3xl"></div>
                    <div class="absolute -bottom-10 -left-10 w-40 h-40 bg-purple-200 rounded-full opacity-50 blur-3xl"></div>
                </div>
            </div>
        </div>
    </div>
</section>
```

## 🌟 SEÇÃO TESTIMONIALS DINÂMICA
```html
<section class="py-24 bg-white overflow-hidden">
    <div class="max-w-7xl mx-auto px-4">
        <div class="text-center mb-16">
            <h2 class="text-4xl font-bold text-gray-900 mb-4">O que Dizem Nossos Clientes</h2>
            <p class="text-xl text-gray-600">Histórias reais de transformação</p>
        </div>
        
        <!-- Carousel Container -->
        <div class="relative">
            <!-- Cards Slider -->
            <div class="flex gap-6 overflow-x-auto scrollbar-hide snap-x snap-mandatory">
                <!-- Testimonial Card 1 -->
                <div class="min-w-[400px] snap-center">
                    <div class="relative bg-gradient-to-br from-primary-50 to-purple-50 rounded-3xl p-8 h-full">
                        <!-- Quote Icon -->
                        <div class="absolute -top-4 -left-4 w-16 h-16 bg-primary-600 rounded-full flex items-center justify-center">
                            <svg class="w-8 h-8 text-white" fill="currentColor">
                                <path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10h-9.983zm-14.017 0v-7.391c0-5.704 3.748-9.57 9-10.609l.996 2.151c-2.433.917-3.996 3.638-3.996 5.849h3.983v10h-9.983z"/>
                            </svg>
                        </div>
                        
                        <!-- Stars -->
                        <div class="flex text-yellow-400 mb-4">
                            ★★★★★
                        </div>
                        
                        <!-- Testimonial -->
                        <p class="text-gray-700 text-lg mb-6 italic">
                            "Transformou completamente nossa forma de trabalhar. Resultados incríveis desde o primeiro dia!"
                        </p>
                        
                        <!-- Author -->
                        <div class="flex items-center gap-4">
                            <img src="..." alt="" class="w-12 h-12 rounded-full">
                            <div>
                                <div class="font-bold text-gray-900">João Silva</div>
                                <div class="text-sm text-gray-600">CEO, TechCorp</div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Testimonial Card 2 -->
                <div class="min-w-[400px] snap-center">
                    <div class="relative bg-gradient-to-br from-green-50 to-blue-50 rounded-3xl p-8 h-full">
                        <!-- Similar structure -->
                    </div>
                </div>
                
                <!-- Mais cards... -->
            </div>
            
            <!-- Navigation Dots -->
            <div class="flex justify-center gap-2 mt-8">
                <button class="w-3 h-3 rounded-full bg-primary-600"></button>
                <button class="w-3 h-3 rounded-full bg-gray-300"></button>
                <button class="w-3 h-3 rounded-full bg-gray-300"></button>
            </div>
        </div>
        
        <!-- Trust Badges -->
        <div class="mt-16 grid grid-cols-2 md:grid-cols-4 gap-8">
            <div class="text-center">
                <div class="text-3xl font-bold text-primary-600">10K+</div>
                <div class="text-gray-600">Clientes Ativos</div>
            </div>
            <div class="text-center">
                <div class="text-3xl font-bold text-purple-600">98%</div>
                <div class="text-gray-600">Satisfação</div>
            </div>
            <div class="text-center">
                <div class="text-3xl font-bold text-green-600">24/7</div>
                <div class="text-gray-600">Suporte</div>
            </div>
            <div class="text-center">
                <div class="text-3xl font-bold text-orange-600">5⭐</div>
                <div class="text-gray-600">Avaliação Média</div>
            </div>
        </div>
    </div>
</section>
---

## 🎪 SEÇÕES EXPERIENCIAIS ÚNICAS

### 🎯 Seção Virtual Reality Preview

```html
<section class="relative py-24 bg-black text-white overflow-hidden">
    <!-- Background particles -->
    <canvas id="vr-particles" class="absolute inset-0"></canvas>
    
    <div class="relative z-10 max-w-6xl mx-auto px-4">
        <div class="text-center mb-16">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-blue-500/20 backdrop-blur-sm rounded-full mb-6">
                <div class="w-2 h-2 bg-blue-400 rounded-full animate-pulse"></div>
                <span class="text-blue-300 text-sm font-medium">Experiência Imersiva</span>
            </div>
            
            <h2 class="text-5xl md:text-6xl font-bold mb-6">
                Entre no
                <span class="bg-gradient-to-r from-cyan-400 to-purple-600 bg-clip-text text-transparent">
                    Futuro
                </span>
            </h2>
            
            <p class="text-xl text-gray-300 max-w-3xl mx-auto">
                Explore nossa plataforma em realidade virtual antes mesmo de começar
            </p>
        </div>
        
        <div class="grid md:grid-cols-2 gap-12 items-center">
            <!-- VR Viewer -->
            <div class="relative">
                <div class="vr-viewer relative bg-gradient-to-br from-gray-800 to-gray-900 rounded-3xl p-8 shadow-2xl">
                    <!-- 360° Preview Container -->
                    <div id="vr-container" class="aspect-square rounded-2xl bg-gray-700 overflow-hidden cursor-grab active:cursor-grabbing">
                        <!-- Panoramic view will be loaded here -->
                        <div class="w-full h-full flex items-center justify-center">
                            <div class="text-center">
                                <div class="w-16 h-16 bg-blue-500 rounded-full flex items-center justify-center mb-4 mx-auto animate-spin">
                                    <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                                        <path d="M10 12a2 2 0 100-4 2 2 0 000 4z"/>
                                        <path fill-rule="evenodd" d="M.458 10C1.732 5.943 5.522 3 10 3s8.268 2.943 9.542 7c-1.274 4.057-5.064 7-9.542 7S1.732 14.057.458 10zM14 10a4 4 0 11-8 0 4 4 0 018 0z" clip-rule="evenodd"/>
                                    </svg>
                                </div>
                                <p class="text-gray-400">Carregando experiência VR...</p>
                            </div>
                        </div>
                    </div>
                    
                    <!-- VR Controls -->
                    <div class="flex justify-center gap-4 mt-6">
                        <button class="vr-control px-4 py-2 bg-white/10 backdrop-blur-sm rounded-xl hover:bg-white/20 transition-colors">
                            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                <path fill-rule="evenodd" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" clip-rule="evenodd"/>
                            </svg>
                        </button>
                        <button class="vr-control px-4 py-2 bg-white/10 backdrop-blur-sm rounded-xl hover:bg-white/20 transition-colors">
                            <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M10 12a2 2 0 100-4 2 2 0 000 4z"/>
                            </svg>
                        </button>
                        <button class="vr-control px-4 py-2 bg-blue-500 rounded-xl hover:bg-blue-600 transition-colors font-semibold">
                            VR Completo
                        </button>
                    </div>
                </div>
                
                <!-- Floating Info Points -->
                <div class="absolute top-4 right-4 w-8 h-8 bg-yellow-400 rounded-full flex items-center justify-center animate-pulse cursor-pointer">
                    <span class="text-xs font-bold text-black">!</span>
                </div>
                
                <div class="absolute bottom-8 left-8 w-8 h-8 bg-green-400 rounded-full flex items-center justify-center animate-pulse cursor-pointer">
                    <span class="text-xs font-bold text-black">?</span>
                </div>
            </div>
            
            <!-- Content -->
            <div>
                <div class="space-y-8">
                    <div class="feature-point opacity-0 transform translate-y-8">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-cyan-500/20 rounded-xl flex items-center justify-center flex-shrink-0">
                                <svg class="w-6 h-6 text-cyan-400" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/>
                                </svg>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold mb-2">Navegação Intuitiva</h3>
                                <p class="text-gray-400">Explore cada funcionalidade com movimentos naturais</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="feature-point opacity-0 transform translate-y-8">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-purple-500/20 rounded-xl flex items-center justify-center flex-shrink-0">
                                <svg class="w-6 h-6 text-purple-400" fill="currentColor" viewBox="0 0 20 20">
                                    <path d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"/>
                                </svg>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold mb-2">Dados em 3D</h3>
                                <p class="text-gray-400">Visualize informações complexas de forma simples</p>
                            </div>
                        </div>
                    </div>
                    
                    <div class="feature-point opacity-0 transform translate-y-8">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 bg-green-500/20 rounded-xl flex items-center justify-center flex-shrink-0">
                                <svg class="w-6 h-6 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M6.672 1.911a1 1 0 10-1.932.518l.259.966a1 1 0 001.932-.518l-.26-.966zM2.429 4.74a1 1 0 10-.517 1.932l.966.259a1 1 0 00.517-1.932l-.966-.26zm8.814-.569a1 1 0 00-1.415-1.414l-.707.707a1 1 0 101.415 1.415l.707-.708zm-7.071 7.072l.707-.707A1 1 0 003.465 9.12l-.708.707a1 1 0 001.415 1.415zm3.2-5.171a1 1 0 00-1.3 1.3l4 10a1 1 0 001.823.075l1.38-2.759 3.018 3.02a1 1 0 001.414-1.415l-3.019-3.02 2.76-1.379a1 1 0 00-.076-1.822l-10-4z" clip-rule="evenodd"/>
                                </svg>
                            </div>
                            <div>
                                <h3 class="text-xl font-bold mb-2">Interação Natural</h3>
                                <p class="text-gray-400">Controles gestuais para máxima imersão</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="mt-12 flex flex-col sm:flex-row gap-4">
                    <button class="px-8 py-4 bg-gradient-to-r from-cyan-500 to-purple-600 rounded-xl font-bold hover:shadow-2xl hover:scale-105 transition-all">
                        Experimentar VR
                    </button>
                    <button class="px-8 py-4 border border-white/20 rounded-xl font-semibold hover:bg-white/10 transition-colors">
                        Ver Demo 2D
                    </button>
                </div>
            </div>
        </div>
    </div>
</section>

<script>
class VRPreview {
    constructor() {
        this.container = document.getElementById('vr-container');
        this.isGrabbing = false;
        this.lastX = 0;
        this.rotation = 0;
        
        this.init();
    }
    
    init() {
        this.createScene();
        this.bindEvents();
        this.animateFeatures();
    }
    
    createScene() {
        // Create a simple 360° panoramic viewer
        this.container.innerHTML = `
            <div class="panorama-viewer relative w-full h-full bg-gradient-to-br from-blue-900 via-purple-900 to-pink-900 overflow-hidden">
                <div class="absolute inset-0 panorama-layer" style="transform: rotateY(${this.rotation}deg)">
                    <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/5 to-transparent"></div>
                    <div class="absolute top-1/4 left-1/4 w-2 h-2 bg-yellow-400 rounded-full animate-ping"></div>
                    <div class="absolute top-1/2 right-1/3 w-2 h-2 bg-green-400 rounded-full animate-ping"></div>
                    <div class="absolute bottom-1/3 left-1/2 w-2 h-2 bg-blue-400 rounded-full animate-ping"></div>
                </div>
                
                <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
                    <div class="w-8 h-8 border-2 border-white/50 rounded-full">
                        <div class="w-2 h-2 bg-white rounded-full m-auto mt-2"></div>
                    </div>
                </div>
            </div>
        `;
    }
    
    bindEvents() {
        this.container.addEventListener('mousedown', (e) => this.startGrab(e));
        this.container.addEventListener('mousemove', (e) => this.onGrab(e));
        this.container.addEventListener('mouseup', () => this.endGrab());
        this.container.addEventListener('mouseleave', () => this.endGrab());
        
        // Touch events
        this.container.addEventListener('touchstart', (e) => this.startGrab(e.touches[0]));
        this.container.addEventListener('touchmove', (e) => this.onGrab(e.touches[0]));
        this.container.addEventListener('touchend', () => this.endGrab());
    }
    
    startGrab(e) {
        this.isGrabbing = true;
        this.lastX = e.clientX;
        this.container.style.cursor = 'grabbing';
    }
    
    onGrab(e) {
        if (!this.isGrabbing) return;
        
        const deltaX = e.clientX - this.lastX;
        this.rotation += deltaX * 0.5;
        this.lastX = e.clientX;
        
        const panoramaLayer = this.container.querySelector('.panorama-layer');
        if (panoramaLayer) {
            panoramaLayer.style.transform = `rotateY(${this.rotation}deg)`;
        }
    }
    
    endGrab() {
        this.isGrabbing = false;
        this.container.style.cursor = 'grab';
    }
    
    animateFeatures() {
        const features = document.querySelectorAll('.feature-point');
        features.forEach((feature, index) => {
            setTimeout(() => {
                feature.style.transition = 'all 0.8s ease-out';
                feature.style.opacity = '1';
                feature.style.transform = 'translateY(0)';
            }, index * 200 + 500);
        });
    }
}

new VRPreview();
</script>
```

### 🌊 Seção Liquid Morphing

```html
<section class="relative py-24 bg-gradient-to-br from-indigo-900 via-purple-900 to-pink-900 overflow-hidden">
    <!-- Liquid Background -->
    <div class="absolute inset-0">
        <svg class="w-full h-full" viewBox="0 0 1200 800" preserveAspectRatio="xMidYMid slice">
            <defs>
                <linearGradient id="liquidGradient" x1="0%" y1="0%" x2="100%" y2="100%">
                    <stop offset="0%" stop-color="#667eea" stop-opacity="0.8"/>
                    <stop offset="50%" stop-color="#764ba2" stop-opacity="0.6"/>
                    <stop offset="100%" stop-color="#f093fb" stop-opacity="0.4"/>
                </linearGradient>
            </defs>
            
            <!-- Animated liquid shapes -->
            <path class="liquid-blob" fill="url(#liquidGradient)" d="M300,400 Q600,200 900,400 Q600,600 300,400 Z">
                <animate attributeName="d" 
                         values="M300,400 Q600,200 900,400 Q600,600 300,400 Z;
                                 M200,300 Q700,150 1000,350 Q700,650 200,300 Z;
                                 M400,300 Q500,250 800,450 Q500,550 400,300 Z;
                                 M300,400 Q600,200 900,400 Q600,600 300,400 Z"
                         dur="8s" 
                         repeatCount="indefinite"/>
            </path>
            
            <path class="liquid-blob" fill="url(#liquidGradient)" d="M100,200 Q400,100 700,300 Q400,500 100,200 Z">
                <animate attributeName="d" 
                         values="M100,200 Q400,100 700,300 Q400,500 100,200 Z;
                                 M150,150 Q450,50 750,250 Q450,450 150,150 Z;
                                 M50,250 Q350,150 650,350 Q350,550 50,250 Z;
                                 M100,200 Q400,100 700,300 Q400,500 100,200 Z"
                         dur="10s" 
                         repeatCount="indefinite"/>
            </path>
        </svg>
    </div>
    
    <div class="relative z-10 max-w-6xl mx-auto px-4">
        <div class="text-center text-white mb-16">
            <h2 class="text-5xl md:text-6xl font-bold mb-6">
                Design que 
                <span class="relative">
                    <span class="morphing-text">Flui</span>
                </span>
            </h2>
            <p class="text-xl text-white/80 max-w-3xl mx-auto">
                Interfaces que se adaptam naturalmente aos seus usuários
            </p>
        </div>
        
        <div class="grid md:grid-cols-3 gap-8">
            <!-- Morphing Cards -->
            <div class="morphing-card group">
                <div class="relative bg-white/10 backdrop-blur-sm rounded-3xl p-8 hover:bg-white/20 transition-all duration-700">
                    <!-- Floating Icon -->
                    <div class="w-16 h-16 bg-white/20 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-12 transition-all duration-700">
                        <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                            <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3z"/>
                        </svg>
                    </div>
                    
                    <h3 class="text-2xl font-bold text-white mb-4">Adaptativo</h3>
                    <p class="text-white/70 mb-6">
                        Interface que aprende com o comportamento do usuário
                    </p>
                    
                    <!-- Morphing progress bar -->
                    <div class="w-full h-2 bg-white/20 rounded-full overflow-hidden">
                        <div class="h-full bg-gradient-to-r from-cyan-400 to-purple-500 rounded-full morphing-progress"
                             style="width: 0%; animation: morphing-fill 3s ease-in-out infinite alternate;"></div>
                    </div>
                </div>
            </div>
            
            <div class="morphing-card group">
                <div class="relative bg-white/10 backdrop-blur-sm rounded-3xl p-8 hover:bg-white/20 transition-all duration-700">
                    <div class="w-16 h-16 bg-white/20 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-12 transition-all duration-700">
                        <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M11.49 3.17c-.38-1.56-2.6-1.56-2.98 0a1.532 1.532 0 01-2.286.948c-1.372-.836-2.942.734-2.106 2.106.54.886.061 2.042-.947 2.287-1.561.379-1.561 2.6 0 2.978a1.532 1.532 0 01.947 2.287c-.836 1.372.734 2.942 2.106 2.106a1.532 1.532 0 012.287.947c.379 1.561 2.6 1.561 2.978 0a1.533 1.533 0 012.287-.947c1.372.836 2.942-.734 2.106-2.106a1.533 1.533 0 01.947-2.287c1.561-.379 1.561-2.6 0-2.978a1.532 1.532 0 01-.947-2.287c.836-1.372-.734-2.942-2.106-2.106a1.532 1.532 0 01-2.287-.947zM10 13a3 3 0 100-6 3 3 0 000 6z" clip-rule="evenodd"/>
                        </svg>
                    </div>
                    
                    <h3 class="text-2xl font-bold text-white mb-4">Inteligente</h3>
                    <p class="text-white/70 mb-6">
                        IA que otimiza automaticamente a experiência
                    </p>
                    
                    <div class="w-full h-2 bg-white/20 rounded-full overflow-hidden">
                        <div class="h-full bg-gradient-to-r from-green-400 to-blue-500 rounded-full morphing-progress"
                             style="width: 0%; animation: morphing-fill 4s ease-in-out infinite alternate 1s;"></div>
                    </div>
                </div>
            </div>
            
            <div class="morphing-card group">
                <div class="relative bg-white/10 backdrop-blur-sm rounded-3xl p-8 hover:bg-white/20 transition-all duration-700">
                    <div class="w-16 h-16 bg-white/20 rounded-2xl flex items-center justify-center mb-6 group-hover:scale-110 group-hover:rotate-12 transition-all duration-700">
                        <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 20 20">
                            <path d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"/>
                        </svg>
                    </div>
                    
                    <h3 class="text-2xl font-bold text-white mb-4">Responsivo</h3>
                    <p class="text-white/70 mb-6">
                        Layout que se molda a qualquer dispositivo
                    </p>
                    
                    <div class="w-full h-2 bg-white/20 rounded-full overflow-hidden">
                        <div class="h-full bg-gradient-to-r from-pink-400 to-orange-500 rounded-full morphing-progress"
                             style="width: 0%; animation: morphing-fill 5s ease-in-out infinite alternate 2s;"></div>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Interactive Demo -->
        <div class="mt-20 text-center">
            <div class="inline-block relative">
                <button class="morphing-demo-btn relative px-12 py-6 bg-white text-purple-900 rounded-full font-bold text-xl overflow-hidden group">
                    <span class="relative z-10">Experimentar Agora</span>
                    
                    <!-- Morphing background -->
                    <div class="absolute inset-0 bg-gradient-to-r from-cyan-400 via-purple-500 to-pink-500 opacity-0 group-hover:opacity-100 transition-all duration-700 morphing-bg"></div>
                </button>
                
                <!-- Floating particles around button -->
                <div class="absolute -inset-8 pointer-events-none">
                    <div class="floating-particle absolute w-2 h-2 bg-cyan-400 rounded-full animate-float" style="top: 10%; left: 20%;"></div>
                    <div class="floating-particle absolute w-2 h-2 bg-purple-500 rounded-full animate-float" style="top: 80%; right: 15%; animation-delay: 1s;"></div>
                    <div class="floating-particle absolute w-2 h-2 bg-pink-400 rounded-full animate-float" style="bottom: 60%; left: 10%; animation-delay: 2s;"></div>
                </div>
            </div>
        </div>
    </div>
</section>

<style>
@keyframes morphing-fill {
    0% { width: 20%; border-radius: 10px 0 0 10px; }
    50% { width: 70%; border-radius: 10px; }
    100% { width: 90%; border-radius: 0 10px 10px 0; }
}

@keyframes morphing-text {
    0%, 100% { transform: scaleX(1) scaleY(1); }
    25% { transform: scaleX(1.1) scaleY(0.9); }
    50% { transform: scaleX(0.9) scaleY(1.1); }
    75% { transform: scaleX(1.05) scaleY(0.95); }
}

@keyframes float {
    0%, 100% { transform: translateY(0px) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(180deg); }
}

.morphing-text {
    animation: morphing-text 4s ease-in-out infinite;
    display: inline-block;
}

.morphing-bg {
    border-radius: 50%;
    transform: scale(0);
    transition: all 0.7s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.morphing-demo-btn:hover .morphing-bg {
    transform: scale(1.5);
    border-radius: 20%;
}

.animate-float {
    animation: float 4s ease-in-out infinite;
}
</style>
```

### 🎮 Seção Gaming Interface

```html
<section class="py-24 bg-gradient-to-br from-gray-900 via-indigo-900 to-purple-900 text-white overflow-hidden">
    <div class="max-w-7xl mx-auto px-4">
        <div class="text-center mb-16">
            <div class="inline-flex items-center gap-2 px-4 py-2 bg-green-500/20 backdrop-blur-sm rounded-full mb-6">
                <div class="w-2 h-2 bg-green-400 rounded-full animate-pulse"></div>
                <span class="text-green-300 text-sm font-medium">Sistema Ativo</span>
            </div>
            
            <h2 class="text-5xl md:text-6xl font-bold mb-6">
                Level Up Your
                <span class="bg-gradient-to-r from-cyan-400 to-purple-600 bg-clip-text text-transparent">
                    Business
                </span>
            </h2>
        </div>
        
        <div class="grid lg:grid-cols-2 gap-12 items-center">
            <!-- Gaming Console -->
            <div class="relative">
                <div class="gaming-console relative bg-gradient-to-br from-gray-800 to-gray-900 rounded-3xl p-8 shadow-2xl">
                    <!-- Screen -->
                    <div class="screen bg-black rounded-2xl p-6 mb-6 relative overflow-hidden">
                        <!-- HUD Elements -->
                        <div class="hud-overlay absolute inset-0">
                            <!-- Health Bar -->
                            <div class="absolute top-4 left-4">
                                <div class="text-xs text-green-400 mb-1">PERFORMANCE</div>
                                <div class="w-32 h-2 bg-gray-700 rounded-full overflow-hidden">
                                    <div class="h-full bg-gradient-to-r from-green-400 to-yellow-400 rounded-full performance-bar"
                                         style="width: 0%; animation: fill-bar 3s ease-out forwards;"></div>
                                </div>
                            </div>
                            
                            <!-- Score -->
                            <div class="absolute top-4 right-4 text-right">
                                <div class="text-xs text-blue-400 mb-1">REVENUE</div>
                                <div class="text-2xl font-bold text-white score-counter" data-target="234567">0</div>
                            </div>
                            
                            <!-- Level -->
                            <div class="absolute bottom-4 left-4">
                                <div class="text-xs text-purple-400 mb-1">LEVEL</div>
                                <div class="text-4xl font-bold text-white level-counter" data-target="42">1</div>
                            </div>
                            
                            <!-- Mini-map -->
                            <div class="absolute bottom-4 right-4 w-24 h-24 bg-gray-800/80 rounded-lg p-2">
                                <div class="w-full h-full bg-gradient-to-br from-blue-900 to-purple-900 rounded relative">
                                    <div class="absolute w-2 h-2 bg-yellow-400 rounded-full animate-ping" style="top: 30%; left: 40%;"></div>
                                    <div class="absolute w-1 h-1 bg-green-400 rounded-full" style="top: 60%; right: 20%;"></div>
                                    <div class="absolute w-1 h-1 bg-red-400 rounded-full" style="bottom: 20%; left: 20%;"></div>
                                </div>
                            </div>
                            
                            <!-- Center crosshair -->
                            <div class="absolute inset-0 flex items-center justify-center">
                                <div class="w-8 h-8 border border-green-400/50 rounded-full">
                                    <div class="w-2 h-2 bg-green-400 rounded-full m-auto mt-2 animate-pulse"></div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Game Scene -->
                        <div class="relative h-48 bg-gradient-to-b from-blue-900 to-purple-900 rounded-lg overflow-hidden">
                            <!-- Floating elements -->
                            <div class="floating-coin absolute w-6 h-6 bg-yellow-400 rounded-full animate-bounce" style="top: 20%; left: 30%;"></div>
                            <div class="floating-coin absolute w-4 h-4 bg-green-400 rounded-full animate-bounce" style="top: 60%; right: 25%; animation-delay: 0.5s;"></div>
                            <div class="floating-coin absolute w-5 h-5 bg-blue-400 rounded-full animate-bounce" style="bottom: 30%; left: 60%; animation-delay: 1s;"></div>
                        </div>
                    </div>
                    
                    <!-- Gaming Controls -->
                    <div class="flex justify-between items-center">
                        <!-- D-Pad -->
                        <div class="relative w-16 h-16">
                            <div class="gaming-dpad absolute inset-0">
                                <div class="absolute top-0 left-1/2 transform -translate-x-1/2 w-4 h-6 bg-gray-600 rounded-t cursor-pointer hover:bg-gray-500 transition-colors"></div>
                                <div class="absolute bottom-0 left-1/2 transform -translate-x-1/2 w-4 h-6 bg-gray-600 rounded-b cursor-pointer hover:bg-gray-500 transition-colors"></div>
                                <div class="absolute left-0 top-1/2 transform -translate-y-1/2 w-6 h-4 bg-gray-600 rounded-l cursor-pointer hover:bg-gray-500 transition-colors"></div>
                                <div class="absolute right-0 top-1/2 transform -translate-y-1/2 w-6 h-4 bg-gray-600 rounded-r cursor-pointer hover:bg-gray-500 transition-colors"></div>
                                <div class="absolute inset-0 flex items-center justify-center">
                                    <div class="w-6 h-6 bg-gray-700 rounded"></div>
                                </div>
                            </div>
                        </div>
                        
                        <!-- Action Buttons -->
                        <div class="flex gap-3">
                            <button class="action-btn w-10 h-10 bg-blue-500 rounded-full font-bold text-white hover:bg-blue-400 transition-all transform hover:scale-110 active:scale-95">
                                A
                            </button>
                            <button class="action-btn w-10 h-10 bg-green-500 rounded-full font-bold text-white hover:bg-green-400 transition-all transform hover:scale-110 active:scale-95">
                                B
                            </button>
                            <button class="action-btn w-10 h-10 bg-red-500 rounded-full font-bold text-white hover:bg-red-400 transition-all transform hover:scale-110 active:scale-95">
                                X
                            </button>
                            <button class="action-btn w-10 h-10 bg-yellow-500 rounded-full font-bold text-white hover:bg-yellow-400 transition-all transform hover:scale-110 active:scale-95">
                                Y
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- Game Stats -->
            <div class="space-y-8">
                <div class="achievement-card bg-gradient-to-r from-yellow-500/20 to-orange-500/20 backdrop-blur-sm rounded-2xl p-6 border border-yellow-500/30">
                    <div class="flex items-center gap-4">
                        <div class="w-16 h-16 bg-yellow-500/20 rounded-xl flex items-center justify-center">
                            <svg class="w-8 h-8 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
                            </svg>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold mb-1">Master Achiever</h3>
                            <p class="text-gray-300">Unlocked advanced analytics</p>
                            <div class="mt-2 text-yellow-400 text-sm">+2,500 XP</div>
                        </div>
                    </div>
                </div>
                
                <div class="achievement-card bg-gradient-to-r from-purple-500/20 to-pink-500/20 backdrop-blur-sm rounded-2xl p-6 border border-purple-500/30">
                    <div class="flex items-center gap-4">
                        <div class="w-16 h-16 bg-purple-500/20 rounded-xl flex items-center justify-center">
                            <svg class="w-8 h-8 text-purple-400" fill="currentColor" viewBox="0 0 20 20">
                                <path fill-rule="evenodd" d="M6.267 3.455a3.066 3.066 0 001.745-.723 3.066 3.066 0 013.976 0 3.066 3.066 0 001.745.723 3.066 3.066 0 012.812 2.812c.051.643.304 1.254.723 1.745a3.066 3.066 0 010 3.976 3.066 3.066 0 00-.723 1.745 3.066 3.066 0 01-2.812 2.812 3.066 3.066 0 00-1.745.723 3.066 3.066 0 01-3.976 0 3.066 3.066 0 00-1.745-.723 3.066 3.066 0 01-2.812-2.812 3.066 3.066 0 00-.723-1.745 3.066 3.066 0 010-3.976 3.066 3.066 0 00.723-1.745 3.066 3.066 0 012.812-2.812zm7.44 5.252a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                            </svg>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold mb-1">Speed Runner</h3>
                            <p class="text-gray-300">Completed setup in record time</p>
                            <div class="mt-2 text-purple-400 text-sm">+5,000 XP</div>
                        </div>
                    </div>
                </div>
                
                <div class="achievement-card bg-gradient-to-r from-green-500/20 to-teal-500/20 backdrop-blur-sm rounded-2xl p-6 border border-green-500/30">
                    <div class="flex items-center gap-4">
                        <div class="w-16 h-16 bg-green-500/20 rounded-xl flex items-center justify-center">
                            <svg class="w-8 h-8 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M2 10.5a1.5 1.5 0 113 0v6a1.5 1.5 0 01-3 0v-6zM6 10.333v5.43a2 2 0 001.106 1.79l.05.025A4 4 0 008.943 18h5.416a2 2 0 001.962-1.608l1.2-6A2 2 0 0015.56 8H12V4a2 2 0 00-2-2 1 1 0 00-1 1v.667a4 4 0 01-.8 2.4L6.8 7.933a4 4 0 00-.8 2.4z"/>
                            </svg>
                        </div>
                        <div>
                            <h3 class="text-xl font-bold mb-1">Team Player</h3>
                            <p class="text-gray-300">Collaborated with 10+ users</p>
                            <div class="mt-2 text-green-400 text-sm">+1,000 XP</div>
                        </div>
                    </div>
                </div>
                
                <!-- Start Game Button -->
                <button class="start-game-btn w-full py-6 bg-gradient-to-r from-green-500 to-teal-500 rounded-2xl font-bold text-xl text-white hover:shadow-2xl hover:scale-105 transition-all relative overflow-hidden group">
                    <span class="relative z-10">START GAME</span>
                    
                    <!-- Animated background -->
                    <div class="absolute inset-0 bg-gradient-to-r from-teal-500 to-green-500 transform scale-x-0 group-hover:scale-x-100 transition-transform origin-left duration-500"></div>
                    
                    <!-- Particles -->
                    <div class="absolute inset-0 opacity-0 group-hover:opacity-100 transition-opacity">
                        <div class="absolute w-1 h-1 bg-white rounded-full animate-ping" style="top: 20%; left: 20%;"></div>
                        <div class="absolute w-1 h-1 bg-white rounded-full animate-ping" style="top: 60%; right: 30%; animation-delay: 0.5s;"></div>
                        <div class="absolute w-1 h-1 bg-white rounded-full animate-ping" style="bottom: 30%; left: 70%; animation-delay: 1s;"></div>
                    </div>
                </button>
            </div>
        </div>
    </div>
</section>

<style>
@keyframes fill-bar {
    0% { width: 0%; }
    100% { width: 85%; }
}

.gaming-console {
    box-shadow: 
        0 0 20px rgba(59, 130, 246, 0.3),
        inset 0 1px 0 rgba(255, 255, 255, 0.1);
}

.action-btn {
    box-shadow: 
        0 4px 0 rgba(0, 0, 0, 0.3),
        0 0 10px rgba(255, 255, 255, 0.1);
}

.action-btn:active {
    box-shadow: 
        0 2px 0 rgba(0, 0, 0, 0.3),
        0 0 5px rgba(255, 255, 255, 0.1);
}

.achievement-card {
    backdrop-filter: blur(10px);
    animation: slideInFromRight 0.8s ease-out forwards;
    opacity: 0;
    transform: translateX(50px);
}

.achievement-card:nth-child(1) { animation-delay: 0.2s; }
.achievement-card:nth-child(2) { animation-delay: 0.4s; }
.achievement-card:nth-child(3) { animation-delay: 0.6s; }

@keyframes slideInFromRight {
    to {
        opacity: 1;
        transform: translateX(0);
    }
}
</style>

<script>
class GamingInterface {
    constructor() {
        this.score = 0;
        this.level = 1;
        this.targetScore = 234567;
        this.targetLevel = 42;
        
        this.init();
    }
    
    init() {
        this.animateCounters();
        this.bindGameControls();
    }
    
    animateCounters() {
        // Score counter
        const scoreElement = document.querySelector('.score-counter');
        this.animateCounter(scoreElement, this.targetScore, 3000);
        
        // Level counter
        const levelElement = document.querySelector('.level-counter');
        this.animateCounter(levelElement, this.targetLevel, 2000);
    }
    
    animateCounter(element, target, duration) {
        const start = 0;
        const startTime = performance.now();
        
        const animate = (currentTime) => {
            const elapsed = currentTime - startTime;
            const progress = Math.min(elapsed / duration, 1);
            
            const current = Math.floor(start + (target - start) * this.easeOutCubic(progress));
            element.textContent = current.toLocaleString();
            
            if (progress < 1) {
                requestAnimationFrame(animate);
            }
        };
        
        requestAnimationFrame(animate);
    }
    
    easeOutCubic(t) {
        return 1 - Math.pow(1 - t, 3);
    }
    
    bindGameControls() {
        // Action buttons
        document.querySelectorAll('.action-btn').forEach(btn => {
            btn.addEventListener('click', () => {
                this.triggerButtonEffect(btn);
            });
        });
        
        // D-pad
        document.querySelectorAll('.gaming-dpad > div').forEach(btn => {
            btn.addEventListener('click', () => {
                this.triggerDpadEffect(btn);
            });
        });
        
        // Start game button
        document.querySelector('.start-game-btn').addEventListener('click', () => {
            this.startGame();
        });
    }
    
    triggerButtonEffect(button) {
        // Add visual feedback
        button.style.transform = 'scale(0.95)';
        button.style.boxShadow = '0 2px 0 rgba(0, 0, 0, 0.3)';
        
        setTimeout(() => {
            button.style.transform = '';
            button.style.boxShadow = '';
        }, 150);
        
        // Add particle effect
        this.createParticles(button);
    }
    
    triggerDpadEffect(button) {
        button.style.background = '#9CA3AF';
        setTimeout(() => {
            button.style.background = '';
        }, 150);
    }
    
    createParticles(element) {
        const rect = element.getBoundingClientRect();
        const centerX = rect.left + rect.width / 2;
        const centerY = rect.top + rect.height / 2;
        
        for (let i = 0; i < 5; i++) {
            const particle = document.createElement('div');
            particle.className = 'game-particle';
            particle.style.cssText = `
                position: fixed;
                width: 4px;
                height: 4px;
                background: white;
                border-radius: 50%;
                pointer-events: none;
                z-index: 9999;
                left: ${centerX}px;
                top: ${centerY}px;
            `;
            
            document.body.appendChild(particle);
            
            // Animate particle
            const angle = (Math.PI * 2 * i) / 5;
            const distance = 50 + Math.random() * 30;
            const x = Math.cos(angle) * distance;
            const y = Math.sin(angle) * distance;
            
            particle.animate([
                { transform: 'translate(0, 0) scale(1)', opacity: 1 },
                { transform: `translate(${x}px, ${y}px) scale(0)`, opacity: 0 }
            ], {
                duration: 600,
                easing: 'cubic-bezier(0.25, 0.46, 0.45, 0.94)'
            }).onfinish = () => {
                particle.remove();
            };
        }
    }
    
    startGame() {
        // Trigger screen flash effect
        const flash = document.createElement('div');
        flash.style.cssText = `
            position: fixed;
            inset: 0;
            background: rgba(255, 255, 255, 0.8);
            z-index: 9999;
            pointer-events: none;
        `;
        
        document.body.appendChild(flash);
        
        flash.animate([
            { opacity: 0 },
            { opacity: 1 },
            { opacity: 0 }
        ], {
            duration: 300,
            easing: 'ease-out'
        }).onfinish = () => {
            flash.remove();
        };
        
        // Add some game logic here
        console.log('Game Started!');
    }
}

// Initialize gaming interface
new GamingInterface();
</script>
```
```