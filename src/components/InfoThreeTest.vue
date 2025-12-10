<template>
  <div class="parent" id="50color">
    <div class="div1">
      <div class="title-wrapper">
        <h1 class="title">
          Plataforma de <strong style="border-bottom: 5px solid #008EB4;">Tratamiento</strong>
        </h1>

        <p class="subtitle">
          Alrededor del 80%–90% de los casos de candidiasis vulvovaginal sintomática 
          son no complicados, y entre el 75%–90% se deben al crecimiento excesivo de C. albicans.
        </p>
      </div>
    </div>

    <div class="div2">
      <img src="../assets/otros/tema3.png" alt="Placeholder Image" class="image" />
    </div>

    <div class="div3">
      <img src="../assets/productos/grupo-productos3.png" alt="Placeholder Image" class="image-centered" />
    </div>
  </div>
</template>

<script>
export default {
  name: "GridLayout"
};
</script>

<style scoped>
.parent {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(5, 1fr);
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 1 / 2 / 13;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  margin: 0;
}

.title-wrapper {
  max-width: 700px;
  padding: 0 16px;
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
  margin-bottom: 0.4em;
}

.subtitle {
  font-size: 1rem;
  line-height: 1.4;
  color: #4b678a;
  margin: 0 auto;
  /* Se quita el line-clamp para evitar los puntos suspensivos */
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  display: flex;
  align-items: center;
  justify-content: center;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div3 {
  grid-area: 2 / 9 / 5 / 12;
  display: flex;
  align-items: center;
  justify-content: center;
}

.div3 .image-centered {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

/* RESPONSIVE */
@media screen and (min-width: 1400px) {
  .div1 .title {
    font-size: 2.4em;
  }
  .subtitle {
    font-size: 1.05rem;
  }
}

@media screen and (min-width: 1024px) and (max-width: 1399px) {
  .div1 .title {
    font-size: 2.1em;
  }
}

@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 115vh;
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .subtitle {
    font-size: 0.95rem;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div3 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .div3 .image-centered {
    max-width: 93%;
  }
}
</style>
