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
---

## 🎪 COMPONENTES 3D E WEBGL

### 🌟 Elemento 3D com Three.js

```html
<!-- Container 3D -->
<div id="three-container" class="w-full h-96 rounded-3xl overflow-hidden bg-gradient-to-br from-gray-900 to-purple-900"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<script>
class ThreeScene {
    constructor(containerId) {
        this.container = document.getElementById(containerId);
        this.scene = new THREE.Scene();
        this.camera = new THREE.PerspectiveCamera(75, this.container.offsetWidth / this.container.offsetHeight, 0.1, 1000);
        this.renderer = new THREE.WebGLRenderer({ antialias: true, alpha: true });
        this.mesh = null;
        this.mouse = { x: 0, y: 0 };
        
        this.init();
    }
    
    init() {
        // Setup renderer
        this.renderer.setSize(this.container.offsetWidth, this.container.offsetHeight);
        this.renderer.setClearColor(0x000000, 0);
        this.container.appendChild(this.renderer.domElement);
        
        // Create geometry
        const geometry = new THREE.IcosahedronGeometry(2, 1);
        
        // Create material with shader
        const material = new THREE.ShaderMaterial({
            uniforms: {
                time: { value: 0 },
                color1: { value: new THREE.Color(0x667eea) },
                color2: { value: new THREE.Color(0x764ba2) },
                mouse: { value: new THREE.Vector2(0, 0) }
            },
            vertexShader: `
                uniform float time;
                uniform vec2 mouse;
                varying float vNoise;
                
                void main() {
                    vec3 pos = position;
                    float noise = sin(pos.x * 2.0 + time) * sin(pos.y * 2.0 + time) * sin(pos.z * 2.0 + time);
                    pos += normal * noise * 0.1;
                    
                    // Mouse interaction
                    pos.x += mouse.x * 0.5;
                    pos.y += mouse.y * 0.5;
                    
                    vNoise = noise;
                    
                    gl_Position = projectionMatrix * modelViewMatrix * vec4(pos, 1.0);
                }
            `,
            fragmentShader: `
                uniform float time;
                uniform vec3 color1;
                uniform vec3 color2;
                varying float vNoise;
                
                void main() {
                    vec3 color = mix(color1, color2, vNoise * 0.5 + 0.5);
                    gl_FragColor = vec4(color, 0.8);
                }
            `,
            transparent: true
        });
        
        this.mesh = new THREE.Mesh(geometry, material);
        this.scene.add(this.mesh);
        
        this.camera.position.z = 5;
        
        // Mouse interaction
        this.container.addEventListener('mousemove', (e) => {
            const rect = this.container.getBoundingClientRect();
            this.mouse.x = ((e.clientX - rect.left) / rect.width) * 2 - 1;
            this.mouse.y = -((e.clientY - rect.top) / rect.height) * 2 + 1;
        });
        
        // Resize handler
        window.addEventListener('resize', () => this.onResize());
        
        this.animate();
    }
    
    animate() {
        requestAnimationFrame(() => this.animate());
        
        // Update uniforms
        this.mesh.material.uniforms.time.value += 0.01;
        this.mesh.material.uniforms.mouse.value.set(this.mouse.x, this.mouse.y);
        
        // Rotate mesh
        this.mesh.rotation.x += 0.005;
        this.mesh.rotation.y += 0.01;
        
        this.renderer.render(this.scene, this.camera);
    }
    
    onResize() {
        this.camera.aspect = this.container.offsetWidth / this.container.offsetHeight;
        this.camera.updateProjectionMatrix();
        this.renderer.setSize(this.container.offsetWidth, this.container.offsetHeight);
    }
}

// Initialize
new ThreeScene('three-container');
</script>
```

### 🎨 Shader Background Dinâmico

