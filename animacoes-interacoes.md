# 🎭 ANIMAÇÕES E INTERAÇÕES AVANÇADAS

## 🎨 CSS CUSTOMIZADO E ANIMAÇÕES
```css
<style>
    /* Animações Customizadas */
    @keyframes gradient-x {
        0%, 100% { background-position: 0% 50%; }
        50% { background-position: 100% 50%; }
    }
    
    @keyframes draw {
        to { stroke-dashoffset: 0; }
    }
    
    @keyframes float-up {
        0% { transform: translateY(100px); opacity: 0; }
        100% { transform: translateY(0); opacity: 1; }
    }
    
    @keyframes morphing {
        0%, 100% { border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%; }
        50% { border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%; }
    }
    
    /* Efeitos de Hover Avançados */
    .magnetic-btn {
        position: relative;
        transition: transform 0.3s;
    }
    
    .flip-card {
        perspective: 1000px;
    }
    
    .flip-card-inner {
        transform-style: preserve-3d;
    }
    
    .backface-hidden {
        backface-visibility: hidden;
    }
    
    .rotate-y-180 {
        transform: rotateY(180deg);
    }
    
    .hover\:rotate-y-180:hover {
        transform: rotateY(180deg);
    }
    
    /* Gradientes Animados */
    .animate-gradient-x {
        background-size: 200% 200%;
        animation: gradient-x 3s ease infinite;
    }
    
    /* Blob Animation */
    .animate-blob {
        animation: morphing 8s ease-in-out infinite;
    }
    
    /* Scroll Animations */
    .timeline-item {
        transform: translateY(50px);
        transition: all 0.8s ease;
    }
    
    .timeline-item.visible {
        opacity: 1;
        transform: translateY(0);
    }
    
    /* Parallax Effect */
    [data-parallax] {
        transition: transform 0.5s;
    }
    
    /* Custom Scrollbar */
    .scrollbar-hide::-webkit-scrollbar {
        display: none;
    }
    
    .scrollbar-hide {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
    
    /* Glow Effects */
    .glow {
        box-shadow: 
            0 0 20px rgba(99, 102, 241, 0.3),
            0 0 40px rgba(99, 102, 241, 0.2),
            0 0 60px rgba(99, 102, 241, 0.1);
    }
    
    /* Typewriter Effect */
    .typewriter::after {
        content: '|';
        animation: blink 1s infinite;
    }
    
    @keyframes blink {
        0%, 50% { opacity: 1; }
        51%, 100% { opacity: 0; }
    }
</style>
```

