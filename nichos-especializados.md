# 🎯 NICHOS ESPECIALIZADOS - Templates por Segmento

## 🏢 FILOSOFIA DA ESPECIALIZAÇÃO

### 💡 Por que Especializar por Nicho?
1. **Linguagem Específica**: Cada setor tem seu vocabulário e necessidades únicas
2. **Psicologia do Público**: Comportamentos e motivações diferentes por indústria
3. **Regulamentações**: Compliance e normas específicas por área
4. **Jornada do Cliente**: Processos de decisão únicos para cada mercado
5. **Concorrência**: Diferenciação através da especialização

---

## 💊 NICHO: SAÚDE E BEM-ESTAR

### 🎨 Características do Público
- **Idade**: 30-65 anos, majoritariamente feminino
- **Motivação**: Dor/problema > Prevenção > Estética
- **Decisão**: Emocional com validação racional
- **Confiança**: Credenciais e depoimentos são cruciais
- **Urgência**: Variável conforme gravidade do problema

### 📋 Template: Clínica Médica

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dr. Silva - Cardiologista | Consulta em 24h | Convênios Aceitos</title>
    <meta name="description" content="Cardiologista especialista com 15 anos de experiência. Atendimento humanizado, tecnologia avançada. Agende sua consulta. Convênios aceitos.">
    
    <script src="https://cdn.twind.style" crossorigin></script>
    <script>
        twind.install({
            theme: {
                extend: {
                    colors: {
                        medical: {
                            50: '#f0f9ff',
                            500: '#0ea5e9',
                            600: '#0284c7',
                            700: '#0369a1',
                            900: '#0c4a6e'
                        },
                        trust: {
                            50: '#f0fdf4',
                            500: '#22c55e',
                            600: '#16a34a'
                        }
                    }
                }
            }
        });
    </script>