```html
<div id="shader-bg" class="fixed inset-0 -z-10"></div>

<script>
class ShaderBackground {
    constructor() {
        this.scene = new THREE.Scene();
        this.camera = new THREE.OrthographicCamera(-1, 1, 1, -1, 0, 1);
        this.renderer = new THREE.WebGLRenderer();
        this.uniforms = {
            time: { value: 0 },
            resolution: { value: new THREE.Vector2() },
            mouse: { value: new THREE.Vector2() }
        };
        
        this.init();
    }
    
    init() {
        const container = document.getElementById('shader-bg');
        this.renderer.setSize(window.innerWidth, window.innerHeight);
        container.appendChild(this.renderer.domElement);
        
        this.uniforms.resolution.value.set(window.innerWidth, window.innerHeight);
        
        const geometry = new THREE.PlaneGeometry(2, 2);
        const material = new THREE.ShaderMaterial({
            uniforms: this.uniforms,
            vertexShader: `
                void main() {
                    gl_Position = vec4(position, 1.0);
                }
            `,
            fragmentShader: `
                uniform float time;
                uniform vec2 resolution;
                uniform vec2 mouse;
                
                vec3 palette(float t) {
                    vec3 a = vec3(0.5, 0.5, 0.5);
                    vec3 b = vec3(0.5, 0.5, 0.5);
                    vec3 c = vec3(1.0, 1.0, 1.0);
                    vec3 d = vec3(0.263, 0.416, 0.557);
                    
                    return a + b * cos(6.28318 * (c * t + d));
                }
                
                void main() {
                    vec2 uv = (gl_FragCoord.xy * 2.0 - resolution.xy) / resolution.y;
                    vec2 uv0 = uv;
                    vec3 finalColor = vec3(0.0);
                    
                    for (float i = 0.0; i < 4.0; i++) {
                        uv = fract(uv * 1.5) - 0.5;
                        
                        float d = length(uv) * exp(-length(uv0));
                        vec3 col = palette(length(uv0) + i * 0.4 + time * 0.4);
                        
                        d = sin(d * 8.0 + time) / 8.0;
                        d = abs(d);
                        d = pow(0.01 / d, 1.2);
                        
                        finalColor += col * d;
                    }
                    
                    gl_FragColor = vec4(finalColor, 0.1);
                }
            `
        });
        
        const mesh = new THREE.Mesh(geometry, material);
        this.scene.add(mesh);
        
        // Mouse tracking
        document.addEventListener('mousemove', (e) => {
            this.uniforms.mouse.value.set(e.clientX, e.clientY);
        });
        
        window.addEventListener('resize', () => this.onResize());
        this.animate();
    }
    
    animate() {
        requestAnimationFrame(() => this.animate());
        this.uniforms.time.value += 0.01;
        this.renderer.render(this.scene, this.camera);
    }
    
    onResize() {
        this.renderer.setSize(window.innerWidth, window.innerHeight);
        this.uniforms.resolution.value.set(window.innerWidth, window.innerHeight);
    }
}

new ShaderBackground();
</script>
```

---

## 🎮 COMPONENTES INTERATIVOS GAMIFICADOS

### 🎯 Quiz Interativo com Pontuação

