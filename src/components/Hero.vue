<template>
  <div class="grid md:grid-cols-2 gap-8 items-center">
    <div>
      <h1 ref="title" class="text-5xl md:text-7xl font-extrabold leading-tight">Design & Motion</h1>
      <p ref="subtitle" class="mt-4 text-lg text-slate-300 max-w-xl">A concise line describing your specialty and the visual vibe from the image you made.</p>
      <div class="mt-8 flex gap-4">
        <a class="btn-primary px-6 py-3 rounded-md bg-amber-500 text-black font-medium" href="#work">See Work</a>
        <a class="px-6 py-3 rounded-md border border-slate-700 text-slate-300" href="#contact">Get In Touch</a>
      </div>
    </div>
    <div class="relative">
      <div ref="art" class="w-full h-80 md:h-96 rounded-xl overflow-hidden bg-gradient-to-br from-pink-600 via-purple-600 to-indigo-700 shadow-2xl">
        <!-- Placeholder for your image. Replace with <img> tag pointing to your artwork. -->
        <div class="w-full h-full flex items-center justify-center text-white/60">Your artwork here</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
import gsap from 'gsap';
import { animate } from '@motionone/dom';

const title = ref(null);
const subtitle = ref(null);
const art = ref(null);

onMounted(() => {
  gsap.from(title.value, { y: 40, opacity: 0, duration: 0.8, ease: 'power3.out' });
  gsap.from(subtitle.value, { y: 20, opacity: 0, duration: 0.9, delay: 0.15, ease: 'power3.out' });
  gsap.from(art.value, { scale: 0.98, opacity: 0, duration: 1.2, delay: 0.25, ease: 'elastic.out(1, .6)' });

  // Motion One subtle hover
  art.value.addEventListener('mouseenter', () => {
    animate(art.value, { scale: 1.03 }, { duration: 0.4 });
  });
  art.value.addEventListener('mouseleave', () => {
    animate(art.value, { scale: 1 }, { duration: 0.6 });
  });
});
</script>

<style scoped>
.btn-primary { transition: transform .15s ease, box-shadow .15s ease; }
.btn-primary:hover { transform: translateY(-3px); box-shadow: 0 10px 25px rgba(249,115,22,0.12); }
</style>