</head>
<body class="font-sans antialiased">
    <!-- Trust Bar -->
    <div class="bg-trust-50 border-b border-trust-200 py-2">
        <div class="max-w-6xl mx-auto px-4 flex flex-wrap justify-center items-center gap-6 text-sm text-trust-700">
            <div class="flex items-center gap-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M6.267 3.455a3.066 3.066 0 001.745-.723 3.066 3.066 0 013.976 0 3.066 3.066 0 001.745.723 3.066 3.066 0 012.812 2.812c.051.643.304 1.254.723 1.745a3.066 3.066 0 010 3.976 3.066 3.066 0 00-.723 1.745 3.066 3.066 0 01-2.812 2.812 3.066 3.066 0 00-1.745.723 3.066 3.066 0 01-3.976 0 3.066 3.066 0 00-1.745-.723 3.066 3.066 0 01-2.812-2.812 3.066 3.066 0 00-.723-1.745 3.066 3.066 0 010-3.976 3.066 3.066 0 00.723-1.745 3.066 3.066 0 012.812-2.812zm7.44 5.252a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                </svg>
                <span>CRM: 12345</span>
            </div>
            <div class="flex items-center gap-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                    <path fill-rule="evenodd" d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z" clip-rule="evenodd"/>
                </svg>
                <span>Dados 100% seguros</span>
            </div>
            <div class="flex items-center gap-2">
                <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                    <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z"/>
                </svg>
                <span>Consulta em 24h</span>
            </div>
        </div>
    </div>

    <!-- HERO SECTION -->
    <section class="bg-gradient-to-br from-medical-50 to-blue-50 py-16">
        <div class="max-w-6xl mx-auto px-4">
            <div class="grid lg:grid-cols-2 gap-12 items-center">
                <!-- Conteúdo -->
                <div>
                    <!-- Credenciais -->
                    <div class="flex items-center gap-4 mb-6">
                        <img class="w-20 h-20 rounded-2xl object-cover shadow-lg" 
                             src="https://images.unsplash.com/photo-1612349317150-e413f6a5b16d?w=80&h=80&fit=crop&crop=face" 
                             alt="Dr. Silva">
                        <div>
                            <h2 class="text-2xl font-bold text-gray-900">Dr. João Silva</h2>
                            <p class="text-medical-600 font-semibold">Cardiologista CRM 12345</p>
                            <div class="flex text-yellow-400 text-sm">★★★★★</div>
                        </div>
                    </div>
                    
                    <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-6 leading-tight">
                        Cuide do seu 
                        <span class="text-medical-600 relative">
                            Coração
                            <svg class="absolute -bottom-2 left-0 w-full" height="8" viewBox="0 0 200 8">
                                <path d="M0 4 Q50 0 100 4 T200 4" stroke="#0284c7" stroke-width="3" fill="none"/>
                            </svg>
                        </span>
                        com quem entende
                    </h1>
                    
                    <p class="text-xl text-gray-600 mb-8 leading-relaxed">
                        <strong>15 anos de experiência</strong> tratando mais de 3.000 pacientes. 
                        Atendimento humanizado com tecnologia de ponta para cuidar da sua saúde cardíaca.
                    </p>
                    
                    <!-- Benefícios Médicos -->
                    <div class="grid grid-cols-2 gap-4 mb-8">
                        <div class="flex items-center gap-3">
                            <div class="w-8 h-8 bg-trust-100 rounded-full flex items-center justify-center">
                                <svg class="w-5 h-5 text-trust-600" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </div>
                            <span class="font-medium text-gray-700">Consulta em 24h</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-8 h-8 bg-trust-100 rounded-full flex items-center justify-center">
                                <svg class="w-5 h-5 text-trust-600" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </div>
                            <span class="font-medium text-gray-700">Convênios aceitos</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-8 h-8 bg-trust-100 rounded-full flex items-center justify-center">
                                <svg class="w-5 h-5 text-trust-600" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </div>
                            <span class="font-medium text-gray-700">Exames no local</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-8 h-8 bg-trust-100 rounded-full flex items-center justify-center">
                                <svg class="w-5 h-5 text-trust-600" fill="currentColor" viewBox="0 0 20 20">
                                    <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                                </svg>
                            </div>
                            <span class="font-medium text-gray-700">15 anos experiência</span>
                        </div>
                    </div>
                    
                    <!-- CTA Médico -->
                    <div class="flex flex-col sm:flex-row gap-4">
                        <button class="px-8 py-4 bg-medical-600 text-white rounded-xl font-semibold text-lg hover:bg-medical-700 transition-colors shadow-lg">
                            Agendar Consulta
                        </button>
                        <button class="px-8 py-4 border-2 border-medical-600 text-medical-600 rounded-xl font-semibold text-lg hover:bg-medical-50 transition-colors">
                            Tire suas Dúvidas
                        </button>
                    </div>
                    
                    <!-- Informações Importantes -->
                    <div class="flex items-center gap-6 mt-6 text-sm text-gray-500">
                        <div class="flex items-center gap-2">
                            <svg class="w-5 h-5 text-trust-500" fill="currentColor" viewBox="0 0 20 20">
                                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
                            </svg>
                            <span>Primeira consulta sem taxa de agendamento</span>
                        </div>
                    </div>
                </div>
                
                <!-- Agendamento Rápido -->
                <div class="bg-white rounded-3xl shadow-2xl p-8">
                    <h3 class="text-2xl font-bold text-gray-900 mb-6 text-center">Agende sua Consulta</h3>
                    
                    <form class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Nome Completo</label>
                            <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent" placeholder="Seu nome completo">
                        </div>
                        
                        <div class="grid grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Telefone</label>
                                <input type="tel" class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent" placeholder="(11) 99999-9999">
                            </div>
                            <div>
                                <label class="block text-sm font-medium text-gray-700 mb-2">Idade</label>
                                <input type="number" class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent" placeholder="35">
                            </div>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Convênio</label>
                            <select class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent">
                                <option>Selecione seu convênio</option>
                                <option>Unimed</option>
                                <option>Bradesco Saúde</option>
                                <option>Amil</option>
                                <option>SulAmérica</option>
                                <option>Particular</option>
                            </select>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Preferência de Horário</label>
                            <select class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent">
                                <option>Manhã (8h às 12h)</option>
                                <option>Tarde (13h às 17h)</option>
                                <option>Qualquer horário</option>
                            </select>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Observações (opcional)</label>
                            <textarea class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-medical-500 focus:border-transparent" rows="3" placeholder="Descreva brevemente seu sintoma ou dúvida"></textarea>
                        </div>
                        
                        <button type="submit" class="w-full bg-trust-500 text-white font-bold py-4 rounded-xl hover:bg-trust-600 transition-colors">
                            Confirmar Agendamento
                        </button>
                    </form>
                    
                    <div class="mt-6 text-center">
                        <div class="flex items-center justify-center gap-2 text-sm text-gray-500">
                            <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                                <path fill-rule="evenodd" d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z" clip-rule="evenodd"/>
                            </svg>
                            <span>Seus dados estão seguros conosco</span>
                        </div>
                        <p class="text-xs text-gray-400 mt-2">Retornaremos em até 2 horas para confirmar sua consulta</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</body>