## 🎯 JAVASCRIPT PARA INTERAÇÕES
```javascript
<script>
    // GSAP Scroll Animations
    gsap.registerPlugin(ScrollTrigger);
    
    // Animação de entrada para elementos
    gsap.utils.toArray('.fade-up').forEach(element => {
        gsap.fromTo(element, 
            { y: 100, opacity: 0 },
            {
                y: 0,
                opacity: 1,
                duration: 1,
                scrollTrigger: {
                    trigger: element,
                    start: 'top 80%',
                    end: 'bottom 20%',
                    toggleActions: 'play none none reverse'
                }
            }
        );
    });
    
    // Timeline Progress Animation
    gsap.to('.timeline-progress', {
        height: '100%',
        scrollTrigger: {
            trigger: '.timeline-container',
            start: 'top center',
            end: 'bottom center',
            scrub: 1
        }
    });
    
    // Parallax Effect
    document.addEventListener('scroll', () => {
        const scrolled = window.pageYOffset;
        const parallaxElements = document.querySelectorAll('[data-parallax]');
        
        parallaxElements.forEach(element => {
            const speed = element.dataset.parallax;
            element.style.transform = `translateY(${scrolled * speed}px)`;
        });
    });
    
    // Typewriter Effect
    const typewriterTexts = [
        'Inovação Digital',
        'Transformação Completa',
        'Resultados Extraordinários'
    ];
    
    let textIndex = 0;
    let charIndex = 0;
    let currentText = '';
    let isDeleting = false;
    
    function typeWriter() {
        const element = document.querySelector('.typewriter');
        if (!element) return;
        
        if (isDeleting) {
            currentText = typewriterTexts[textIndex].substring(0, charIndex - 1);
            charIndex--;
        } else {
            currentText = typewriterTexts[textIndex].substring(0, charIndex + 1);
            charIndex++;
        }
        
        element.textContent = currentText;
        
        let typeSpeed = isDeleting ? 50 : 150;
        
        if (!isDeleting && charIndex === typewriterTexts[textIndex].length) {
            typeSpeed = 2000;
            isDeleting = true;
        } else if (isDeleting && charIndex === 0) {
            isDeleting = false;
            textIndex = (textIndex + 1) % typewriterTexts.length;
            typeSpeed = 500;
        }
        
        setTimeout(typeWriter, typeSpeed);
    }
    
    // Iniciar typewriter
    typeWriter();
    
    // Magnetic Button Effect
    document.querySelectorAll('.magnetic-btn').forEach(btn => {
        btn.addEventListener('mousemove', (e) => {
            const rect = btn.getBoundingClientRect();
            const x = e.clientX - rect.left - rect.width / 2;
            const y = e.clientY - rect.top - rect.height / 2;
            
            btn.style.transform = `translate(${x * 0.3}px, ${y * 0.3}px)`;
        });
        
        btn.addEventListener('mouseleave', () => {
            btn.style.transform = 'translate(0, 0)';
        });
    });
    
    // Tabs Interaction
    const tabItems = document.querySelectorAll('.tab-item');
    const tabContents = document.querySelectorAll('.tab-content');
    
    tabItems.forEach(tab => {
        tab.addEventListener('click', () => {
            const tabId = tab.dataset.tab;
            
            // Remove active classes
            tabItems.forEach(t => t.classList.remove('border-primary-600'));
            tabContents.forEach(c => c.classList.add('hidden'));
            
            // Add active classes
            tab.classList.add('border-primary-600');
            document.querySelector(`[data-content="${tabId}"]`)?.classList.remove('hidden');
        });
    });
    
    // Particle Background
    function createParticles() {
        const canvas = document.getElementById('particles-canvas');
        if (!canvas) return;
        
        const ctx = canvas.getContext('2d');
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
        
        const particles = [];
        const particleCount = 100;
        
        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.size = Math.random() * 3 + 1;
                this.speedX = Math.random() * 3 - 1.5;
                this.speedY = Math.random() * 3 - 1.5;
                this.opacity = Math.random() * 0.5 + 0.5;
            }
            
            update() {
                this.x += this.speedX;
                this.y += this.speedY;
                
                if (this.x > canvas.width) this.x = 0;
                if (this.x < 0) this.x = canvas.width;
                if (this.y > canvas.height) this.y = 0;
                if (this.y < 0) this.y = canvas.height;
            }
            
            draw() {
                ctx.fillStyle = `rgba(255, 255, 255, ${this.opacity})`;
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
                ctx.fill();
            }
        }
        
        for (let i = 0; i < particleCount; i++) {
            particles.push(new Particle());
        }
        
        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            particles.forEach(particle => {
                particle.update();
                particle.draw();
            });
            
            requestAnimationFrame(animate);
        }
        
        animate();
    }
    
    // Inicializar partículas
    createParticles();
    
    // Smooth Scroll
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
```

---

## 🎆 MICRO-INTERAÇÕES AVANÇADAS

### 🎯 Botões com Feedback Tátil

```html
<!-- Botão com Ripple Effect -->
<button class="relative overflow-hidden px-8 py-4 bg-blue-600 text-white rounded-xl font-semibold transition-all duration-300 transform hover:scale-105 active:scale-95 ripple-btn">
    <span class="relative z-10">Clique Aqui</span>
</button>

<style>
.ripple-btn {
    position: relative;
    overflow: hidden;
}

.ripple-btn::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.5);
    transform: translate(-50%, -50%);
    transition: width 0.6s, height 0.6s;
}

.ripple-btn:active::before {
    width: 300px;
    height: 300px;
}
</style>
```

### 🌊 Hover Effects Magnéticos

