<script setup>
import HelloWorld from './components/HelloWorld.vue';
import Lorem from './components/Lorem.vue';
import { ref } from 'vue';
import Lorem2 from './components/Lorem2.vue';

let s = ref(0); // Usando ref para reatividade

// Função que alterna a variável `s`
function proxPage() {
  if (s.value < pages.length - 1) {
    s.value++; // Avança para a próxima página, mas sem ultrapassar o número total de páginas
  }
}

function antPage() {
  if (s.value > 0) {
    s.value--; // Volta para a página anterior, mas sem ultrapassar a página inicial
  }
}

const pages = [HelloWorld, Lorem, Lorem2];
</script>

<template>
  <main>
    <transition name="fade" mode="out-in">
      <component :is="pages[s]" @prox-page="proxPage" @ant-page="antPage" :key="s" />
    </transition>
  </main>
</template>

<style scoped>
/* Transição de opacidade */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.2s ease-out;
}

/* Inicialmente, a página vai estar invisível (opacidade 0) */
.fade-enter, .fade-leave-to /* .fade-leave-active em versões anteriores do Vue */ {
  opacity: 0;
}

/* Quando a página entra, ela vai ter opacidade 1 */
.fade-enter-to {
  opacity: 1;
}
</style>