</html>
```

---

## 💰 NICHO: SERVIÇOS FINANCEIROS

### 🎨 Características do Público
- **Idade**: 25-55 anos, variado por produto
- **Motivação**: Segurança > Rentabilidade > Facilidade
- **Decisão**: Racional com validação social
- **Confiança**: Regulamentações e credenciais essenciais
- **Urgência**: Moderada, relacionada a oportunidades

### 📋 Template: Consultoria Financeira

```html
<!-- Header com certificações -->
<header class="bg-slate-900 text-white py-4">
    <div class="max-w-6xl mx-auto px-4 flex justify-between items-center">
        <div class="flex items-center gap-4">
            <div class="font-bold text-xl">FinancesPro</div>
            <div class="text-sm bg-green-600 px-3 py-1 rounded-full">CNPI • CPA-20 • CFP</div>
        </div>
        <div class="text-sm">
            <span class="text-green-400">95%</span> dos clientes aumentaram patrimônio
        </div>
    </div>
</header>

<!-- Hero Section -->
<section class="bg-gradient-to-br from-slate-50 to-blue-50 py-20">
    <div class="max-w-4xl mx-auto px-4 text-center">
        <div class="inline-flex items-center gap-2 px-4 py-2 bg-green-100 rounded-full mb-6">
            <svg class="w-5 h-5 text-green-600" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M2.166 4.999A11.954 11.954 0 0010 1.944 11.954 11.954 0 0017.834 5c.11.65.166 1.32.166 2.001 0 5.225-3.34 9.67-8 11.317C5.34 16.67 2 12.225 2 7c0-.682.057-1.35.166-2.001zm11.541 3.708a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"/>
            </svg>
            <span class="text-green-800 font-medium">Regulamentado CVM • Bacen • Susep</span>
        </div>
        
        <h1 class="text-5xl font-bold text-gray-900 mb-6">
            Transforme <span class="text-blue-600">R$ 1.000</span> em 
            <span class="text-green-600">R$ 100.000</span> em 10 Anos
        </h1>
        
        <p class="text-xl text-gray-600 mb-8 max-w-3xl mx-auto">
            Planejamento financeiro estratégico que já ajudou <strong>2.847 famílias</strong> 
            a conquistar independência financeira de forma segura e consistente.
        </p>
        
        <!-- Calculadora Simples -->
        <div class="bg-white rounded-3xl shadow-2xl p-8 max-w-md mx-auto mb-8">
            <h3 class="text-xl font-bold mb-4">Calcule seu Potencial de Crescimento</h3>
            <div class="space-y-4">
                <div>
                    <label class="block text-sm font-medium mb-2">Quanto você pode investir mensalmente?</label>
                    <input type="range" min="100" max="10000" value="1000" class="w-full" id="monthlyInput">
                    <div class="text-center text-2xl font-bold text-blue-600">R$ <span id="monthlyValue">1.000</span></div>
                </div>
                <div class="bg-gray-50 rounded-xl p-4">
                    <div class="text-sm text-gray-600">Em 10 anos você terá:</div>
                    <div class="text-3xl font-bold text-green-600">R$ <span id="futureValue">185.000</span></div>
                </div>
            </div>
            <button class="w-full bg-blue-600 text-white font-bold py-3 rounded-xl mt-4 hover:bg-blue-700 transition-colors">
                Quero Meu Plano Personalizado
            </button>
        </div>
    </div>