```css
.magnetic-element {
    transition: transform 0.3s cubic-bezier(0.23, 1, 0.320, 1);
    cursor: pointer;
}

.magnetic-element:hover {
    transform: scale(1.05);
}

/* JavaScript para efeito magnético */
<script>
document.querySelectorAll('.magnetic-element').forEach(element => {
    element.addEventListener('mousemove', (e) => {
        const rect = element.getBoundingClientRect();
        const centerX = rect.left + rect.width / 2;
        const centerY = rect.top + rect.height / 2;
        
        const deltaX = (e.clientX - centerX) * 0.15;
        const deltaY = (e.clientY - centerY) * 0.15;
        
        element.style.transform = `translate(${deltaX}px, ${deltaY}px) scale(1.05)`;
    });
    
    element.addEventListener('mouseleave', () => {
        element.style.transform = 'translate(0px, 0px) scale(1)';
    });
});
</script>
```

### ⚡ Loading States Criativos

```html
<!-- Skeleton Loading -->
<div class="skeleton-container">
    <div class="skeleton-item">
        <div class="skeleton-avatar"></div>
        <div class="skeleton-text">
            <div class="skeleton-line skeleton-line-title"></div>
            <div class="skeleton-line skeleton-line-subtitle"></div>
        </div>
    </div>
</div>

<style>
.skeleton-item {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1rem;
}

.skeleton-avatar {
    width: 60px;
    height: 60px;
    border-radius: 50%;
    background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
    background-size: 200% 100%;
    animation: skeleton-loading 1.5s infinite;
}

.skeleton-line {
    height: 16px;
    border-radius: 8px;
    background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
    background-size: 200% 100%;
    animation: skeleton-loading 1.5s infinite;
    margin-bottom: 8px;
}

.skeleton-line-title {
    width: 80%;
    height: 20px;
}

.skeleton-line-subtitle {
    width: 60%;
}

@keyframes skeleton-loading {
    0% { background-position: 200% 0; }
    100% { background-position: -200% 0; }
}
</style>
```

### 🎪 Morphing Icons

```html
<!-- Hamburger to X Animation -->
<button class="hamburger-btn" onclick="toggleMenu()">
    <div class="hamburger-line line1"></div>
    <div class="hamburger-line line2"></div>
    <div class="hamburger-line line3"></div>
</button>

<style>
.hamburger-btn {
    width: 30px;
    height: 30px;
    position: relative;
    background: none;
    border: none;
    cursor: pointer;
}

.hamburger-line {
    width: 100%;
    height: 3px;
    background: #333;
    position: absolute;
    transition: all 0.3s ease;
}

.line1 { top: 6px; }
.line2 { top: 15px; }
.line3 { top: 24px; }

.hamburger-btn.active .line1 {
    transform: rotate(45deg);
    top: 15px;
}

.hamburger-btn.active .line2 {
    opacity: 0;
}

.hamburger-btn.active .line3 {
    transform: rotate(-45deg);
    top: 15px;
}
</style>

<script>
function toggleMenu() {
    const btn = document.querySelector('.hamburger-btn');
    btn.classList.toggle('active');
}
</script>
```

---

## 🎨 ANIMAÇÕES DE SCROLL AVANÇADAS

### 📊 Progress Indicators

