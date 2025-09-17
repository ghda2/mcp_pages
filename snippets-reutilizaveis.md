# 🧰 BIBLIOTECA DE SNIPPETS REUTILIZÁVEIS

## 🚀 COMPONENTES PRONTOS PARA USO

### 🎨 Buttons Collection

```html
<!-- Primary Button -->
<button class="btn btn-primary">
    <span class="btn-text">Começar Agora</span>
    <svg class="btn-icon" width="16" height="16" fill="currentColor">
        <path d="M8 0a.5.5 0 01.5.5v7H15a.5.5 0 010 1H8.5v7a.5.5 0 01-1 0V8.5H0a.5.5 0 010-1h7.5V.5A.5.5 0 018 0z"/>
    </svg>
</button>

<!-- Loading Button -->
<button class="btn btn-primary" disabled>
    <svg class="btn-spinner" width="16" height="16" fill="currentColor">
        <circle cx="8" cy="8" r="6" stroke="currentColor" stroke-width="2" fill="none"/>
    </svg>
    <span class="btn-text">Processando...</span>
</button>
```

### 📝 Quick Form Components

```html
<!-- Input Field with Label -->
<div class="form-field">
    <label for="email" class="form-label">
        Email Address <span class="required">*</span>
    </label>
    <input type="email" id="email" name="email" class="form-input" required>
    <div class="form-error" id="email-error"></div>
</div>
```

---

## 🎯 JAVASCRIPT UTILITIES ESSENCIAIS

### 🔧 DOM Helpers Rápidos

```javascript
// Quick DOM utilities
const $ = {
    qs: (s, p = document) => p.querySelector(s),
    qsa: (s, p = document) => [...p.querySelectorAll(s)],
    on: (el, ev, fn) => el.addEventListener(ev, fn),
    ready: (fn) => document.readyState === 'loading' ? 
        document.addEventListener('DOMContentLoaded', fn) : fn()
};
```

### ⚡ Performance Helpers

```javascript
// Debounce function
const debounce = (func, delay = 250) => {
    let timeoutId;
    return (...args) => {
        clearTimeout(timeoutId);
        timeoutId = setTimeout(() => func.apply(null, args), delay);
    };
};

// Lazy loading images
const lazyLoadImages = () => {
    const images = document.querySelectorAll('img[data-src]');
    const imageObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const img = entry.target;
                img.src = img.dataset.src;
                img.classList.add('loaded');
                imageObserver.unobserve(img);
            }
        });
    });
    images.forEach(img => imageObserver.observe(img));
};
```

---

## 🎨 CSS SNIPPETS RÁPIDOS

### 🌈 Utility Classes Essenciais

```css
/* Flexbox helpers */
.flex { display: flex; }
.flex-col { flex-direction: column; }
.items-center { align-items: center; }
.justify-center { justify-content: center; }
.justify-between { justify-content: space-between; }

/* Spacing */
.p-4 { padding: 1rem; }
.p-8 { padding: 2rem; }
.m-4 { margin: 1rem; }
.mx-auto { margin: 0 auto; }

/* Text */
.text-center { text-align: center; }
.font-bold { font-weight: 700; }
.text-lg { font-size: 1.125rem; }
.text-xl { font-size: 1.25rem; }

/* Animations */
.fade-in { animation: fadeIn 0.5s ease-in; }
.slide-up { animation: slideUp 0.5s ease-out; }

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

@keyframes slideUp {
    from { transform: translateY(20px); opacity: 0; }
    to { transform: translateY(0); opacity: 1; }
}
```

---

## 🎨 QUICK COPY TEMPLATES

### 📝 Headlines Impactantes

```html
<!-- Urgência -->
<h1>ÚLTIMAS 24 HORAS: Descubra o Segredo que 97% dos Empresários Desconhecem</h1>

<!-- Benefício específico -->
<h1>Como Gerar R$ 50.000 em 30 Dias Trabalhando Apenas 2 Horas por Dia</h1>

<!-- Problema + Solução -->
<h1>Pare de Perder Clientes para a Concorrência - Sistema Aprovado por 5.000+ Empresas</h1>
```

### 🎯 CTAs Persuasivos

```html
<!-- Benefício claro -->
<button>Quero Economizar R$ 5.000 Agora</button>

<!-- Remove risco -->
<button>Começar Teste Gratuito de 30 Dias</button>

<!-- Urgência -->
<button>Garantir Minha Vaga (Só 10 Restam)</button>

<!-- Transformação -->
<button>Transformar Meu Negócio Hoje</button>
```