</section>
```

---

## 🎓 NICHO: EDUCAÇÃO ONLINE

### 🎨 Características do Público
- **Idade**: 22-45 anos, profissionais em transição
- **Motivação**: Crescimento profissional > Certificação > Networking
- **Decisão**: Racional baseada em resultados comprovados
- **Confiança**: Credenciais do instrutor e casos de sucesso
- **Urgência**: Baixa a média, relacionada a oportunidades

### 📋 Template: Curso Online

```html
<!-- Hero Section -->
<section class="bg-gradient-to-br from-purple-900 via-blue-900 to-indigo-900 text-white py-20">
    <div class="max-w-6xl mx-auto px-4">
        <div class="grid lg:grid-cols-2 gap-12 items-center">
            <!-- Conteúdo -->
            <div>
                <!-- Badge Instrutor -->
                <div class="inline-flex items-center gap-3 px-6 py-3 bg-white/20 rounded-full mb-6 backdrop-blur-sm">
                    <img class="w-8 h-8 rounded-full" src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=32&h=32&fit=crop&crop=face" alt="Instrutor">
                    <span class="font-medium">Prof. Carlos Silva • Google • Meta • 50k+ alunos</span>
                </div>
                
                <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
                    Torne-se um 
                    <span class="text-yellow-400 relative">
                        Especialista
                        <svg class="absolute -bottom-2 left-0 w-full" height="8" viewBox="0 0 200 8">
                            <path d="M0 4 Q50 0 100 4 T200 4" stroke="#fbbf24" stroke-width="3" fill="none"/>
                        </svg>
                    </span>
                    em Data Science
                </h1>
                
                <p class="text-xl text-blue-100 mb-8">
                    Do zero ao profissional em <strong>12 semanas</strong>. 
                    Curso completo com projetos reais e certificação reconhecida pelo mercado.
                </p>
                
                <!-- Estatísticas -->
                <div class="grid grid-cols-3 gap-6 mb-8">
                    <div class="text-center">
                        <div class="text-3xl font-bold text-yellow-400">89%</div>
                        <div class="text-sm text-blue-200">Conseguiram emprego</div>
                    </div>
                    <div class="text-center">
                        <div class="text-3xl font-bold text-yellow-400">R$ 8.5k</div>
                        <div class="text-sm text-blue-200">Salário médio</div>
                    </div>
                    <div class="text-center">
                        <div class="text-3xl font-bold text-yellow-400">47k+</div>
                        <div class="text-sm text-blue-200">Alunos formados</div>
                    </div>
                </div>
                
                <!-- CTAs -->
                <div class="flex flex-col sm:flex-row gap-4">
                    <button class="px-8 py-4 bg-yellow-400 text-gray-900 rounded-xl font-bold text-lg hover:bg-yellow-300 transition-colors">
                        Começar Agora • R$ 497
                    </button>
                    <button class="px-8 py-4 border-2 border-white text-white rounded-xl font-semibold text-lg hover:bg-white/10 transition-colors">
                        Aulas Gratuitas
                    </button>
                </div>
                
                <!-- Garantias -->
                <div class="flex items-center gap-6 mt-6 text-sm">
                    <div class="flex items-center gap-2">
                        <svg class="w-5 h-5 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                        </svg>
                        <span>Certificado reconhecido</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <svg class="w-5 h-5 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                        </svg>
                        <span>Garantia 30 dias</span>
                    </div>
                    <div class="flex items-center gap-2">
                        <svg class="w-5 h-5 text-green-400" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"/>
                        </svg>
                        <span>Acesso vitalício</span>
                    </div>
                </div>
            </div>
            
            <!-- Preview do Curso -->
            <div class="relative">
                <div class="bg-white rounded-3xl shadow-2xl p-8">
                    <!-- Video Preview -->
                    <div class="aspect-video bg-gray-900 rounded-2xl mb-6 flex items-center justify-center cursor-pointer group">
                        <div class="w-20 h-20 bg-white rounded-full flex items-center justify-center group-hover:scale-110 transition-transform">
                            <svg class="w-8 h-8 text-purple-600 ml-1" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M6.3 2.841A1.5 1.5 0 004 4.11V15.89a1.5 1.5 0 002.3 1.269l9.344-5.89a1.5 1.5 0 000-2.538L6.3 2.84z"/>
                            </svg>
                        </div>
                    </div>
                    
                    <!-- Conteúdo do Curso -->
                    <h3 class="text-xl font-bold text-gray-900 mb-4">O que você vai aprender:</h3>
                    <div class="space-y-3">
                        <div class="flex items-center gap-3">
                            <div class="w-6 h-6 bg-purple-100 rounded-full flex items-center justify-center">
                                <span class="text-xs font-bold text-purple-600">1</span>
                            </div>
                            <span class="text-gray-700">Python para Data Science</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-6 h-6 bg-purple-100 rounded-full flex items-center justify-center">
                                <span class="text-xs font-bold text-purple-600">2</span>
                            </div>
                            <span class="text-gray-700">Machine Learning na prática</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-6 h-6 bg-purple-100 rounded-full flex items-center justify-center">
                                <span class="text-xs font-bold text-purple-600">3</span>
                            </div>
                            <span class="text-gray-700">Projetos para portfólio</span>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-6 h-6 bg-purple-100 rounded-full flex items-center justify-center">
                                <span class="text-xs font-bold text-purple-600">4</span>
                            </div>
                            <span class="text-gray-700">Preparação para entrevistas</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
