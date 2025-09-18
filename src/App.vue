<template>
  <div class="min-h-screen w-full bg-gradient-to-br from-[#f8fafc] via-[#f1f5f9] to-[#f0e7ff] text-[#23272f] font-['Inter','Merriweather','serif'] flex flex-col">
    <header class="w-full flex justify-between items-center px-8 py-6 bg-white/80 shadow-lg fixed top-0 left-0 z-30">
      <span class="text-xl font-bold tracking-tight text-[#6366f1]">Daan<span class="text-[#e1306c]">RC</span></span>
      <nav class="flex gap-8 text-base font-medium">
        <a href="#tecnologias" class="hover:text-[#6366f1] transition">Skills</a>
        <a href="#proyectos" class="hover:text-[#e1306c] transition">Proyectos</a>
        <a href="#contacto" class="hover:text-[#25d366] transition">Contacto</a>
      </nav>
    </header>
    <section class="relative flex flex-col md:flex-row items-center justify-center gap-10 pt-32 pb-16 px-6 md:px-0 animate-fade-in">
      <div class="relative flex-shrink-0">
        <img :src="fotoDAANRC" alt="Daniel Adrian Roque Cortes" class="w-44 h-44 md:w-56 md:h-56 rounded-full border-8 border-[#6366f1] shadow-2xl object-cover object-center z-10 hover:scale-105 transition-transform duration-300" />
        <div class="absolute -bottom-4 -right-4 flex gap-2">
          <a href="https://github.com/FuckingGodRoque" target="_blank" class="rounded-full bg-white shadow-lg p-3 hover:bg-[#23272f] hover:scale-110 transition-all"><img :src="github" class="w-8 h-8 object-contain" title="GitHub" /></a>
          <a href="https://instagram.com/adrn.rc" target="_blank" class="rounded-full bg-white shadow-lg p-3 hover:bg-[#e1306c] hover:scale-110 transition-all"><img :src="instagram" class="w-8 h-8 object-contain" title="Instagram" /></a>
          <a href="https://wa.me/524439241432" target="_blank" class="rounded-full bg-white shadow-lg p-3 hover:bg-[#25d366] hover:scale-110 transition-all"><img :src="whatsapp" class="w-8 h-8 object-contain" title="WhatsApp" /></a>
          <a href="mailto:droque.cts@gmail.com" class="rounded-full bg-white shadow-lg p-3 hover:bg-[#ea4335] hover:scale-110 transition-all"><img :src="gmail" class="w-8 h-8 object-contain" title="Gmail" /></a>
        </div>
      </div>
      <div class="max-w-xl text-center md:text-left">
        <h1 class="text-4xl md:text-5xl font-extrabold mb-3 leading-tight"><span class="text-[#6366f1]">Daniel Adrian</span> Roque Cortes</h1>
  <p class="text-[#64748b] text-lg mb-4 font-medium">Full Stack Developer <span class="text-[#e1306c]">|</span> Estudiante de ingeniería en sistemas computacionales</p>
        <p class="text-[#23272f] text-base md:text-lg leading-relaxed mb-2">Apasionado por crear experiencias digitales <span class="bg-[#f3e8ff] px-2 rounded">visuales</span>, <span class="bg-[#dbeafe] px-2 rounded">interactivas</span> y <span class="bg-[#bbf7d0] px-2 rounded">modernas</span>. Creativo, responsable y siempre aprendiendo nuevas tecnologías.</p>
      </div>
    </section>
    <section id="tecnologias" class="w-full max-w-4xl mx-auto px-4 py-8 animate-slide-in">
      <h2 class="text-2xl font-bold text-[#6366f1] mb-6 text-center">Skills & Tecnologías</h2>
      <div class="flex flex-wrap justify-center gap-4">
        <div v-for="tech in tecnologias" :key="tech.name" class="flex items-center gap-2 px-5 py-2 rounded-full bg-gradient-to-r from-[#f3e8ff] to-[#dbeafe] shadow hover:from-[#6366f1]/20 hover:to-[#e1306c]/20 transition-all border border-[#e0e7ef]">
          <img :src="tech.logo" :alt="tech.name" class="w-7 h-7 object-contain" :title="tech.name" />
          <span class="text-base font-semibold text-[#475569]">{{ tech.name }}</span>
        </div>
      </div>
    </section>
    <section id="proyectos" class="w-full max-w-6xl mx-auto px-4 py-12 animate-fade-in">
      <h2 class="text-2xl font-bold text-[#e1306c] mb-8 text-center">Proyectos Destacados</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10">
        <a v-for="proyecto in proyectos" :key="proyecto.name" :href="proyecto.link" target="_blank" class="group relative rounded-3xl shadow-2xl bg-gradient-to-br from-[#f3e8ff] to-[#dbeafe] hover:from-[#6366f1]/10 hover:to-[#e1306c]/10 transition-all duration-300 p-7 flex flex-col items-center hover:scale-105 border-2 border-transparent hover:border-[#6366f1]">
          <div class="w-28 h-28 flex items-center justify-center rounded-2xl bg-white shadow-lg mb-4 group-hover:ring-4 group-hover:ring-[#a5b4fc] transition-all duration-300">
            <img :src="proyecto.logo" :alt="proyecto.name" class="w-20 h-20 object-contain transition-transform duration-300 group-hover:scale-110" />
          </div>
          <span class="text-lg font-bold text-[#23272f] group-hover:text-[#6366f1] text-center">{{ proyecto.name }}</span>
          <span class="text-xs text-[#64748b] text-center mt-2">{{ proyecto.desc }}</span>
        </a>
      </div>
    </section>
    <section id="contacto" class="w-full max-w-3xl mx-auto px-4 py-12 animate-slide-in">
      <h2 class="text-2xl font-bold text-[#25d366] mb-8 text-center">Contacto</h2>
      <div class="flex flex-wrap justify-center gap-8">
        <a href="https://wa.me/524439241432" target="_blank" class="flex flex-col items-center gap-2 group">
          <div class="rounded-full bg-white shadow-lg p-5 hover:bg-[#25d366] transition-all"><img :src="whatsapp" class="w-10 h-10 object-contain group-hover:scale-110 transition-transform" alt="WhatsApp"/></div>
          <span class="font-semibold text-[#23272f] group-hover:text-[#25d366]">WhatsApp</span>
          <span class="text-sm text-[#64748b]">443 924 1432</span>
        </a>
        <a href="https://instagram.com/adrn.rc" target="_blank" class="flex flex-col items-center gap-2 group">
          <div class="rounded-full bg-white shadow-lg p-5 hover:bg-[#e1306c] transition-all"><img :src="instagram" class="w-10 h-10 object-contain group-hover:scale-110 transition-transform" alt="Instagram"/></div>
          <span class="font-semibold text-[#23272f] group-hover:text-[#e1306c]">Instagram</span>
          <span class="text-sm text-[#64748b]">@adrn.rc</span>
        </a>
        <a href="mailto:droque.cts@gmail.com" class="flex flex-col items-center gap-2 group">
          <div class="rounded-full bg-white shadow-lg p-5 hover:bg-[#ea4335] transition-all"><img :src="gmail" class="w-10 h-10 object-contain group-hover:scale-110 transition-transform" alt="Gmail"/></div>
          <span class="font-semibold text-[#23272f] group-hover:text-[#ea4335]">Correo</span>
          <span class="text-sm text-[#64748b]">droque.cts@gmail.com</span>
        </a>
        <a href="https://github.com/FuckingGodRoque" target="_blank" class="flex flex-col items-center gap-2 group">
          <div class="rounded-full bg-white shadow-lg p-5 hover:bg-[#23272f] transition-all"><img :src="github" class="w-10 h-10 object-contain group-hover:scale-110 transition-transform" alt="GitHub"/></div>
          <span class="font-semibold text-[#23272f] group-hover:text-[#6366f1]">GitHub</span>
          <span class="text-sm text-[#64748b]">github.com/FuckingGodRoque</span>
        </a>
      </div>
    </section>
    <!-- (Eliminado contenido duplicado y footer antiguo) -->
  </div>