```html
<div class="quiz-container max-w-4xl mx-auto p-8 bg-white rounded-3xl shadow-2xl">
    <div class="quiz-header mb-8">
        <div class="flex justify-between items-center mb-4">
            <h2 class="text-3xl font-bold text-gray-900">Quiz Interativo</h2>
            <div class="score-display bg-gradient-to-r from-purple-500 to-pink-500 text-white px-6 py-2 rounded-full font-bold">
                Pontos: <span id="score">0</span>
            </div>
        </div>
        
        <!-- Progress Bar -->
        <div class="w-full bg-gray-200 rounded-full h-3">
            <div id="progress-bar" class="bg-gradient-to-r from-green-400 to-blue-500 h-3 rounded-full transition-all duration-500" style="width: 0%"></div>
        </div>
        <div class="text-center mt-2 text-gray-600">
            Pergunta <span id="current-question">1</span> de <span id="total-questions">5</span>
        </div>
    </div>
    
    <div id="quiz-content">
        <!-- Questions will be inserted here -->
    </div>
    
    <div id="quiz-results" class="hidden text-center">
        <div class="mb-6">
            <div class="text-6xl mb-4">🎉</div>
            <h3 class="text-3xl font-bold text-gray-900 mb-2">Parabéns!</h3>
            <p class="text-xl text-gray-600">Você completou o quiz!</p>
        </div>
        
        <div class="final-score bg-gradient-to-r from-purple-100 to-pink-100 rounded-2xl p-8 mb-6">
            <div class="text-4xl font-bold text-purple-700 mb-2">
                <span id="final-score">0</span> / <span id="max-score">0</span>
            </div>
            <p class="text-purple-600">Pontuação Final</p>
        </div>
        
        <button class="restart-quiz bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-xl font-semibold hover:shadow-lg transition-shadow">
            Tentar Novamente
        </button>
    </div>
</div>

<style>
.quiz-option {
    @apply w-full p-6 text-left border-2 border-gray-200 rounded-xl transition-all duration-300 hover:border-purple-300 hover:bg-purple-50;
}

.quiz-option.correct {
    @apply border-green-500 bg-green-50 text-green-800;
}

.quiz-option.incorrect {
    @apply border-red-500 bg-red-50 text-red-800;
}

.quiz-option.selected {
    @apply border-purple-500 bg-purple-50;
}

@keyframes celebrate {
    0%, 100% { transform: scale(1) rotate(0deg); }
    25% { transform: scale(1.1) rotate(5deg); }
    75% { transform: scale(1.1) rotate(-5deg); }
}

.celebrate {
    animation: celebrate 0.6s ease-in-out;
}
</style>

<script>
class InteractiveQuiz {
    constructor() {
        this.questions = [
            {
                question: "Qual é a principal vantagem de usar micro-interações em interfaces?",
                options: [
                    "Reduzir o tempo de carregamento",
                    "Melhorar a experiência do usuário",
                    "Diminuir o código necessário",
                    "Aumentar a velocidade do servidor"
                ],
                correct: 1,
                points: 20
            },
            {
                question: "O que é GSAP?",
                options: [
                    "Uma linguagem de programação",
                    "Um framework CSS",
                    "Uma biblioteca de animações JavaScript",
                    "Um tipo de servidor"
                ],
                correct: 2,
                points: 20
            },
            // Add more questions...
        ];
        
        this.currentQuestion = 0;
        this.score = 0;
        this.selectedAnswers = [];
        
        this.init();
    }
    
    init() {
        this.updateProgress();
        this.showQuestion();
        
        document.querySelector('.restart-quiz').addEventListener('click', () => {
            this.restart();
        });
    }
    
    showQuestion() {
        const question = this.questions[this.currentQuestion];
        const content = document.getElementById('quiz-content');
        
        content.innerHTML = `
            <div class="question-card">
                <h3 class="text-2xl font-bold text-gray-900 mb-8">${question.question}</h3>
                <div class="options-grid space-y-4">
                    ${question.options.map((option, index) => `
                        <button class="quiz-option" onclick="quiz.selectAnswer(${index})">
                            <div class="flex items-center justify-between">
                                <span>${option}</span>
                                <div class="option-indicator w-6 h-6 border-2 border-gray-300 rounded-full"></div>
                            </div>
                        </button>
                    `).join('')}
                </div>
                
                <div class="mt-8 text-center">
                    <button id="next-btn" class="hidden bg-purple-600 text-white px-8 py-3 rounded-xl font-semibold hover:bg-purple-700 transition-colors" onclick="quiz.nextQuestion()">
                        ${this.currentQuestion === this.questions.length - 1 ? 'Ver Resultado' : 'Próxima Pergunta'}
                    </button>
                </div>
            </div>
        `;
    }
    
    selectAnswer(selectedIndex) {
        const question = this.questions[this.currentQuestion];
        const options = document.querySelectorAll('.quiz-option');
        const indicators = document.querySelectorAll('.option-indicator');
        
        // Clear previous selections
        options.forEach(option => option.classList.remove('selected', 'correct', 'incorrect'));
        
        // Mark selected answer
        options[selectedIndex].classList.add('selected');
        
        // Show correct/incorrect after a delay
        setTimeout(() => {
            options.forEach((option, index) => {
                if (index === question.correct) {
                    option.classList.add('correct');
                    indicators[index].innerHTML = '✓';
                    indicators[index].classList.add('bg-green-500', 'text-white');
                } else if (index === selectedIndex && index !== question.correct) {
                    option.classList.add('incorrect');
                    indicators[index].innerHTML = '✗';
                    indicators[index].classList.add('bg-red-500', 'text-white');
                }
            });
            
            // Update score
            if (selectedIndex === question.correct) {
                this.score += question.points;
                this.updateScore();
                this.showCelebration();
            }
            
            document.getElementById('next-btn').classList.remove('hidden');
        }, 500);
        
        this.selectedAnswers[this.currentQuestion] = selectedIndex;
    }
    
    nextQuestion() {
        this.currentQuestion++;
        
        if (this.currentQuestion < this.questions.length) {
            this.updateProgress();
            this.showQuestion();
        } else {
            this.showResults();
        }
    }
    
    updateProgress() {
        const progress = ((this.currentQuestion) / this.questions.length) * 100;
        document.getElementById('progress-bar').style.width = progress + '%';
        document.getElementById('current-question').textContent = this.currentQuestion + 1;
        document.getElementById('total-questions').textContent = this.questions.length;
    }
    
    updateScore() {
        document.getElementById('score').textContent = this.score;
    }
    
    showCelebration() {
        const scoreDisplay = document.querySelector('.score-display');
        scoreDisplay.classList.add('celebrate');
        setTimeout(() => {
            scoreDisplay.classList.remove('celebrate');
        }, 600);
    }
    
    showResults() {
        const maxScore = this.questions.reduce((total, q) => total + q.points, 0);
        
        document.getElementById('quiz-content').classList.add('hidden');
        document.getElementById('quiz-results').classList.remove('hidden');
        document.getElementById('final-score').textContent = this.score;
        document.getElementById('max-score').textContent = maxScore;
        
        // Update progress to 100%
        document.getElementById('progress-bar').style.width = '100%';
    }
    
    restart() {
        this.currentQuestion = 0;
        this.score = 0;
        this.selectedAnswers = [];
        
        document.getElementById('quiz-content').classList.remove('hidden');
        document.getElementById('quiz-results').classList.add('hidden');
        
        this.updateProgress();
        this.updateScore();
        this.showQuestion();
    }
}

// Initialize quiz
const quiz = new InteractiveQuiz();
</script>
```