```html
<!-- Reading Progress Bar -->
<div class="reading-progress">
    <div class="reading-progress-bar"></div>
</div>

<!-- Section Progress Dots -->
<div class="scroll-progress-dots">
    <div class="progress-dot active" data-section="hero"></div>
    <div class="progress-dot" data-section="features"></div>
    <div class="progress-dot" data-section="testimonials"></div>
    <div class="progress-dot" data-section="pricing"></div>
    <div class="progress-dot" data-section="contact"></div>
</div>

<style>
.reading-progress {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background: rgba(0, 0, 0, 0.1);
    z-index: 1000;
}

.reading-progress-bar {
    height: 100%;
    background: linear-gradient(90deg, #667eea, #764ba2);
    width: 0%;
    transition: width 0.1s ease;
}

.scroll-progress-dots {
    position: fixed;
    right: 2rem;
    top: 50%;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    gap: 1rem;
    z-index: 1000;
}

.progress-dot {
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background: rgba(0, 0, 0, 0.3);
    cursor: pointer;
    transition: all 0.3s ease;
    position: relative;
}

.progress-dot.active {
    background: #667eea;
    transform: scale(1.2);
}

.progress-dot::after {
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    border-radius: 50%;
    background: rgba(102, 126, 234, 0.3);
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: all 0.3s ease;
}

.progress-dot.active::after {
    width: 24px;
    height: 24px;
}
</style>

<script>
// Reading Progress
function updateReadingProgress() {
    const docHeight = document.documentElement.scrollHeight - window.innerHeight;
    const scrollTop = window.pageYOffset;
    const scrollPercent = (scrollTop / docHeight) * 100;
    
    document.querySelector('.reading-progress-bar').style.width = scrollPercent + '%';
}

// Section Progress
function updateSectionProgress() {
    const sections = document.querySelectorAll('section[id]');
    const dots = document.querySelectorAll('.progress-dot');
    
    sections.forEach((section, index) => {
        const rect = section.getBoundingClientRect();
        const isInView = rect.top <= window.innerHeight / 2 && rect.bottom >= window.innerHeight / 2;
        
        if (isInView) {
            dots.forEach(dot => dot.classList.remove('active'));
            if (dots[index]) dots[index].classList.add('active');
        }
    });
}

window.addEventListener('scroll', () => {
    updateReadingProgress();
    updateSectionProgress();
});
</script>
```

### 🌈 Parallax Avançado

```html
<!-- Multi-layer Parallax -->
<section class="parallax-container">
    <div class="parallax-layer" data-speed="0.2">
        <!-- Background mountains -->
        <img src="mountains-bg.jpg" alt="Background">
    </div>
    <div class="parallax-layer" data-speed="0.5">
        <!-- Mid-ground trees -->
        <img src="trees-mid.png" alt="Trees">
    </div>
    <div class="parallax-layer" data-speed="0.8">
        <!-- Foreground content -->
        <div class="content">
            <h2>Parallax Content</h2>
            <p>This moves at normal speed</p>
        </div>
    </div>
</section>

<style>
.parallax-container {
    position: relative;
    height: 100vh;
    overflow: hidden;
}

.parallax-layer {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 120%; /* Extra height for parallax effect */
}

.parallax-layer img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
</style>

<script>
function updateParallax() {
    const scrollY = window.pageYOffset;
    const parallaxLayers = document.querySelectorAll('.parallax-layer');
    
    parallaxLayers.forEach(layer => {
        const speed = layer.dataset.speed;
        const yPos = -(scrollY * speed);
        layer.style.transform = `translateY(${yPos}px)`;
    });
}

window.addEventListener('scroll', updateParallax);
</script>
```

---

## 🎭 ELEMENTOS INTERATIVOS ÚNICOS

### 🎯 Cursor Personalizado

```html
<div class="custom-cursor">
    <div class="cursor-dot"></div>
    <div class="cursor-outline"></div>
</div>

<style>
body {
    cursor: none;
}

.custom-cursor {
    position: fixed;
    top: 0;
    left: 0;
    pointer-events: none;
    z-index: 9999;
}

.cursor-dot {
    width: 8px;
    height: 8px;
    background: #667eea;
    border-radius: 50%;
    position: absolute;
    transform: translate(-50%, -50%);
    transition: all 0.1s ease;
}

.cursor-outline {
    width: 32px;
    height: 32px;
    border: 2px solid rgba(102, 126, 234, 0.5);
    border-radius: 50%;
    position: absolute;
    transform: translate(-50%, -50%);
    transition: all 0.3s ease;
}

.cursor-hover .cursor-outline {
    width: 48px;
    height: 48px;
    border-color: #667eea;
}

.cursor-click .cursor-dot {
    transform: translate(-50%, -50%) scale(1.5);
}
</style>

<script>
const cursor = document.querySelector('.custom-cursor');
const cursorDot = document.querySelector('.cursor-dot');
const cursorOutline = document.querySelector('.cursor-outline');

document.addEventListener('mousemove', (e) => {
    const x = e.clientX;
    const y = e.clientY;
    
    cursorDot.style.left = x + 'px';
    cursorDot.style.top = y + 'px';
    
    cursorOutline.style.left = x + 'px';
    cursorOutline.style.top = y + 'px';
});

// Hover effects
document.querySelectorAll('a, button, .clickable').forEach(element => {
    element.addEventListener('mouseenter', () => {
        cursor.classList.add('cursor-hover');
    });
    
    element.addEventListener('mouseleave', () => {
        cursor.classList.remove('cursor-hover');
    });
    
    element.addEventListener('mousedown', () => {
        cursor.classList.add('cursor-click');
    });
    
    element.addEventListener('mouseup', () => {
        cursor.classList.remove('cursor-click');
    });
});
</script>
```

