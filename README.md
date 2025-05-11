<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>FLEX - Premium Fitness Experience</title>
<script src="https://cdn.tailwindcss.com/3.4.16"></script>
<script>
tailwind.config={
theme:{
extend:{
colors:{
primary:'#00FFFF',
secondary:'#8A2BE2',
dark: '#000000',
darkGray: '#1A1A1A',
lightGray: '#E0E0E0'
},
borderRadius:{
'none':'0px',
'sm':'4px',
DEFAULT:'8px',
'md':'12px',
'lg':'16px',
'xl':'20px',
'2xl':'24px',
'3xl':'32px',
'full':'9999px',
'button':'8px'
}
}
}
}
</script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Pacifico&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/remixicon/4.6.0/remixicon.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/echarts/5.5.0/echarts.min.js"></script>
<style>
:where([class^="ri-"])::before { content: "\f3c2"; }
body {
font-family: 'Montserrat', sans-serif;
background-color: #000000;
color: #E0E0E0;
overflow-x: hidden;
width: 100%;
}

/* Responsive styles */
@media (max-width: 640px) {
  .container {
    padding-left: 16px;
    padding-right: 16px;
  }
  
  .text-4xl {
    font-size: 1.875rem;
  }
  
  .py-20 {
    padding-top: 3rem;
    padding-bottom: 3rem;
  }
  
  .mb-16 {
    margin-bottom: 2rem;
  }
  
  .gap-8 {
    gap: 1rem;
  }
  
  .grid {
    grid-template-columns: repeat(1, minmax(0, 1fr)) !important;
  }
  
  .whitespace-nowrap {
    font-size: 0.875rem;
    padding: 0.5rem 1rem;
  }
}

/* Make images responsive */
img {
  max-width: 100%;
  height: auto;
}