### 🎪 Carousel 3D Infinito

```html
<div class="carousel-3d-container relative h-96 overflow-hidden">
    <div id="carousel-3d" class="carousel-3d h-full flex items-center justify-center">
        <!-- Items will be inserted here -->
    </div>
    
    <div class="carousel-controls absolute bottom-6 left-1/2 transform -translate-x-1/2 flex gap-4">
        <button class="carousel-prev bg-white/20 backdrop-blur-sm text-white p-3 rounded-full hover:bg-white/30 transition-colors">
            <svg class="w-6 h-6" fill="none" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
            </svg>
        </button>
        <button class="carousel-next bg-white/20 backdrop-blur-sm text-white p-3 rounded-full hover:bg-white/30 transition-colors">
            <svg class="w-6 h-6" fill="none" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
            </svg>
        </button>
    </div>
</div>

<style>
.carousel-3d-container {
    perspective: 1000px;
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.carousel-item {
    position: absolute;
    width: 300px;
    height: 200px;
    background: white;
    border-radius: 20px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    font-weight: bold;
    color: #333;
    transition: all 0.6s cubic-bezier(0.23, 1, 0.320, 1);
    cursor: pointer;
}

.carousel-item:hover {
    transform: scale(1.05) !important;
    box-shadow: 0 30px 60px rgba(0,0,0,0.2);
}
</style>

<script>
class Carousel3D {
    constructor() {
        this.items = [
            { title: "Item 1", color: "#FF6B6B" },
            { title: "Item 2", color: "#4ECDC4" },
            { title: "Item 3", color: "#45B7D1" },
            { title: "Item 4", color: "#96CEB4" },
            { title: "Item 5", color: "#FFEAA7" },
            { title: "Item 6", color: "#DDA0DD" },
        ];
        
        this.currentIndex = 0;
        this.container = document.getElementById('carousel-3d');
        this.itemElements = [];
        
        this.init();
    }
    
    init() {
        this.createItems();
        this.positionItems();
        this.bindEvents();
        
        // Auto-rotate
        setInterval(() => {
            this.next();
        }, 4000);
    }
    
    createItems() {
        this.items.forEach((item, index) => {
            const element = document.createElement('div');
            element.className = 'carousel-item';
            element.style.background = `linear-gradient(135deg, ${item.color}, ${this.shadeColor(item.color, -20)})`;
            element.innerHTML = `
                <div class="text-center">
                    <div class="text-2xl font-bold mb-2">${item.title}</div>
                    <div class="text-sm opacity-75">Descrição do item</div>
                </div>
            `;
            
            this.container.appendChild(element);
            this.itemElements.push(element);
        });
    }
    
    positionItems() {
        const radius = 350;
        const angleStep = (2 * Math.PI) / this.items.length;
        
        this.itemElements.forEach((element, index) => {
            const angle = angleStep * (index - this.currentIndex);
            const x = Math.sin(angle) * radius;
            const z = Math.cos(angle) * radius;
            const scale = z > 0 ? 0.8 : 1.2;
            const opacity = z > 0 ? 0.7 : 1;
            const rotateY = -(angle * 180 / Math.PI);
            
            element.style.transform = `
                translateX(${x}px) 
                translateZ(${z}px) 
                scale(${scale}) 
                rotateY(${rotateY}deg)
            `;
            element.style.opacity = opacity;
            element.style.zIndex = Math.round(z);
        });
    }
    
    next() {
        this.currentIndex = (this.currentIndex + 1) % this.items.length;
        this.positionItems();
    }
    
    prev() {
        this.currentIndex = (this.currentIndex - 1 + this.items.length) % this.items.length;
        this.positionItems();
    }
    
    bindEvents() {
        document.querySelector('.carousel-next').addEventListener('click', () => this.next());
        document.querySelector('.carousel-prev').addEventListener('click', () => this.prev());
        
        // Touch/swipe support
        let startX = 0;
        this.container.addEventListener('touchstart', (e) => {
            startX = e.touches[0].clientX;
        });
        
        this.container.addEventListener('touchend', (e) => {
            const endX = e.changedTouches[0].clientX;
            const diff = startX - endX;
            
            if (Math.abs(diff) > 50) {
                if (diff > 0) {
                    this.next();
                } else {
                    this.prev();
                }
            }
        });
    }
    
    shadeColor(color, percent) {
        const R = parseInt(color.substring(1, 3), 16);
        const G = parseInt(color.substring(3, 5), 16);
        const B = parseInt(color.substring(5, 7), 16);
        
        const newR = Math.round(R * (100 + percent) / 100);
        const newG = Math.round(G * (100 + percent) / 100);
        const newB = Math.round(B * (100 + percent) / 100);
        
        return `#${newR.toString(16).padStart(2, '0')}${newG.toString(16).padStart(2, '0')}${newB.toString(16).padStart(2, '0')}`;
    }
}