```

---

## 🏠 NICHO: IMOBILIÁRIO

### 🎨 Características do Público
- **Idade**: 25-60 anos, variado por tipo de imóvel
- **Motivação**: Localização > Preço > Facilidades
- **Decisão**: Emocional validada por dados técnicos
- **Confiança**: Credenciais profissionais e transparência
- **Urgência**: Alta para oportunidades, baixa para pesquisa

### 📋 Template: Construtora/Imobiliária

```html
<!-- Hero com Mapa/Localização -->
<section class="relative bg-gray-900 text-white py-20">
    <!-- Background Video/Imagem -->
    <div class="absolute inset-0 opacity-50">
        <img class="w-full h-full object-cover" src="https://images.unsplash.com/photo-1560518883-ce09059eeffa?w=1200&h=600&fit=crop" alt="Empreendimento">
    </div>
    
    <div class="relative z-10 max-w-6xl mx-auto px-4">
        <div class="grid lg:grid-cols-2 gap-12 items-center">
            <!-- Conteúdo -->
            <div>
                <!-- Badge Localização -->
                <div class="inline-flex items-center gap-2 px-4 py-2 bg-green-500 rounded-full mb-6">
                    <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                        <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd"/>
                    </svg>
                    <span class="font-semibold">Vila Olímpia • 500m do Metrô</span>
                </div>
                
                <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
                    Seu Apartamento dos 
                    <span class="text-yellow-400">Sonhos</span> 
                    te Esperando
                </h1>
                
                <p class="text-xl text-gray-200 mb-8">
                    <strong>Últimas 15 unidades</strong> do empreendimento mais desejado da região. 
                    Financiamento direto com a construtora e chaves em 18 meses.
                </p>
                
                <!-- Facilidades -->
                <div class="grid grid-cols-2 gap-4 mb-8">
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 bg-blue-500 rounded-xl flex items-center justify-center">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
                                <path d="M10.394 2.08a1 1 0 00-.788 0l-7 3a1 1 0 000 1.84L5.25 8.051a.999.999 0 01.356-.257l4-1.714a1 1 0 11.788 1.838L7.667 9.088l1.94.831a1 1 0 00.787 0l7-3a1 1 0 000-1.838l-7-3zM3.31 9.397L5 10.12v4.102a8.969 8.969 0 00-1.05-.174 1 1 0 01-.89-.89 11.115 11.115 0 01.25-3.762zM9.3 16.573A9.026 9.026 0 007 14.935v-3.957l1.818.78a3 3 0 002.364 0l5.508-2.361a11.026 11.026 0 01.25 3.762 1 1 0 01-.89.89 8.968 8.968 0 00-5.35 2.524 1 1 0 01-1.4 0zM6 18a1 1 0 001-1v-2.065a8.935 8.935 0 00-2-.712V17a1 1 0 001 1z"/>
                            </svg>
                        </div>
                        <div>
                            <div class="font-semibold">Financiamento Próprio</div>
                            <div class="text-sm text-gray-300">Taxa 0% nos primeiros 12 meses</div>
                        </div>
                    </div>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 bg-green-500 rounded-xl flex items-center justify-center">
                            <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 20 20">
                                <path fill-rule="evenodd" d="M6 6V5a3 3 0 013-3h2a3 3 0 013 3v1h2a2 2 0 012 2v3.57A22.952 22.952 0 0110 13a22.95 22.95 0 01-8-1.43V8a2 2 0 012-2h2zm2-1a1 1 0 011-1h2a1 1 0 011 1v1H8V5zm1 5a1 1 0 011-1h.01a1 1 0 110 2H10a1 1 0 01-1-1z" clip-rule="evenodd"/>
                                <path d="M2 13.692V16a2 2 0 002 2h12a2 2 0 002-2v-2.308A24.974 24.974 0 0110 15c-2.796 0-5.487-.46-8-1.308z"/>
                            </svg>
                        </div>
                        <div>
                            <div class="font-semibold">Pronto para Morar</div>
                            <div class="text-sm text-gray-300">Entrega em Dezembro 2024</div>
                        </div>
                    </div>
                </div>
                
                <!-- Preços -->
                <div class="bg-white/10 backdrop-blur-sm rounded-2xl p-6 mb-8">
                    <div class="grid grid-cols-3 gap-4 text-center">
                        <div>
                            <div class="text-2xl font-bold text-yellow-400">45m²</div>
                            <div class="text-sm">A partir de</div>
                            <div class="text-xl font-semibold">R$ 280k</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-yellow-400">65m²</div>
                            <div class="text-sm">A partir de</div>
                            <div class="text-xl font-semibold">R$ 420k</div>
                        </div>
                        <div>
                            <div class="text-2xl font-bold text-yellow-400">85m²</div>
                            <div class="text-sm">A partir de</div>
                            <div class="text-xl font-semibold">R$ 580k</div>
                        </div>
                    </div>
                </div>
                
                <!-- CTAs -->
                <div class="flex flex-col sm:flex-row gap-4">
                    <button class="px-8 py-4 bg-yellow-400 text-gray-900 rounded-xl font-bold text-lg hover:bg-yellow-300 transition-colors">
                        Agendar Visita
                    </button>
                    <button class="px-8 py-4 border-2 border-white text-white rounded-xl font-semibold text-lg hover:bg-white/10 transition-colors">
                        Simular Financiamento
                    </button>
                </div>
            </div>
            
            <!-- Formulário de Interesse -->
            <div class="bg-white rounded-3xl shadow-2xl p-8">
                <h3 class="text-2xl font-bold text-gray-900 mb-6">Receba Informações Exclusivas</h3>
                
                <form class="space-y-4">
                    <div>
                        <input type="text" class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-blue-500 focus:border-transparent" placeholder="Seu nome completo">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <input type="email" class="px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-blue-500 focus:border-transparent" placeholder="E-mail">
                        <input type="tel" class="px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-blue-500 focus:border-transparent" placeholder="WhatsApp">
                    </div>
                    <div>
                        <select class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            <option>Interessado em...</option>
                            <option>1 dormitório (45m²)</option>
                            <option>2 dormitórios (65m²)</option>
                            <option>3 dormitórios (85m²)</option>
                            <option>Cobertura</option>
                        </select>
                    </div>
                    <div>
                        <select class="w-full px-4 py-3 border border-gray-300 rounded-xl focus:ring-2 focus:ring-blue-500 focus:border-transparent">
                            <option>Pretende comprar em...</option>
                            <option>Próximos 30 dias</option>
                            <option>Próximos 3 meses</option>
                            <option>Próximos 6 meses</option>
                            <option>Ainda estou pesquisando</option>
                        </select>
                    </div>
                    
                    <button type="submit" class="w-full bg-blue-600 text-white font-bold py-4 rounded-xl hover:bg-blue-700 transition-colors">
                        QUERO RECEBER INFORMAÇÕES
                    </button>
                </form>
                
                <div class="mt-6 text-center text-sm text-gray-500">
                    <div class="flex items-center justify-center gap-2">
                        <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 20 20">
                            <path fill-rule="evenodd" d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z" clip-rule="evenodd"/>
                        </svg>
                        <span>Seus dados estão protegidos</span>
                    </div>
                    <p class="mt-1">Entraremos em contato em até 1 hora</p>
                </div>
            </div>
        </div>
    </div>