/* Improve table responsiveness */
table {
  display: block;
  width: 100%;
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
}
.gradient-bg {
background: linear-gradient(135deg, #000000, #1A1A1A);
}
.glass-effect {
background: rgba(26, 26, 26, 0.7);
backdrop-filter: blur(10px);
border: 1px solid rgba(255, 255, 255, 0.1);
}
.neon-border {
box-shadow: 0 0 5px #00FFFF, 0 0 10px rgba(0, 255, 255, 0.5);
}
.neon-text {
text-shadow: 0 0 5px #00FFFF, 0 0 10px rgba(0, 255, 255, 0.5);
}
.purple-neon-text {
text-shadow: 0 0 5px #8A2BE2, 0 0 10px rgba(138, 43, 226, 0.5);
}
.gradient-text {
background: linear-gradient(90deg, #00FFFF, #8A2BE2);
-webkit-background-clip: text;
background-clip: text;
color: transparent;
}
.orbitron {
font-family: 'Orbitron', sans-serif;
}
.hero-bg {
background-image: url('https://readdy.ai/api/search-image?query=modern%20gym%20interior%20with%20high-tech%20equipment%2C%20dark%20atmosphere%20with%20blue%20and%20purple%20neon%20lighting%2C%20sleek%20black%20surfaces%2C%20futuristic%20design%2C%20professional%20photography%2C%20ultra-realistic%2C%20cinematic%20lighting%2C%20dramatic%20shadows&width=1600&height=800&seq=hero1&orientation=landscape');
background-size: cover;
background-position: center;
position: relative;
}
.hero-bg::before {
content: '';
position: absolute;
top: 0;
left: 0;
right: 0;
bottom: 0;
background: linear-gradient(90deg, rgba(0,0,0,0.9) 0%, rgba(0,0,0,0.7) 50%, rgba(0,0,0,0.5) 100%);
}
.progress-ring {
transform: rotate(-90deg);
}
.progress-ring-circle {
transition: stroke-dashoffset 0.5s;
transform-origin: center;
}
.exercise-card {
transition: all 0.3s ease;
}
.exercise-card:hover {
transform: translateY(-10px) scale(1.03);
}
.program-card {
transition: all 0.3s ease;
}
.program-card:hover {
transform: translateY(-5px);
}
.custom-scrollbar::-webkit-scrollbar {
width: 6px;
}
.custom-scrollbar::-webkit-scrollbar-track {
background: #1A1A1A;
}
.custom-scrollbar::-webkit-scrollbar-thumb {
background: #00FFFF;
border-radius: 10px;
}
.custom-cursor {
width: 20px;
height: 20px;
border: 2px solid #00FFFF;
border-radius: 50%;
position: fixed;
pointer-events: none;
z-index: 9999;
mix-blend-mode: difference;
transition: transform 0.2s;
}
.pulse-animation {
animation: pulse 2s infinite;
}
@keyframes pulse {
0% {
box-shadow: 0 0 0 0 rgba(0, 255, 255, 0.7);
}
70% {
box-shadow: 0 0 0 10px rgba(0, 255, 255, 0);
}
100% {
box-shadow: 0 0 0 0 rgba(0, 255, 255, 0);
}
}
.rotate-animation {
animation: rotate 10s linear infinite;
}
@keyframes rotate {
from {
transform: rotate(0deg);
}
to {
transform: rotate(360deg);
}
}
.float-animation {
animation: float 3s ease-in-out infinite;
}
@keyframes float {
0% {
transform: translateY(0px);
}
50% {
transform: translateY(-10px);
}
100% {
transform: translateY(0px);
}
}
.custom-switch {
position: relative;
display: inline-block;
width: 50px;
height: 24px;
}
.custom-switch input {
opacity: 0;
width: 0;
height: 0;
}
.switch-slider {
position: absolute;
cursor: pointer;
top: 0;
left: 0;
right: 0;
bottom: 0;
background-color: #1A1A1A;
transition: .4s;
border-radius: 34px;
}
.switch-slider:before {
position: absolute;
content: "";
height: 16px;
width: 16px;
left: 4px;
bottom: 4px;
background-color: #E0E0E0;
transition: .4s;
border-radius: 50%;
}
input:checked + .switch-slider {
background-color: #00FFFF;
}
input:checked + .switch-slider:before {
transform: translateX(26px);
}
/* Custom radio button */
.custom-radio {
position: relative;
padding-left: 30px;
cursor: pointer;
user-select: none;
}
.custom-radio input {
position: absolute;
opacity: 0;
cursor: pointer;
}
.radio-checkmark {
position: absolute;
top: 0;
left: 0;
height: 20px;
width: 20px;
background-color: #1A1A1A;
border-radius: 50%;
border: 1px solid #333;
}
.custom-radio:hover input ~ .radio-checkmark {
background-color: #333;
}
.custom-radio input:checked ~ .radio-checkmark {
background-color: #1A1A1A;
border: 1px solid #00FFFF;
}
.radio-checkmark:after {
content: "";
position: absolute;
display: none;
}
.custom-radio input:checked ~ .radio-checkmark:after {
display: block;
}
.custom-radio .radio-checkmark:after {
top: 5px;
left: 5px;
width: 8px;
height: 8px;
border-radius: 50%;
background: #00FFFF;
}
/* Custom checkbox */
.custom-checkbox {
position: relative;
padding-left: 30px;
cursor: pointer;
user-select: none;
}
.custom-checkbox input {
position: absolute;
opacity: 0;
cursor: pointer;
}
.checkbox-checkmark {
position: absolute;
top: 0;
left: 0;
height: 20px;
width: 20px;
background-color: #1A1A1A;
border-radius: 4px;
border: 1px solid #333;
}
.custom-checkbox:hover input ~ .checkbox-checkmark {
background-color: #333;
}
.custom-checkbox input:checked ~ .checkbox-checkmark {
background-color: #00FFFF;
border: 1px solid #00FFFF;
}
.checkbox-checkmark:after {
content: "";
position: absolute;
display: none;
}
.custom-checkbox input:checked ~ .checkbox-checkmark:after {
display: block;
}
.custom-checkbox .checkbox-checkmark:after {
left: 7px;
top: 3px;
width: 5px;
height: 10px;
border: solid white;
border-width: 0 2px 2px 0;
transform: rotate(45deg);
}
/* Custom range slider */
.custom-range {
-webkit-appearance: none;
width: 100%;
height: 6px;
background: #1A1A1A;
border-radius: 5px;
outline: none;
}
.custom-range::-webkit-slider-thumb {
-webkit-appearance: none;
appearance: none;
width: 18px;
height: 18px;
background: #00FFFF;
border-radius: 50%;
cursor: pointer;
transition: all 0.2s;
}
.custom-range::-webkit-slider-thumb:hover {
box-shadow: 0 0 10px #00FFFF;
}
.custom-range::-moz-range-thumb {
width: 18px;
height: 18px;
background: #00FFFF;
border-radius: 50%;
cursor: pointer;
border: none;
transition: all 0.2s;
}
.custom-range::-moz-range-thumb:hover {
box-shadow: 0 0 10px #00FFFF;
}
</style>
</head>
<body class="custom-scrollbar">
<!-- Header Section -->
<header class="glass-effect fixed top-0 left-0 right-0 z-50 transition-all duration-300">
<div class="container mx-auto px-4 sm:px-6 py-4">
<div class="flex items-center justify-between">
<div class="flex items-center">
<div class="mr-2 w-10 h-10 flex items-center justify-center rotate-animation bg-primary rounded-lg">
<i class="ri-boxing-line ri-2x text-black"></i>
</div>
<div>
<h1 class="text-2xl font-['Pacifico'] gradient-text tracking-wider">FLEX</h1>
<span class="text-[10px] text-lightGray uppercase tracking-[0.2em] -mt-1 block">Premium Fitness</span>
</div>
</div>
<nav class="hidden lg:flex items-center space-x-8">
<a href="#" class="nav-link orbitron text-lightGray hover:text-primary hover:neon-text transition-all duration-300">HOME</a>
<a href="#workouts" class="nav-link orbitron text-lightGray hover:text-primary hover:neon-text transition-all duration-300">WORKOUTS</a>
<a href="#exercises" class="nav-link orbitron text-lightGray hover:text-primary hover:neon-text transition-all duration-300">EXERCISES</a>
<a href="#programs" class="nav-link orbitron text-lightGray hover:text-primary hover:neon-text transition-all duration-300">PROGRAMS</a>
<a href="#community" class="nav-link orbitron text-lightGray hover:text-primary hover:neon-text transition-all duration-300">COMMUNITY</a>
</nav>
<div class="hidden lg:flex items-center space-x-4">
<form onsubmit="return handleSearch(event)" class="relative">
<input type="text" id="searchInput" placeholder="Search exercises, programs..." class="bg-transparent border border-darkGray focus:border-primary rounded-full px-4 py-2 w-40 focus:w-52 transition-all duration-300 focus:outline-none text-sm">
<button type="submit" class="absolute right-3 top-2.5 w-5 h-5 flex items-center justify-center">
<i class="ri-search-line text-lightGray"></i>
</button>
</form>
<div class="w-10 h-10 flex items-center justify-center bg-darkGray rounded-full cursor-pointer hover:neon-border transition-all duration-300">
<i class="ri-user-line text-lightGray"></i>
</div>
</div>
<div class="lg:hidden">
<button onclick="toggleMobileMenu()" class="w-10 h-10 flex items-center justify-center">
<i class="ri-menu-line ri-2x text-lightGray"></i>
</button>
</div>
</div>
</div>
</header>

<!-- Mobile Menu -->
<div id="mobileMenu" class="fixed inset-0 bg-black bg-opacity-90 z-50 hidden">
<div class="container mx-auto px-4 py-8">
<div class="flex justify-end mb-8">
<button onclick="toggleMobileMenu()" class="w-10 h-10 flex items-center justify-center">
<i class="ri-close-line ri-2x text-lightGray"></i>
</button>
</div>
<nav class="flex flex-col items-center space-y-6">
<a href="#" onclick="toggleMobileMenu()" class="nav-link orbitron text-2xl text-lightGray hover:text-primary hover:neon-text transition-all duration-300">HOME</a>
<a href="#workouts" onclick="toggleMobileMenu()" class="nav-link orbitron text-2xl text-lightGray hover:text-primary hover:neon-text transition-all duration-300">WORKOUTS</a>
<a href="#exercises" onclick="toggleMobileMenu()" class="nav-link orbitron text-2xl text-lightGray hover:text-primary hover:neon-text transition-all duration-300">EXERCISES</a>
<a href="#programs" onclick="toggleMobileMenu()" class="nav-link orbitron text-2xl text-lightGray hover:text-primary hover:neon-text transition-all duration-300">PROGRAMS</a>
<a href="#community" onclick="toggleMobileMenu()" class="nav-link orbitron text-2xl text-lightGray hover:text-primary hover:neon-text transition-all duration-300">COMMUNITY</a>
</nav>
<form onsubmit="return handleSearch(event)" class="relative mt-8">
<input type="text" id="mobileSearchInput" placeholder="Search exercises, programs..." class="w-full bg-transparent border border-darkGray focus:border-primary rounded-full px-4 py-2 transition-all duration-300 focus:outline-none text-sm">
<button type="submit" class="absolute right-3 top-2.5 w-5 h-5 flex items-center justify-center">
<i class="ri-search-line text-lightGray"></i>
</button>
</form>
</div>
</div>
<!-- Hero Section -->
<section class="hero-bg min-h-screen flex items-center relative">
<div class="container mx-auto px-6 py-20 relative z-10">
<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
<div class="space-y-8">
<h1 class="orbitron text-5xl md:text-6xl lg:text-7xl font-bold">
<span class="block gradient-text">TRANSFORM</span>
<span class="block text-white">YOUR BODY</span>
<span class="block gradient-text">YOUR MIND</span>
</h1>
<p class="text-lg md:text-xl text-lightGray">
Experience the next generation of fitness with our cutting-edge 3D workout technology. Track progress, visualize results, and push beyond your limits.
</p>
<div class="flex flex-wrap gap-4">
<a href="#pricing" class="bg-primary text-black font-bold py-3 px-8 !rounded-button pulse-animation whitespace-nowrap inline-block">
START FREE TRIAL
</a>
<a href="#workouts" class="bg-transparent border border-primary text-primary font-bold py-3 px-8 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
EXPLORE WORKOUTS
</a>
</div>
<div class="flex flex-wrap gap-8 mt-12">
<div class="float-animation">
<div class="text-3xl font-bold gradient-text">1200+</div>
<div class="text-sm text-lightGray">WORKOUT ROUTINES</div>
</div>
<div class="float-animation" style="animation-delay: 0.2s">
<div class="text-3xl font-bold gradient-text">24/7</div>
<div class="text-sm text-lightGray">TRAINER SUPPORT</div>
</div>
<div class="float-animation" style="animation-delay: 0.4s">
<div class="text-3xl font-bold gradient-text">98%</div>
<div class="text-sm text-lightGray">SUCCESS RATE</div>
</div>
</div>
</div>
<div class="hidden lg:block">
<!-- This div is intentionally left empty as the hero background image covers this area -->
</div>
</div>
</div>
</section>
<!-- Workout Progress Tracker -->
<section id="workouts" class="py-20 gradient-bg">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">TRACK YOUR PROGRESS</h2>
<p class="text-lightGray max-w-2xl mx-auto">Monitor your fitness journey with our interactive 3D progress tracker. Visualize your improvements and stay motivated.</p>
</div>
<div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
<div class="glass-effect p-8 rounded-lg">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Weekly Stats</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-bar-chart-line text-primary"></i>
</div>
</div>
<div class="grid grid-cols-2 gap-4 mb-8">
<div class="glass-effect p-4 rounded-lg text-center">
<div class="text-3xl font-bold gradient-text">12</div>
<div class="text-sm text-lightGray">WORKOUTS</div>
</div>
<div class="glass-effect p-4 rounded-lg text-center">
<div class="text-3xl font-bold gradient-text">6.5</div>
<div class="text-sm text-lightGray">HOURS</div>
</div>
<div class="glass-effect p-4 rounded-lg text-center">
<div class="text-3xl font-bold gradient-text">4,350</div>
<div class="text-sm text-lightGray">CALORIES</div>
</div>
<div class="glass-effect p-4 rounded-lg text-center">
<div class="text-3xl font-bold gradient-text">18</div>
<div class="text-sm text-lightGray">EXERCISES</div>
</div>
</div>
<div class="mb-6">
<div class="flex justify-between mb-2">
<span class="text-sm text-lightGray">Weekly Goal</span>
<span class="text-sm text-primary">75%</span>
</div>
<div class="h-2 bg-darkGray rounded-full overflow-hidden">
<div class="h-full bg-primary rounded-full" style="width: 75%"></div>
</div>
</div>
<button class="w-full bg-transparent border border-primary text-primary font-bold py-3 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap">
VIEW DETAILED STATS
</button>
</div>
<div class="glass-effect p-8 rounded-lg">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Body Metrics</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-heart-pulse-line text-primary"></i>
</div>
</div>
<div id="bodyMetricsChart" class="w-full h-64 mb-8"></div>
<div class="flex flex-wrap gap-4">
<label class="custom-radio">
<input type="radio" name="metricType" checked>
<span class="radio-checkmark"></span>
<span class="text-sm">Weight</span>
</label>
<label class="custom-radio">
<input type="radio" name="metricType">
<span class="radio-checkmark"></span>
<span class="text-sm">Body Fat</span>
</label>
<label class="custom-radio">
<input type="radio" name="metricType">
<span class="radio-checkmark"></span>
<span class="text-sm">Muscle Mass</span>
</label>
</div>
</div>
<div class="glass-effect p-8 rounded-lg">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Muscle Focus</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-body-scan-line text-primary"></i>
</div>
</div>
<div class="grid grid-cols-2 gap-6 mb-8">
<div>
<div class="relative w-28 h-28 mx-auto mb-4">
<svg class="progress-ring" width="120" height="120">
<circle class="text-darkGray" stroke="currentColor" stroke-width="8" fill="transparent" r="50" cx="60" cy="60"/>
<circle class="progress-ring-circle text-primary" stroke="currentColor" stroke-width="8" fill="transparent" r="50" cx="60" cy="60" stroke-dasharray="314" stroke-dashoffset="78.5"/>
</svg>
<div class="absolute inset-0 flex items-center justify-center">
<span class="text-2xl font-bold text-white">75%</span>
</div>
</div>
<div class="text-center">
<h4 class="text-white font-semibold">Upper Body</h4>
<p class="text-xs text-lightGray">Last: Chest & Back</p>
</div>
</div>
<div>
<div class="relative w-28 h-28 mx-auto mb-4">
<svg class="progress-ring" width="120" height="120">
<circle class="text-darkGray" stroke="currentColor" stroke-width="8" fill="transparent" r="50" cx="60" cy="60"/>
<circle class="progress-ring-circle text-secondary" stroke="currentColor" stroke-width="8" fill="transparent" r="50" cx="60" cy="60" stroke-dasharray="314" stroke-dashoffset="157"/>
</svg>
<div class="absolute inset-0 flex items-center justify-center">
<span class="text-2xl font-bold text-white">50%</span>
</div>
</div>
<div class="text-center">
<h4 class="text-white font-semibold">Lower Body</h4>
<p class="text-xs text-lightGray">Last: Legs & Glutes</p>
</div>
</div>
</div>
<div>
<h4 class="text-white font-semibold mb-3">Recovery Status</h4>
<div class="flex items-center justify-between mb-2">
<span class="text-sm">Chest</span>
<div class="h-2 bg-darkGray rounded-full overflow-hidden w-2/3">
<div class="h-full bg-green-500 rounded-full" style="width: 90%"></div>
</div>
<span class="text-sm text-green-500">90%</span>
</div>
<div class="flex items-center justify-between mb-2">
<span class="text-sm">Back</span>
<div class="h-2 bg-darkGray rounded-full overflow-hidden w-2/3">
<div class="h-full bg-yellow-500 rounded-full" style="width: 65%"></div>
</div>
<span class="text-sm text-yellow-500">65%</span>
</div>
<div class="flex items-center justify-between mb-2">
<span class="text-sm">Legs</span>
<div class="h-2 bg-darkGray rounded-full overflow-hidden w-2/3">
<div class="h-full bg-red-500 rounded-full" style="width: 30%"></div>
</div>
<span class="text-sm text-red-500">30%</span>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- Exercise Library -->
<section id="exercises" class="py-20">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">EXERCISE LIBRARY</h2>
<p class="text-lightGray max-w-2xl mx-auto">Explore our comprehensive collection of exercises with 3D muscle visualizations and detailed instructions.</p>
</div>
<div class="flex flex-wrap justify-center gap-4 mb-12">
<button onclick="filterExercises('all')" class="exercise-filter-btn bg-primary text-black font-bold py-2 px-6 !rounded-button whitespace-nowrap">ALL</button>
<button onclick="filterExercises('chest')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">CHEST</button>
<button onclick="filterExercises('back')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">BACK</button>
<button onclick="filterExercises('shoulders')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">SHOULDERS</button>
<button onclick="filterExercises('arms')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">ARMS</button>
<button onclick="filterExercises('legs')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">LEGS</button>
<button onclick="filterExercises('core')" class="exercise-filter-btn bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">CORE</button>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=man%20performing%20bench%20press%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20blue%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex1&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Bench Press</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Chest, Triceps, Shoulders</span>
</div>
<p class="text-sm text-lightGray mb-6">The bench press is a compound exercise that develops the chest. Lie on a bench, lower the bar to your chest, then push it back up.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=man%20performing%20deadlift%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20purple%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex2&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Deadlift</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Back, Legs, Core, Traps</span>
</div>
<p class="text-sm text-lightGray mb-6">The deadlift is a compound exercise that targets multiple muscle groups. Lift a barbell from the ground to hip level, then lower it back down.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=woman%20performing%20squat%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20blue%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex3&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Squats</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Quads, Glutes, Hamstrings, Core</span>
</div>
<p class="text-sm text-lightGray mb-6">The squat is a compound exercise that primarily targets the legs. Stand with feet shoulder-width apart, lower your body, then push back up.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=man%20performing%20pull-up%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20purple%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex4&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Pull-Ups</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Back, Biceps, Shoulders</span>
</div>
<p class="text-sm text-lightGray mb-6">Pull-ups are a compound upper-body exercise. Hang from a bar with palms facing away, pull your body up until your chin is over the bar.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=woman%20performing%20shoulder%20press%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20blue%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex5&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Shoulder Press</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Shoulders, Triceps</span>
</div>
<p class="text-sm text-lightGray mb-6">The shoulder press targets the deltoid muscles. Sit or stand with a weight at shoulder level, then press it overhead until arms are extended.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
<div class="exercise-card glass-effect rounded-lg overflow-hidden" data-category="chest triceps shoulders">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=man%20performing%20bicep%20curl%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20purple%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=ex6&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Bicep Curls</h3>
<div class="flex space-x-1">
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-primary"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
<div class="w-2 h-2 rounded-full bg-darkGray"></div>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-focus-3-line text-primary"></i>
</div>
<span>Biceps, Forearms</span>
</div>
<p class="text-sm text-lightGray mb-6">Bicep curls isolate and develop the biceps. Hold weights with arms extended, then curl the weights toward your shoulders.</p>
<div class="flex justify-between">
<a href="#exercises" class="bg-transparent border border-primary text-primary font-bold py-2 px-4 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap inline-block">
VIEW DETAILS
</a>
<div class="w-10 h-10 flex items-center justify-center bg-primary/10 rounded-full cursor-pointer hover:bg-primary/20 transition-all duration-300">
<i class="ri-play-circle-line text-primary"></i>
</div>
</div>
</div>
</div>
</div>
<div class="text-center mt-12">
<button class="bg-transparent border border-primary text-primary font-bold py-3 px-8 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap">
LOAD MORE EXERCISES
</button>
</div>
</div>
</section>
<!-- Training Programs -->
<section id="programs" class="py-20 gradient-bg">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">TRAINING PROGRAMS</h2>
<p class="text-lightGray max-w-2xl mx-auto">Discover personalized workout programs designed by professional trainers to help you achieve your fitness goals.</p>
</div>
<div class="flex flex-wrap justify-center gap-4 mb-12">
<button class="bg-primary text-black font-bold py-2 px-6 !rounded-button whitespace-nowrap">ALL PROGRAMS</button>
<button class="bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">STRENGTH</button>
<button class="bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">HYPERTROPHY</button>
<button class="bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">WEIGHT LOSS</button>
<button class="bg-transparent border border-darkGray text-lightGray font-bold py-2 px-6 !rounded-button hover:border-primary hover:text-primary transition-all duration-300 whitespace-nowrap">ENDURANCE</button>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center relative" style="background-image: url('https://readdy.ai/api/search-image?query=muscular%20man%20lifting%20heavy%20weights%20in%20gym%2C%20focused%20expression%2C%20dark%20atmosphere%20with%20blue%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog1&orientation=landscape')">
<div class="absolute top-4 right-4 bg-primary text-black font-bold text-xs py-1 px-3 rounded-full">POPULAR</div>
</div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Power Building</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.9</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>12 Weeks • 5 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Strength</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Hypertrophy</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Advanced</span>
</div>
<p class="text-sm text-lightGray mb-6">A comprehensive program designed to build both strength and muscle mass simultaneously through periodized training blocks.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$89.99</span>
<span class="text-sm text-lightGray line-through ml-2">$129.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20woman%20performing%20HIIT%20workout%20in%20gym%2C%20intense%20expression%2C%20dark%20atmosphere%20with%20purple%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog2&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">HIIT Shred</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.7</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>8 Weeks • 4 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Fat Loss</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Conditioning</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Intermediate</span>
</div>
<p class="text-sm text-lightGray mb-6">High-intensity interval training program designed to maximize calorie burn, improve cardiovascular health, and shred body fat.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$69.99</span>
<span class="text-sm text-lightGray line-through ml-2">$99.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=bodybuilder%20with%20massive%20muscles%20posing%20in%20gym%2C%20detailed%20muscle%20definition%2C%20dark%20atmosphere%20with%20blue%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog3&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Mass Gainer</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.8</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>16 Weeks • 5 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Hypertrophy</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Bulking</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Intermediate</span>
</div>
<p class="text-sm text-lightGray mb-6">Focused on maximizing muscle growth through progressive overload, optimal volume, and nutrition strategies for muscle building.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$99.99</span>
<span class="text-sm text-lightGray line-through ml-2">$149.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=fit%20person%20in%20plank%20position%20in%20gym%2C%20core%20workout%2C%20detailed%20muscle%20definition%2C%20dark%20atmosphere%20with%20purple%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog4&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Core Crusher</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.6</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>6 Weeks • 3 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Core</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Stability</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">All Levels</span>
</div>
<p class="text-sm text-lightGray mb-6">Specialized program targeting all aspects of core development including abs, obliques, and lower back for improved stability and aesthetics.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$49.99</span>
<span class="text-sm text-lightGray line-through ml-2">$79.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20stretching%20in%20gym%2C%20flexibility%20workout%2C%20dark%20atmosphere%20with%20blue%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog5&orientation=landscape')"></div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Mobility Master</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.9</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>4 Weeks • 4 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Flexibility</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Recovery</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">All Levels</span>
</div>
<p class="text-sm text-lightGray mb-6">Comprehensive mobility program designed to improve range of motion, reduce injury risk, and enhance overall movement quality.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$39.99</span>
<span class="text-sm text-lightGray line-through ml-2">$59.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
<div class="program-card glass-effect rounded-lg overflow-hidden">
<div class="h-48 bg-cover bg-center relative" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20running%20on%20treadmill%20in%20gym%2C%20cardio%20workout%2C%20dark%20atmosphere%20with%20purple%20lighting%2C%20professional%20photography%2C%20ultra-realistic&width=600&height=400&seq=prog6&orientation=landscape')">
<div class="absolute top-4 right-4 bg-secondary text-white font-bold text-xs py-1 px-3 rounded-full">NEW</div>
</div>
<div class="p-6">
<div class="flex justify-between items-center mb-4">
<h3 class="text-xl font-bold text-white">Endurance Elite</h3>
<div class="flex">
<div class="w-5 h-5 flex items-center justify-center mr-1">
<i class="ri-star-fill text-primary"></i>
</div>
<span class="text-white">4.7</span>
</div>
</div>
<div class="flex items-center text-sm text-lightGray mb-4">
<div class="w-5 h-5 flex items-center justify-center mr-2">
<i class="ri-time-line text-primary"></i>
</div>
<span>10 Weeks • 5 Days/Week</span>
</div>
<div class="flex flex-wrap gap-2 mb-6">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Cardio</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Endurance</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Intermediate</span>
</div>
<p class="text-sm text-lightGray mb-6">Progressive endurance training program designed to improve cardiovascular capacity, stamina, and overall athletic performance.</p>
<div class="flex justify-between items-center">
<div>
<span class="text-xl font-bold text-white">$79.99</span>
<span class="text-sm text-lightGray line-through ml-2">$119.99</span>
</div>
<a href="#pricing" class="bg-primary text-black font-bold py-2 px-4 !rounded-button whitespace-nowrap inline-block">
ENROLL NOW
</a>
</div>
</div>
</div>
</div>
<div class="text-center mt-12">
<button class="bg-transparent border border-primary text-primary font-bold py-3 px-8 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap">
VIEW ALL PROGRAMS
</button>
</div>
</div>
</section>
<!-- Community Section -->
<section id="community" class="py-20">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">JOIN OUR COMMUNITY</h2>
<p class="text-lightGray max-w-2xl mx-auto">Connect with like-minded fitness enthusiasts, share your progress, and compete in challenges to stay motivated.</p>
</div>
<div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
<div class="glass-effect rounded-lg p-8">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Leaderboard</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-trophy-line text-primary"></i>
</div>
</div>
<div class="space-y-4">
<div class="flex items-center p-3 bg-darkGray/50 rounded-lg">
<div class="w-8 h-8 flex items-center justify-center bg-primary rounded-full mr-4">
<span class="font-bold text-black">1</span>
</div>
<div class="w-10 h-10 rounded-full bg-cover bg-center mr-4" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=user1&orientation=squarish')"></div>
<div class="flex-1">
<h4 class="text-white font-semibold">Alexander Mitchell</h4>
<p class="text-xs text-lightGray">Power Building Elite</p>
</div>
<div class="text-primary font-bold">12,450</div>
</div>
<div class="flex items-center p-3 bg-darkGray/50 rounded-lg">
<div class="w-8 h-8 flex items-center justify-center bg-secondary/80 rounded-full mr-4">
<span class="font-bold text-white">2</span>
</div>
<div class="w-10 h-10 rounded-full bg-cover bg-center mr-4" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20female%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=user2&orientation=squarish')"></div>
<div class="flex-1">
<h4 class="text-white font-semibold">Sophia Rodriguez</h4>
<p class="text-xs text-lightGray">HIIT Specialist</p>
</div>
<div class="text-primary font-bold">11,875</div>
</div>
<div class="flex items-center p-3 bg-darkGray/50 rounded-lg">
<div class="w-8 h-8 flex items-center justify-center bg-orange-500/80 rounded-full mr-4">
<span class="font-bold text-white">3</span>
</div>
<div class="w-10 h-10 rounded-full bg-cover bg-center mr-4" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=user3&orientation=squarish')"></div>
<div class="flex-1">
<h4 class="text-white font-semibold">Marcus Johnson</h4>
<p class="text-xs text-lightGray">Strength Champion</p>
</div>
<div class="text-primary font-bold">10,920</div>
</div>
<div class="flex items-center p-3 bg-darkGray/50 rounded-lg">
<div class="w-8 h-8 flex items-center justify-center bg-darkGray rounded-full mr-4">
<span class="font-bold text-lightGray">4</span>
</div>
<div class="w-10 h-10 rounded-full bg-cover bg-center mr-4" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20female%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=user4&orientation=squarish')"></div>
<div class="flex-1">
<h4 class="text-white font-semibold">Emily Chen</h4>
<p class="text-xs text-lightGray">Endurance Pro</p>
</div>
<div class="text-primary font-bold">9,845</div>
</div>
<div class="flex items-center p-3 bg-darkGray/50 rounded-lg">
<div class="w-8 h-8 flex items-center justify-center bg-darkGray rounded-full mr-4">
<span class="font-bold text-lightGray">5</span>
</div>
<div class="w-10 h-10 rounded-full bg-cover bg-center mr-4" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=user5&orientation=squarish')"></div>
<div class="flex-1">
<h4 class="text-white font-semibold">James Wilson</h4>
<p class="text-xs text-lightGray">Bodybuilding Expert</p>
</div>
<div class="text-primary font-bold">9,210</div>
</div>
</div>
<button class="w-full bg-transparent border border-primary text-primary font-bold py-3 !rounded-button hover:bg-primary/10 transition-all duration-300 mt-6 whitespace-nowrap">
VIEW FULL LEADERBOARD
</button>
</div>
<div class="glass-effect rounded-lg p-8">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Active Challenges</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-fire-line text-primary"></i>
</div>
</div>
<div class="space-y-6">
<div class="glass-effect p-4 rounded-lg">
<div class="flex justify-between items-center mb-3">
<h4 class="text-white font-semibold">30-Day Squat Challenge</h4>
<span class="text-xs bg-primary/20 text-primary py-1 px-2 rounded">5 DAYS LEFT</span>
</div>
<p class="text-sm text-lightGray mb-4">Complete 100 squats daily for 30 days to strengthen your lower body and core.</p>
<div class="flex justify-between items-center">
<div class="flex -space-x-2">
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c1&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c2&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c3&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark flex items-center justify-center bg-darkGray">
<span class="text-xs text-white">+42</span>
</div>
</div>
<button class="bg-primary/10 text-primary font-bold py-1 px-4 text-sm !rounded-button hover:bg-primary/20 transition-all duration-300 whitespace-nowrap">
JOIN
</button>
</div>
</div>
<div class="glass-effect p-4 rounded-lg">
<div class="flex justify-between items-center mb-3">
<h4 class="text-white font-semibold">10K Steps Daily</h4>
<span class="text-xs bg-secondary/20 text-secondary py-1 px-2 rounded">ONGOING</span>
</div>
<p class="text-sm text-lightGray mb-4">Commit to walking 10,000 steps every day for improved cardiovascular health and weight management.</p>
<div class="flex justify-between items-center">
<div class="flex -space-x-2">
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c4&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c5&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c6&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark flex items-center justify-center bg-darkGray">
<span class="text-xs text-white">+89</span>
</div>
</div>
<button class="bg-primary/10 text-primary font-bold py-1 px-4 text-sm !rounded-button hover:bg-primary/20 transition-all duration-300 whitespace-nowrap">
JOIN
</button>
</div>
</div>
<div class="glass-effect p-4 rounded-lg">
<div class="flex justify-between items-center mb-3">
<h4 class="text-white font-semibold">Bench Press PR</h4>
<span class="text-xs bg-primary/20 text-primary py-1 px-2 rounded">2 WEEKS LEFT</span>
</div>
<p class="text-sm text-lightGray mb-4">Increase your bench press personal record by at least 10% within the challenge period.</p>
<div class="flex justify-between items-center">
<div class="flex -space-x-2">
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c7&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c8&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20person%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=c9&orientation=squarish')"></div>
<div class="w-8 h-8 rounded-full border-2 border-dark flex items-center justify-center bg-darkGray">
<span class="text-xs text-white">+36</span>
</div>
</div>
<button class="bg-primary/10 text-primary font-bold py-1 px-4 text-sm !rounded-button hover:bg-primary/20 transition-all duration-300 whitespace-nowrap">
JOIN
</button>
</div>
</div>
</div>
<button class="w-full bg-transparent border border-primary text-primary font-bold py-3 !rounded-button hover:bg-primary/10 transition-all duration-300 mt-6 whitespace-nowrap">
CREATE A CHALLENGE
</button>
</div>
<div class="glass-effect rounded-lg p-8">
<div class="flex justify-between items-center mb-8">
<h3 class="orbitron text-2xl font-bold text-white">Activity Feed</h3>
<div class="w-8 h-8 flex items-center justify-center">
<i class="ri-pulse-line text-primary"></i>
</div>
</div>
<div class="space-y-6 max-h-[500px] overflow-y-auto custom-scrollbar pr-2">
<div class="flex gap-4">
<div class="w-10 h-10 rounded-full bg-cover bg-center flex-shrink-0" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20female%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=a1&orientation=squarish')"></div>
<div>
<div class="flex items-center gap-2 mb-1">
<h4 class="text-white font-semibold">Olivia Parker</h4>
<span class="text-xs text-lightGray">15 min ago</span>
</div>
<p class="text-sm text-lightGray mb-2">Just completed the HIIT Shred workout! Burned 450 calories in just 30 minutes. 🔥</p>
<div class="flex gap-4">
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-heart-line"></i>
</div>
<span>24</span>
</div>
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-chat-1-line"></i>
</div>
<span>5</span>
</div>
</div>
</div>
</div>
<div class="flex gap-4">
<div class="w-10 h-10 rounded-full bg-cover bg-center flex-shrink-0" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=a2&orientation=squarish')"></div>
<div>
<div class="flex items-center gap-2 mb-1">
<h4 class="text-white font-semibold">Ryan Thompson</h4>
<span class="text-xs text-lightGray">42 min ago</span>
</div>
<p class="text-sm text-lightGray mb-2">New deadlift PR! 405 lbs for 3 reps. Hard work is paying off. 💪</p>
<div class="glass-effect p-3 rounded-lg mb-2">
<div class="flex items-center gap-2 mb-1">
<div class="w-6 h-6 rounded-full bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=a3&orientation=squarish')"></div>
<h5 class="text-white text-sm font-semibold">David Williams</h5>
</div>
<p class="text-xs text-lightGray">Beast mode! Keep crushing it man!</p>
</div>
<div class="flex gap-4">
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-heart-line"></i>
</div>
<span>56</span>
</div>
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-chat-1-line"></i>
</div>
<span>12</span>
</div>
</div>
</div>
</div>
<div class="flex gap-4">
<div class="w-10 h-10 rounded-full bg-cover bg-center flex-shrink-0" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20female%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=a4&orientation=squarish')"></div>
<div>
<div class="flex items-center gap-2 mb-1">
<h4 class="text-white font-semibold">Jessica Lee</h4>
<span class="text-xs text-lightGray">1 hour ago</span>
</div>
<p class="text-sm text-lightGray mb-2">Day 15 of the 30-Day Squat Challenge complete! My legs are on fire but I'm loving the results already!</p>
<div class="h-40 bg-cover bg-center rounded-lg mb-2" style="background-image: url('https://readdy.ai/api/search-image?query=woman%20performing%20squat%20exercise%20in%20gym%2C%20detailed%20muscle%20definition%2C%20professional%20lighting%2C%20dark%20atmosphere%20with%20blue%20highlights%2C%20ultra-realistic%2C%20high-quality%20fitness%20photography&width=600&height=400&seq=a5&orientation=landscape')"></div>
<div class="flex gap-4">
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-heart-line"></i>
</div>
<span>78</span>
</div>
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-chat-1-line"></i>
</div>
<span>23</span>
</div>
</div>
</div>
</div>
<div class="flex gap-4">
<div class="w-10 h-10 rounded-full bg-cover bg-center flex-shrink-0" style="background-image: url('https://readdy.ai/api/search-image?query=athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=a6&orientation=squarish')"></div>
<div>
<div class="flex items-center gap-2 mb-1">
<h4 class="text-white font-semibold">Michael Anderson</h4>
<span class="text-xs text-lightGray">3 hours ago</span>
</div>
<p class="text-sm text-lightGray mb-2">Just signed up for the Power Building program! Excited to start this journey. Any tips from those who've completed it?</p>
<div class="flex gap-4">
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-heart-line"></i>
</div>
<span>32</span>
</div>
<div class="flex items-center gap-1 text-sm text-lightGray cursor-pointer hover:text-primary transition-colors">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-chat-1-line"></i>
</div>
<span>18</span>
</div>
</div>
</div>
</div>
</div>
<div class="mt-6 relative">
<input type="text" placeholder="Share your workout..." class="w-full bg-darkGray border-none rounded-lg px-4 py-3 pr-12 focus:outline-none focus:ring-2 focus:ring-primary text-white text-sm">
<button class="absolute right-3 top-1/2 transform -translate-y-1/2 w-8 h-8 flex items-center justify-center bg-primary rounded-full">
<i class="ri-send-plane-fill text-black"></i>
</button>
</div>
</div>
</div>
</div>
</section>
<!-- Success Stories -->
<section class="py-20">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">SUCCESS STORIES</h2>
<p class="text-lightGray max-w-2xl mx-auto">Real transformations from our dedicated members who achieved their fitness goals.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
<div class="glass-effect rounded-lg overflow-hidden">
<div class="h-64 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=before%20and%20after%20fitness%20transformation%2C%20muscular%20male%20body%2C%20professional%20lighting%2C%20dark%20background%20with%20blue%20highlights%2C%20ultra-realistic&width=600&height=400&seq=trans1&orientation=landscape')"></div>
<div class="p-6">
<div class="flex items-center gap-4 mb-4">
<div class="w-12 h-12 rounded-full bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=confident%20athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=test1&orientation=squarish')"></div>
<div>
<h4 class="text-white font-bold">Christopher Bennett</h4>
<p class="text-sm text-lightGray">Lost 45 lbs in 6 months</p>
</div>
</div>
<p class="text-lightGray text-sm mb-4">"The Power Building program completely transformed my approach to fitness. Not only did I lose weight, but I also gained significant muscle mass and strength."</p>
<div class="flex justify-between items-center">
<div class="flex gap-2">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Power Building</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Nutrition</span>
</div>
<button class="text-primary hover:text-white transition-colors">Read More</button>
</div>
</div>
</div>
<div class="glass-effect rounded-lg overflow-hidden">
<div class="h-64 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=before%20and%20after%20fitness%20transformation%2C%20athletic%20female%20body%2C%20professional%20lighting%2C%20dark%20background%20with%20purple%20highlights%2C%20ultra-realistic&width=600&height=400&seq=trans2&orientation=landscape')"></div>
<div class="p-6">
<div class="flex items-center gap-4 mb-4">
<div class="w-12 h-12 rounded-full bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=confident%20athletic%20female%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=test2&orientation=squarish')"></div>
<div>
<h4 class="text-white font-bold">Sarah Martinez</h4>
<p class="text-sm text-lightGray">Gained strength & confidence</p>
</div>
</div>
<p class="text-lightGray text-sm mb-4">"HIIT Shred helped me break through plateaus I never thought possible. The community support and expert guidance made all the difference."</p>
<div class="flex justify-between items-center">
<div class="flex gap-2">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">HIIT Shred</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Cardio</span>
</div>
<button class="text-primary hover:text-white transition-colors">Read More</button>
</div>
</div>
</div>
<div class="glass-effect rounded-lg overflow-hidden">
<div class="h-64 bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=before%20and%20after%20fitness%20transformation%2C%20muscular%20male%20body%2C%20professional%20lighting%2C%20dark%20background%20with%20blue%20highlights%2C%20ultra-realistic&width=600&height=400&seq=trans3&orientation=landscape')"></div>
<div class="p-6">
<div class="flex items-center gap-4 mb-4">
<div class="w-12 h-12 rounded-full bg-cover bg-center" style="background-image: url('https://readdy.ai/api/search-image?query=confident%20athletic%20male%20face%20portrait%2C%20professional%20lighting%2C%20dark%20background%2C%20realistic&width=100&height=100&seq=test3&orientation=squarish')"></div>
<div>
<h4 class="text-white font-bold">Marcus Johnson</h4>
<p class="text-sm text-lightGray">Achieved competition goals</p>
</div>
</div>
<p class="text-lightGray text-sm mb-4">"The Mass Gainer program helped me add 15 lbs of lean muscle mass. The detailed nutrition plans and workout routines were game-changers."</p>
<div class="flex justify-between items-center">
<div class="flex gap-2">
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Mass Gainer</span>
<span class="bg-darkGray text-lightGray text-xs py-1 px-3 rounded-full">Strength</span>
</div>
<button class="text-primary hover:text-white transition-colors">Read More</button>
</div>
</div>
</div>
</div>
<div class="text-center mt-12">
<button class="bg-transparent border border-primary text-primary font-bold py-3 px-8 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap">
VIEW ALL SUCCESS STORIES
</button>
</div>
</div>
</section>
<!-- Features Section -->
<section class="py-20 gradient-bg">
<div class="container mx-auto px-6">
<div class="text-center mb-16">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-4">WHY CHOOSE US</h2>
<p class="text-lightGray max-w-2xl mx-auto">Experience the future of fitness with our cutting-edge features and expert guidance.</p>
</div>
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
<div class="glass-effect p-6 rounded-lg text-center">
<div class="w-16 h-16 mx-auto mb-6 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-3d-cube-line text-primary text-3xl"></i>
</div>
<h3 class="text-white text-xl font-bold mb-4">3D Exercise Modeling</h3>
<p class="text-lightGray">Visualize proper form and technique with interactive 3D exercise demonstrations.</p>
</div>
<div class="glass-effect p-6 rounded-lg text-center">
<div class="w-16 h-16 mx-auto mb-6 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-ai-generate text-primary text-3xl"></i>
</div>
<h3 class="text-white text-xl font-bold mb-4">AI-Powered Training</h3>
<p class="text-lightGray">Get personalized workout recommendations based on your progress and goals.</p>
</div>
<div class="glass-effect p-6 rounded-lg text-center">
<div class="w-16 h-16 mx-auto mb-6 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-team-line text-primary text-3xl"></i>
</div>
<h3 class="text-white text-xl font-bold mb-4">Expert Trainers</h3>
<p class="text-lightGray">Access to certified fitness professionals for guidance and support.</p>
</div>
<div class="glass-effect p-6 rounded-lg text-center">
<div class="w-16 h-16 mx-auto mb-6 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-heart-pulse-line text-primary text-3xl"></i>
</div>
<h3 class="text-white text-xl font-bold mb-4">Health Analytics</h3>
<p class="text-lightGray">Track your progress with detailed health and fitness metrics.</p>
</div>
</div>
<div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mt-12">
<div class="glass-effect p-8 rounded-lg">
<h3 class="text-white text-2xl font-bold mb-6">Membership Benefits</h3>
<div class="space-y-4">
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-lightGray">Unlimited access to all workout programs</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-lightGray">Personalized nutrition plans and tracking</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-lightGray">24/7 access to certified trainers</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-check-line text-primary"></i>
</div>
<p class="text-lightGray">Progress tracking and analytics</p>
</div>
</div>
</div>
<div class="glass-effect p-8 rounded-lg">
<h3 class="text-white text-2xl font-bold mb-6">Training Approach</h3>
<div class="space-y-4">
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-focus-3-line text-primary"></i>
</div>
<p class="text-lightGray">Scientifically proven workout methodologies</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-heart-line text-primary"></i>
</div>
<p class="text-lightGray">Focus on sustainable, long-term results</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-shield-check-line text-primary"></i>
</div>
<p class="text-lightGray">Safe and effective progression systems</p>
</div>
<div class="flex items-center gap-4">
<div class="w-8 h-8 flex items-center justify-center bg-primary/10 rounded-full">
<i class="ri-customer-service-2-line text-primary"></i>
</div>
<p class="text-lightGray">Continuous support and motivation</p>
</div>
</div>
</div>
</div>
</div>
</section>
<!-- Call to Action -->
<section class="py-20 relative">
<div class="absolute inset-0 bg-cover bg-center opacity-30" style="background-image: url('https://readdy.ai/api/search-image?query=modern%20gym%20interior%20with%20high-tech%20equipment%2C%20dark%20atmosphere%20with%20blue%20and%20purple%20neon%20lighting%2C%20sleek%20black%20surfaces%2C%20futuristic%20design%2C%20professional%20photography%2C%20ultra-realistic%2C%20cinematic%20lighting&width=1600&height=800&seq=cta&orientation=landscape')"></div>
<div class="container mx-auto px-6 relative z-10">
<div class="max-w-3xl mx-auto text-center">
<h2 class="orbitron text-4xl md:text-5xl font-bold gradient-text mb-6">READY TO TRANSFORM YOUR BODY?</h2>
<p class="text-lightGray text-lg mb-10">Join thousands of members who have already changed their lives with our cutting-edge fitness platform. Start your journey today with a 7-day free trial.</p>
<div class="flex flex-col sm:flex-row justify-center gap-4">
<button class="bg-primary text-black font-bold py-3 px-8 !rounded-button pulse-animation whitespace-nowrap">
START FREE TRIAL
</button>
<button class="bg-transparent border border-primary text-primary font-bold py-3 px-8 !rounded-button hover:bg-primary/10 transition-all duration-300 whitespace-nowrap">
SCHEDULE A DEMO
</button>
</div>
<div class="mt-12 flex flex-col md:flex-row items-center justify-center gap-8">
<div class="flex items-center gap-2">
<div class="w-6 h-6 flex items-center justify-center">
<i class="ri-check-line text-primary"></i>
</div>
<span class="text-white">No Credit Card Required</span>
</div>
<div class="flex items-center gap-2">
<div class="w-6 h-6 flex items-center justify-center">
<i class="ri-check-line text-primary"></i>
</div>
<span class="text-white">Cancel Anytime</span>
</div>
<div class="flex items-center gap-2">
<div class="w-6 h-6 flex items-center justify-center">
<i class="ri-check-line text-primary"></i>
</div>
<span class="text-white">Full Access to All Features</span>
</div>
</div>
</div>
</div>
</section>
<!-- Footer -->
<footer class="gradient-bg py-16">
<div class="container mx-auto px-6">
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12">
<div>
<div class="flex items-center mb-6">
<div class="mr-2 w-10 h-10 flex items-center justify-center bg-primary rounded-lg">
<i class="ri-boxing-line ri-2x text-black"></i>
</div>
<div>
<h1 class="text-2xl font-['Pacifico'] gradient-text tracking-wider">FLEX</h1>
<span class="text-[10px] text-lightGray uppercase tracking-[0.2em] -mt-1 block">Premium Fitness</span>
</div>
</div>
<p class="text-lightGray mb-6">Experience the next generation of fitness with our cutting-edge 3D workout technology. Track progress, visualize results, and push beyond your limits.</p>
<div class="flex space-x-4">
<a href="https://facebook.com" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center bg-darkGray rounded-full hover:bg-primary/20 transition-all duration-300">
<i class="ri-facebook-fill text-primary"></i>
</a>
<a href="https://twitter.com" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center bg-darkGray rounded-full hover:bg-primary/20 transition-all duration-300">
<i class="ri-twitter-x-fill text-primary"></i>
</a>
<a href="https://instagram.com" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center bg-darkGray rounded-full hover:bg-primary/20 transition-all duration-300">
<i class="ri-instagram-fill text-primary"></i>
</a>
<a href="https://youtube.com" target="_blank" rel="noopener noreferrer" class="w-10 h-10 flex items-center justify-center bg-darkGray rounded-full hover:bg-primary/20 transition-all duration-300">
<i class="ri-youtube-fill text-primary"></i>
</a>
</div>
</div>
<div>
<h3 class="text-white font-bold text-xl mb-6">Quick Links</h3>
<ul class="space-y-3">
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Home</a></li>
<li><a href="#workouts" class="text-lightGray hover:text-primary transition-colors">Workouts</a></li>
<li><a href="#exercises" class="text-lightGray hover:text-primary transition-colors">Exercise Library</a></li>
<li><a href="#programs" class="text-lightGray hover:text-primary transition-colors">Training Programs</a></li>
<li><a href="#community" class="text-lightGray hover:text-primary transition-colors">Community</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">About Us</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Contact</a></li>
</ul>
</div>
<div>
<h3 class="text-white font-bold text-xl mb-6">Support</h3>
<ul class="space-y-3">
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Help Center</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">FAQ</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Privacy Policy</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Terms of Service</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Refund Policy</a></li>
<li><a href="#" class="text-lightGray hover:text-primary transition-colors">Cookie Policy</a></li>
</ul>
</div>
<div>
<h3 class="text-white font-bold text-xl mb-6">Subscribe</h3>
<p class="text-lightGray mb-4">Get the latest news and updates directly to your inbox.</p>
<div class="relative mb-6">
<input type="email" placeholder="Your email address" class="w-full bg-darkGray border-none rounded-lg px-4 py-3 pr-12 focus:outline-none focus:ring-2 focus:ring-primary text-white text-sm">
<button class="absolute right-3 top-1/2 transform -translate-y-1/2 w-8 h-8 flex items-center justify-center bg-primary rounded-full">
<i class="ri-arrow-right-line text-black"></i>
</button>
</div>
<div class="space-y-3">
<div class="flex items-center gap-3">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-map-pin-line text-primary"></i>
</div>
<span class="text-lightGray">123 Fitness Street, Gym City, GC 12345</span>
</div>
<div class="flex items-center gap-3">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-mail-line text-primary"></i>
</div>
<span class="text-lightGray">info@flexgym.com</span>
</div>
<div class="flex items-center gap-3">
<div class="w-5 h-5 flex items-center justify-center">
<i class="ri-phone-line text-primary"></i>
</div>
<span class="text-lightGray">+1 (555) 123-4567</span>
</div>
</div>
</div>
</div>
<div class="mt-12 pt-8 border-t border-darkGray flex flex-col md:flex-row justify-between items-center">
<p class="text-lightGray text-sm mb-4 md:mb-0">© 2025 FLEX. All rights reserved.</p>
<div class="flex items-center space-x-4">
<div class="w-8 h-5 flex items-center justify-center">
<i class="ri-visa-fill text-lightGray"></i>
</div>
<div class="w-8 h-5 flex items-center justify-center">
<i class="ri-mastercard-fill text-lightGray"></i>
</div>
<div class="w-8 h-5 flex items-center justify-center">
<i class="ri-paypal-fill text-lightGray"></i>
</div>
<div class="w-8 h-5 flex items-center justify-center">
<i class="ri-apple-fill text-lightGray"></i>
</div>
<div class="w-8 h-5 flex items-center justify-center">
<i class="ri-google-fill text-lightGray"></i>
</div>
</div>
</div>
</div>
</footer>
<script>
// Exercise filtering function
function filterExercises(category) {
// Get all exercise filter buttons
const filterButtons = document.querySelectorAll('.exercise-filter-btn');
// Remove active state from all buttons
filterButtons.forEach(btn => {
btn.classList.remove('bg-primary', 'text-black');
btn.classList.add('bg-transparent', 'text-lightGray');
});
// Add active state to clicked button
const activeButton = document.querySelector(`.exercise-filter-btn:nth-child(${
category === 'all' ? 1 :
category === 'chest' ? 2 :
category === 'back' ? 3 :
category === 'shoulders' ? 4 :
category === 'arms' ? 5 :
category === 'legs' ? 6 : 7
})`);
if (activeButton) {
activeButton.classList.remove('bg-transparent', 'text-lightGray');
activeButton.classList.add('bg-primary', 'text-black');
}
// Get all exercise cards
const exerciseCards = document.querySelectorAll('.exercise-card');
exerciseCards.forEach(card => {
const cardCategory = card.getAttribute('data-category') || '';
if (category === 'all' || cardCategory.includes(category)) {
card.style.display = 'block';
card.classList.add('animate-fade-in');
} else {
card.style.display = 'none';
card.classList.remove('animate-fade-in');
}
});
// Show feedback message
const feedback = document.createElement('div');
feedback.className = 'fixed top-24 left-1/2 transform -translate-x-1/2 bg-primary text-black px-4 py-2 rounded-full text-sm z-50';
feedback.textContent = `Showing ${category.toUpperCase()} exercises`;
document.body.appendChild(feedback);
setTimeout(() => feedback.remove(), 2000);
}
// Handle all navigation buttons
document.addEventListener('DOMContentLoaded', function() {
// Add click handlers for all navigation buttons
const navButtons = document.querySelectorAll('a[href^="#"], button[data-target]');
navButtons.forEach(button => {
button.addEventListener('click', function(e) {
const target = this.getAttribute('href') || this.getAttribute('data-target');
if (target && target.startsWith('#')) {
e.preventDefault();
const targetElement = document.querySelector(target);
if (targetElement) {
const headerHeight = document.querySelector('header').offsetHeight;
const targetPosition = targetElement.offsetTop - headerHeight;
window.scrollTo({
top: targetPosition,
behavior: 'smooth'
});
}
}
});
});
});
function handleSearch(event) {
event.preventDefault();
const searchTerm = document.getElementById('searchInput').value.toLowerCase();
const sections = ['workouts', 'exercises', 'programs'];
for (const section of sections) {
const sectionElement = document.getElementById(section);
if (sectionElement && sectionElement.textContent.toLowerCase().includes(searchTerm)) {
sectionElement.scrollIntoView({ behavior: 'smooth' });
// Create and show feedback message
const feedback = document.createElement('div');
feedback.className = 'fixed top-24 left-1/2 transform -translate-x-1/2 bg-primary text-black px-4 py-2 rounded-full text-sm z-50';
feedback.textContent = `Found matches in ${section.charAt(0).toUpperCase() + section.slice(1)} section`;
document.body.appendChild(feedback);
// Remove feedback after 3 seconds
setTimeout(() => feedback.remove(), 3000);
return false;
}
}
// Show no results found message
const noResults = document.createElement('div');
noResults.className = 'fixed top-24 left-1/2 transform -translate-x-1/2 bg-red-500 text-white px-4 py-2 rounded-full text-sm z-50';
noResults.textContent = 'No results found';
document.body.appendChild(noResults);
setTimeout(() => noResults.remove(), 3000);
return false;
}
document.addEventListener('DOMContentLoaded', function() {
// Navigation smooth scroll
const navLinks = document.querySelectorAll('.nav-link');
navLinks.forEach(link => {
link.addEventListener('click', function(e) {
e.preventDefault();
const targetId = this.getAttribute('href');
if(targetId === '#') {
window.scrollTo({
top: 0,
behavior: 'smooth'
});
} else {
const targetSection = document.querySelector(targetId);
if(targetSection) {
const headerHeight = document.querySelector('header').offsetHeight;
const targetPosition = targetSection.offsetTop - headerHeight;
window.scrollTo({
top: targetPosition,
behavior: 'smooth'
});
}
}
// Update active state
navLinks.forEach(navLink => navLink.classList.remove('text-primary', 'neon-text'));
this.classList.add('text-primary', 'neon-text');
});
});
// Update active menu item on scroll
window.addEventListener('scroll', function() {
const sections = document.querySelectorAll('section');
const headerHeight = document.querySelector('header').offsetHeight;
sections.forEach(section => {
const sectionTop = section.offsetTop - headerHeight - 100;
const sectionBottom = sectionTop + section.offsetHeight;
const scrollPosition = window.scrollY;
const sectionId = '#' + section.getAttribute('id');
if(scrollPosition >= sectionTop && scrollPosition < sectionBottom) {
navLinks.forEach(link => {
link.classList.remove('text-primary', 'neon-text');
if(link.getAttribute('href') === sectionId) {
link.classList.add('text-primary', 'neon-text');
}
});
}
});
// Handle home link active state
if(window.scrollY < 100) {
navLinks.forEach(link => {
link.classList.remove('text-primary', 'neon-text');
if(link.getAttribute('href') === '#') {
link.classList.add('text-primary', 'neon-text');
}
});
}
});
// Header scroll effect
const header = document.querySelector('header');
window.addEventListener('scroll', function() {
if (window.scrollY > 50) {
header.classList.add('py-2');
header.classList.remove('py-4');
} else {
header.classList.add('py-4');
header.classList.remove('py-2');
}
});
// Body metrics chart
const bodyMetricsChart = echarts.init(document.getElementById('bodyMetricsChart'));
const bodyMetricsOption = {
animation: false,
color: ['rgba(87, 181, 231, 1)'],
tooltip: {
trigger: 'axis',
backgroundColor: 'rgba(255, 255, 255, 0.8)',
textStyle: {
color: '#1f2937'
}
},
grid: {
top: 10,
right: 10,
bottom: 20,
left: 40
},
xAxis: {
type: 'category',
data: ['Week 1', 'Week 2', 'Week 3', 'Week 4', 'Week 5', 'Week 6', 'Week 7', 'Week 8'],
axisLine: {
lineStyle: {
color: '#333'
}
},
axisLabel: {
color: '#E0E0E0',
fontSize: 10
}
},
yAxis: {
type: 'value',
axisLine: {
lineStyle: {
color: '#333'
}
},
splitLine: {
lineStyle: {
color: '#333'
}
},
axisLabel: {
color: '#E0E0E0',
fontSize: 10
}
},
series: [{
data: [185, 183, 181, 179, 177, 176, 174, 172],
type: 'line',
smooth: true,
symbol: 'none',
lineStyle: {
width: 3
},
areaStyle: {
color: new echarts.graphic.LinearGradient(0, 0, 0, 1, [
{
offset: 0,
color: 'rgba(87, 181, 231, 0.3)'
},
{
offset: 1,
color: 'rgba(87, 181, 231, 0.1)'
}
])
}
}]
};
bodyMetricsChart.setOption(bodyMetricsOption);
// Radio button change event
const radioButtons = document.querySelectorAll('input[name="metricType"]');
radioButtons.forEach(radio => {
radio.addEventListener('change', function() {
if (this.checked && this.nextElementSibling.nextElementSibling.textContent === 'Weight') {
bodyMetricsOption.series[0].data = [185, 183, 181, 179, 177, 176, 174, 172];
} else if (this.checked && this.nextElementSibling.nextElementSibling.textContent === 'Body Fat') {
bodyMetricsOption.series[0].data = [22, 21, 20, 19, 18.5, 18, 17.5, 17];
} else if (this.checked && this.nextElementSibling.nextElementSibling.textContent === 'Muscle Mass') {
bodyMetricsOption.series[0].data = [145, 147, 149, 151, 152, 154, 155, 157];
}
bodyMetricsChart.setOption(bodyMetricsOption);
});
});
// Resize chart when window size changes
window.addEventListener('resize', function() {
bodyMetricsChart.resize();
});
});
</script>
</body>
</html>
