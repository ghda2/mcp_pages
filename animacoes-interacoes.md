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