### 🌟 Text Reveal Animations

```html
<!-- Split Text Animation -->
<h1 class="split-text" data-text="Texto Incrível">Texto Incrível</h1>

<style>
.split-text {
    overflow: hidden;
}

.split-text .char {
    display: inline-block;
    transform: translateY(100%);
    transition: transform 0.6s cubic-bezier(0.23, 1, 0.320, 1);
}

.split-text.animate .char {
    transform: translateY(0);
}

.split-text .char:nth-child(1) { transition-delay: 0.1s; }
.split-text .char:nth-child(2) { transition-delay: 0.2s; }
.split-text .char:nth-child(3) { transition-delay: 0.3s; }
/* ... continue for more characters */
</style>

<script>
function splitText() {
    const elements = document.querySelectorAll('.split-text');
    
    elements.forEach(element => {
        const text = element.textContent;
        element.innerHTML = '';
        
        [...text].forEach((char, index) => {
            const span = document.createElement('span');
            span.classList.add('char');
            span.textContent = char === ' ' ? '\u00A0' : char;
            span.style.transitionDelay = `${index * 0.1}s`;
            element.appendChild(span);
        });
    });
}

// Trigger animation on scroll
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('animate');
        }
    });
});

document.addEventListener('DOMContentLoaded', () => {
    splitText();
    document.querySelectorAll('.split-text').forEach(el => {
        observer.observe(el);
    });
});
</script>
```

### 🎨 Canvas Background Interativo

```html
<canvas id="interactive-canvas"></canvas>

<style>
#interactive-canvas {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: -1;
    pointer-events: none;
}
</style>

<script>
class InteractiveCanvas {
    constructor() {
        this.canvas = document.getElementById('interactive-canvas');
        this.ctx = this.canvas.getContext('2d');
        this.particles = [];
        this.mouse = { x: 0, y: 0 };
        this.colors = ['#667eea', '#764ba2', '#f093fb', '#f5576c'];
        
        this.init();
    }
    
    init() {
        this.resize();
        this.createParticles();
        this.bindEvents();
        this.animate();
    }
    
    resize() {
        this.canvas.width = window.innerWidth;
        this.canvas.height = window.innerHeight;
    }
    
    createParticles() {
        const particleCount = Math.floor((this.canvas.width * this.canvas.height) / 10000);
        
        for (let i = 0; i < particleCount; i++) {
            this.particles.push({
                x: Math.random() * this.canvas.width,
                y: Math.random() * this.canvas.height,
                vx: (Math.random() - 0.5) * 0.5,
                vy: (Math.random() - 0.5) * 0.5,
                size: Math.random() * 3 + 1,
                color: this.colors[Math.floor(Math.random() * this.colors.length)],
                alpha: Math.random() * 0.5 + 0.1
            });
        }
    }
    
    bindEvents() {
        window.addEventListener('resize', () => this.resize());
        
        document.addEventListener('mousemove', (e) => {
            this.mouse.x = e.clientX;
            this.mouse.y = e.clientY;
        });
    }
    
    animate() {
        this.ctx.clearRect(0, 0, this.canvas.width, this.canvas.height);
        
        this.particles.forEach(particle => {
            // Mouse interaction
            const dx = this.mouse.x - particle.x;
            const dy = this.mouse.y - particle.y;
            const distance = Math.sqrt(dx * dx + dy * dy);
            
            if (distance < 100) {
                particle.vx += dx * 0.00001;
                particle.vy += dy * 0.00001;
            }
            
            // Update position
            particle.x += particle.vx;
            particle.y += particle.vy;
            
            // Boundaries
            if (particle.x < 0 || particle.x > this.canvas.width) particle.vx *= -1;
            if (particle.y < 0 || particle.y > this.canvas.height) particle.vy *= -1;
            
            // Draw particle
            this.ctx.beginPath();
            this.ctx.arc(particle.x, particle.y, particle.size, 0, Math.PI * 2);
            this.ctx.fillStyle = particle.color;
            this.ctx.globalAlpha = particle.alpha;
            this.ctx.fill();
            
            // Draw connections
            this.particles.forEach(other => {
                const dist = Math.sqrt(
                    (particle.x - other.x) ** 2 + (particle.y - other.y) ** 2
                );
                
                if (dist < 80) {
                    this.ctx.beginPath();
                    this.ctx.moveTo(particle.x, particle.y);
                    this.ctx.lineTo(other.x, other.y);
                    this.ctx.strokeStyle = particle.color;
                    this.ctx.globalAlpha = (80 - dist) / 80 * 0.2;
                    this.ctx.stroke();
                }
            });
        });
        
        requestAnimationFrame(() => this.animate());
    }
}

// Initialize
new InteractiveCanvas();
</script>
```

