<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>DailyFunChallenges • Build habits you actually enjoy</title>
  <meta name="description" content="DailyFunChallenges blends daily and mini challenges, a progress-driven avatar, streaks, leaderboards, and rich insights to make personal growth fun." />
  <meta property="og:title" content="DailyFunChallenges" />
  <meta property="og:description" content="Gamified habits • Daily & mini challenges • Avatar • Leaderboards" />
  <meta property="og:type" content="website" />
  <meta name="theme-color" content="#0f172a" />
  <link rel="preconnect" href="https://fonts.googleapis.com"/>
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet"/>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'system-ui', 'ui-sans-serif', 'Segoe UI', 'Roboto', 'Helvetica', 'Arial', 'Apple Color Emoji', 'Segoe UI Emoji'],
            mono: ['JetBrains Mono','ui-monospace','SFMono-Regular','Menlo','Monaco','Consolas','Liberation Mono','monospace']
          },
          colors: {
            brand: {
              50: '#eefdfc',
              100: '#defaf6',
              200: '#b8f2ea',
              300: '#86e6d9',
              400: '#4cd2c2',
              500: '#1eb5a5',
              600: '#158f84',
              700: '#136f66',
              800: '#125a53',
              900: '#104a45'
            }
          },
          boxShadow: {
            soft: '0 12px 40px rgba(2,6,23,0.10)',
            glow: '0 10px 30px rgba(30,181,165,0.35)'
          },
          keyframes: {
            floaty: { '0%,100%': { transform: 'translateY(0)' }, '50%': { transform: 'translateY(-6px)' } },
            shimmer: {
              '0%': { backgroundPosition: '200% 0' },
              '100%': { backgroundPosition: '-200% 0' }
            }
          },
          animation: {
            floaty: 'floaty 5s ease-in-out infinite',
            shimmer: 'shimmer 6s linear infinite'
          }
        }
      }
    }
  </script>
  <style>
    :root { --ink:#0f172a; --ink-2:#1f2937; --ring:#1eb5a5; }
    html { scroll-behavior:smooth; }
    body { font-feature-settings: 'cv02','cv03','cv04','cv11'; }
    .glass { backdrop-filter: blur(10px); background: rgba(255,255,255,.65); }
    .dark .glass { background: rgba(2,6,23,.55); }
    .grad { background: linear-gradient(120deg, #fb7185 0%, #fbbf24 25%, #34d399 55%, #22d3ee 85%); }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 dark:bg-slate-950 dark:text-slate-200">
  <!-- Top Notice -->
  <div class="w-full grad bg-[length:300%_100%] animate-shimmer text-center text-slate-900 dark:text-slate-900">
    <div class="max-w-7xl mx-auto px-4 py-2 text-sm font-semibold">Beta preview — feedback welcome ✨</div>
  </div>

  <!-- NAV -->
  <header class="sticky top-0 z-50 border-b border-slate-200/70 dark:border-slate-800/80 backdrop-blur">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-3 flex items-center gap-4">
      <a href="#" class="flex items-center gap-3 group">
        <!-- Logo (target + arrow) -->
        <svg width="34" height="34" viewBox="0 0 160 160" xmlns="http://www.w3.org/2000/svg" class="drop-shadow" aria-hidden="true">
          <circle cx="80" cy="80" r="72" fill="#fde68a" stroke="#0f172a" stroke-width="10"/>
          <circle cx="80" cy="80" r="48" fill="#fca5a5" stroke="#0f172a" stroke-width="10"/>
          <circle cx="80" cy="80" r="24" fill="#86efac" stroke="#0f172a" stroke-width="10"/>
          <path d="M80 80 L132 28" stroke="#0f172a" stroke-width="14" stroke-linecap="round"/>
          <path d="M132 28 l-2 28 28-2z" fill="#0f172a"/>
        </svg>
        <span class="font-extrabold tracking-tight text-slate-900 dark:text-white">DailyFunChallenges</span>
      </a>
      <nav class="ml-auto hidden md:flex items-center gap-6 text-sm">
        <a href="#features" class="hover:text-brand-600">Features</a>
        <a href="#preview" class="hover:text-brand-600">Preview</a>
        <a href="#docs" class="hover:text-brand-600">Docs</a>
        <a href="#roadmap" class="hover:text-brand-600">Roadmap</a>
        <a href="#pricing" class="hover:text-brand-600">Pricing</a>
        <a href="#contact" class="hover:text-brand-600">Contact</a>
        <button id="themeBtn" class="rounded-xl px-3 py-1.5 ring-1 ring-slate-300 dark:ring-slate-700">🌙</button>
      </nav>
      <button class="ml-auto md:hidden rounded-xl px-3 py-1.5 ring-1 ring-slate-300" id="menuBtn">Menu</button>
    </div>
    <div id="mobileMenu" class="hidden md:hidden border-t border-slate-200 dark:border-slate-800">
      <div class="px-4 py-3 flex flex-wrap gap-3 text-sm">
        <a href="#features" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Features</a>
        <a href="#preview" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Preview</a>
        <a href="#docs" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Docs</a>
        <a href="#roadmap" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Roadmap</a>
        <a href="#pricing" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Pricing</a>
        <a href="#contact" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Contact</a>
        <button id="themeBtn2" class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Toggle Theme</button>
      </div>
    </div>
  </header>

  <!-- HERO -->
  <section class="relative">
    <div class="absolute inset-0 -z-10 grad opacity-30 dark:opacity-25"></div>
    <div class="max-w-7xl mx-auto px-4 sm:px-6 py-16 md:py-24 grid lg:grid-cols-2 gap-12 items-center">
      <div>
        <p class="inline-flex items-center gap-2 text-xs font-semibold uppercase tracking-wide text-brand-700 bg-brand-50 dark:bg-brand-900/30 ring-1 ring-brand-200 dark:ring-brand-800 px-3 py-1 rounded-full">Gamified Habits</p>
        <h1 class="mt-4 text-4xl sm:text-5xl font-extrabold leading-tight text-slate-900 dark:text-white">Build habits you <span class="text-brand-600">actually</span> enjoy.</h1>
        <p class="mt-4 text-slate-600 dark:text-slate-300 text-lg">Daily & mini challenges, a Sim‑style avatar that grows with you, streaks, leaderboards, and rich insights. Designed for delight and consistency.</p>
        <div class="mt-6 flex flex-wrap gap-3">
          <a class="px-5 py-3 rounded-2xl bg-slate-900 text-white hover:bg-slate-800 shadow-soft" href="#download">Download (soon)</a>
          <a class="px-5 py-3 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 hover:bg-slate-50 dark:hover:bg-slate-800 shadow-soft" href="#preview">See Preview</a>
          <a class="px-5 py-3 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 hover:bg-slate-50 dark:hover:bg-slate-800 shadow-soft" href="#docs">Developer Docs</a>
        </div>
        <div class="mt-6 text-sm text-slate-500 dark:text-slate-400">Free to try • No ads • Privacy‑first</div>
      </div>
      <div class="relative">
        <div class="rounded-3xl glass ring-1 ring-slate-200/70 dark:ring-slate-800/70 shadow-soft p-6">
          <div class="flex items-center justify-between">
            <div class="font-semibold">Today’s Challenges</div>
            <span class="text-xs px-2 py-1 rounded-full bg-brand-100 text-brand-900 dark:bg-brand-900/30 dark:text-brand-200">Live</span>
          </div>
          <ul class="mt-4 space-y-3">
            <li class="p-3 rounded-2xl bg-white/70 dark:bg-slate-900/60 ring-1 ring-slate-200 dark:ring-slate-800 flex items-center justify-between">
              <div>
                <div class="font-medium">10‑minute stretch</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Fitness • Medium • +20 XP</div>
              </div>
              <button class="text-brand-700 dark:text-brand-400 text-sm font-semibold">Skip → Replace</button>
            </li>
            <li class="p-3 rounded-2xl bg-white/70 dark:bg-slate-900/60 ring-1 ring-slate-200 dark:ring-slate-800 flex items-center justify-between">
              <div>
                <div class="font-medium">Box‑breathing 4×4</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Mindfulness • Easy • +15 XP</div>
              </div>
              <button class="text-brand-700 dark:text-brand-400 text-sm font-semibold">Complete ✓</button>
            </li>
            <li class="p-3 rounded-2xl bg-white/70 dark:bg-slate-900/60 ring-1 ring-slate-200 dark:ring-slate-800 flex items-center justify-between">
              <div>
                <div class="font-medium">Read 3 pages</div>
                <div class="text-xs text-slate-500 dark:text-slate-400">Learning • Easy • +10 XP</div>
              </div>
              <button class="text-brand-700 dark:text-brand-400 text-sm font-semibold">Complete ✓</button>
            </li>
          </ul>
          <div class="mt-6 grid grid-cols-3 gap-3 text-center">
            <div class="p-3 rounded-2xl bg-brand-50 dark:bg-brand-900/20 ring-1 ring-brand-200 dark:ring-brand-800">
              <div class="text-xs text-brand-800 dark:text-brand-200">Streak</div>
              <div class="text-2xl font-extrabold text-brand-900 dark:text-brand-100">7</div>
            </div>
            <div class="p-3 rounded-2xl bg-white/70 dark:bg-slate-900/60 ring-1 ring-slate-200 dark:ring-slate-800">
              <div class="text-xs text-slate-500 dark:text-slate-400">Level</div>
              <div class="text-2xl font-extrabold">4</div>
            </div>
            <div class="p-3 rounded-2xl bg-white/70 dark:bg-slate-900/60 ring-1 ring-slate-200 dark:ring-slate-800">
              <div class="text-xs text-slate-500 dark:text-slate-400">XP</div>
              <div class="text-2xl font-extrabold">840</div>
            </div>
          </div>
        </div>
        <div class="absolute -right-6 -bottom-6 hidden md:block">
          <div class="w-40 h-40 rounded-full grad opacity-60 blur-2xl animate-floaty"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- TRUST / SOCIAL PROOF -->
  <section class="py-8 md:py-12 border-t border-slate-200/70 dark:border-slate-800/70">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="grid md:grid-cols-4 gap-6">
        <div class="p-4 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 text-center">
          <div class="text-2xl font-extrabold">10k+</div><div class="text-xs text-slate-500">Daily completions</div>
        </div>
        <div class="p-4 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 text-center">
          <div class="text-2xl font-extrabold">4.9★</div><div class="text-xs text-slate-500">Early testers</div>
        </div>
        <div class="p-4 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 text-center">
          <div class="text-2xl font-extrabold">98%</div><div class="text-xs text-slate-500">Report better habits</div>
        </div>
        <div class="p-4 rounded-2xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 text-center">
          <div class="text-2xl font-extrabold">#1</div><div class="text-xs text-slate-500">In friend groups 😉</div>
        </div>
      </div>
    </div>
  </section>

  <!-- FEATURES GRID -->
  <section id="features" class="py-16 md:py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <h2 class="text-3xl md:text-4xl font-extrabold">What’s inside</h2>
      <p class="mt-2 text-slate-600 dark:text-slate-300">Built for delight, designed for consistency.</p>
      <div class="mt-10 grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">📅</div>
          <h3 class="mt-3 font-semibold text-lg">Daily Challenges</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">3 curated tasks per day by category & difficulty. Skip instantly replaces—no empty slots.</p>
        </article>
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">⚡</div>
          <h3 class="mt-3 font-semibold text-lg">Mini Challenges</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">5‑minute bursts to keep momentum when time is tight. Earn XP and keep the streak.</p>
        </article>
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">📈</div>
          <h3 class="mt-3 font-semibold text-lg">Progress Tracking</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">View completed & skipped, XP to next level, streaks, and per‑category insights.</p>
        </article>
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">🧩</div>
          <h3 class="mt-3 font-semibold text-lg">Avatar Attributes</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">Your avatar upgrades visually as each category develops—like leveling a Sim.</p>
        </article>
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">🎉</div>
          <h3 class="mt-3 font-semibold text-lg">Gamification</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">XP, levels, streaks, celebrations, and a gentle leveling curve keep momentum.</p>
        </article>
        <article class="p-6 rounded-3xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <div class="text-2xl">🏆</div>
          <h3 class="mt-3 font-semibold text-lg">Leaderboards</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">Friends & Global modes with top‑100 view to spark friendly competition.</p>
        </article>
      </div>
    </div>
  </section>

  <!-- PREVIEW TABS -->
  <section id="preview" class="py-16 md:py-20 bg-slate-50 dark:bg-slate-900/30">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="flex items-center justify-between">
        <h2 class="text-3xl md:text-4xl font-extrabold">Product Preview</h2>
        <div class="flex items-center gap-2 text-xs">
          <button class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800" data-tab="dash">Dashboard</button>
          <button class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800" data-tab="progress">Progress</button>
          <button class="px-3 py-1.5 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800" data-tab="avatar">Avatar</button>
        </div>
      </div>
      <div class="mt-8 grid md:grid-cols-3 gap-6" id="tabPanels">
        <div data-panel="dash" class="rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft p-4">
          <div class="h-[460px] rounded-2xl bg-gradient-to-br from-amber-200 via-rose-200 to-emerald-200 dark:from-amber-300/20 dark:via-rose-300/20 dark:to-emerald-300/20 flex items-center justify-center text-slate-800 dark:text-slate-200 font-semibold">Dashboard</div>
        </div>
        <div data-panel="progress" class="hidden rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft p-4">
          <div class="h-[460px] rounded-2xl bg-gradient-to-br from-emerald-200 via-cyan-200 to-indigo-200 dark:from-emerald-300/20 dark:via-cyan-300/20 dark:to-indigo-300/20 flex items-center justify-center text-slate-800 dark:text-slate-200 font-semibold">Progress</div>
        </div>
        <div data-panel="avatar" class="hidden rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft p-4">
          <div class="h-[460px] rounded-2xl bg-gradient-to-br from-violet-200 via-fuchsia-200 to-amber-200 dark:from-violet-300/20 dark:via-fuchsia-300/20 dark:to-amber-300/20 flex items-center justify-center text-slate-800 dark:text-slate-200 font-semibold">Avatar</div>
        </div>
      </div>
      <p class="mt-4 text-sm text-slate-500 dark:text-slate-400">Tip: replace placeholders with real screenshots before launch.</p>
    </div>
  </section>

  <!-- DOCS / API-like SPEC -->
  <section id="docs" class="py-16 md:py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 grid lg:grid-cols-3 gap-10 items-start">
      <div>
        <h2 class="text-3xl md:text-4xl font-extrabold">Developer Docs</h2>
        <p class="mt-2 text-slate-600 dark:text-slate-300">Integrate, extend, and contribute. Lightweight by design.</p>
        <ul class="mt-6 space-y-2 text-sm">
          <li><a href="#" class="underline underline-offset-4">Getting Started</a></li>
          <li><a href="#" class="underline underline-offset-4">Component Library</a></li>
          <li><a href="#" class="underline underline-offset-4">Data Model</a></li>
          <li><a href="#" class="underline underline-offset-4">Theming</a></li>
        </ul>
      </div>
      <div class="lg:col-span-2 space-y-6">
        <div class="rounded-2xl bg-slate-900 text-slate-100 p-5 font-mono text-xs leading-relaxed overflow-auto ring-1 ring-slate-800">
<pre>// Challenge schema (TypeScript)
export type Category =
  | 'fitness' | 'mindfulness' | 'learning' | 'creativity' | 'productivity'
  | 'finance' | 'social' | 'adventure' | 'digital_detox' | 'self_care'
  | 'communication' | 'cooking' | 'home';

export interface Challenge {
  id: string;
  title: string;
  category: Category;
  difficulty: 'easy' | 'medium' | 'hard';
  isMini?: boolean; // default: false
  xp: number; // XP reward
}

export interface UserStats {
  completed: number;
  skipped: number;
  streak: number;
  xp: number;
  level: number;
}
</pre>
        </div>
        <div class="rounded-2xl bg-white dark:bg-slate-950 p-5 ring-1 ring-slate-200 dark:ring-slate-800">
          <h3 class="font-semibold">Skip → Replace Logic</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">When a user skips, select a new challenge not present in today’s set and aligned with user prefs.</p>
          <div class="mt-3 rounded-xl bg-slate-900 text-slate-100 p-4 font-mono text-xs overflow-auto ring-1 ring-slate-800">
<pre>// Pseudocode
function skipReplace(today, pool, prefs) {
  const titles = new Set(today.map(c => c.title.toLowerCase()));
  const candidates = pool
    .filter(c => !titles.has(c.title.toLowerCase()))
    .filter(c => prefs.categories.includes(c.category))
    .filter(c => prefs.difficulties.includes(c.difficulty));
  return candidates[Math.floor(Math.random() * candidates.length)];
}
</pre>
          </div>
        </div>
        <div class="rounded-2xl bg-white dark:bg-slate-950 p-5 ring-1 ring-slate-200 dark:ring-slate-800">
          <h3 class="font-semibold">Avatar Attribute Mapping</h3>
          <p class="mt-2 text-sm text-slate-600 dark:text-slate-400">Each category maps to an attribute node; XP flows into its score and updates visuals.</p>
          <ul class="mt-3 grid sm:grid-cols-2 gap-2 text-sm">
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Mindfulness → Head</li>
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Fitness → Body</li>
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Learning → Book icon</li>
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Creativity → Palette</li>
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Self‑Care → Water droplet</li>
            <li class="p-3 rounded-xl ring-1 ring-slate-200 dark:ring-slate-800">Adventure → Compass</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

  <!-- ROADMAP / TIMELINE -->
  <section id="roadmap" class="py-16 md:py-20 bg-slate-50 dark:bg-slate-900/30">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <h2 class="text-3xl md:text-4xl font-extrabold">Roadmap</h2>
      <p class="mt-2 text-slate-600 dark:text-slate-300">Clear milestones from beta to v1.</p>
      <div class="mt-8 relative">
        <div class="absolute left-3 top-0 bottom-0 w-1 bg-slate-200 dark:bg-slate-800 rounded"></div>
        <div class="space-y-6">
          <div class="pl-10 relative">
            <div class="absolute left-0 top-1 w-6 h-6 rounded-full bg-brand-500 shadow-glow"></div>
            <div class="p-5 rounded-2xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800">
              <h3 class="font-semibold">Beta (Now)</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Daily & mini challenges, avatar attributes, leaderboards.</p>
            </div>
          </div>
          <div class="pl-10 relative">
            <div class="absolute left-0 top-1 w-6 h-6 rounded-full bg-amber-500"></div>
            <div class="p-5 rounded-2xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800">
              <h3 class="font-semibold">v0.9</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Theme packs, insights 2.0, shareable moments, privacy audit.</p>
            </div>
          </div>
          <div class="pl-10 relative">
            <div class="absolute left-0 top-1 w-6 h-6 rounded-full bg-emerald-500"></div>
            <div class="p-5 rounded-2xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800">
              <h3 class="font-semibold">v1.0</h3>
              <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Cloud sync, social clubs, global events, iPad layout.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <section id="pricing" class="py-16 md:py-20">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <h2 class="text-3xl md:text-4xl font-extrabold">Pricing</h2>
      <p class="mt-2 text-slate-600 dark:text-slate-300">Fair and simple. Free forever tier.</p>
      <div class="mt-10 grid lg:grid-cols-3 gap-6">
        <div class="p-8 rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <h3 class="text-lg font-bold">Free</h3>
          <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Start your streak.</p>
          <ul class="mt-4 space-y-2 text-sm list-disc list-inside">
            <li>Daily & mini challenges</li>
            <li>Streaks & XP</li>
            <li>Avatar attributes</li>
            <li>Friends leaderboard</li>
          </ul>
          <button class="mt-6 w-full px-4 py-2 rounded-xl bg-slate-900 text-white hover:bg-slate-800">Get Started</button>
        </div>
        <div class="p-8 rounded-3xl bg-white dark:bg-slate-950 ring-2 ring-brand-500 shadow-glow relative">
          <span class="absolute -top-3 right-6 text-xs px-2 py-1 rounded-full bg-brand-500 text-white">Popular</span>
          <h3 class="text-lg font-bold">Pro</h3>
          <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Unlock deep insights.</p>
          <ul class="mt-4 space-y-2 text-sm list-disc list-inside">
            <li>Category analytics 2.0</li>
            <li>Custom themes & icon packs</li>
            <li>Global leaderboard boosts</li>
            <li>Cloud sync & backup</li>
          </ul>
          <button class="mt-6 w-full px-4 py-2 rounded-xl bg-brand-600 text-white hover:bg-brand-700">Upgrade</button>
        </div>
        <div class="p-8 rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <h3 class="text-lg font-bold">Teams</h3>
          <p class="text-sm text-slate-600 dark:text-slate-400 mt-1">Clubs & cohorts.</p>
          <ul class="mt-4 space-y-2 text-sm list-disc list-inside">
            <li>Team challenges & events</li>
            <li>Coach dashboards</li>
            <li>API access</li>
            <li>Priority support</li>
          </ul>
          <button class="mt-6 w-full px-4 py-2 rounded-xl bg-white dark:bg-slate-900 ring-1 ring-slate-200 dark:ring-slate-800">Contact Sales</button>
        </div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <section class="py-16 md:py-20 bg-slate-50 dark:bg-slate-900/30">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <h2 class="text-3xl md:text-4xl font-extrabold">What early users say</h2>
      <div class="mt-8 grid md:grid-cols-3 gap-6">
        <blockquote class="p-6 rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <p>“I open it every morning before coffee. The mini challenges keep my streak alive on busy days.”</p>
          <footer class="mt-3 text-sm text-slate-500">— Alex, student</footer>
        </blockquote>
        <blockquote class="p-6 rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <p>“Seeing my avatar level up was the nudge I needed to stay consistent.”</p>
          <footer class="mt-3 text-sm text-slate-500">— Priya, PM</footer>
        </blockquote>
        <blockquote class="p-6 rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 shadow-soft">
          <p>“Skip → Replace is genius. No more empty dashboards.”</p>
          <footer class="mt-3 text-sm text-slate-500">— Marco, designer</footer>
        </blockquote>
      </div>
    </div>
  </section>

  <!-- FAQ -->
  <section id="faq" class="py-16 md:py-20">
    <div class="max-w-5xl mx-auto px-4 sm:px-6">
      <h2 class="text-3xl md:text-4xl font-extrabold">FAQ</h2>
      <div class="mt-8 divide-y divide-slate-200 dark:divide-slate-800">
        <details class="group py-4">
          <summary class="flex cursor-pointer items-center justify-between font-medium">How do mini challenges work?<span class="group-open:rotate-45 transition">➕</span></summary>
          <p class="mt-3 text-slate-600 dark:text-slate-400">They’re 5‑minute tasks that award smaller XP but keep momentum when you’re short on time.</p>
        </details>
        <details class="group py-4">
          <summary class="flex cursor-pointer items-center justify-between font-medium">What happens if I skip?<span class="group-open:rotate-45 transition">➕</span></summary>
          <p class="mt-3 text-slate-600 dark:text-slate-400">Skipping instantly replaces the challenge with a new one, so your dashboard always stays full.</p>
        </details>
        <details class="group py-4">
          <summary class="flex cursor-pointer items-center justify-between font-medium">Is my data private?<span class="group-open:rotate-45 transition">➕</span></summary>
          <p class="mt-3 text-slate-600 dark:text-slate-400">Yes. We use local storage by default and only sync to cloud if you opt in.</p>
        </details>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact" class="py-16 md:py-20 bg-slate-50 dark:bg-slate-900/30">
    <div class="max-w-7xl mx-auto px-4 sm:px-6">
      <div class="rounded-3xl bg-white dark:bg-slate-950 ring-1 ring-slate-200 dark:ring-slate-800 p-8 shadow-soft grid lg:grid-cols-2 gap-8">
        <div>
          <h2 class="text-3xl font-extrabold">Get in touch</h2>
          <p class="mt-2 text-slate-600 dark:text-slate-400">For partnerships, feedback, or beta access.</p>
        </div>
        <form class="grid grid-cols-1 gap-4" onsubmit="event.preventDefault(); alert('Thanks! We\'ll reach out soon.'); this.reset();">
          <input required placeholder="Your name" class="px-4 py-3 rounded-xl ring-1 ring-slate-300 dark:ring-slate-800 bg-white dark:bg-slate-900"/>
          <input required type="email" placeholder="Email" class="px-4 py-3 rounded-xl ring-1 ring-slate-300 dark:ring-slate-800 bg-white dark:bg-slate-900"/>
          <textarea rows="4" placeholder="Message" class="px-4 py-3 rounded-xl ring-1 ring-slate-300 dark:ring-slate-800 bg-white dark:bg-slate-900"></textarea>
          <button class="px-5 py-3 rounded-2xl bg-slate-900 text-white hover:bg-slate-800 dark:bg-white dark:text-slate-900">Send</button>
        </form>
      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer class="py-10 border-t border-slate-200/70 dark:border-slate-800/70">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 flex flex-col md:flex-row items-center justify-between gap-4 text-sm">
      <div class="flex items-center gap-2">
        <svg width="22" height="22" viewBox="0 0 160 160" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
          <circle cx="80" cy="80" r="72" fill="#fde68a" stroke="#0f172a" stroke-width="10"/>
          <circle cx="80" cy="80" r="48" fill="#fca5a5" stroke="#0f172a" stroke-width="10"/>
          <circle cx="80" cy="80" r="24" fill="#86efac" stroke="#0f172a" stroke-width="10"/>
          <path d="M80 80 L132 28" stroke="#0f172a" stroke-width="14" stroke-linecap="round"/>
          <path d="M132 28 l-2 28 28-2z" fill="#0f172a"/>
        </svg>
        <span>© <span id="year"></span> DailyFunChallenges</span>
      </div>
      <div class="flex items-center gap-4">
        <a class="hover:text-slate-700 dark:hover:text-slate-200" href="#">Privacy</a>
        <a class="hover:text-slate-700 dark:hover:text-slate-200" href="#">Terms</a>
        <a class="hover:text-slate-700 dark:hover:text-slate-200" href="mailto:hello@example.com">Email</a>
      </div>
    </div>
  </footer>

  <!-- SCRIPTS -->
  <script>
    // Theme toggle
    const prefersDark = window.matchMedia('(prefers-color-scheme: dark)').matches;
    const root = document.documentElement;
    const applyTheme = (val) => {
      if(val === 'dark' || (val === 'system' && prefersDark)) {
        root.classList.add('dark');
      } else { root.classList.remove('dark'); }
      localStorage.setItem('theme', val);
    };
    const saved = localStorage.getItem('theme') || 'system';
    applyTheme(saved);
    document.getElementById('themeBtn').onclick = () => applyTheme(root.classList.contains('dark') ? 'light' : 'dark');
    document.getElementById('themeBtn2').onclick = () => applyTheme(root.classList.contains('dark') ? 'light' : 'dark');

    // Mobile menu
    document.getElementById('menuBtn').onclick = () => {
      const m = document.getElementById('mobileMenu');
      m.classList.toggle('hidden');
    };

    // Tabs in preview
    const tabs = document.querySelectorAll('[data-tab]');
    const panels = document.querySelectorAll('[data-panel]');
    tabs.forEach(t => t.addEventListener('click', () => {
      const key = t.getAttribute('data-tab');
      panels.forEach(p => p.classList.toggle('hidden', p.getAttribute('data-panel') !== key));
    }));

    // Year
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
