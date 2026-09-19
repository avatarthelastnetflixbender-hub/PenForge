<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PenForge - Build Your Ultimate Custom Pen</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #f1f5f9; }
        ::-webkit-scrollbar-thumb { background: #cbd5e1; border-radius: 4px; }
        ::-webkit-scrollbar-thumb:hover { background: #94a3b8; }
    </style>
</head>
<body class="bg-slate-50 text-slate-800 font-sans antialiased min-h-screen flex flex-col selection:bg-amber-500 selection:text-white">

    <header class="sticky top-0 z-50 bg-white/90 backdrop-blur-md border-b border-slate-200/80 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            <!-- Logo -->
            <a href="#hero" onclick="window.switchTab('home')" class="flex items-center gap-3 group">
                <div class="w-11 h-11 rounded-2xl bg-gradient-to-tr from-amber-600 via-orange-500 to-amber-400 flex items-center justify-center text-white font-bold text-xl shadow-lg shadow-amber-500/30 group-hover:scale-105 transition-transform">
                    <i class="fa-solid fa-pen-nib"></i>
                </div>
                <div>
                    <span class="text-xl font-extrabold tracking-tight bg-gradient-to-r from-slate-900 to-slate-700 bg-clip-text text-transparent">PenForge</span>
                    <span class="block text-[10px] font-bold uppercase tracking-widest text-amber-600">Custom Engineering Studio</span>
                </div>
            </a>

            <!-- Navigation Tabs -->
            <nav class="hidden md:flex items-center gap-1 bg-slate-100 p-1.5 rounded-2xl border border-slate-200/60">
                <button onclick="window.switchTab('home')" id="nav-home" class="nav-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all bg-white text-slate-900 shadow-sm">
                    <i class="fa-solid fa-house mr-2 text-amber-600"></i>Home
                </button>
                <button onclick="window.switchTab('builder')" id="nav-builder" class="nav-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all text-slate-600 hover:text-slate-900">
                    <i class="fa-solid fa-screwdriver-wrench mr-2 text-amber-600"></i>Pen Builder
                </button>
                <button onclick="window.switchTab('anatomy')" id="nav-anatomy" class="nav-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all text-slate-600 hover:text-slate-900">
                    <i class="fa-solid fa-book-bookmark mr-2 text-amber-600"></i>Pen Anatomy
                </button>
                <button onclick="window.switchTab('catalog')" id="nav-catalog" class="nav-btn px-5 py-2 rounded-xl text-sm font-semibold transition-all text-slate-600 hover:text-slate-900">
                    <i class="fa-solid fa-book-open mr-2 text-amber-600"></i>Part Catalog
                </button>
            </nav>

            <!-- CTA Action -->
            <div class="flex items-center gap-3">
                <button onclick="window.switchTab('builder')" class="px-5 py-2.5 rounded-xl bg-amber-600 text-white font-bold text-sm hover:bg-amber-700 shadow-lg shadow-amber-600/25 transition-all hover:-translate-y-0.5 flex items-center gap-2">
                    <i class="fa-solid fa-wand-magic-sparkles"></i> Build Custom Pen
                </button>
            </div>
        </div>
    </header>

    <main class="flex-grow">

        <section id="view-home" class="view-section">
            <div class="relative pt-20 pb-28 md:pt-32 md:pb-36 overflow-hidden bg-gradient-to-b from-amber-50/60 via-white to-slate-50">
                <div class="absolute top-1/3 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[700px] h-[700px] bg-amber-200/30 rounded-full blur-3xl pointer-events-none -z-10"></div>
                <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-8">
                    <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-amber-100/80 border border-amber-200 text-amber-800 text-xs font-bold uppercase tracking-wider">
                        <i class="fa-solid fa-fire text-amber-600"></i> The Ultimate Pen Customization Studio
                    </div>

                    <h1 class="text-4xl sm:text-6xl lg:text-7xl font-extrabold tracking-tight text-slate-900 max-w-4xl mx-auto leading-[1.1]">
                        Mix, match, and craft your <span class="bg-gradient-to-r from-amber-600 via-orange-500 to-amber-500 bg-clip-text text-transparent">perfect writing instrument.</span>
                    </h1>

                    <p class="text-lg sm:text-xl text-slate-600 max-w-2xl mx-auto font-normal leading-relaxed">
                        Combine fountain nibs, rollerball tips, gel cartridges, ergonomic grips, and exotic barrels to build a custom writing tool that is uniquely yours.
                    </p>

                    <div class="flex flex-col sm:flex-row items-center justify-center gap-4 pt-4">
                        <button onclick="window.switchTab('builder')" class="w-full sm:w-auto px-8 py-4 rounded-2xl bg-amber-600 text-white font-bold text-base hover:bg-amber-700 shadow-xl shadow-amber-600/30 transition-all hover:-translate-y-0.5 flex items-center justify-center gap-3">
                            <i class="fa-solid fa-screwdriver-wrench"></i> Launch Pen Builder
                        </button>
                        <button onclick="window.switchTab('catalog')" class="w-full sm:w-auto px-8 py-4 rounded-2xl bg-white border-2 border-slate-200 text-slate-700 font-bold text-base hover:bg-slate-50 transition-all flex items-center justify-center gap-3">
                            <i class="fa-solid fa-book-open"></i> Browse Part Catalog
                        </button>
                    </div>

                    <!-- Feature Highlights Grid -->
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-6 pt-16 max-w-5xl mx-auto text-left">
                        <div class="p-6 rounded-3xl bg-white border border-slate-200/80 shadow-xl shadow-slate-200/50 space-y-3">
                            <div class="w-12 h-12 rounded-2xl bg-amber-100 text-amber-700 flex items-center justify-center text-xl font-bold">
                                <i class="fa-solid fa-puzzle-piece"></i>
                            </div>
                            <h3 class="font-bold text-slate-900 text-lg">Cross-Brand Compatibility</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">Swap grips, barrels, clips, and tips across legendary design archetypes without friction.</p>
                        </div>

                        <div class="p-6 rounded-3xl bg-white border border-slate-200/80 shadow-xl shadow-slate-200/50 space-y-3">
                            <div class="w-12 h-12 rounded-2xl bg-orange-100 text-orange-700 flex items-center justify-center text-xl font-bold">
                                <i class="fa-solid fa-chart-pie"></i>
                            </div>
                            <h3 class="font-bold text-slate-900 text-lg">Real-Time Stats</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">Instantly calculate total weight, center of balance, grip comfort rating, and ink flow dynamics.</p>
                        </div>

                        <div class="p-6 rounded-3xl bg-white border border-slate-200/80 shadow-xl shadow-slate-200/50 space-y-3">
                            <div class="w-12 h-12 rounded-2xl bg-amber-100 text-amber-700 flex items-center justify-center text-xl font-bold">
                                <i class="fa-solid fa-floppy-disk"></i>
                            </div>
                            <h3 class="font-bold text-slate-900 text-lg">Save & Share Builds</h3>
                            <p class="text-slate-600 text-sm leading-relaxed">Export your custom pen configurations or copy your build specs in one click.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="view-builder" class="view-section hidden py-10 bg-slate-100/60 min-h-[calc(100vh-5rem)]">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                
                <!-- Builder Header -->
                <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8 bg-white p-6 rounded-3xl border border-slate-200/80 shadow-sm">
                    <div>
                        <h2 class="text-2xl font-extrabold text-slate-900">Interactive Pen Forge Studio</h2>
                        <p class="text-slate-500 text-sm">Select tips, grips, barrels, and clips from our expanded library to assemble your ultimate writing tool.</p>
                    </div>
                    <div class="flex items-center gap-3">
                        <button onclick="window.randomizePen()" class="px-4 py-2.5 rounded-xl bg-slate-100 hover:bg-slate-200 text-slate-700 font-bold text-xs transition-colors flex items-center gap-2">
                            <i class="fa-solid fa-shuffle text-amber-600"></i> Randomize Build
                        </button>
                        <button onclick="window.savePenBuild()" class="px-5 py-2.5 rounded-xl bg-amber-600 hover:bg-amber-700 text-white font-bold text-xs transition-colors shadow-lg shadow-amber-600/20 flex items-center gap-2">
                            <i class="fa-solid fa-bookmark"></i> Save Build Specs
                        </button>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
                    
                    <!-- LEFT COLUMN: Live Visual Preview & Stats -->
                    <div class="lg:col-span-5 space-y-6">
                        <!-- Live Visual Pen Preview Card -->
                        <div class="bg-white rounded-3xl p-6 border border-slate-200/80 shadow-xl shadow-slate-200/50 flex flex-col items-center relative overflow-hidden">
                            <div class="absolute top-4 left-4">
                                <span class="px-3 py-1 rounded-full bg-emerald-50 text-emerald-700 text-xs font-bold uppercase tracking-wider border border-emerald-200 flex items-center gap-1.5">
                                    <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span> Live Assembly
                                </span>
                            </div>

                            <!-- Interactive Pen Graphic Render -->
                            <div class="w-full py-12 flex flex-col items-center justify-center my-6 relative min-h-[300px]">
                                <!-- Clip Preview -->
                                <div id="render-clip" class="w-16 h-12 transition-all duration-300 flex items-center justify-center mb-[-10px] z-20"></div>
                                <!-- Nib / Tip Preview -->
                                <div id="render-nib" class="w-16 h-20 transition-all duration-300 flex items-center justify-center z-10"></div>
                                <!-- Grip Preview -->
                                <div id="render-grip" class="w-20 h-16 transition-all duration-300 flex items-center justify-center -mt-1 z-10"></div>
                                <!-- Barrel Preview -->
                                <div id="render-barrel" class="w-24 h-48 transition-all duration-300 flex items-center justify-center -mt-1 rounded-b-3xl shadow-2xl"></div>
                            </div>

                            <div id="display-pen-name" class="text-center font-bold text-slate-800 text-base">
                                Custom Frankpen Build
                            </div>
                            <div id="display-builder-summary" class="text-center text-xs text-slate-500 mt-1">
                                Assembled from 4 distinct models
                            </div>
                        </div>

                        <!-- Live Stats Card -->
                        <div class="bg-white rounded-3xl p-6 border border-slate-200/80 shadow-xl shadow-slate-200/50 space-y-4">
                            <h3 class="font-bold text-slate-900 text-base flex items-center gap-2">
                                <i class="fa-solid fa-chart-column text-amber-600"></i> Ergonomic & Performance Stats
                            </h3>

                            <div class="space-y-3">
                                <div>
                                    <div class="flex justify-between text-xs font-semibold mb-1">
                                        <span class="text-slate-600">Total Weight</span>
                                        <span id="stat-weight-val" class="text-slate-900">32g</span>
                                    </div>
                                    <div class="w-full bg-slate-100 h-2.5 rounded-full overflow-hidden">
                                        <div id="stat-weight-bar" class="bg-amber-600 h-full rounded-full transition-all duration-300" style="width: 50%"></div>
                                    </div>
                                </div>

                                <div>
                                    <div class="flex justify-between text-xs font-semibold mb-1">
                                        <span class="text-slate-600">Grip Ergonomics & Texture</span>
                                        <span id="stat-grip-val" class="text-slate-900">92% (High Comfort)</span>
                                    </div>
                                    <div class="w-full bg-slate-100 h-2.5 rounded-full overflow-hidden">
                                        <div id="stat-grip-bar" class="bg-emerald-500 h-full rounded-full transition-all duration-300" style="width: 90%"></div>
                                    </div>
                                </div>

                                <div>
                                    <div class="flex justify-between text-xs font-semibold mb-1">
                                        <span class="text-slate-600">Ink Flow & Wetness</span>
                                        <span id="stat-flow-val" class="text-slate-900">Ultra Smooth</span>
                                    </div>
                                    <div class="w-full bg-slate-100 h-2.5 rounded-full overflow-hidden">
                                        <div id="stat-flow-bar" class="bg-blue-600 h-full rounded-full transition-all duration-300" style="width: 85%"></div>
                                    </div>
                                </div>

                                <div>
                                    <div class="flex justify-between text-xs font-semibold mb-1">
                                        <span class="text-slate-600">Center of Balance</span>
                                        <span id="stat-balance-val" class="text-slate-900">Perfect Center</span>
                                    </div>
                                    <div class="w-full bg-slate-100 h-2.5 rounded-full overflow-hidden">
                                        <div id="stat-balance-bar" class="bg-violet-600 h-full rounded-full transition-all duration-300" style="width: 95%"></div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- RIGHT COLUMN: Component Selectors -->
                    <div class="lg:col-span-7 space-y-6">
                        <div class="bg-white rounded-3xl p-2 border border-slate-200/80 shadow-sm flex items-center gap-1 overflow-x-auto">
                            <button onclick="window.switchComponentTab('nib')" id="ctab-nib" class="comp-tab-btn flex-1 py-3 px-4 rounded-2xl font-bold text-xs transition-all bg-amber-600 text-white shadow-md shadow-amber-600/20 whitespace-nowrap">
                                <i class="fa-solid fa-pen-nib mr-1.5"></i> 1. Tips & Nibs
                            </button>
                            <button onclick="window.switchComponentTab('grip')" id="ctab-grip" class="comp-tab-btn flex-1 py-3 px-4 rounded-2xl font-bold text-xs transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">
                                <i class="fa-solid fa-hand mr-1.5"></i> 2. Grip Sections
                            </button>
                            <button onclick="window.switchComponentTab('barrel')" id="ctab-barrel" class="comp-tab-btn flex-1 py-3 px-4 rounded-2xl font-bold text-xs transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">
                                <i class="fa-solid fa-cylinder mr-1.5"></i> 3. Barrel Bodies
                            </button>
                            <button onclick="window.switchComponentTab('clip')" id="ctab-clip" class="comp-tab-btn flex-1 py-3 px-4 rounded-2xl font-bold text-xs transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">
                                <i class="fa-solid fa-paperclip mr-1.5"></i> 4. Pocket Clips
                            </button>
                        </div>

                        <div class="bg-white rounded-3xl p-6 border border-slate-200/80 shadow-xl shadow-slate-200/50 space-y-4">
                            <div class="flex items-center justify-between border-b border-slate-100 pb-4">
                                <h3 id="component-list-title" class="font-extrabold text-slate-900 text-lg">Select Tip / Nib Component</h3>
                                <span id="component-count-badge" class="text-xs bg-slate-100 text-slate-600 font-bold px-3 py-1 rounded-full">Options Available</span>
                            </div>

                            <div id="component-options-grid" class="grid grid-cols-1 sm:grid-cols-2 gap-4 max-h-[500px] overflow-y-auto pr-2"></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="view-anatomy" class="view-section hidden py-12 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
                <div class="text-center max-w-3xl mx-auto space-y-4">
                    <h2 class="text-xs font-bold text-amber-600 uppercase tracking-widest bg-amber-50 py-1 px-3 rounded-full inline-block">Educational Breakdown</h2>
                    <h3 class="text-3xl sm:text-4xl font-extrabold text-slate-900 tracking-tight">What Each Part of the Pen Is & Does</h3>
                    <p class="text-slate-600 text-base">Understand the anatomy of a writing instrument so you can make informed choices when building your custom pen.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 pt-4">
                    <!-- Part 1: Nib -->
                    <div class="p-8 rounded-3xl bg-slate-50 border border-slate-200/80 shadow-sm space-y-4 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex items-center justify-between">
                                <div class="w-14 h-14 rounded-2xl bg-amber-100 text-amber-700 flex items-center justify-center text-2xl font-bold">
                                    <i class="fa-solid fa-pen-nib"></i>
                                </div>
                                <span class="px-3 py-1 rounded-full bg-amber-100 text-amber-800 font-bold text-xs">Part 01</span>
                            </div>
                            <h4 class="text-xl font-extrabold text-slate-900">Tips & Nibs</h4>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it is:</strong> The terminal point of the writing instrument that interacts directly with paper—ranging from flexible fountain tines and ceramic rollerballs to precision carbide ballpoints.
                            </p>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it does:</strong> Controls ink delivery rate, line width, and feedback resistance. Different tip materials offer varied bounce, slip resistance, and stroke character.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-slate-200 flex items-center justify-between text-xs text-slate-500 font-semibold">
                            <span>Impact: Line Quality & Feedback</span>
                            <button onclick="window.switchTab('builder'); window.switchComponentTab('nib');" class="text-amber-600 hover:text-amber-700 font-bold flex items-center gap-1">
                                Customize Tips <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>

                    <!-- Part 2: Grip Section -->
                    <div class="p-8 rounded-3xl bg-slate-50 border border-slate-200/80 shadow-sm space-y-4 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex items-center justify-between">
                                <div class="w-14 h-14 rounded-2xl bg-orange-100 text-orange-700 flex items-center justify-center text-2xl font-bold">
                                    <i class="fa-solid fa-hand"></i>
                                </div>
                                <span class="px-3 py-1 rounded-full bg-orange-100 text-orange-800 font-bold text-xs">Part 02</span>
                            </div>
                            <h4 class="text-xl font-extrabold text-slate-900">The Grip Section</h4>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it is:</strong> The contoured or textured sleeve right below the barrel where your fingers pinch and hold the pen during extended writing sessions.
                            </p>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it does:</strong> Provides ergonomic finger comfort, prevents finger fatigue, and absorbs or counters slippery finger oils. Options include knurled brass, soft silicone, and polished resin.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-slate-200 flex items-center justify-between text-xs text-slate-500 font-semibold">
                            <span>Impact: Ergonomics & Fatigue Reduction</span>
                            <button onclick="window.switchTab('builder'); window.switchComponentTab('grip');" class="text-amber-600 hover:text-amber-700 font-bold flex items-center gap-1">
                                Customize Grips <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>

                    <!-- Part 3: Barrel Body -->
                    <div class="p-8 rounded-3xl bg-slate-50 border border-slate-200/80 shadow-sm space-y-4 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex items-center justify-between">
                                <div class="w-14 h-14 rounded-2xl bg-emerald-100 text-emerald-700 flex items-center justify-center text-2xl font-bold">
                                    <i class="fa-solid fa-cylinder"></i>
                                </div>
                                <span class="px-3 py-1 rounded-full bg-emerald-100 text-emerald-800 font-bold text-xs">Part 03</span>
                            </div>
                            <h4 class="text-xl font-extrabold text-slate-900">The Barrel Body</h4>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it is:</strong> The primary cylindrical main shaft of the pen that houses the ink reservoir, converter, or cartridge. It forms the bulk of the pen's physical appearance and weight.
                            </p>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it does:</strong> Determines overall pen weight, balance point, and visual aesthetic. Heavy materials like brass shift balance forward, while aerospace titanium provides lightweight rigidity.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-slate-200 flex items-center justify-between text-xs text-slate-500 font-semibold">
                            <span>Impact: Weight & Center of Balance</span>
                            <button onclick="window.switchTab('builder'); window.switchComponentTab('barrel');" class="text-amber-600 hover:text-amber-700 font-bold flex items-center gap-1">
                                Customize Barrels <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>

                    <!-- Part 4: Pocket Clip -->
                    <div class="p-8 rounded-3xl bg-slate-50 border border-slate-200/80 shadow-sm space-y-4 flex flex-col justify-between">
                        <div class="space-y-4">
                            <div class="flex items-center justify-between">
                                <div class="w-14 h-14 rounded-2xl bg-violet-100 text-violet-700 flex items-center justify-center text-2xl font-bold">
                                    <i class="fa-solid fa-paperclip"></i>
                                </div>
                                <span class="px-3 py-1 rounded-full bg-violet-100 text-violet-800 font-bold text-xs">Part 04</span>
                            </div>
                            <h4 class="text-xl font-extrabold text-slate-900">The Pocket Clip</h4>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it is:</strong> The spring-loaded or rigid metal attachment fixed near the cap/top end of the writing instrument.
                            </p>
                            <p class="text-slate-600 text-sm leading-relaxed">
                                <strong>What it does:</strong> Secures the pen safely to shirt pockets, notebook folios, or pouches to prevent rolling or dropping. Can also be removed entirely for a streamlined clipless feel.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-slate-200 flex items-center justify-between text-xs text-slate-500 font-semibold">
                            <span>Impact: Portability & Retention</span>
                            <button onclick="window.switchTab('builder'); window.switchComponentTab('clip');" class="text-amber-600 hover:text-amber-700 font-bold flex items-center gap-1">
                                Customize Clips <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Call to action banner -->
                <div class="p-8 rounded-3xl bg-gradient-to-r from-amber-600 to-orange-600 text-white flex flex-col md:flex-row items-center justify-between gap-6 shadow-xl">
                    <div class="space-y-2 text-center md:text-left">
                        <h4 class="text-2xl font-extrabold">Ready to assemble your custom pen?</h4>
                        <p class="text-amber-100 text-sm">Mix and match any of these parts across legendary models in our interactive studio.</p>
                    </div>
                    <button onclick="window.switchTab('builder')" class="px-8 py-3.5 rounded-2xl bg-white text-slate-900 font-extrabold text-sm hover:bg-amber-50 shadow-lg transition-all shrink-0">
                        Launch Pen Builder
                    </button>
                </div>
            </div>
        </section>

        <section id="view-catalog" class="view-section hidden py-12 bg-white">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 space-y-12">
                <div class="text-center max-w-3xl mx-auto space-y-4">
                    <h2 class="text-xs font-bold text-amber-600 uppercase tracking-widest bg-amber-50 py-1 px-3 rounded-full inline-block">Complete Inventory</h2>
                    <h3 class="text-3xl sm:text-4xl font-extrabold text-slate-900 tracking-tight">Popular Pens & Component Library</h3>
                    <p class="text-slate-600 text-base">Explore complete pen archetypes and individual modular parts available for your custom builds.</p>
                </div>

                <!-- Complete Models Showcase -->
                <div class="space-y-6">
                    <h4 class="text-xl font-bold text-slate-900 border-b border-slate-100 pb-3 flex items-center gap-2">
                        <i class="fa-solid fa-trophy text-amber-600"></i> Featured Iconic Pen Archetypes
                    </h4>
                    <div id="catalog-models-grid" class="grid grid-cols-1 md:grid-cols-3 gap-6"></div>
                </div>

                <!-- Individual Parts Catalog with Sub-Tabs -->
                <div class="space-y-6 pt-6">
                    <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 border-b border-slate-100 pb-3">
                        <h4 class="text-xl font-bold text-slate-900 flex items-center gap-2">
                            <i class="fa-solid fa-toolbox text-amber-600"></i> All Individual Interchangeable Parts
                        </h4>
                        <!-- Catalog Sub-Tabs -->
                        <div class="flex items-center gap-1.5 bg-slate-100 p-1 rounded-xl overflow-x-auto">
                            <button onclick="window.filterCatalogParts('all')" id="catalog-subtab-all" class="catalog-subtab-btn px-3 py-1.5 rounded-lg text-xs font-bold transition-all bg-amber-600 text-white shadow-sm whitespace-nowrap">All Parts</button>
                            <button onclick="window.filterCatalogParts('nib')" id="catalog-subtab-nib" class="catalog-subtab-btn px-3 py-1.5 rounded-lg text-xs font-bold transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">Tips & Nibs</button>
                            <button onclick="window.filterCatalogParts('grip')" id="catalog-subtab-grip" class="catalog-subtab-btn px-3 py-1.5 rounded-lg text-xs font-bold transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">Grip Sections</button>
                            <button onclick="window.filterCatalogParts('barrel')" id="catalog-subtab-barrel" class="catalog-subtab-btn px-3 py-1.5 rounded-lg text-xs font-bold transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">Barrels</button>
                            <button onclick="window.filterCatalogParts('clip')" id="catalog-subtab-clip" class="catalog-subtab-btn px-3 py-1.5 rounded-lg text-xs font-bold transition-all text-slate-600 hover:text-slate-900 whitespace-nowrap">Clips</button>
                        </div>
                    </div>
                    <div id="catalog-parts-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6"></div>
                </div>
            </div>
        </section>

    </main>

    <!-- Save Modal Popup -->
    <div id="save-modal" class="fixed inset-0 z-50 bg-slate-900/60 backdrop-blur-sm hidden flex items-center justify-center p-4">
        <div class="bg-white rounded-3xl max-w-lg w-full p-8 shadow-2xl space-y-6 relative animate-in fade-in zoom-in duration-200">
            <div class="flex items-center justify-between border-b border-slate-100 pb-4">
                <h3 class="text-xl font-extrabold text-slate-900 flex items-center gap-2">
                    <i class="fa-solid fa-bookmark text-amber-600"></i> Custom Pen Build Specifications
                </h3>
                <button onclick="window.closeModal()" class="w-8 h-8 rounded-full bg-slate-100 hover:bg-slate-200 text-slate-500 flex items-center justify-center font-bold">
                    <i class="fa-solid fa-xmark"></i>
                </button>
            </div>

            <div id="modal-build-details" class="space-y-4 text-sm text-slate-600 bg-slate-50 p-4 rounded-2xl border border-slate-200"></div>

            <div class="flex items-center gap-4">
                <button onclick="window.copyBuildSpecs()" class="flex-1 py-3.5 bg-amber-600 hover:bg-amber-700 text-white font-bold rounded-xl text-sm shadow-lg shadow-amber-600/20 transition-all flex items-center justify-center gap-2">
                    <i class="fa-solid fa-copy"></i> Copy Build Specification
                </button>
                <button onclick="window.closeModal()" class="px-6 py-3.5 bg-slate-200 hover:bg-slate-300 text-slate-700 font-bold rounded-xl text-sm transition-all">
                    Close
                </button>
            </div>
        </div>
    </div>

    <footer class="bg-slate-900 text-white py-12 border-t border-slate-800 mt-20">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center justify-between gap-6 text-center md:text-left">
            <div class="flex items-center gap-3">
                <div class="w-10 h-10 rounded-xl bg-gradient-to-tr from-amber-600 to-amber-400 flex items-center justify-center text-white font-bold text-lg shadow-lg shadow-amber-500/30">
                    <i class="fa-solid fa-pen-nib"></i>
                </div>
                <div>
                    <span class="text-lg font-bold text-white">PenForge</span>
                    <p class="text-xs text-slate-400">The Custom Pen Engineering Studio &copy; 2026</p>
                </div>
            </div>
            <div class="flex items-center gap-6 text-sm text-slate-400">
                <a href="#hero" onclick="window.switchTab('home')" class="hover:text-white transition-colors">Home</a>
                <a href="#builder" onclick="window.switchTab('builder')" class="hover:text-white transition-colors">Pen Builder</a>
                <a href="#anatomy" onclick="window.switchTab('anatomy')" class="hover:text-white transition-colors">Pen Anatomy</a>
                <a href="#catalog" onclick="window.switchTab('catalog')" class="hover:text-white transition-colors">Part Catalog</a>
            </div>
        </div>
    </footer>

    <script>
        const penDatabase = {
            nibs: [
                { id: 'nib_gold', name: '18K Sovereign Gold Nib', model: 'Monarch Elite', weight: 4, flow: 'Ultra Smooth', comfort: 95, color: 'from-amber-400 to-yellow-600', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M25 0 C28 20 40 40 40 60 L25 75 L10 60 C10 40 22 20 25 0 Z" fill="url(#goldGrad)"/><circle cx="25" cy="55" r="3" fill="#92400e"/><defs><linearGradient id="goldGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#fde047"/><stop offset="100%" stop-color="#d97706"/></linearGradient></defs></svg>' },
                { id: 'nib_titanium', name: 'Matte Titanium Flex Nib', model: 'Titan Forge', weight: 6, flow: 'Responsive Wet', comfort: 90, color: 'from-slate-400 to-slate-600', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M25 0 C28 20 38 42 38 60 L25 78 L12 60 C12 42 22 20 25 0 Z" fill="url(#titGrad)"/><circle cx="25" cy="55" r="2.5" fill="#1e293b"/><defs><linearGradient id="titGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#cbd5e1"/><stop offset="100%" stop-color="#475569"/></linearGradient></defs></svg>' },
                { id: 'nib_steel', name: 'Stainless Steel Needlepoint', model: 'Urban Draft', weight: 3, flow: 'Precise Fine', comfort: 88, color: 'from-slate-200 to-slate-400', svg: '<svg class="w-10 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M25 0 C27 25 34 45 34 65 L25 80 L16 65 C16 45 23 25 25 0 Z" fill="url(#steelGrad)"/><circle cx="25" cy="65" r="2" fill="#0f172a"/><defs><linearGradient id="steelGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#f8fafc"/><stop offset="100%" stop-color="#94a3b8"/></linearGradient></defs></svg>' },
                { id: 'nib_calligraphy', name: 'Stubb Italic Calligraphy Nib', model: 'Renaissance', weight: 5, flow: 'Variable Broad', comfort: 82, color: 'from-amber-600 to-amber-900', svg: '<svg class="w-14 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M20 0 L30 0 C35 25 40 45 40 60 L25 75 L10 60 C10 45 15 25 20 0 Z" fill="url(#calliGrad)"/><rect x="22" y="52" width="6" height="4" fill="#451a03"/><defs><linearGradient id="calliGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#b45309"/><stop offset="100%" stop-color="#78350f"/></linearGradient></defs></svg>' },
                { id: 'nib_rollerball', name: 'Ceramic Rollerball Refill Tip', model: 'GlideSmooth', weight: 5, flow: 'Consistent Wet', comfort: 96, color: 'from-blue-500 to-indigo-700', svg: '<svg class="w-10 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M20 10 L30 10 C32 35 32 55 30 65 L25 75 L20 65 C18 55 18 35 20 10 Z" fill="#3b82f6"/><circle cx="25" cy="72" r="3.5" fill="#1e3a8a"/></svg>' },
                { id: 'nib_gel', name: '0.5mm Hybrid Gel Ink Tip', model: 'Precision Pro', weight: 4, flow: 'Crisp & Fast Dry', comfort: 94, color: 'from-rose-500 to-red-700', svg: '<svg class="w-10 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M22 10 L28 10 L30 65 L25 78 L20 65 Z" fill="#f43f5e"/><circle cx="25" cy="75" r="2.5" fill="#881337"/></svg>' },
                { id: 'nib_glass', name: 'Hand-Pulled Spiral Glass Dip Nib', model: 'Venetian Crystal', weight: 7, flow: 'Shading Expressive', comfort: 80, color: 'from-cyan-400 to-blue-600', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M25 0 Q35 30 38 60 L25 80 L12 60 Q15 30 25 0 Z" fill="url(#glassGrad)"/><path d="M18 20 Q25 35 32 50" stroke="#ffffff" stroke-width="2" fill="none"/><defs><linearGradient id="glassGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#67e8f9"/><stop offset="100%" stop-color="#0284c7"/></linearGradient></defs></svg>' },
                { id: 'nib_brush', name: 'Flexible Synthetic Hair Brush Tip', model: 'Kalligrapher', weight: 4, flow: 'High Dynamic Flow', comfort: 89, color: 'from-purple-600 to-indigo-900', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 50 80"><path d="M20 10 C20 30 15 50 25 78 C35 50 30 30 30 10 Z" fill="#4338ca"/><circle cx="25" cy="10" r="5" fill="#312e81"/></svg>' }
            ],
            grips: [
                { id: 'grip_rubber', name: 'Ergonomic Soft Silicone Grip', model: 'ErgoPro', weight: 8, comfort: 98, flow: 'Standard', color: 'bg-slate-800 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="8" fill="#1e293b"/><line x1="15" y1="15" x2="45" y2="15" stroke="#475569" stroke-width="3"/><line x1="15" y1="25" x2="45" y2="25" stroke="#475569" stroke-width="3"/><line x1="15" y1="35" x2="45" y2="35" stroke="#475569" stroke-width="3"/></svg>' },
                { id: 'grip_knurled', name: 'Diamond-Knurled Brass Grip', model: 'Architect', weight: 14, comfort: 91, flow: 'Heavy Stability', color: 'bg-amber-600 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="6" fill="#d97706"/><path d="M10 15 L50 25 M10 25 L50 35 M10 35 L50 45" stroke="#b45309" stroke-width="2"/></svg>' },
                { id: 'grip_resin', name: 'Polished Amber Resin Section', model: 'Monarch Elite', weight: 6, comfort: 89, color: 'bg-amber-100 text-amber-900', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="10" fill="#fef3c7"/><ellipse cx="30" cy="25" rx="15" ry="8" fill="#fde68a"/></svg>' },
                { id: 'grip_carbon', name: 'Carbon Fiber Weave Grip', model: 'Titan Forge', weight: 7, comfort: 94, color: 'bg-slate-900 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="6" fill="#0f172a"/><path d="M10 5 L50 45 M50 5 L10 45" stroke="#334155" stroke-width="2"/></svg>' },
                { id: 'grip_leather', name: 'Padded Genuine Leather Wrap Grip', model: 'Executive', weight: 9, comfort: 97, flow: 'Soft Tactile', color: 'bg-amber-900 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="6" fill="#78350f"/><path d="M10 20 Q30 30 50 20" stroke="#451a03" stroke-width="4" fill="none"/></svg>' },
                { id: 'grip_titanium', name: 'Micro-Ribbed Titanium Grip', model: 'AeroMaster', weight: 11, comfort: 92, flow: 'Rigid Balance', color: 'bg-slate-500 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="6" fill="#64748b"/><line x1="10" y1="18" x2="50" y2="18" stroke="#334155" stroke-width="2"/><line x1="10" y1="32" x2="50" y2="32" stroke="#334155" stroke-width="2"/></svg>' },
                { id: 'grip_wooden', name: 'Contoured African Rosewood Grip', model: 'WoodCraft', weight: 8, comfort: 95, flow: 'Natural Warm', color: 'bg-amber-700 text-white', svg: '<svg class="w-16 h-14 drop-shadow-md" viewBox="0 0 60 50"><rect x="10" y="5" width="40" height="40" rx="10" fill="#92400e"/><ellipse cx="30" cy="25" rx="12" ry="6" fill="#78350f"/></svg>' }
            ],
            barrels: [
                { id: 'barrel_titanium', name: 'Aerospace Grade Titanium Barrel', model: 'Titan Forge', weight: 22, comfort: 92, flow: 'Balanced', color: 'bg-slate-600 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#64748b"/><line x1="40" y1="0" x2="40" y2="140" stroke="#475569" stroke-width="3"/></svg>' },
                { id: 'barrel_wood', name: 'Stabilized Burl Walnut Wood', model: 'WoodCraft', weight: 16, comfort: 96, flow: 'Warm Balance', color: 'bg-amber-800 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#92400e"/><path d="M20 30 Q50 50 20 70 M20 90 Q50 110 20 130" stroke="#78350f" stroke-width="3" fill="none"/></svg>' },
                { id: 'barrel_resin', name: 'Deep Nebula Swirl Resin', model: 'Astral', weight: 18, comfort: 89, flow: 'Standard', color: 'bg-indigo-900 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="url(#resinGrad)"/><defs><linearGradient id="resinGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0%" stop-color="#312e81"/><stop offset="50%" stop-color="#701a75"/><stop offset="100%" stop-color="#0f172a"/></linearGradient></defs></svg>' },
                { id: 'barrel_brass', name: 'Heavyweight Patina Brass', model: 'Architect', weight: 34, comfort: 85, flow: 'Forward Balanced', color: 'bg-amber-600 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#b45309"/><line x1="40" y1="0" x2="40" y2="140" stroke="#d97706" stroke-width="4"/></svg>' },
                { id: 'barrel_carbon', name: 'Full Carbon Fiber Monocoque Barrel', model: 'Stealth', weight: 14, comfort: 95, flow: 'Featherweight', color: 'bg-slate-900 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#0f172a"/><path d="M20 0 L60 140 M60 0 L20 140" stroke="#1e293b" stroke-width="2"/></svg>' },
                { id: 'barrel_copper', name: 'Living Copper Antique Barrel', model: 'Alchemist', weight: 32, comfort: 88, flow: 'Patina Shift', color: 'bg-orange-700 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#c2410c"/><line x1="40" y1="0" x2="40" y2="140" stroke="#9a3412" stroke-width="3"/></svg>' },
                { id: 'barrel_ebonite', name: 'Hand-Turned Vintage Ebonite Barrel', model: 'Heritage', weight: 19, comfort: 97, flow: 'Classic Smooth', color: 'bg-stone-800 text-white', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#292524"/><line x1="20" y1="40" x2="60" y2="40" stroke="#44403c" stroke-width="2"/><line x1="20" y1="80" x2="60" y2="80" stroke="#44403c" stroke-width="2"/></svg>' },
                { id: 'barrel_ceramic', name: 'Matte Porcelain White Ceramic', model: 'Minimalist', weight: 26, comfort: 91, flow: 'Cool Touch', color: 'bg-slate-100 text-slate-800', svg: '<svg class="w-20 h-36 drop-shadow-lg" viewBox="0 0 80 140"><path d="M20 0 L60 0 C65 40 65 100 60 130 C60 135 55 140 40 140 C25 140 20 135 20 130 C15 100 15 40 20 0 Z" fill="#f8fafc"/><line x1="40" y1="0" x2="40" y2="140" stroke="#e2e8f0" stroke-width="2"/></svg>' }
            ],
            clips: [
                { id: 'clip_spring', name: 'Flexible Steel Pocket Clip', model: 'Urban Draft', weight: 3, comfort: 95, flow: 'Standard', color: 'bg-slate-300 text-slate-800', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 40 60"><path d="M15 0 L25 0 L25 45 C25 55 20 58 20 58 C20 58 15 55 15 45 Z" fill="#cbd5e1"/><rect x="18" y="5" width="4" height="35" fill="#94a3b8"/></svg>' },
                { id: 'clip_gold', name: 'Gold-Plated Executive Clip', model: 'Monarch Elite', weight: 4, comfort: 95, flow: 'Standard', color: 'bg-amber-400 text-slate-900', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 40 60"><path d="M15 0 L25 0 L25 45 C25 55 20 58 20 58 C20 58 15 55 15 45 Z" fill="#facc15"/><rect x="18" y="5" width="4" height="35" fill="#eab308"/></svg>' },
                { id: 'clip_minimal', name: 'Matte Minimalist Wire Clip', model: 'Titan Forge', weight: 2, comfort: 95, flow: 'Standard', color: 'bg-slate-800 text-white', svg: '<svg class="w-12 h-16 drop-shadow-md" viewBox="0 0 40 60"><line x1="20" y1="0" x2="20" y2="50" stroke="#1e293b" stroke-width="4"/><circle cx="20" cy="52" r="3" fill="#1e293b"/></svg>' },
                { id: 'clip_none', name: 'Streamlined Clip-less Design', model: 'Zenith', weight: 0, comfort: 98, flow: 'Standard', color: 'bg-slate-200 text-slate-600', svg: '<svg class="w-12 h-16" viewBox="0 0 40 60"><text x="20" y="30" font-size="10" text-anchor="middle" fill="#94a3b8">None</text></svg>' }
            ]
        };

        const popularPens = [
            { name: 'Monarch Executive Sovereign', desc: 'Crafted with 18K Sovereign Gold Nib and Polished Amber Resin.', img: 'https://placehold.co/400x250/d97706/ffffff?text=Monarch+Sovereign' },
            { name: 'Titanium Forge Pro', desc: 'Aerospace titanium barrel combined with a flexible matte tip.', img: 'https://placehold.co/400x250/475569/ffffff?text=Titanium+Forge' },
            { name: 'Architect Brass Heavyweight', desc: 'Diamond-knurled brass grip balanced with patina barrel body.', img: 'https://placehold.co/400x250/b45309/ffffff?text=Architect+Brass' }
        ];

        let currentBuild = {
            nib: penDatabase.nibs[0],
            grip: penDatabase.grips[0],
            barrel: penDatabase.barrels[0],
            clip: penDatabase.clips[0]
        };

        let activeComponentTab = 'nib';
        let currentCatalogFilter = 'all';

        window.switchTab = function(tabId) {
            document.querySelectorAll('.view-section').forEach(el => el.classList.add('hidden'));
            const targetView = document.getElementById(`view-${tabId}`);
            if (targetView) targetView.classList.remove('hidden');

            document.querySelectorAll('.nav-btn').forEach(btn => {
                btn.classList.remove('bg-white', 'text-slate-900', 'shadow-sm');
                btn.classList.add('text-slate-600');
            });
            const activeBtn = document.getElementById(`nav-${tabId}`);
            if (activeBtn) {
                activeBtn.classList.add('bg-white', 'text-slate-900', 'shadow-sm');
                activeBtn.classList.remove('text-slate-600');
            }

            window.scrollTo({ top: 0, behavior: 'smooth' });
            if (tabId === 'catalog') {
                window.renderCatalog();
            }
        };

        window.filterCatalogParts = function(filterKey) {
            currentCatalogFilter = filterKey;
            document.querySelectorAll('.catalog-subtab-btn').forEach(btn => {
                btn.classList.remove('bg-amber-600', 'text-white', 'shadow-sm');
                btn.classList.add('text-slate-600');
            });
            const activeSubBtn = document.getElementById(`catalog-subtab-${filterKey}`);
            if (activeSubBtn) {
                activeSubBtn.classList.add('bg-amber-600', 'text-white', 'shadow-sm');
                activeSubBtn.classList.remove('text-slate-600');
            }
            window.renderCatalogPartsGrid();
        };

        window.switchComponentTab = function(category) {
            activeComponentTab = category;
            document.querySelectorAll('.comp-tab-btn').forEach(btn => {
                btn.classList.remove('bg-amber-600', 'text-white', 'shadow-md', 'shadow-amber-600/20');
                btn.classList.add('text-slate-600');
            });
            const activeTabBtn = document.getElementById(`ctab-${category}`);
            if (activeTabBtn) {
                activeTabBtn.classList.add('bg-amber-600', 'text-white', 'shadow-md', 'shadow-amber-600/20');
                activeTabBtn.classList.remove('text-slate-600');
            }

            window.renderComponentOptions();
        };

        window.renderComponentOptions = function() {
            const container = document.getElementById('component-options-grid');
            const titleEl = document.getElementById('component-list-title');
            const countBadge = document.getElementById('component-count-badge');
            
            let items = penDatabase[activeComponentTab] || penDatabase['nibs'];
            let displayName = activeComponentTab === 'nib' ? 'Tip / Nib' : activeComponentTab === 'grip' ? 'Grip Section' : activeComponentTab === 'barrel' ? 'Barrel Body' : 'Pocket Clip';
            if (titleEl) titleEl.textContent = `Select ${displayName} Component`;
            if (countBadge) countBadge.textContent = `${items.length} Options Available`;

            if (!container) return;
            container.innerHTML = '';
            items.forEach(item => {
                const isSelected = currentBuild[activeComponentTab]?.id === item.id;
                const card = document.createElement('div');
                card.className = `p-4 rounded-2xl border-2 cursor-pointer transition-all flex items-center justify-between ${isSelected ? 'border-amber-600 bg-amber-50/50 shadow-md shadow-amber-500/10' : 'border-slate-200 hover:border-slate-300 bg-white'}`;
                card.onclick = () => window.selectComponent(activeComponentTab, item.id);

                card.innerHTML = `
                    <div class="flex items-center gap-3">
                        <div class="w-12 h-12 rounded-xl bg-slate-100 flex items-center justify-center p-1 border border-slate-200">
                            ${item.svg}
                        </div>
                        <div>
                            <h4 class="font-bold text-slate-900 text-sm">${item.name}</h4>
                            <p class="text-xs text-slate-500">Model: ${item.model} &bull; Weight: ${item.weight}g</p>
                        </div>
                    </div>
                    <div>
                        <span class="w-6 h-6 rounded-full flex items-center justify-center ${isSelected ? 'bg-amber-600 text-white' : 'bg-slate-100 text-slate-400'}">
                            <i class="fa-solid ${isSelected ? 'fa-check text-xs' : 'fa-plus text-xs'}"></i>
                        </span>
                    </div>
                `;
                container.appendChild(card);
            });
        };

        window.selectComponent = function(category, itemId) {
            // Map singular category key to plural database key
            const dbKeyMap = {
                'nib': 'nibs',
                'grip': 'grips',
                'barrel': 'barrels',
                'clip': 'clips'
            };
            const targetDbKey = dbKeyMap[category] || category + 's';
            const collection = penDatabase[targetDbKey] || penDatabase[category];
            
            if (!collection) {
                console.error('Invalid category collection:', category);
                return;
            }

            const found = collection.find(i => i.id === itemId);
            if (found) {
                currentBuild[category] = found;
                window.updateBuilderUI();
                window.renderComponentOptions();
            }
        };

        window.updateBuilderUI = function() {
            const clipEl = document.getElementById('render-clip');
            const nibEl = document.getElementById('render-nib');
            const gripEl = document.getElementById('render-grip');
            const barrelEl = document.getElementById('render-barrel');

            if (clipEl) clipEl.innerHTML = currentBuild.clip.svg;
            if (nibEl) nibEl.innerHTML = currentBuild.nib.svg;
            if (gripEl) gripEl.innerHTML = currentBuild.grip.svg;
            if (barrelEl) barrelEl.innerHTML = currentBuild.barrel.svg;

            const nameEl = document.getElementById('display-pen-name');
            if (nameEl) nameEl.textContent = `${currentBuild.barrel.model} x ${currentBuild.nib.model} Hybrid`;

            const summaryEl = document.getElementById('display-builder-summary');
            if (summaryEl) summaryEl.textContent = `Assembled from ${currentBuild.nib.model}, ${currentBuild.grip.model}, ${currentBuild.barrel.model}, ${currentBuild.clip.model}`;

            const totalWeight = currentBuild.nib.weight + currentBuild.grip.weight + currentBuild.barrel.weight + currentBuild.clip.weight;
            const avgComfort = Math.round((currentBuild.nib.comfort + currentBuild.grip.comfort + currentBuild.barrel.comfort + currentBuild.clip.comfort) / 4);

            const weightVal = document.getElementById('stat-weight-val');
            if (weightVal) weightVal.textContent = `${totalWeight}g`;
            const weightBar = document.getElementById('stat-weight-bar');
            if (weightBar) weightBar.style.width = `${Math.min(100, (totalWeight / 50) * 100)}%`;

            const gripVal = document.getElementById('stat-grip-val');
            if (gripVal) gripVal.textContent = `${avgComfort}% Comfort`;
            const gripBar = document.getElementById('stat-grip-bar');
            if (gripBar) gripBar.style.width = `${avgComfort}%`;

            const flowVal = document.getElementById('stat-flow-val');
            if (flowVal) flowVal.textContent = currentBuild.nib.flow;
            const flowBar = document.getElementById('stat-flow-bar');
            if (flowBar) flowBar.style.width = currentBuild.nib.flow.includes('Smooth') || currentBuild.nib.flow.includes('Consistent') ? '90%' : '75%';

            const balanceVal = document.getElementById('stat-balance-val');
            if (balanceVal) balanceVal.textContent = totalWeight > 30 ? 'Forward Weighted' : 'Balanced Center';
            const balanceBar = document.getElementById('stat-balance-bar');
            if (balanceBar) balanceBar.style.width = `${Math.max(50, 100 - (totalWeight * 1.2))}%`;
        };

        window.randomizePen = function() {
            currentBuild.nib = penDatabase.nibs[Math.floor(Math.random() * penDatabase.nibs.length)];
            currentBuild.grip = penDatabase.grips[Math.floor(Math.random() * penDatabase.grips.length)];
            currentBuild.barrel = penDatabase.barrels[Math.floor(Math.random() * penDatabase.barrels.length)];
            currentBuild.clip = penDatabase.clips[Math.floor(Math.random() * penDatabase.clips.length)];

            window.updateBuilderUI();
            window.renderComponentOptions();
        };

        window.savePenBuild = function() {
            const totalWeight = currentBuild.nib.weight + currentBuild.grip.weight + currentBuild.barrel.weight + currentBuild.clip.weight;

            const detailsHtml = `
                <p><strong>Pen Configuration Name:</strong> ${currentBuild.barrel.model} x ${currentBuild.nib.model}</p>
                <ul class="list-disc pl-5 space-y-1 pt-2">
                    <li><strong>Tip / Nib:</strong> ${currentBuild.nib.name}</li>
                    <li><strong>Grip Section:</strong> ${currentBuild.grip.name}</li>
                    <li><strong>Barrel Body:</strong> ${currentBuild.barrel.name}</li>
                    <li><strong>Pocket Clip:</strong> ${currentBuild.clip.name}</li>
                </ul>
                <div class="pt-2 border-t border-slate-200 flex justify-between text-xs text-slate-500">
                    <span>Total Weight: ${totalWeight}g</span>
                    <span>Ink Flow: ${currentBuild.nib.flow}</span>
                </div>
            `;

            const modalDetails = document.getElementById('modal-build-details');
            if (modalDetails) modalDetails.innerHTML = detailsHtml;
            const saveModal = document.getElementById('save-modal');
            if (saveModal) saveModal.classList.remove('hidden');
        };

        window.closeModal = function() {
            const saveModal = document.getElementById('save-modal');
            if (saveModal) saveModal.classList.add('hidden');
        };

        window.copyBuildSpecs = function() {
            const textToCopy = `PenForge Custom Build Specifications:\n- Tip/Nib: ${currentBuild.nib.name}\n- Grip: ${currentBuild.grip.name}\n- Barrel: ${currentBuild.barrel.name}\n- Clip: ${currentBuild.clip.name}`;
            const textarea = document.createElement('textarea');
            textarea.value = textToCopy;
            document.body.appendChild(textarea);
            textarea.select();
            document.execCommand('copy');
            document.body.removeChild(textarea);
            alert('Build specifications copied to clipboard!');
        };

        window.renderCatalog = function() {
            const modelsGrid = document.getElementById('catalog-models-grid');
            if (modelsGrid) {
                modelsGrid.innerHTML = '';
                popularPens.forEach(p => {
                    const card = document.createElement('div');
                    card.className = 'bg-white rounded-3xl overflow-hidden border border-slate-200/80 shadow-xl shadow-slate-200/50 flex flex-col justify-between';
                    card.innerHTML = `
                        <img src="${p.img}" alt="${p.name}" class="w-full h-48 object-cover">
                        <div class="p-6 space-y-2 flex-grow">
                            <h4 class="font-bold text-slate-900 text-lg">${p.name}</h4>
                            <p class="text-slate-600 text-xs leading-relaxed">${p.desc}</p>
                        </div>
                        <div class="p-6 pt-0">
                            <button onclick="window.switchTab('builder')" class="w-full py-2.5 rounded-xl bg-slate-100 hover:bg-amber-600 hover:text-white text-slate-800 font-bold text-xs transition-colors flex items-center justify-center gap-2">
                                <i class="fa-solid fa-wand-magic-sparkles"></i> Customize Model
                            </button>
                        </div>
                    `;
                    modelsGrid.appendChild(card);
                });
            }

            window.renderCatalogPartsGrid();
        };

        window.renderCatalogPartsGrid = function() {
            const partsGrid = document.getElementById('catalog-parts-grid');
            if (!partsGrid) return;
            partsGrid.innerHTML = '';

            let allParts = [
                ...penDatabase.nibs.map(i => ({ ...i, categoryKey: 'nib', type: 'Tip / Nib' })),
                ...penDatabase.grips.map(i => ({ ...i, categoryKey: 'grip', type: 'Grip Section' })),
                ...penDatabase.barrels.map(i => ({ ...i, categoryKey: 'barrel', type: 'Barrel Body' })),
                ...penDatabase.clips.map(i => ({ ...i, categoryKey: 'clip', type: 'Pocket Clip' }))
            ];

            if (currentCatalogFilter !== 'all') {
                allParts = allParts.filter(p => p.categoryKey === currentCatalogFilter);
            }

            allParts.forEach(part => {
                const card = document.createElement('div');
                card.className = 'bg-slate-50 p-6 rounded-3xl border border-slate-200/80 space-y-4 flex flex-col justify-between';
                card.innerHTML = `
                    <div class="space-y-3">
                        <div class="flex items-center justify-between">
                            <span class="text-[10px] font-bold uppercase tracking-wider px-2.5 py-1 rounded-md bg-amber-100 text-amber-800">${part.type}</span>
                            <span class="text-xs text-slate-500 font-medium">${part.weight}g</span>
                        </div>
                        <div class="w-full h-24 flex items-center justify-center bg-white rounded-2xl border border-slate-200 p-2">
                            ${part.svg}
                        </div>
                        <h4 class="font-bold text-slate-900 text-sm">${part.name}</h4>
                        <p class="text-xs text-slate-500">Series: ${part.model}</p>
                    </div>
                    <button onclick="window.switchTab('builder'); window.switchComponentTab('${part.categoryKey}');" class="w-full py-2 rounded-xl bg-slate-900 hover:bg-amber-600 text-white font-bold text-xs transition-colors">
                        Use in Builder
                    </button>
                `;
                partsGrid.appendChild(card);
            });
        };

        window.onload = function() {
            window.updateBuilderUI();
            window.renderComponentOptions();
        };
    </script>
</body>
</html>