---

## 🚀 GSAP ANIMATIONS PROFISSIONAIS

### 🎪 Timeline Complexa

```javascript
// Master Timeline
const masterTL = gsap.timeline();

// Hero Animation Sequence
const heroTL = gsap.timeline();
heroTL
    .from('.hero-badge', { y: -50, opacity: 0, duration: 0.8, ease: 'back.out(1.7)' })
    .from('.hero-title', { 
        y: 100, 
        opacity: 0, 
        duration: 1.2, 
        ease: 'power3.out',
        stagger: 0.1 
    }, '-=0.4')
    .from('.hero-subtitle', { 
        y: 50, 
        opacity: 0, 
        duration: 0.8, 
        ease: 'power2.out' 
    }, '-=0.6')
    .from('.hero-cta', { 
        scale: 0.8, 
        opacity: 0, 
        duration: 0.6, 
        ease: 'back.out(1.7)' 
    }, '-=0.3');

// Features Scroll Animation
gsap.utils.toArray('.feature-card').forEach((card, index) => {
    gsap.fromTo(card, 
        {
            y: 100,
            opacity: 0,
            rotationX: 45
        },
        {
            y: 0,
            opacity: 1,
            rotationX: 0,
            duration: 1,
            delay: index * 0.2,
            ease: 'power3.out',
            scrollTrigger: {
                trigger: card,
                start: 'top 80%',
                end: 'bottom 20%',
                toggleActions: 'play none none reverse',
                onEnter: () => {
                    gsap.to(card.querySelector('.feature-icon'), {
                        rotation: 360,
                        duration: 0.8,
                        ease: 'back.out(1.7)'
                    });
                }
            }
        }
    );
});

// Morphing Shape Animation
gsap.to('.morph-shape', {
    morphSVG: '#final-shape',
    duration: 2,
    ease: 'power2.inOut',
    repeat: -1,
    yoyo: true,
    scrollTrigger: {
        trigger: '.morph-container',
        start: 'top center',
        end: 'bottom center',
        scrub: 1
    }
});

// Text Scramble Effect
function scrambleText(element, newText) {
    const chars = '!<>-_\\/[]{}—=+*^?#________';
    let iteration = 0;
    
    const interval = setInterval(() => {
        element.textContent = newText
            .split('')
            .map((letter, index) => {
                if (index < iteration) {
                    return newText[index];
                }
                return chars[Math.floor(Math.random() * chars.length)];
            })
            .join('');
        
        if (iteration >= newText.length) clearInterval(interval);
        iteration += 1 / 3;
    }, 30);
}

// Reveal Text on Scroll
ScrollTrigger.create({
    trigger: '.scramble-text',
    start: 'top 80%',
    onEnter: () => {
        const element = document.querySelector('.scramble-text');
        scrambleText(element, element.dataset.text);
    }
});
```

### 🎨 Advanced Hover States

