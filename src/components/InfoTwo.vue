<template>
  <div class="parent" id="45">
    <div class="div1">
      <h1 class="title">Intibon <strong style="border-bottom: 5px solid #008EB4;">45+</strong></h1>
      <p class="description">La sequedad vaginal es un síntoma que surge del síndrome genitourinario de la menopausia (SGM), y aunque <br> principalmente se asocia a mujeres en fase posmenopáusica, puede aparecer a cualquier edad debido a factores <br> de estrés, diabetes, lactancia y afectaciones inflamatorias.<sup>2</sup> <br><br> Intibon lanza la línea especializada <strong>Intibon 45+ desarrollada con ginecólogo experto</strong> para solucionar las <br> principales necesidades de las <strong>mujeres en etapa de menopausia.</strong></p>
      <p class="note">2. Mark JKK, SamsudinS, LooiI, YuenKH. Vaginal dryness: a reviewofcurrent understandingand managementstrategies. Climacteric. Junio de 2024;27(3):236-244.</p>
    </div>
    <div class="div2">
      <img src="../assets/otros/tema2.png" alt="Placeholder Image" class="image" />
    </div>
    <div class="div4">
      <img src="../assets/logos-sellos/grupo-sellos.png" alt="Placeholder Image" class="image-centered" />
    </div>
    <div class="div3">
      <img src="../assets/productos/grupo-produtos22.png" alt="Placeholder Image" class="image-centered" />
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
  grid-column-gap: 0px;
  grid-row-gap: 0px;
  width: 100%;
  height: 100vh;
  padding: 0;
  box-sizing: border-box;
}

.div1 {
  grid-area: 1 / 1 / 2 / 13;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 0;
  position: relative;
  text-align: center;
}

.div1 .title {
  font-size: 2em;
  font-weight: 300;
  color: #214F79;
}

.div1 .description {
  font-size: 1em;
  color: #214F79;
  margin-top: 10px;
  text-align: left;
  max-width: 80%;
}

.div1 .note {
  font-size: 0.7em;
  color: #666;
  margin-top: 6px;
  text-align: left;
  max-width: 80%;
}

.div2 {
  grid-area: 2 / 1 / 6 / 8;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
  margin: 0;
}

.div2 .image {
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.div4 {
  grid-area: 2 / 9 / 3 / 12;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 80px;
  margin: 0;
}

.div4 .image-centered {
  max-width: 140%;
  max-height: 140%;
  object-fit: contain;
}

.div3 {
  grid-area: 3 / 9 / 5 / 12;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5em;
  height: 100%;
  margin: 0;
}

.div3 .image-centered {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

@media screen and (min-width: 1400px) {
  .div4 {
    height: 190px;
  }

  .div4 .image-centered {
    max-width: 120%;
    max-width: 120%;
  }

  .div3 {
    height: 117%;
  }

  .div3 .image-centered {
    max-height: 127%;
  }
}

/* portatiles medianos */
@media screen and (min-width: 1024px) and (max-width: 1399px) {
  .parent {
    height: 134vh;
  }

  .div4 {
    height: 90px;
  }

  .div4 .image-centered {
    max-width: 116%;
    max-height: 116%;
  }

  .div3 {
    height: 133%;
  }

  .div3 .image-centered {
    max-height: 116%;
  }
}

@media screen and (max-width: 768px) {
  .parent {
    grid-template-columns: repeat(6, 1fr);
    grid-template-rows: auto;
    height: 195vh; /* 164vh */
  }

  .div1 {
    grid-area: 1 / 1 / 2 / 7;
  }

  .div1 .title {
    font-size: 1.5em;
  }

  .div2 {
    grid-area: 2 / 1 / 3 / 7;
  }

  .div4 {
    grid-area: 3 / 1 / 4 / 7;
  }

  .div4 .image-centered {
    max-width: 100%;
    max-height: 100%;
  }

  .div3 {
    grid-area: 4 / 1 / 5 / 7;
  }

  .div3 .image-centered {
    max-width: 90%;
  }
}
</style>