new Carousel3D();
</script>
```

---

## 🎨 COMPONENTES DE DADOS VISUAIS

### 📊 Dashboard Interativo

```html
<div class="dashboard-grid grid grid-cols-1 md:grid-cols-3 gap-6 p-6">
    <!-- Metric Card -->
    <div class="metric-card bg-white rounded-2xl p-6 shadow-lg hover:shadow-xl transition-shadow">
        <div class="flex items-center justify-between mb-4">
            <div class="metric-icon w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center">
                <svg class="w-6 h-6 text-blue-600" fill="currentColor" viewBox="0 0 20 20">
                    <path d="M2 11a1 1 0 011-1h2a1 1 0 011 1v5a1 1 0 01-1 1H3a1 1 0 01-1-1v-5zM8 7a1 1 0 011-1h2a1 1 0 011 1v9a1 1 0 01-1 1H9a1 1 0 01-1-1V7zM14 4a1 1 0 011-1h2a1 1 0 011 1v12a1 1 0 01-1 1h-2a1 1 0 01-1-1V4z"/>
                </svg>
            </div>
            <div class="metric-trend text-green-500 text-sm font-semibold">+12.5%</div>
        </div>
        <div class="metric-value text-3xl font-bold text-gray-900 mb-1" data-target="2847">0</div>
        <div class="metric-label text-gray-600">Usuários Ativos</div>
        
        <!-- Mini Chart -->
        <div class="mt-4">
            <canvas class="mini-chart" width="200" height="50"></canvas>
        </div>
    </div>
    
    <!-- Progress Ring -->
    <div class="progress-ring-card bg-gradient-to-br from-purple-500 to-pink-500 rounded-2xl p-6 text-white">
        <div class="flex items-center justify-between mb-4">
            <h3 class="text-lg font-semibold">Meta Mensal</h3>
            <div class="text-sm opacity-75">75% completo</div>
        </div>
        
        <div class="flex items-center justify-center">
            <div class="relative w-32 h-32">
                <svg class="w-32 h-32 transform -rotate-90" viewBox="0 0 100 100">
                    <!-- Background circle -->
                    <circle cx="50" cy="50" r="40" stroke="rgba(255,255,255,0.2)" stroke-width="8" fill="none"/>
                    <!-- Progress circle -->
                    <circle cx="50" cy="50" r="40" stroke="white" stroke-width="8" fill="none" 
                            stroke-linecap="round" stroke-dasharray="251.2" stroke-dashoffset="62.8"
                            class="progress-circle"/>
                </svg>
                <div class="absolute inset-0 flex items-center justify-center">
                    <div class="text-center">
                        <div class="text-2xl font-bold">75%</div>
                        <div class="text-xs opacity-75">R$ 75k</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    
    <!-- Activity Chart -->
    <div class="activity-chart-card bg-white rounded-2xl p-6 shadow-lg">
        <h3 class="text-lg font-semibold text-gray-900 mb-4">Atividade Semanal</h3>
        <canvas id="activity-chart" width="300" height="150"></canvas>
    </div>
</div>

<script>
class Dashboard {
    constructor() {
        this.animateMetrics();
        this.createCharts();
        this.animateProgressRing();
    }
    
    animateMetrics() {
        document.querySelectorAll('.metric-value').forEach(element => {
            const target = parseInt(element.dataset.target);
            const duration = 2000;
            const increment = target / (duration / 16);
            let current = 0;
            
            const timer = setInterval(() => {
                current += increment;
                if (current >= target) {
                    current = target;
                    clearInterval(timer);
                }
                element.textContent = Math.floor(current).toLocaleString();
            }, 16);
        });
    }
    
    createCharts() {
        // Mini Chart
        const miniCharts = document.querySelectorAll('.mini-chart');
        miniCharts.forEach(canvas => {
            const ctx = canvas.getContext('2d');
            const data = [65, 72, 68, 75, 82, 78, 85, 88, 92, 89, 95, 98];
            
            this.drawMiniChart(ctx, data, canvas.width, canvas.height);
        });
        
        // Activity Chart
        const activityCanvas = document.getElementById('activity-chart');
        if (activityCanvas) {
            this.drawActivityChart(activityCanvas);
        }
    }
    