</section>
```

---

## 🔧 CONFIGURAÇÃO POR NICHO

### Sistema de Cores por Segmento
```javascript
const nicheColors = {
    saude: {
        primary: '#0ea5e9',    // Azul confiança
        secondary: '#22c55e',  // Verde saúde
        accent: '#f59e0b'      // Amarelo atenção
    },
    financeiro: {
        primary: '#1e40af',    // Azul escuro
        secondary: '#059669',  // Verde dinheiro
        accent: '#dc2626'      // Vermelho urgência
    },
    educacao: {
        primary: '#7c3aed',    // Roxo conhecimento
        secondary: '#2563eb',  // Azul tech
        accent: '#f59e0b'      // Amarelo destaque
    },
    imobiliario: {
        primary: '#1f2937',    // Cinza sofisticado
        secondary: '#059669',  // Verde investimento
        accent: '#f59e0b'      // Dourado luxo
    }
};
```

### Copywriting por Segmento
```javascript
const nicheCopywriting = {
    saude: {
        tone: 'empático e confiável',
        keywords: ['saúde', 'bem-estar', 'cuidado', 'especialista', 'experiência'],
        urgency: 'moderada, baseada em sintomas',
        social_proof: 'depoimentos de pacientes, credenciais médicas'
    },
    financeiro: {
        tone: 'seguro e técnico',
        keywords: ['retorno', 'segurança', 'crescimento', 'patrimônio', 'rentabilidade'],
        urgency: 'oportunidades de mercado',
        social_proof: 'resultados comprovados, certificações'
    },
    educacao: {
        tone: 'inspirador e prático',
        keywords: ['aprender', 'crescer', 'certificação', 'carreira', 'futuro'],
        urgency: 'oportunidades profissionais',
        social_proof: 'casos de sucesso, credenciais do instrutor'
    }
};
```

### Formulários Otimizados por Nicho
```javascript
const nicheFormFields = {
    saude: ['nome', 'telefone', 'idade', 'convenio', 'sintomas', 'horario_preferencia'],
    financeiro: ['nome', 'email', 'telefone', 'patrimonio_atual', 'objetivo', 'prazo'],
    educacao: ['nome', 'email', 'experiencia_atual', 'objetivo_profissional', 'disponibilidade'],
    imobiliario: ['nome', 'telefone', 'tipo_imovel', 'orcamento', 'prazo_compra', 'financiamento']
};
```

---

## 📊 MÉTRICAS POR NICHO

### Benchmarks de Conversão
- **Saúde**: 8-15% (consultas), 3-8% (tratamentos)
- **Financeiro**: 5-12% (consultoria), 2-5% (investimentos)
- **Educação**: 15-25% (cursos online), 8-15% (presencial)
- **Imobiliário**: 3-8% (vendas), 10-20% (visitas)

### Tempos de Decisão
- **Saúde**: Imediata (emergência) a 30 dias (prevenção)
- **Financeiro**: 7-90 dias (análise de risco)
- **Educação**: 3-30 dias (pesquisa de opções)
- **Imobiliário**: 30-180 dias (processo longo)

---

## 🚀 IMPLEMENTAÇÃO RÁPIDA

### Checklist por Nicho
1. **Definir público-alvo específico**
2. **Escolher paleta de cores adequada**
3. **Adaptar tom de voice**
4. **Configurar formulários otimizados**
5. **Incluir credenciais e regulamentações**
6. **Ajustar provas sociais**
7. **Configurar métricas específicas**
8. **Testar com público real**

### Recursos Essenciais
- **Compliance**: Regulamentações por setor
- **Credenciais**: Certificações obrigatórias
- **Linguagem**: Terminologia técnica adequada
- **Urgência**: Gatilhos específicos por nicho
- **Confiança**: Elementos de credibilidade únicos