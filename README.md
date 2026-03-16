<div align="center">
  <script src="https://cdn.tailwindcss.com"></script>
  
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&amp;family=Space+Grotesk:wght@500;600&amp;display=swap');
    
    :root {
      --accent: 168 85 247;
    }
    
    .hero-bg {
      background: linear-gradient(135deg, #0f172a 0%, #1e2937 100%);
      position: relative;
      overflow: hidden;
    }
    
    .hero-bg::before {
      content: '';
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: radial-gradient(circle at 30% 20%, rgba(168,85,247,0.15) 0%, transparent 70%);
      animation: glow 8s ease-in-out infinite alternate;
      pointer-events: none;
    }
    
    @keyframes glow {
      0% { opacity: 0.6; transform: scale(1); }
      100% { opacity: 1; transform: scale(1.08); }
    }
    
    .name {
      font-family: 'Space Grotesk', sans-serif;
      font-size: 4.5rem;
      letter-spacing: -0.05em;
      background: linear-gradient(90deg, #fff, #a855f7, #fff);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientShift 6s ease infinite;
    }
    
    @keyframes gradientShift {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }
    
    .typing {
      overflow: hidden;
      border-right: 3px solid #a855f7;
      white-space: nowrap;
      animation: typing 3.5s steps(30, end) forwards, blink 0.8s step-end infinite;
    }
    
    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }
    
    @keyframes blink {
      50% { border-color: transparent }
    }
    
    .tech-card {
      transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    }
    
    .tech-card:hover {
      transform: translateY(-12px) scale(1.05);
      box-shadow: 0 25px 50px -12px rgb(168 85 247 / 0.4);
    }
    
    .project-card {
      transition: all 0.5s cubic-bezier(0.34, 1.56, 0.64, 1);
    }
    
    .project-card:hover {
      transform: scale(1.03) rotate(1deg);
    }
    
    .contact-btn {
      position: relative;
      overflow: hidden;
    }
    
    .contact-btn::after {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 40%;
      height: 300%;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.3), transparent);
      transform: skewX(-25deg);
      animation: shine 4s infinite;
    }
    
    @keyframes shine {
      0% { transform: translateX(-150%) skewX(-25deg); }
      20% { transform: translateX(300%) skewX(-25deg); }
      100% { transform: translateX(300%) skewX(-25deg); }
    }
  </style>

  <div class="hero-bg min-h-screen flex items-center justify-center py-20 px-6 text-white">
    <div class="max-w-5xl mx-auto text-center">
      
      <!-- Avatar + Nome -->
      <div class="mb-8 flex justify-center">
        <div class="w-32 h-32 rounded-3xl bg-gradient-to-br from-violet-500 to-fuchsia-500 p-1 shadow-2xl">
          <div class="w-full h-full bg-zinc-900 rounded-3xl flex items-center justify-center text-6xl transition-transform hover:rotate-12 duration-700">
            👩‍💻
          </div>
        </div>
      </div>
      
      <h1 class="name font-bold tracking-tighter mb-3">Arlete De Lira</h1>
      
      <div class="typing text-2xl font-medium text-violet-300 mx-auto max-w-md">
        Estudante de Desenvolvimento de Sistemas • Futura Analista de Sistemas
      </div>
      
      <p class="mt-10 max-w-2xl mx-auto text-lg text-zinc-400 leading-relaxed">
        Transformo café em código e experiência em soluções inteligentes.<br>
        <span class="text-violet-400 font-semibold">Leitura Técnica</span> — meu projeto educacional que nasceu na Oracle e hoje inspira milhares a aprender melhor.
      </p>

      <div class="mt-12 flex gap-6 justify-center">
        <a href="https://www.linkedin.com/in/arletedelira/" 
           target="_blank"
           class="contact-btn px-8 py-4 bg-white text-zinc-900 font-semibold rounded-2xl flex items-center gap-3 hover:bg-violet-200 transition-all duration-300">
          <span>Conectar no LinkedIn</span>
          <span class="text-xl">↗</span>
        </a>
        
        <a href="https://github.com/arletedelira-TI" 
           target="_blank"
           class="px-8 py-4 border border-white/30 hover:border-white rounded-2xl font-medium transition-all duration-300">
          Ver GitHub
        </a>
      </div>
    </div>
  </div>

  <!-- Sobre -->
  <div class="bg-zinc-950 py-20">
    <div class="max-w-4xl mx-auto px-6">
      <div class="text-center mb-16">
        <span class="inline-block px-6 py-2 bg-violet-500/10 text-violet-400 text-sm font-medium rounded-full mb-4">MINHA JORNADA</span>
        <h2 class="text-5xl font-bold text-white mb-4">Olá, mundo! 👋</h2>
        <p class="text-xl text-zinc-400 max-w-xl mx-auto">
          Estou cursando Desenvolvimento de Sistemas e minha missão é me tornar uma <span class="text-emerald-400 font-semibold">Analista de Sistemas</span> capaz de transformar problemas complexos em soluções elegantes e humanas.
        </p>
      </div>
      
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-zinc-900/70 border border-white/10 p-8 rounded-3xl hover:border-violet-500/30 transition-all duration-500 group">
          <div class="text-4xl mb-6">🧠</div>
          <h3 class="text-2xl font-semibold mb-3">Análise &amp; Metacognição</h3>
          <p class="text-zinc-400">Acredito que o melhor sistema começa na cabeça. Por isso criei o Leitura Técnica: conteúdo que ensina a aprender melhor.</p>
        </div>
        
        <div class="bg-zinc-900/70 border border-white/10 p-8 rounded-3xl hover:border-violet-500/30 transition-all duration-500 group">
          <div class="text-4xl mb-6">🔬</div>
          <h3 class="text-2xl font-semibold mb-3">Experiência Real</h3>
          <p class="text-zinc-400">3 anos na Oracle me ensinaram que tecnologia só faz sentido quando resolve dor real de quem usa.</p>
        </div>
        
        <div class="bg-zinc-900/70 border border-white/10 p-8 rounded-3xl hover:border-violet-500/30 transition-all duration-500 group">
          <div class="text-4xl mb-6">🌱</div>
          <h3 class="text-2xl font-semibold mb-3">Em constante evolução</h3>
          <p class="text-zinc-400">Hoje desenvolvo, amanhã analiso. E sempre compartilho tudo que aprendo.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Tecnologias -->
  <div class="py-20 bg-black">
    <div class="max-w-5xl mx-auto px-6">
      <div class="text-center mb-12">
        <span class="text-sm tracking-widest text-violet-400">STACK ATUAL</span>
        <h2 class="text-4xl font-bold mt-2">Tecnologias que eu domino e amo</h2>
      </div>
      
      <div class="grid grid-cols-2 md:grid-cols-4 gap-6">
        <!-- Linux -->
        <div class="tech-card bg-zinc-900 border border-zinc-800 rounded-3xl p-8 text-center group">
          <div class="mx-auto w-16 h-16 flex items-center justify-center text-5xl mb-6 transition-transform group-hover:rotate-12">🐧</div>
          <h4 class="text-2xl font-semibold mb-1">Linux</h4>
          <p class="text-zinc-500 text-sm">Meu sistema operacional do dia a dia</p>
        </div>
        
        <!-- Python -->
        <div class="tech-card bg-zinc-900 border border-zinc-800 rounded-3xl p-8 text-center group">
          <div class="mx-auto w-16 h-16 flex items-center justify-center text-5xl mb-6 transition-transform group-hover:scale-125">🐍</div>
          <h4 class="text-2xl font-semibold mb-1">Python</h4>
          <p class="text-zinc-500 text-sm">Automação, dados e inteligência</p>
        </div>
        
        <!-- HTML -->
        <div class="tech-card bg-zinc-900 border border-zinc-800 rounded-3xl p-8 text-center group">
          <div class="mx-auto w-16 h-16 flex items-center justify-center text-5xl mb-6 transition-transform group-hover:-rotate-6">📘</div>
          <h4 class="text-2xl font-semibold mb-1">HTML5</h4>
          <p class="text-zinc-500 text-sm">Estrutura semântica e acessível</p>
        </div>
        
        <!-- CSS -->
        <div class="tech-card bg-zinc-900 border border-zinc-800 rounded-3xl p-8 text-center group">
          <div class="mx-auto w-16 h-16 flex items-center justify-center text-5xl mb-6 transition-transform group-hover:rotate-6">🎨</div>
          <h4 class="text-2xl font-semibold mb-1">CSS3</h4>
          <p class="text-zinc-500 text-sm">Design moderno e animações</p>
        </div>
      </div>
    </div>
  </div>

  <!-- Projeto Destaque -->
  <div class="py-24 bg-gradient-to-b from-zinc-950 to-black">
    <div class="max-w-4xl mx-auto px-6">
      <div class="project-card bg-zinc-900 border border-violet-500/30 rounded-3xl overflow-hidden">
        <div class="h-2 bg-gradient-to-r from-violet-500 to-fuchsia-500"></div>
        
        <div class="p-12">
          <div class="flex items-center gap-4 mb-8">
            <div class="text-6xl">📖</div>
            <div>
              <span class="px-5 py-1.5 bg-violet-500/10 text-violet-400 text-xs font-bold rounded-full">PROJETO EM DESTAQUE</span>
              <h3 class="text-4xl font-bold mt-3">Leitura Técnica</h3>
            </div>
          </div>
          
          <p class="text-xl text-zinc-300 max-w-2xl">
            Projeto educacional 100% gratuito que nasceu da minha experiência na Oracle. 
            Artigos profundos, resumos analíticos e técnicas de metacognição para quem quer aprender de verdade.
          </p>
          
          <div class="mt-10 flex flex-wrap gap-4">
            <a href="https://github.com/arletedelira-TI" 
               target="_blank"
               class="inline-flex items-center gap-3 bg-white text-black px-8 py-5 rounded-2xl font-semibold hover:shadow-2xl transition-all">
              Explorar repositório
              <span class="text-xl">→</span>
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Contato -->
  <div class="bg-zinc-950 py-20 border-t border-white/10">
    <div class="max-w-4xl mx-auto px-6 text-center">
      <h2 class="text-4xl font-bold mb-4">Vamos construir algo incrível juntos?</h2>
      <p class="text-zinc-400 mb-12">Estou aberta a colaborações, ideias e conversas sobre sistemas, análise e aprendizado.</p>
      
      <div class="flex flex-wrap justify-center gap-6">
        <a href="https://www.linkedin.com/in/arletedelira/" target="_blank"
           class="contact-btn group flex items-center gap-4 bg-zinc-900 hover:bg-zinc-800 border border-white/10 px-10 py-6 rounded-3xl transition-all">
          <span class="text-3xl">💼</span>
          <div class="text-left">
            <div class="font-semibold text-lg">LinkedIn</div>
            <div class="text-violet-400 text-sm">arletedelira</div>
          </div>
        </a>
        
        <a href="mailto:arletedelira.ti@gmail.com"
           class="contact-btn group flex items-center gap-4 bg-zinc-900 hover:bg-zinc-800 border border-white/10 px-10 py-6 rounded-3xl transition-all">
          <span class="text-3xl">✉️</span>
          <div class="text-left">
            <div class="font-semibold text-lg">E-mail</div>
            <div class="text-emerald-400 text-sm">arletedelira.ti@gmail.com</div>
          </div>
        </a>
        
        <a href="https://arletedelira-ti.blogspot.com/" target="_blank"
           class="contact-btn group flex items-center gap-4 bg-zinc-900 hover:bg-zinc-800 border border-white/10 px-10 py-6 rounded-3xl transition-all">
          <span class="text-3xl">🌐</span>
          <div class="text-left">
            <div class="font-semibold text-lg">Site Pessoal</div>
            <div class="text-amber-400 text-sm">Blog &amp; Portfólio</div>
          </div>
        </a>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <div class="py-12 bg-black text-center text-zinc-500 text-sm border-t border-white/5">
    <p class="flex items-center justify-center gap-2">
      Feito com ❤️, café e Tailwind • 
      <span class="text-violet-400">Arlete De Lira © 2026</span>
    </p>
    <p class="mt-2">Sempre em evolução • 🇧🇷 Brasil</p>
  </div>
</div>