    drawMiniChart(ctx, data, width, height) {
        const padding = 10;
        const chartWidth = width - padding * 2;
        const chartHeight = height - padding * 2;
        
        const max = Math.max(...data);
        const min = Math.min(...data);
        const range = max - min;
        
        ctx.strokeStyle = '#3B82F6';
        ctx.lineWidth = 2;
        ctx.beginPath();
        
        data.forEach((value, index) => {
            const x = padding + (chartWidth / (data.length - 1)) * index;
            const y = padding + chartHeight - ((value - min) / range) * chartHeight;
            
            if (index === 0) {
                ctx.moveTo(x, y);
            } else {
                ctx.lineTo(x, y);
            }
        });
        
        ctx.stroke();
        
        // Add gradient fill
        ctx.globalAlpha = 0.2;
        ctx.fillStyle = '#3B82F6';
        ctx.lineTo(width - padding, height - padding);
        ctx.lineTo(padding, height - padding);
        ctx.closePath();
        ctx.fill();
    }
    
    drawActivityChart(canvas) {
        const ctx = canvas.getContext('2d');
        const data = [12, 19, 8, 15, 25, 18, 22];
        const labels = ['Dom', 'Seg', 'Ter', 'Qua', 'Qui', 'Sex', 'Sáb'];
        
        const barWidth = 30;
        const barSpacing = 10;
        const chartHeight = 100;
        const maxValue = Math.max(...data);
        
        data.forEach((value, index) => {
            const barHeight = (value / maxValue) * chartHeight;
            const x = index * (barWidth + barSpacing);
            const y = canvas.height - barHeight - 30;
            
            // Draw bar with gradient
            const gradient = ctx.createLinearGradient(0, y, 0, y + barHeight);
            gradient.addColorStop(0, '#8B5CF6');
            gradient.addColorStop(1, '#3B82F6');
            
            ctx.fillStyle = gradient;
            ctx.fillRect(x, y, barWidth, barHeight);
            
            // Draw label
            ctx.fillStyle = '#6B7280';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            ctx.fillText(labels[index], x + barWidth / 2, canvas.height - 10);
            
            // Draw value
            ctx.fillStyle = '#1F2937';
            ctx.font = 'bold 14px Arial';
            ctx.fillText(value, x + barWidth / 2, y - 5);
        });
    }
    
    animateProgressRing() {
        const circle = document.querySelector('.progress-circle');
        if (circle) {
            const circumference = 2 * Math.PI * 40; // radius = 40
            const progress = 75; // 75%
            const offset = circumference - (progress / 100) * circumference;
            
            // Animate the stroke-dashoffset
            let currentOffset = circumference;
            const animation = setInterval(() => {
                currentOffset -= 5;
                if (currentOffset <= offset) {
                    currentOffset = offset;
                    clearInterval(animation);
                }
                circle.style.strokeDashoffset = currentOffset;
            }, 20);
        }
    }
}

new Dashboard();
</script>
```

---

## 🚀 COMPONENTES DE PERFORMANCE

### ⚡ Lazy Loading Inteligente

```html
<div class="lazy-container">
    <div class="lazy-placeholder bg-gray-200 rounded-2xl animate-pulse" style="height: 300px;">
        <div class="flex items-center justify-center h-full">
            <div class="text-gray-400">Carregando...</div>
        </div>
    </div>
</div>

<script>
class IntelligentLazyLoading {
    constructor() {
        this.observer = null;
        this.imageCache = new Map();
        this.prefetchQueue = [];
        this.loadingPromises = new Map();
        
        this.init();
    }
    
    init() {
        this.createObserver();
        this.observeLazyElements();
        this.prefetchNearbyImages();
    }
    
