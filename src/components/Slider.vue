<template>
  <div class="slider-container">
    <div class="slider">
      <!-- Renderizamos el componente actual -->
      <component :is="pages[currentPage]" />
    </div>

    <!-- Botones de navegación -->
    <button class="nav-button left" @click="prevPage">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="hotpink" width="24px" height="24px">
        <path d="M15.41 16.59L10.83 12l4.58-4.59L14 6l-6 6 6 6z"/>
      </svg>
    </button>
    <button class="nav-button right" @click="nextPage">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="hotpink" width="24px" height="24px">
        <path d="M8.59 16.59L13.17 12 8.59 7.41 10 6l6 6-6 6z"/>
      </svg>
    </button>
  </div>
</template>

<script>
import PageOne from './PageOne.vue';
import PageTwo from './PageTwo.vue';
import PageThree from './PageThree.vue';

export default {
  name: 'Slider',
  components: {
    PageOne,
    PageTwo,
    PageThree,
  },
  data() {
    return {
      currentPage: 0, // Página inicial
      pages: ['PageOne', 'PageTwo', 'PageThree'], // Lista de componentes
    };
  },
  methods: {
    nextPage() {
      this.currentPage = (this.currentPage + 1) % this.pages.length;
    },
    prevPage() {
      this.currentPage = (this.currentPage - 1 + this.pages.length) % this.pages.length;
    },
  },
};
</script>

<style>
.slider-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: auto; /* Altura ajustada */
  position: relative;
  overflow: hidden;
}

.slider {
  width: 100%;
  height: auto; /* Ajuste de altura interna */
  /* border: 1px solid #ccc; */
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-button {
  position: absolute;
  top: 34%;
  transform: translateY(-50%);
  background-color: rgba(255, 192, 203, 0.8);
  border: none;
  border-radius: 50%;
  width: 50px;
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  font-size: 1.5rem;
  color: hotpink;
  outline: none;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.nav-button.left {
  left: 10px;
}

.nav-button.right {
  right: 10px;
}

.nav-button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

/* Responsividad */
.slider-container {
  height: auto; /* Ajuste también para la responsividad */
}

.slider {
  height: auto;
  /* max-height: 700px; */
}

.nav-button {
  width: 40px;
  height: 40px;
  font-size: 1.2rem;
}

@media (max-width: 768px) {
  .slider {
    height: 90%;
  }

  .nav-button {
    width: 35px;
    height: 35px;
    font-size: 1rem;
    top: 68%;
  }
}
</style>