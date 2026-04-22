<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Netaji Subhas Chandra Bose — Legacy of Courage</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://code.iconify.design/iconify-icon/1.0.7/iconify-icon.min.js"></script>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            'sans': ['Inter', 'sans-serif'],
            'dm': ['DM Sans', 'sans-serif'],
          },
          colors: {
            netaji: {
              50: '#f0fdf4',
              100: '#dcfce7',
              200: '#bbf7d0',
              300: '#86efac',
              400: '#4ade80',
              500: '#22c55e',
              600: '#16a34a',
              700: '#15803d',
              800: '#166534',
              900: '#14532d',
              950: '#052e16',
            },
            navy: '#0f172a',
          }
        }
      }
    }
  </script>
  <style>
    body {
      background-color: #020617;
      font-family: 'Inter', sans-serif;
    }

    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #0f172a; }
    ::-webkit-scrollbar-thumb { background: #22c55e; border-radius: 3px; }

    .bg-grid {
      background-image:
        linear-gradient(rgba(34,197,94,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(34,197,94,0.03) 1px, transparent 1px);
      background-size: 60px 60px;
      mask-image: radial-gradient(ellipse at center, black 40%, transparent 80%);
    }

    .hero-gradient {
      background: linear-gradient(to bottom, #ffffff, #ffffff, #94a3b8);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .green-glow {
      text-shadow: 0 0 40px rgba(34,197,94,0.3);
    }

    .hero-glow {
      background: radial-gradient(ellipse at 50% 30%, rgba(34,197,94,0.12) 0%, rgba(34,197,94,0.04) 40%, transparent 70%);
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(1deg); }
    }
    .animate-float { animation: float 6s ease-in-out infinite; }
    .animate-float-delay { animation: float 8s ease-in-out 2s infinite; }

    @keyframes pulse-ring {
      0% { transform: scale(1); opacity: 0.6; }
      100% { transform: scale(1.8); opacity: 0; }
    }
    .pulse-ring::before {
      content: '';
      position: absolute;
      inset: -8px;
      border: 2px solid rgba(34,197,94,0.4);
      border-radius: 50%;
      animation: pulse-ring 2s ease-out infinite;
    }

    .timeline-line {
      background: linear-gradient(to bottom, transparent, rgba(34,197,94,0.4), rgba(34,197,94,0.4), transparent);
    }

    .card-hover {
      transition: all 300ms ease;
      border: 1px solid rgba(255,255,255,0.05);
    }
    .card-hover:hover {
      border-color: rgba(34,197,94,0.3);
      transform: translateY(-4px);
      box-shadow: 0 25px 50px -12px rgba(0,0,0,0.4);
    }

    .quote-card {
      background: linear-gradient(135deg, rgba(34,197,94,0.05), rgba(15,23,42,0.8));
      border: 1px solid rgba(34,197,94,0.15);
    }

    .reveal {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
    }
    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    .tricolor-top {
      background: linear-gradient(90deg, #FF9933 33.33%, #FFFFFF 33.33%, #FFFFFF 66.66%, #138808 66.66%);
      height: 4px;
    }

    .portrait-frame {
      position: relative;
    }
    .portrait-frame::after {
      content: '';
      position: absolute;
      inset: -4px;
      border: 2px solid rgba(34,197,94,0.3);
      border-radius: 1rem;
      pointer-events: none;
    }

    html { scroll-behavior: smooth; }

    .nav-link {
      position: relative;
      transition: color 150ms;
    }
    .nav-link::after {
      content: '';
      position: absolute;
      bottom: -4px;
      left: 50%;
      width: 0;
      height: 2px;
      background: #22c55e;
      transition: all 200ms;
      transform: translateX(-50%);
    }
    .nav-link:hover::after,
    .nav-link.active::after {
      width: 100%;
    }

    .ina-badge {
      background: linear-gradient(135deg, #22c55e, #16a34a);
      color: #ffffff;
    }

    .netaji-img {
      filter: sepia(0.15) contrast(1.05) brightness(0.95);
      transition: filter 0.5s ease;
    }
    .netaji-img:hover {
      filter: sepia(0) contrast(1.1) brightness(1);
    }

    @keyframes subtle-zoom {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.03); }
    }
    .subtle-zoom { animation: subtle-zoom 12s ease-in-out infinite; }
  </style>
</head>
<body class="text-white overflow-x-hidden">

  <!-- Tricolor Top Bar -->
  <div class="tricolor-top fixed top-0 left-0 right-0 z-[60]"></div>

  <!-- Navigation -->
  <nav class="fixed top-1 left-0 right-0 z-50 flex justify-center px-4 mt-2">
    <div class="flex items-center gap-1 px-2 py-2 rounded-full bg-slate-900/80 backdrop-blur-xl border border-white/10 shadow-2xl">
      <a href="#hero" class="nav-link flex items-center gap-2 px-4 py-2 text-sm font-medium text-netaji-400 rounded-full hover:bg-white/5">
        <iconify-icon icon="solar:star-bold" width="16"></iconify-icon>
        <span class="hidden sm:inline">Netaji</span>
      </a>
      <a href="#about" class="nav-link px-4 py-2 text-sm font-medium text-slate-400 hover:text-white rounded-full hover:bg-white/5">About</a>
      <a href="#timeline" class="nav-link px-4 py-2 text-sm font-medium text-slate-400 hover:text-white rounded-full hover:bg-white/5">Timeline</a>
      <a href="#ina" class="nav-link px-4 py-2 text-sm font-medium text-slate-400 hover:text-white rounded-full hover:bg-white/5">INA</a>
      <a href="#quotes" class="nav-link px-4 py-2 text-sm font-medium text-slate-400 hover:text-white rounded-full hover:bg-white/5">Quotes</a>
      <a href="#legacy" class="nav-link px-4 py-2 text-sm font-medium text-slate-400 hover:text-white rounded-full hover:bg-white/5">Legacy</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="hero" class="relative min-h-screen flex items-center justify-center overflow-hidden">
    <div class="absolute inset-0 bg-grid"></div>
    <div class="absolute inset-0 hero-glow"></div>
    <div class="absolute top-1/4 -left-32 w-96 h-96 bg-green-500/5 rounded-full blur-3xl animate-float"></div>
    <div class="absolute bottom-1/4 -right-32 w-80 h-80 bg-emerald-500/5 rounded-full blur-3xl animate-float-delay"></div>

    <div class="relative z-10 max-w-6xl mx-auto px-6 pt-32 pb-20 flex flex-col lg:flex-row items-center gap-12 lg:gap-16">
      <!-- Left Content -->
      <div class="flex-1 text-center lg:text-left">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-8">
          <iconify-icon icon="solar:flag-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">Father of the Nation's Armed Struggle</span>
        </div>

        <h1 class="font-dm text-5xl md:text-7xl lg:text-8xl font-light tracking-tight leading-[1.05] hero-gradient mb-6">
          Netaji<br>
          <span class="font-semibold text-netaji-400 green-glow" style="-webkit-text-fill-color: #4ade80;">Subhas Chandra</span><br>
          Bose
        </h1>

        <p class="text-lg md:text-xl text-slate-400 font-light leading-relaxed max-w-xl mx-auto lg:mx-0 mb-10">
          "Give me blood, and I shall give you freedom!" — A revolutionary leader who dared to challenge the mightiest empire on Earth, and awakened a nation to fight for its destiny.
        </p>

        <div class="flex flex-col sm:flex-row items-center gap-4 justify-center lg:justify-start">
          <a href="#about" class="group inline-flex items-center gap-2 px-8 py-4 bg-netaji-500 text-white font-semibold rounded-full hover:bg-netaji-400 transition-all duration-150 shadow-lg shadow-green-500/20">
            Explore His Legacy
            <iconify-icon icon="solar:arrow-right-linear" width="20" class="group-hover:translate-x-1 transition-transform"></iconify-icon>
          </a>
          <a href="#quotes" class="inline-flex items-center gap-2 px-8 py-4 border border-white/10 text-white font-medium rounded-full hover:border-netaji-500/30 hover:bg-white/5 transition-all duration-150">
            <iconify-icon icon="solar:chat-square-like-linear" width="20" class="text-netaji-400"></iconify-icon>
            His Words
          </a>
        </div>

        <div class="flex items-center gap-8 mt-12 justify-center lg:justify-start">
          <div>
            <div class="text-2xl font-semibold text-white">1897</div>
            <div class="text-xs text-slate-500 uppercase tracking-wider">Born</div>
          </div>
          <div class="w-px h-10 bg-white/10"></div>
          <div>
            <div class="text-2xl font-semibold text-white">INA</div>
            <div class="text-xs text-slate-500 uppercase tracking-wider">Founded</div>
          </div>
          <div class="w-px h-10 bg-white/10"></div>
          <div>
            <div class="text-2xl font-semibold text-white">₹</div>
            <div class="text-xs text-slate-500 uppercase tracking-wider">Azad Hind Bank</div>
          </div>
        </div>
      </div>

      <!-- Right: Portrait - Real Netaji Image -->
      <div class="flex-shrink-0 relative">
        <div class="relative animate-float">
          <div class="absolute inset-0 bg-netaji-500/20 rounded-3xl blur-3xl scale-110"></div>
          <div class="portrait-frame relative rounded-2xl overflow-hidden shadow-2xl" style="box-shadow: 0 25px 50px -12px rgba(34,197,94,0.15);">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Subhas_Chandra_Bose_NRB.jpg" alt="Netaji Subhas Chandra Bose" class="w-72 md:w-80 lg:w-96 h-auto object-cover netaji-img subtle-zoom">
            <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-transparent to-transparent"></div>
            <div class="absolute bottom-6 left-6 right-6">
              <div class="text-xs font-semibold tracking-widest uppercase text-netaji-400 mb-1">Jan 23, 1897 — Aug 18, 1945</div>
              <div class="text-white font-medium">Revolutionary • Leader • Patriot</div>
            </div>
          </div>
        </div>

        <div class="absolute -top-4 -right-4 animate-float-delay">
          <div class="ina-badge px-4 py-2 rounded-full text-xs font-bold tracking-wider uppercase shadow-lg">
            <iconify-icon icon="solar:shield-star-bold" width="14" class="mr-1"></iconify-icon>
            Azad Hind Fauj
          </div>
        </div>

        <div class="absolute -bottom-4 -left-4 animate-float">
          <div class="w-16 h-16 rounded-full bg-slate-900 border-2 border-netaji-500/40 flex items-center justify-center shadow-xl">
            <iconify-icon icon="solar:medal-ribbons-star-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
        </div>
      </div>
    </div>

    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2">
      <span class="text-xs text-slate-500 tracking-widest uppercase">Scroll</span>
      <div class="w-5 h-8 border border-white/20 rounded-full flex items-start justify-center p-1">
        <div class="w-1 h-2 bg-netaji-400 rounded-full animate-bounce"></div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-grid opacity-50"></div>
    <div class="relative z-10 max-w-7xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:user-circle-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">The Legend</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">Who Was <span class="text-netaji-400 font-medium">Netaji</span>?</h2>
        <p class="text-slate-400 text-lg max-w-2xl mx-auto font-light">One of the most dynamic and controversial leaders of the Indian independence movement.</p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Image - Real Netaji Image -->
        <div class="reveal">
          <div class="relative rounded-2xl overflow-hidden group">
            <img src="https://upload.wikimedia.org/wikipedia/commons/1/1a/Subhas_Chandra_Bose_During_WWII.jpg" alt="Netaji Subhas Chandra Bose during World War II" class="w-full h-80 lg:h-[28rem] object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
            <div class="absolute inset-0 bg-gradient-to-t from-slate-950 via-slate-950/30 to-transparent"></div>
            <div class="absolute bottom-6 left-6 right-6">
              <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-full bg-netaji-500/20 flex items-center justify-center">
                  <iconify-icon icon="solar:microphone-3-bold" width="20" class="text-netaji-400"></iconify-icon>
                </div>
                <div>
                  <div class="text-white font-medium text-sm">Netaji in Southeast Asia</div>
                  <div class="text-slate-400 text-xs">During World War II, 1943</div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Content -->
        <div class="reveal space-y-6">
          <div class="space-y-4 text-slate-300 font-light leading-relaxed">
            <p>
              <span class="text-white font-medium">Subhas Chandra Bose</span> was born on <span class="text-netaji-400">January 23, 1897</span>, in Cuttack, Odisha. A brilliant student, he stood fourth in the Indian Civil Services examination but resigned, choosing to serve his motherland instead of the British Raj.
            </p>
            <p>
              His journey from a young nationalist to the Supreme Commander of the <span class="text-white font-medium">Indian National Army (INA)</span> is a saga of unparalleled courage, strategic brilliance, and unwavering commitment to India's freedom.
            </p>
            <p>
              Netaji's famous escape from house arrest in 1941 — traveling through Afghanistan, the Soviet Union, Germany, and finally reaching Southeast Asia — remains one of the most daring exploits in modern history.
            </p>
          </div>

          <div class="grid grid-cols-2 gap-4 pt-4">
            <div class="card-hover p-5 rounded-2xl bg-white/[0.03] backdrop-blur-sm">
              <iconify-icon icon="solar:map-point-bold" width="24" class="text-netaji-400 mb-3"></iconify-icon>
              <div class="text-white font-medium text-sm">Birthplace</div>
              <div class="text-slate-400 text-xs">Cuttack, Odisha</div>
            </div>
            <div class="card-hover p-5 rounded-2xl bg-white/[0.03] backdrop-blur-sm">
              <iconify-icon icon="solar:square-academic-cap-bold" width="24" class="text-netaji-400 mb-3"></iconify-icon>
              <div class="text-white font-medium text-sm">Education</div>
              <div class="text-slate-400 text-xs">Cambridge University</div>
            </div>
            <div class="card-hover p-5 rounded-2xl bg-white/[0.03] backdrop-blur-sm">
              <iconify-icon icon="solar:crown-bold" width="24" class="text-netaji-400 mb-3"></iconify-icon>
              <div class="text-white font-medium text-sm">Title</div>
              <div class="text-slate-400 text-xs">Netaji (Respected Leader)</div>
            </div>
            <div class="card-hover p-5 rounded-2xl bg-white/[0.03] backdrop-blur-sm">
              <iconify-icon icon="solar:heart-bold" width="24" class="text-netaji-400 mb-3"></iconify-icon>
              <div class="text-white font-medium text-sm">Philosophy</div>
              <div class="text-slate-400 text-xs">Armed Resistance</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Stats Section -->
  <section class="relative py-20 overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-b from-slate-950 via-slate-900/50 to-slate-950"></div>
    <div class="relative z-10 max-w-5xl mx-auto px-6">
      <div class="reveal grid grid-cols-2 md:grid-cols-4 gap-8">
        <div class="text-center">
          <div class="text-4xl md:text-5xl font-light text-netaji-400 mb-2">60,000+</div>
          <div class="text-sm text-slate-400">INA Soldiers</div>
        </div>
        <div class="text-center">
          <div class="text-4xl md:text-5xl font-light text-netaji-400 mb-2">1943</div>
          <div class="text-sm text-slate-400">Provisional Govt.</div>
        </div>
        <div class="text-center">
          <div class="text-4xl md:text-5xl font-light text-netaji-400 mb-2">48</div>
          <div class="text-sm text-slate-400">Years of Age</div>
        </div>
        <div class="text-center">
          <div class="text-4xl md:text-5xl font-light text-netaji-400 mb-2">∞</div>
          <div class="text-sm text-slate-400">Legacy Lives On</div>
        </div>
      </div>
    </div>
  </section>

  <!-- Timeline Section -->
  <section id="timeline" class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-grid opacity-30"></div>
    <div class="relative z-10 max-w-5xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:clock-circle-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">Journey of a Hero</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">Life <span class="text-netaji-400 font-medium">Timeline</span></h2>
        <p class="text-slate-400 text-lg max-w-2xl mx-auto font-light">From a curious child in Cuttack to the Supreme Commander of the Indian National Army.</p>
      </div>

      <div class="relative">
        <div class="absolute left-6 md:left-1/2 top-0 bottom-0 w-px timeline-line md:-translate-x-px"></div>

        <div class="space-y-12">
          <!-- Event 1 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:text-right md:pr-12 pl-16 md:pl-0">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1897</div>
              <h3 class="text-white font-medium text-lg mb-2">Birth in Cuttack</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Born on January 23 to Janakinath Bose and Prabhavati Devi in Cuttack, Odisha. The ninth child in a prominent Bengali family.</p>
            </div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16"></div>
          </div>

          <!-- Event 2 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:pr-12 pl-16 md:pl-0"></div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1919</div>
              <h3 class="text-white font-medium text-lg mb-2">Return from Cambridge</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Resigned from the Indian Civil Service after clearing the exam, choosing to join India's freedom struggle instead of serving the British Empire.</p>
            </div>
          </div>

          <!-- Event 3 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:text-right md:pr-12 pl-16 md:pl-0">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1921</div>
              <h3 class="text-white font-medium text-lg mb-2">Joins Gandhiji's Movement</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Joined the Indian National Congress and worked closely with Deshbandhu Chittaranjan Das in the Non-Cooperation Movement.</p>
            </div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16"></div>
          </div>

          <!-- Event 4 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:pr-12 pl-16 md:pl-0"></div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1938</div>
              <h3 class="text-white font-medium text-lg mb-2">Congress President</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Elected President of the Indian National Congress at the Haripura session. Re-elected in 1939 at Tripuri, defeating Gandhiji's nominee.</p>
            </div>
          </div>

          <!-- Event 5 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:text-right md:pr-12 pl-16 md:pl-0">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1941</div>
              <h3 class="text-white font-medium text-lg mb-2">The Great Escape</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Escaped from house arrest in Calcutta disguised as a Pathan, traveling through Afghanistan, USSR, Germany, and eventually reaching Japan by submarine.</p>
            </div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16"></div>
          </div>

          <!-- Event 6 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:pr-12 pl-16 md:pl-0"></div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1943</div>
              <h3 class="text-white font-medium text-lg mb-2">Azad Hind Government</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Formed the Provisional Government of Free India (Azad Hind) in Singapore on October 21, 1943. Declared war on Britain and the United States.</p>
            </div>
          </div>

          <!-- Event 7 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:text-right md:pr-12 pl-16 md:pl-0">
              <div class="text-netaji-400 font-dm text-2xl font-semibold mb-2">1944</div>
              <h3 class="text-white font-medium text-lg mb-2">Battle of Imphal & Kohima</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Led the INA with the battle cry "Dilli Chalo" (On to Delhi). The INA planted the Indian tricolor on Indian soil at Moirang, Manipur.</p>
            </div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500 border-4 border-slate-950 pulse-ring relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16"></div>
          </div>

          <!-- Event 8 -->
          <div class="reveal relative flex flex-col md:flex-row items-start md:items-center gap-6 md:gap-12">
            <div class="md:w-1/2 md:pr-12 pl-16 md:pl-0"></div>
            <div class="absolute left-4 md:left-1/2 md:-translate-x-1/2 w-5 h-5 rounded-full bg-netaji-500/50 border-4 border-slate-950 relative z-10"></div>
            <div class="md:w-1/2 md:pl-12 pl-16">
              <div class="text-netaji-400/70 font-dm text-2xl font-semibold mb-2">1945</div>
              <h3 class="text-white font-medium text-lg mb-2">The Mysterious Disappearance</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Reportedly died in a plane crash in Taipei on August 18, 1945. However, the circumstances remain one of India's greatest unsolved mysteries.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- INA Section -->
  <section id="ina" class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-b from-slate-950 via-slate-900/30 to-slate-950"></div>
    <div class="absolute top-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-netaji-500/20 to-transparent"></div>
    <div class="absolute bottom-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-netaji-500/20 to-transparent"></div>

    <div class="relative z-10 max-w-7xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:shield-star-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">Indian National Army</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">The <span class="text-netaji-400 font-medium">Azad Hind Fauj</span></h2>
        <p class="text-slate-400 text-lg max-w-2xl mx-auto font-light">An army born not of territory, but of hope — forged from prisoners of war who chose freedom over captivity.</p>
      </div>

      <!-- INA Image -->
      <div class="reveal mb-12">
        <div class="relative rounded-2xl overflow-hidden group max-w-4xl mx-auto">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Netaji_Subhas_Chandra_Bose_Rally.jpg/1280px-Netaji_Subhas_Chandra_Bose_Rally.jpg" alt="Netaji Subhas Chandra Bose addressing INA rally" class="w-full h-64 md:h-96 object-cover object-center netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/80 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-6 left-6 right-6 flex items-end justify-between">
            <div>
              <div class="text-netaji-400 text-xs font-semibold tracking-widest uppercase mb-1">Historic Photograph</div>
              <div class="text-white font-medium">Netaji addressing a massive rally</div>
            </div>
            <div class="hidden sm:flex items-center gap-2 px-3 py-1.5 rounded-full bg-white/10 backdrop-blur-sm border border-white/10">
              <iconify-icon icon="solar:camera-bold" width="14" class="text-netaji-400"></iconify-icon>
              <span class="text-white text-xs">Authentic archival photo</span>
            </div>
          </div>
        </div>
      </div>

      <div class="grid md:grid-cols-3 gap-6">
        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:users-group-rounded-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">Formation</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">Originally formed in 1942 by Captain Mohan Singh with Indian POWs captured by Japan. Netaji revitalized it in 1943, transforming it into a formidable fighting force of 60,000+ soldiers.</p>
        </div>

        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:flag-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">The Tricolor</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">The Azad Hind flag — a horizontal tricolor of saffron, white, and green with a springing tiger — became a symbol of resistance. First hoisted on Indian soil at Moirang, Manipur on April 14, 1944.</p>
        </div>

        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:music-note-2-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">Anthem & Motto</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">
            <span class="text-white italic">"Kadam Kadam Badhaye Ja"</span> — the marching song that inspired millions. The INA motto: <span class="text-white italic">"Ittefaq, Itmad, Qurbani"</span> (Unity, Faith, Sacrifice).
          </p>
        </div>

        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:sword-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">Military Campaigns</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">The INA fought alongside Japanese forces in the Burma campaign, reaching the gates of India. The battles of Imphal and Kohima became legendary in military history.</p>
        </div>

        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:buildings-2-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">Azad Hind Government</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">A complete government-in-exile with its own currency (Azad Hind Bank), postage stamps, courts, and civil administration — recognized by 11 countries including Japan, Germany, and Italy.</p>
        </div>

        <div class="reveal card-hover p-8 rounded-2xl bg-white/[0.03] backdrop-blur-sm group">
          <div class="w-14 h-14 rounded-2xl bg-netaji-500/10 flex items-center justify-center mb-6 group-hover:bg-netaji-500/20 transition-colors">
            <iconify-icon icon="solar:fire-bold" width="28" class="text-netaji-400"></iconify-icon>
          </div>
          <h3 class="text-white font-medium text-xl mb-3">Red Fort Trials</h3>
          <p class="text-slate-400 text-sm font-light leading-relaxed">The 1945 trials of INA officers at the Red Fort ignited nationwide fury. The resulting naval mutiny of 1946 convinced the British that they could no longer hold India by force.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Quotes Section -->
  <section id="quotes" class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-grid opacity-20"></div>
    <div class="relative z-10 max-w-5xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:chat-square-like-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">His Words</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">Words That <span class="text-netaji-400 font-medium">Ignited a Nation</span></h2>
      </div>

      <div class="grid md:grid-cols-2 gap-6">
        <div class="reveal quote-card rounded-2xl p-8 relative cursor-pointer">
          <iconify-icon icon="solar:quote-up-square-bold" width="40" class="text-netaji-500/20 absolute top-6 right-6"></iconify-icon>
          <p class="text-white text-lg font-light leading-relaxed mb-6 italic">"Give me blood, and I shall give you freedom!"</p>
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-full bg-netaji-500/20 flex items-center justify-center">
              <iconify-icon icon="solar:microphone-3-bold" width="16" class="text-netaji-400"></iconify-icon>
            </div>
            <div class="text-xs text-slate-400">Rally in Burma, 1944</div>
          </div>
        </div>

        <div class="reveal quote-card rounded-2xl p-8 relative cursor-pointer">
          <iconify-icon icon="solar:quote-up-square-bold" width="40" class="text-netaji-500/20 absolute top-6 right-6"></iconify-icon>
          <p class="text-white text-lg font-light leading-relaxed mb-6 italic">"Freedom is not given — it is taken."</p>
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-full bg-netaji-500/20 flex items-center justify-center">
              <iconify-icon icon="solar:pen-new-square-bold" width="16" class="text-netaji-400"></iconify-icon>
            </div>
            <div class="text-xs text-slate-400">Written statement</div>
          </div>
        </div>

        <div class="reveal quote-card rounded-2xl p-8 relative cursor-pointer">
          <iconify-icon icon="solar:quote-up-square-bold" width="40" class="text-netaji-500/20 absolute top-6 right-6"></iconify-icon>
          <p class="text-white text-lg font-light leading-relaxed mb-6 italic">"One individual may die for an idea, but that idea will, after his death, incarnate itself in a thousand lives."</p>
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-full bg-netaji-500/20 flex items-center justify-center">
              <iconify-icon icon="solar:book-bold" width="16" class="text-netaji-400"></iconify-icon>
            </div>
            <div class="text-xs text-slate-400">From his writings</div>
          </div>
        </div>

        <div class="reveal quote-card rounded-2xl p-8 relative cursor-pointer">
          <iconify-icon icon="solar:quote-up-square-bold" width="40" class="text-netaji-500/20 absolute top-6 right-6"></iconify-icon>
          <p class="text-white text-lg font-light leading-relaxed mb-6 italic">"It is blood alone that can pay the price of freedom. Give me blood and I promise you freedom."</p>
          <div class="flex items-center gap-3">
            <div class="w-8 h-8 rounded-full bg-netaji-500/20 flex items-center justify-center">
              <iconify-icon icon="solar:microphone-3-bold" width="16" class="text-netaji-400"></iconify-icon>
            </div>
            <div class="text-xs text-slate-400">Speech to INA soldiers</div>
          </div>
        </div>

        <div class="reveal quote-card rounded-2xl p-8 relative md:col-span-2 cursor-pointer">
          <iconify-icon icon="solar:quote-up-square-bold" width="40" class="text-netaji-500/20 absolute top-6 right-6"></iconify-icon>
          <p class="text-white text-xl md:text-2xl font-light leading-relaxed mb-6 italic text-center">"The secret of political bargaining is to look more strong than what you really are."</p>
          <div class="flex items-center gap-3 justify-center">
            <div class="w-8 h-8 rounded-full bg-netaji-500/20 flex items-center justify-center">
              <iconify-icon icon="solar:chat-round-dots-bold" width="16" class="text-netaji-400"></iconify-icon>
            </div>
            <div class="text-xs text-slate-400">Political strategy</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Portrait Gallery - Only Netaji's Real Photos -->
  <section class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-b from-slate-950 via-slate-900/30 to-slate-950"></div>
    <div class="relative z-10 max-w-7xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:gallery-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">Archival Photographs</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">Faces of <span class="text-netaji-400 font-medium">Courage</span></h2>
        <p class="text-slate-400 text-lg max-w-2xl mx-auto font-light">Authentic photographs from the life of Netaji Subhas Chandra Bose — from public domain archives.</p>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
        <!-- Photo 1 - Congress President era -->
        <div class="reveal relative rounded-2xl overflow-hidden group cursor-pointer">
          <img src="https://upload.wikimedia.org/wikipedia/commons/e/e5/Subhas_Chandra_Bose_1938.jpg" alt="Netaji as Congress President, 1938" class="w-full h-64 md:h-72 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-5 left-5 right-5">
            <div class="text-netaji-400 text-[10px] font-semibold tracking-widest uppercase mb-1">1938</div>
            <div class="text-white text-sm font-medium">Congress President Era</div>
          </div>
        </div>

        <!-- Photo 2 - WWII Period -->
        <div class="reveal relative rounded-2xl overflow-hidden group cursor-pointer">
          <img src="https://upload.wikimedia.org/wikipedia/commons/1/1a/Subhas_Chandra_Bose_During_WWII.jpg" alt="Netaji during WWII" class="w-full h-64 md:h-72 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-5 left-5 right-5">
            <div class="text-netaji-400 text-[10px] font-semibold tracking-widest uppercase mb-1">1943</div>
            <div class="text-white text-sm font-medium">World War II Period</div>
          </div>
        </div>

        <!-- Photo 3 - Classic Portrait -->
        <div class="reveal relative rounded-2xl overflow-hidden group cursor-pointer">
          <img src="https://upload.wikimedia.org/wikipedia/commons/7/7a/Subhas_Chandra_Bose_NRB.jpg" alt="Classic portrait of Netaji" class="w-full h-64 md:h-72 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-5 left-5 right-5">
            <div class="text-netaji-400 text-[10px] font-semibold tracking-widest uppercase mb-1">Iconic</div>
            <div class="text-white text-sm font-medium">The Classic Portrait</div>
          </div>
        </div>

        <!-- Photo 4 - With Mahatma Gandhi -->
        <div class="reveal col-span-2 relative rounded-2xl overflow-hidden group cursor-pointer">
          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0c/Subhas_Chandra_Bose_with_Mahatma_Gandhi_in_1938.jpg/1280px-Subhas_Chandra_Bose_with_Mahatma_Gandhi_in_1938.jpg" alt="Netaji with Mahatma Gandhi, 1938" class="w-full h-64 md:h-72 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-5 left-5 right-5">
            <div class="text-netaji-400 text-[10px] font-semibold tracking-widest uppercase mb-1">1938 • Historic Meeting</div>
            <div class="text-white text-sm font-medium">Netaji with Mahatma Gandhi at the Haripura Congress Session</div>
          </div>
        </div>

        <!-- Photo 5 - In uniform -->
        <div class="reveal relative rounded-2xl overflow-hidden group cursor-pointer">
          <img src="https://upload.wikimedia.org/wikipedia/commons/5/5f/Subhas_Chandra_Bose_in_Uniform.jpg" alt="Netaji in INA uniform" class="w-full h-64 md:h-72 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
          <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/20 to-transparent"></div>
          <div class="absolute bottom-5 left-5 right-5">
            <div class="text-netaji-400 text-[10px] font-semibold tracking-widest uppercase mb-1">INA Commander</div>
            <div class="text-white text-sm font-medium">Netaji in Uniform</div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Legacy Section -->
  <section id="legacy" class="relative py-24 overflow-hidden">
    <div class="absolute inset-0 bg-grid opacity-20"></div>
    <div class="absolute inset-0 hero-glow opacity-50"></div>
    <div class="relative z-10 max-w-7xl mx-auto px-6">
      <div class="reveal text-center mb-16">
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-netaji-500/10 border border-netaji-500/20 mb-6">
          <iconify-icon icon="solar:star-shine-bold" width="16" class="text-netaji-400"></iconify-icon>
          <span class="text-xs font-semibold tracking-widest uppercase text-netaji-400">Everlasting Impact</span>
        </div>
        <h2 class="font-dm text-4xl md:text-5xl font-light tracking-tight text-white mb-4">The <span class="text-netaji-400 font-medium">Living Legacy</span></h2>
        <p class="text-slate-400 text-lg max-w-2xl mx-auto font-light">Netaji's impact transcends his mortal life — he lives in every Indian's heart as the ultimate symbol of courage and sacrifice.</p>
      </div>

      <div class="grid md:grid-cols-2 gap-8 items-start">
        <div class="reveal space-y-6">
          <div class="flex gap-5 p-6 rounded-2xl bg-white/[0.03] border border-white/5 hover:border-netaji-500/20 transition-all duration-300">
            <div class="w-12 h-12 rounded-xl bg-netaji-500/10 flex items-center justify-center flex-shrink-0">
              <iconify-icon icon="solar:landmark-bold" width="24" class="text-netaji-400"></iconify-icon>
            </div>
            <div>
              <h3 class="text-white font-medium text-lg mb-2">Netaji Subhas Chandra Bose International Airport</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Kolkata's international airport bears his name — a fitting tribute to the son of Bengal who dreamed of a free India.</p>
            </div>
          </div>

          <div class="flex gap-5 p-6 rounded-2xl bg-white/[0.03] border border-white/5 hover:border-netaji-500/20 transition-all duration-300">
            <div class="w-12 h-12 rounded-xl bg-netaji-500/10 flex items-center justify-center flex-shrink-0">
              <iconify-icon icon="solar:medal-ribbons-star-bold" width="24" class="text-netaji-400"></iconify-icon>
            </div>
            <div>
              <h3 class="text-white font-medium text-lg mb-2">Bharat Ratna (Posthumous, 1992)</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">India's highest civilian award was conferred on him posthumously, though it was later controversially withdrawn due to legal reasons regarding the absence of proof of death.</p>
            </div>
          </div>

          <div class="flex gap-5 p-6 rounded-2xl bg-white/[0.03] border border-white/5 hover:border-netaji-500/20 transition-all duration-300">
            <div class="w-12 h-12 rounded-xl bg-netaji-500/10 flex items-center justify-center flex-shrink-0">
              <iconify-icon icon="solar:calendar-bold" width="24" class="text-netaji-400"></iconify-icon>
            </div>
            <div>
              <h3 class="text-white font-medium text-lg mb-2">Parakram Diwas — January 23</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Netaji's birthday is celebrated as Parakram Diwas (Day of Valor) across India, honoring his extraordinary courage and contribution to the freedom struggle.</p>
            </div>
          </div>

          <div class="flex gap-5 p-6 rounded-2xl bg-white/[0.03] border border-white/5 hover:border-netaji-500/20 transition-all duration-300">
            <div class="w-12 h-12 rounded-xl bg-netaji-500/10 flex items-center justify-center flex-shrink-0">
              <iconify-icon icon="solar:island-bold" width="24" class="text-netaji-400"></iconify-icon>
            </div>
            <div>
              <h3 class="text-white font-medium text-lg mb-2">Netaji Subhas Chandra Bose Island</h3>
              <p class="text-slate-400 text-sm font-light leading-relaxed">Ross Island in the Andamans was renamed in his honor in 2018 — the very islands where he hoisted the tricolor in 1943 as head of the Azad Hind government.</p>
            </div>
          </div>
        </div>

        <div class="reveal space-y-6">
          <!-- Netaji Statue Image -->
          <div class="relative rounded-2xl overflow-hidden group">
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Subhas_Chandra_Bose_in_Uniform.jpg/800px-Subhas_Chandra_Bose_in_Uniform.jpg" alt="Netaji in INA Uniform - The Supreme Commander" class="w-full h-64 lg:h-80 object-cover object-top netaji-img transition-transform duration-700 group-hover:scale-105">
            <div class="absolute inset-0 bg-gradient-to-t from-slate-950/90 via-slate-950/30 to-transparent"></div>
            <div class="absolute bottom-6 left-6 right-6">
              <div class="text-netaji-400 text-xs font-semibold tracking-widest uppercase mb-2">Supreme Commander</div>
              <div class="text-white font-medium">Netaji in his iconic INA uniform</div>
            </div>
          </div>

          <div class="relative p-8 rounded-2xl overflow-hidden" style="background: linear-gradient(135deg, rgba(34,197,94,0.15), rgba(34,197,94,0.03));">
            <div class="absolute top-0 right-0 w-32 h-32 bg-netaji-500/10 rounded-full blur-2xl"></div>
            <div class="relative z-10">
              <iconify-icon icon="solar:hand-shake-bold" width="36" class="text-netaji-400 mb-4"></iconify-icon>
              <h3 class="text-white font-dm text-2xl font-medium mb-3">"Jai Hind!"</h3>
              <p class="text-slate-300 text-sm font-light leading-relaxed mb-6">These two words — "Jai Hind" — given to the nation by Netaji, became the rallying cry of India's freedom movement and remains our national salute to this day.</p>
              <div class="flex items-center gap-2">
                <div class="w-2 h-2 rounded-full bg-netaji-400 animate-pulse"></div>
                <span class="text-netaji-300 text-xs font-medium">His spirit lives on in 1.4 billion hearts</span>
              </div>
            </div>
          </div>

          <div class="p-6 rounded-2xl bg-white/[0.03] border border-white/5">
            <div class="flex items-center gap-3 mb-4">
              <div class="w-10 h-10 rounded-xl bg-red-500/10 flex items-center justify-center">
                <iconify-icon icon="solar:question-circle-bold" width="22" class="text-red-400"></iconify-icon>
              </div>
              <div>
                <h3 class="text-white font-medium">The Unresolved Mystery</h3>
                <div class="text-xs text-slate-500">Multiple commissions, no answers</div>
              </div>
            </div>
            <p class="text-slate-400 text-sm font-light leading-relaxed">Three government commissions (Shah Nawaz, Khosla, Mukherjee) have investigated Netaji's disappearance. The Mukherjee Commission (2006) concluded he did not die in the 1945 plane crash, yet the mystery endures — making it India's greatest historical enigma.</p>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- INA Motto Banner -->
  <section class="relative py-20 overflow-hidden">
    <div class="absolute inset-0" style="background: linear-gradient(135deg, rgba(34,197,94,0.08), rgba(34,197,94,0.02));"></div>
    <div class="absolute inset-0 bg-grid opacity-10"></div>
    <div class="relative z-10 max-w-4xl mx-auto px-6 text-center">
      <div class="reveal">
        <div class="text-netaji-500/30 text-8xl md:text-9xl font-dm font-bold mb-4" style="line-height: 1;">इत्तेफ़ाक़</div>
        <div class="flex flex-col md:flex-row items-center justify-center gap-6 md:gap-12 mb-8">
          <div class="text-center">
            <div class="text-white font-dm text-3xl md:text-4xl font-light">Ittefaq</div>
            <div class="text-netaji-400 text-sm">Unity</div>
          </div>
          <div class="w-px h-12 bg-netaji-500/30 hidden md:block"></div>
          <div class="text-center">
            <div class="text-white font-dm text-3xl md:text-4xl font-light">Itmad</div>
            <div class="text-netaji-400 text-sm">Faith</div>
          </div>
          <div class="w-px h-12 bg-netaji-500/30 hidden md:block"></div>
          <div class="text-center">
            <div class="text-white font-dm text-3xl md:text-4xl font-light">Qurbani</div>
            <div class="text-netaji-400 text-sm">Sacrifice</div>
          </div>
        </div>
        <p class="text-slate-400 text-sm font-light max-w-xl mx-auto">The immortal motto of the Indian National Army — three words that encapsulated the spirit of an entire generation fighting for freedom.</p>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="relative py-16 overflow-hidden">
    <div class="absolute inset-0 bg-gradient-to-b from-transparent via-slate-900/50 to-slate-950"></div>
    <div class="absolute top-0 left-0 right-0 h-px bg-gradient-to-r from-transparent via-white/10 to-transparent"></div>
    <div class="relative z-10 max-w-7xl mx-auto px-6">
      <div class="grid md:grid-cols-3 gap-12 mb-12">
        <div>
          <div class="flex items-center gap-3 mb-4">
            <div class="w-10 h-10 rounded-xl bg-netaji-500/10 flex items-center justify-center">
              <iconify-icon icon="solar:star-bold" width="20" class="text-netaji-400"></iconify-icon>
            </div>
            <div>
              <div class="text-white font-dm text-lg font-medium">Netaji</div>
              <div class="text-slate-500 text-xs">1897 — Forever</div>
            </div>
          </div>
          <p class="text-slate-400 text-sm font-light leading-relaxed">A tribute website dedicated to the life, legacy, and immortal spirit of Netaji Subhas Chandra Bose — the warrior who taught India to fight for its freedom.</p>
        </div>

        <div>
          <h4 class="text-white font-medium text-sm mb-4 tracking-wider uppercase">Explore</h4>
          <div class="space-y-3">
            <a href="#about" class="block text-slate-400 text-sm hover:text-netaji-400 transition-colors">Early Life & Education</a>
            <a href="#timeline" class="block text-slate-400 text-sm hover:text-netaji-400 transition-colors">Complete Timeline</a>
            <a href="#ina" class="block text-slate-400 text-sm hover:text-netaji-400 transition-colors">Indian National Army</a>
            <a href="#quotes" class="block text-slate-400 text-sm hover:text-netaji-400 transition-colors">Famous Quotes</a>
            <a href="#legacy" class="block text-slate-400 text-sm hover:text-netaji-400 transition-colors">Legacy & Memorials</a>
          </div>
        </div>

        <div>
          <h4 class="text-white font-medium text-sm mb-4 tracking-wider uppercase">References</h4>
          <div class="space-y-3">
            <div class="text-slate-400 text-sm font-light">"The Indian Struggle" — Netaji</div>
            <div class="text-slate-400 text-sm font-light">"Netaji: The Forgotten Hero" — Film</div>
            <div class="text-slate-400 text-sm font-light">Netaji Research Bureau, Kolkata</div>
            <div class="text-slate-400 text-sm font-light">Ministry of Culture, Govt. of India</div>
            <div class="text-slate-400 text-sm font-light">National Archives of India</div>
          </div>
        </div>
      </div>

      <div class="pt-8 border-t border-white/5 flex flex-col md:flex-row items-center justify-between gap-4">
        <div class="text-slate-500 text-xs font-light">
          Tribute website. All photographs sourced from Wikimedia Commons (public domain). Content is for educational and inspirational purposes.
        </div>
        <div class="flex items-center gap-1 text-slate-500 text-xs">
          <span>Made with</span>
          <iconify-icon icon="solar:heart-bold" width="14" class="text-netaji-400"></iconify-icon>
          <span>for Bharat</span>
          <span class="mx-2">•</span>
          <span class="text-netaji-400 font-medium">जय हिंद</span>
        </div>
      </div>
    </div>
  </footer>

  <!-- Back to Top -->
  <button id="backToTop" class="fixed bottom-8 right-8 z-50 w-12 h-12 rounded-full bg-netaji-500 text-white flex items-center justify-center shadow-lg shadow-green-500/20 opacity-0 translate-y-4 transition-all duration-300 hover:bg-netaji-400" style="pointer-events: none;">
    <iconify-icon icon="solar:arrow-up-linear" width="22"></iconify-icon>
  </button>

  <!-- Toast -->
  <div id="toast" class="fixed bottom-8 left-8 z-50 px-6 py-3 rounded-full bg-slate-900 border border-netaji-500/20 text-netaji-300 text-sm font-medium shadow-xl opacity-0 translate-y-4 transition-all duration-300" style="pointer-events: none;">
    <iconify-icon icon="solar:hand-shake-bold" width="16" class="mr-2"></iconify-icon>
    <span id="toastMsg">Jai Hind!</span>
  </div>

  <script>
    const revealElements = document.querySelectorAll('.reveal');
    const revealObserver = new IntersectionObserver((entries) => {
      entries.forEach((entry, index) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            entry.target.classList.add('active');
          }, index * 80);
          revealObserver.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -50px 0px' });
    revealElements.forEach(el => revealObserver.observe(el));

    const sections = document.querySelectorAll('section[id]');
    const navLinks = document.querySelectorAll('.nav-link');

    window.addEventListener('scroll', () => {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop - 120;
        if (window.scrollY >= sectionTop) {
          current = section.getAttribute('id');
        }
      });

      navLinks.forEach(link => {
        link.classList.remove('active', 'text-netaji-400');
        link.classList.add('text-slate-400');
        if (link.getAttribute('href') === '#' + current) {
          link.classList.add('active', 'text-netaji-400');
          link.classList.remove('text-slate-400');
        }
      });

      const backToTop = document.getElementById('backToTop');
      if (window.scrollY > 600) {
        backToTop.style.opacity = '1';
        backToTop.style.transform = 'translateY(0)';
        backToTop.style.pointerEvents = 'auto';
      } else {
        backToTop.style.opacity = '0';
        backToTop.style.transform = 'translateY(16px)';
        backToTop.style.pointerEvents = 'none';
      }
    });

    document.getElementById('backToTop').addEventListener('click', () => {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    });

    function showToast(msg) {
      const toast = document.getElementById('toast');
      const toastMsg = document.getElementById('toastMsg');
      toastMsg.textContent = msg;
      toast.style.opacity = '1';
      toast.style.transform = 'translateY(0)';
      toast.style.pointerEvents = 'auto';
      setTimeout(() => {
        toast.style.opacity = '0';
        toast.style.transform = 'translateY(16px)';
        toast.style.pointerEvents = 'none';
      }, 3000);
    }

    setTimeout(() => {
      showToast('जय हिंद — Welcome to Netaji\'s Legacy');
    }, 2000);

    window.addEventListener('scroll', () => {
      const scrolled = window.scrollY;
      const hero = document.getElementById('hero');
      if (hero && scrolled < window.innerHeight) {
        const heroContent = hero.querySelector('.relative.z-10');
        if (heroContent) {
          heroContent.style.transform = `translateY(${scrolled * 0.15}px)`;
          heroContent.style.opacity = 1 - (scrolled / (window.innerHeight * 0.8));
        }
      }
    });

    document.querySelectorAll('.quote-card').forEach(card => {
      card.addEventListener('click', () => {
        const quote = card.querySelector('p').textContent.replace(/"/g, '');
        showToast(quote);
      });
    });
  </script>
</body>
</html>