    createObserver() {
        const options = {
            root: null,
            rootMargin: '50px 0px', // Start loading 50px before entering viewport
            threshold: 0.1
        };
        
        this.observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    this.loadElement(entry.target);
                    this.observer.unobserve(entry.target);
                }
            });
        }, options);
    }
    
    observeLazyElements() {
        document.querySelectorAll('[data-lazy]').forEach(element => {
            this.observer.observe(element);
        });
    }
    
    async loadElement(element) {
        const src = element.dataset.lazy;
        const type = element.dataset.lazyType || 'image';
        
        try {
            element.classList.add('lazy-loading');
            
            switch (type) {
                case 'image':
                    await this.loadImage(element, src);
                    break;
                case 'video':
                    await this.loadVideo(element, src);
                    break;
                case 'iframe':
                    await this.loadIframe(element, src);
                    break;
                default:
                    await this.loadGeneric(element, src);
            }
            
            element.classList.remove('lazy-loading');
            element.classList.add('lazy-loaded');
            
            // Trigger custom event
            element.dispatchEvent(new CustomEvent('lazyLoaded', {
                detail: { element, src, type }
            }));
            
        } catch (error) {
            console.error('Failed to load lazy element:', error);
            element.classList.add('lazy-error');
        }
    }
    
    loadImage(element, src) {
        return new Promise((resolve, reject) => {
            // Check cache first
            if (this.imageCache.has(src)) {
                element.src = src;
                resolve();
                return;
            }
            
            // Load with progress tracking
            const img = new Image();
            
            img.onload = () => {
                this.imageCache.set(src, img);
                element.src = src;
                
                // Fade in animation
                gsap.fromTo(element, 
                    { opacity: 0, scale: 1.1 },
                    { opacity: 1, scale: 1, duration: 0.6, ease: 'power2.out' }
                );
                
                resolve();
            };
            
            img.onerror = reject;
            img.src = src;
        });
    }
    
    loadVideo(element, src) {
        return new Promise((resolve, reject) => {
            element.src = src;
            element.load();
            
            element.addEventListener('canplaythrough', resolve, { once: true });
            element.addEventListener('error', reject, { once: true });
        });
    }
    
    loadIframe(element, src) {
        return new Promise((resolve) => {
            element.src = src;
            element.addEventListener('load', resolve, { once: true });
        });
    }
    
    loadGeneric(element, src) {
        return fetch(src)
            .then(response => response.text())
            .then(content => {
                element.innerHTML = content;
            });
    }
    
    prefetchNearbyImages() {
        // Prefetch images that are likely to be needed soon
        const nearbyImages = document.querySelectorAll('[data-lazy-prefetch]');
        
        nearbyImages.forEach(element => {
            const src = element.dataset.lazyPrefetch;
            if (!this.imageCache.has(src)) {
                this.prefetchQueue.push(src);
            }
        });
        
        // Process prefetch queue gradually
        this.processPrefetchQueue();
    }
    
    processPrefetchQueue() {
        if (this.prefetchQueue.length === 0) return;
        
        const src = this.prefetchQueue.shift();
        const img = new Image();
        
        img.onload = () => {
            this.imageCache.set(src, img);
            // Process next item after a small delay to avoid blocking
            setTimeout(() => this.processPrefetchQueue(), 100);
        };
        
        img.onerror = () => {
            // Still process next item even on error
            setTimeout(() => this.processPrefetchQueue(), 100);
        };
        
        img.src = src;
    }
    
    // Public method to manually trigger loading
    loadNow(element) {
        if (element.hasAttribute('data-lazy')) {
            this.loadElement(element);
            this.observer.unobserve(element);
        }
    }
    
    // Preload critical images
    preloadCritical(urls) {
        urls.forEach(url => {
            const link = document.createElement('link');
            link.rel = 'preload';
            link.as = 'image';
            link.href = url;
            document.head.appendChild(link);
        });
    }
}

// Initialize
const lazyLoader = new IntelligentLazyLoading();

// Usage examples:
// <img data-lazy="/path/to/image.jpg" data-lazy-type="image" alt="Description">
// <video data-lazy="/path/to/video.mp4" data-lazy-type="video" controls></video>
// <iframe data-lazy="/path/to/content.html" data-lazy-type="iframe"></iframe>
</script>
```

### 🎯 Progressive Enhancement

```javascript
class ProgressiveEnhancement {
    constructor() {
        this.features = {
            css: this.detectCSSFeatures(),
            js: this.detectJSFeatures(),
            device: this.detectDevice(),
            performance: this.detectPerformance()
        };
        
        this.applyEnhancements();
    }
    
    detectCSSFeatures() {
        const testElement = document.createElement('div');
        return {
            grid: CSS.supports('display', 'grid'),
            flexbox: CSS.supports('display', 'flex'),
            customProperties: CSS.supports('--test', '0'),
            backdrop: CSS.supports('backdrop-filter', 'blur(1px)'),
            clipPath: CSS.supports('clip-path', 'circle(50%)'),
            transforms3d: this.test3DTransforms()
        };
    }
    
    detectJSFeatures() {
        return {
            intersectionObserver: 'IntersectionObserver' in window,
            webGL: this.testWebGL(),
            serviceWorker: 'serviceWorker' in navigator,
            webAssembly: 'WebAssembly' in window,
            modules: 'noModule' in document.createElement('script')
        };
    }
    
    detectDevice() {
        return {
            mobile: window.innerWidth < 768,
            tablet: window.innerWidth >= 768 && window.innerWidth < 1024,
            desktop: window.innerWidth >= 1024,
            touchDevice: 'ontouchstart' in window,
            highDPI: window.devicePixelRatio > 1,
            reducedMotion: window.matchMedia('(prefers-reduced-motion: reduce)')?.matches
        };
    }
    