```javascript
// Magnetic Button Effect
gsap.utils.toArray('.magnetic-btn').forEach(btn => {
    btn.addEventListener('mouseenter', () => {
        gsap.to(btn, {
            scale: 1.1,
            duration: 0.3,
            ease: 'power2.out'
        });
    });
    
    btn.addEventListener('mouseleave', () => {
        gsap.to(btn, {
            scale: 1,
            x: 0,
            y: 0,
            duration: 0.5,
            ease: 'elastic.out(1, 0.3)'
        });
    });
    
    btn.addEventListener('mousemove', (e) => {
        const rect = btn.getBoundingClientRect();
        const x = e.clientX - rect.left - rect.width / 2;
        const y = e.clientY - rect.top - rect.height / 2;
        
        gsap.to(btn, {
            x: x * 0.3,
            y: y * 0.3,
            duration: 0.3,
            ease: 'power2.out'
        });
    });
});

// Card Tilt Effect
gsap.utils.toArray('.tilt-card').forEach(card => {
    card.addEventListener('mousemove', (e) => {
        const rect = card.getBoundingClientRect();
        const centerX = rect.left + rect.width / 2;
        const centerY = rect.top + rect.height / 2;
        
        const rotateX = (e.clientY - centerY) / 10;
        const rotateY = (centerX - e.clientX) / 10;
        
        gsap.to(card, {
            rotationX: rotateX,
            rotationY: rotateY,
            transformPerspective: 1000,
            transformOrigin: 'center',
            duration: 0.3,
            ease: 'power2.out'
        });
        
        // Inner elements parallax
        gsap.to(card.querySelector('.card-inner'), {
            x: (e.clientX - centerX) * 0.1,
            y: (e.clientY - centerY) * 0.1,
            duration: 0.3,
            ease: 'power2.out'
        });
    });
    
    card.addEventListener('mouseleave', () => {
        gsap.to(card, {
            rotationX: 0,
            rotationY: 0,
            duration: 0.5,
            ease: 'elastic.out(1, 0.3)'
        });
        
        gsap.to(card.querySelector('.card-inner'), {
            x: 0,
            y: 0,
            duration: 0.5,
            ease: 'elastic.out(1, 0.3)'
        });
    });
});
```

---

## 🎵 SOUND DESIGN PARA WEB

### 🔊 Audio Feedback Sutil

```javascript
class SoundDesign {
    constructor() {
        this.sounds = {
            hover: new Audio('/sounds/hover.mp3'),
            click: new Audio('/sounds/click.mp3'),
            success: new Audio('/sounds/success.mp3'),
            error: new Audio('/sounds/error.mp3'),
            notification: new Audio('/sounds/notification.mp3')
        };
        
        // Configure volumes
        Object.values(this.sounds).forEach(sound => {
            sound.volume = 0.1; // Very subtle
        });
        
        this.init();
    }
    
    init() {
        // Button hover sounds
        document.querySelectorAll('button, .btn').forEach(btn => {
            btn.addEventListener('mouseenter', () => {
                this.play('hover');
            });
            
            btn.addEventListener('click', () => {
                this.play('click');
            });
        });
        
        // Form submission sounds
        document.querySelectorAll('form').forEach(form => {
            form.addEventListener('submit', (e) => {
                e.preventDefault();
                this.play('success');
                // Handle form submission
            });
        });
        
        // Notification sounds
        this.observeNotifications();
    }
    
    play(soundName) {
        if (this.sounds[soundName]) {
            this.sounds[soundName].currentTime = 0;
            this.sounds[soundName].play().catch(() => {
                // Ignore autoplay restrictions
            });
        }
    }
    
    observeNotifications() {
        const observer = new MutationObserver((mutations) => {
            mutations.forEach((mutation) => {
                mutation.addedNodes.forEach((node) => {
                    if (node.classList && node.classList.contains('notification')) {
                        this.play('notification');
                    }
                });
            });
        });
        
        observer.observe(document.body, {
            childList: true,
            subtree: true
        });
    }
}

// Initialize (only if user has interacted with page)
document.addEventListener('click', () => {
    if (!window.soundDesignInitialized) {
        new SoundDesign();
        window.soundDesignInitialized = true;
    }
}, { once: true });
```