</template>

<script setup>
import fotoDAANRC from './images/fotoDAANRC.jpg';
import github from './images/github.svg';
import instagram from './images/instagram.svg';
import whatsapp from './images/whatsapp.svg';
import gmail from './images/gmail.svg';
import tailwindcss from './images/tailwindcss.svg';
import react from './images/react.svg';
import nodejs from './images/nodejs.svg';
import mongodb from './images/mongodb.svg';
import js from './images/js.svg';
import ts from './images/ts.svg';
import python from './images/python.svg';
import html5 from './images/html5.svg';
import css3 from './images/css3.svg';
import csharp from './images/csharp.svg';
import java from './images/java.svg';
import sqlserver from './images/sqlserver.svg';
import postgres from './images/postgres.svg';
import logoBloomBeauty from './images/LogoBloomBeauty.png';
import logoCoffeeShop from './images/LogoCooffeeShop-App.png';
import logoTripTalk from './images/LogoTripTalk.png';

const tecnologias = [
  { name: 'JavaScript', logo: js },
  { name: 'TypeScript', logo: ts },
  { name: 'Python', logo: python },
  { name: 'React', logo: react },
  { name: 'Node.js', logo: nodejs },
  { name: 'MongoDB', logo: mongodb },
  { name: 'TailwindCSS', logo: tailwindcss },
  { name: 'HTML5', logo: html5 },
  { name: 'CSS3', logo: css3 },
  { name: 'C#', logo: csharp },
  { name: 'Java', logo: java },
  { name: 'SQL Server', logo: sqlserver },
  { name: 'PostgreSQL', logo: postgres },
];

const proyectos = [
  {
    name: 'Bloom Beauty',
    logo: logoBloomBeauty,
    link: 'https://github.com/FuckingGodRoque/Bloom-Beauty',
    desc: 'E-commerce de productos de belleza. React, Firebase, TailwindCSS. Permite explorar, comprar y gestionar productos de belleza de forma intuitiva.'
  },
  {
    name: 'CoffeeShop App',
    logo: logoCoffeeShop,
    link: 'https://github.com/ArmandoCasanova/coffeeshop-app',
    desc: 'App de pedidos para cafetería. React Native, Node.js, Firebase. Gestiona pedidos, menús y pagos en tiempo real para cafeterías.'
  },
  {
    name: 'TripTalk',
    logo: logoTripTalk,
    link: 'https://github.com/FuckingGodRoque/TripTalk',
    desc: 'Red social para viajeros. React, Node.js, MongoDB, TailwindCSS. Conecta viajeros, comparte experiencias y planifica viajes en comunidad.'
  },
];
</script>

<style>
@keyframes fade-in { 
  from { opacity: 0; } 
  to { opacity: 1; } 
}

@keyframes slide-in { 
  from { transform: translateY(40px); opacity: 0; } 
  to { transform: translateY(0); opacity: 1; } 
}

.animate-fade-in { 
  animation: fade-in 1.2s cubic-bezier(.4,0,.2,1) both; 
}

.animate-slide-in { 
  animation: slide-in 1.2s cubic-bezier(.4,0,.2,1) both; 
}
</style>