    detectPerformance() {
        const connection = navigator.connection || navigator.mozConnection || navigator.webkitConnection;
        const memory = navigator.deviceMemory || 4; // Default to 4GB if not available
        
        return {
            slowConnection: connection ? connection.effectiveType === 'slow-2g' || connection.effectiveType === '2g' : false,
            saveData: connection ? connection.saveData : false,
            lowMemory: memory < 4,
            cores: navigator.hardwareConcurrency || 4
        };
    }
    
    test3DTransforms() {
        const testElement = document.createElement('div');
        testElement.style.transform = 'translateZ(0)';
        return testElement.style.transform !== '';
    }
    
    testWebGL() {
        try {
            const canvas = document.createElement('canvas');
            return !!(canvas.getContext('webgl') || canvas.getContext('experimental-webgl'));
        } catch (e) {
            return false;
        }
    }
    
    applyEnhancements() {
        // Add feature classes to body
        const featureClasses = [];
        
        Object.entries(this.features).forEach(([category, features]) => {
            Object.entries(features).forEach(([feature, supported]) => {
                featureClasses.push(supported ? `has-${feature}` : `no-${feature}`);
            });
        });
        
        document.body.classList.add(...featureClasses);
        
        // Apply specific enhancements
        this.enhanceAnimations();
        this.enhanceImages();
        this.enhanceInteractions();
        this.enhancePerformance();
    }
    
    enhanceAnimations() {
        if (this.features.device.reducedMotion) {
            // Disable or reduce animations
            document.body.classList.add('reduced-motion');
            
            // Override GSAP defaults
            if (window.gsap) {
                gsap.defaults({ duration: 0.1 });
            }
        } else if (this.features.css.transforms3d) {
            // Enable 3D transforms
            document.body.classList.add('enhanced-animations');
        }
    }
    
    enhanceImages() {
        if (this.features.performance.saveData || this.features.performance.slowConnection) {
            // Use lower quality images
            document.querySelectorAll('img[data-src-hq]').forEach(img => {
                img.src = img.dataset.srcLq || img.dataset.src;
            });
        } else if (this.features.device.highDPI) {
            // Use high-DPI images
            document.querySelectorAll('img[data-src-2x]').forEach(img => {
                img.src = img.dataset.src2x;
            });
        }
    }
    
    enhanceInteractions() {
        if (!this.features.device.touchDevice) {
            // Add hover effects for non-touch devices
            document.body.classList.add('has-hover');
        }
        
        if (this.features.js.intersectionObserver) {
            // Use Intersection Observer for scroll animations
            this.enableScrollAnimations();
        } else {
            // Fallback to scroll events
            this.fallbackScrollAnimations();
        }
    }
    
    enhancePerformance() {
        if (this.features.performance.lowMemory || this.features.performance.slowConnection) {
            // Reduce memory usage
            this.optimizeForLowEnd();
        }
        
        if (this.features.js.serviceWorker) {
            // Register service worker
            this.registerServiceWorker();
        }
    }
    
    enableScrollAnimations() {
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('in-view');
                }
            });
        });
        
        document.querySelectorAll('.animate-on-scroll').forEach(el => {
            observer.observe(el);
        });
    }
    
    fallbackScrollAnimations() {
        let throttleTimer = null;
        
        const checkVisibility = () => {
            document.querySelectorAll('.animate-on-scroll:not(.in-view)').forEach(el => {
                const rect = el.getBoundingClientRect();
                if (rect.top < window.innerHeight && rect.bottom > 0) {
                    el.classList.add('in-view');
                }
            });
        };
        
        window.addEventListener('scroll', () => {
            if (throttleTimer) return;
            throttleTimer = setTimeout(() => {
                checkVisibility();
                throttleTimer = null;
            }, 100);
        });
        
        checkVisibility(); // Initial check
    }
    
    optimizeForLowEnd() {
        // Disable expensive animations
        document.body.classList.add('low-performance');
        
        // Reduce particle counts
        if (window.particleSystem) {
            window.particleSystem.setParticleCount(50); // Reduce from default
        }
        
        // Disable WebGL effects
        document.querySelectorAll('.webgl-effect').forEach(el => {
            el.style.display = 'none';
        });
    }
    
    registerServiceWorker() {
        if ('serviceWorker' in navigator) {
            navigator.serviceWorker.register('/sw.js')
                .then(registration => {
                    console.log('Service Worker registered');
                })
                .catch(error => {
                    console.log('Service Worker registration failed');
                });
        }
    }
    
    // Public API
    getFeatureSupport(feature) {
        const [category, featureName] = feature.split('.');
        return this.features[category]?.[featureName] || false;
    }
    
    isLowEnd() {
        return this.features.performance.lowMemory || 
               this.features.performance.slowConnection ||
               this.features.performance.cores < 4;
    }
}

// Initialize
const enhancement = new ProgressiveEnhancement();
</script>
```
```