<template>
  <div class="faq-container">
    <div class="top-line"></div>
    <h2 class="faq-title">
      Preguntas <span class="highlight">Frecuentes</span>
    </h2>
    <div class="faq-content">
      <div class="faq-image">
        <img src="../assets/otros/doctora.png" alt="Imagen relacionada" />
      </div>
      <div class="faq-accordion-container">
        <div class="faq-accordion">
          <div v-for="(question, index) in questions" :key="index" class="accordion-item">
            <button class="accordion-header" @click="toggle(index)">
              {{ question.title }}
              <span :class="{'rotate': activeIndex === index}" class="accordion-icon">+</span>
            </button>
            <div v-if="activeIndex === index" class="accordion-body">
              <p>{{ question.content }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="bottom-line"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: null,
      questions: [
        {
          title: "¿Qué pH tienen los jabones íntimos de Intibon?",
          content: "Los jabones íntimos Intibon contienen ácido láctico, que provee a la delicada fórmula de la acidez necesaria para generar un medio ligeramente ácido que favorezca que se mantengan las condiciones de proliferación de Lactobacillus acidophilus. Tienen un pH similar al de la vagina entre 3.8 y 4.5.",
        },
        {
          title: "¿Los jabones íntimos Intibon son Syndet?",
          content: "Sí, todos nuestros jabones íntimos son Syndet, Los jabones íntimos de Intibon®, han sido diseñados meticulosamente utilizando exclusivamente surfactantes Syndet para proporcionar una limpieza suave en la zona íntima. Entre sus ingredientes limpiadores se incluyen Sodium Lauroyl Methyl Isethionate, Sodium Methyl Oleoyl Taurate, Lauryl Glucoside, Coco-Glucoside, Sodium Methyl Cocoyl Taurate y Disodium 2- Sulfolaurate, conocidos por retirar residuos de secreciones sin causar daño a la piel. Además, estas formulaciones cuentan con un pH ajustado a la zona íntima femenina (mujer y niñas), e ingredientes como: 1. Alantoína: Con propiedades protectoras que previenen daños en la piel y alivian molestias. 2. Ácido láctico: Regula el pH y proporciona hidratación. 3. Ingredientes naturales como caléndula, avena, sábila y extracto de menta, reconocidos por sus beneficios cutáneos."
        },
        {
          title: "¿Intibon tiene productos con prebióticos para la zona íntima?",
          content: "Sí, contamos con jabón íntimo Intibon 0% y Pañitos húmedos íntimos Intibon 0%, que contienen prebióticos, que estimula el desarrollo y crecimiento de bacterias beneficiosas de la flora vaginal.",
        },
        {
          title: "¿El hidratante vaginal es libre de estrógenos?",
          content: "Sí, el Hidratante Vaginal Intibon 45+ es libre de estrógenos, fragancias y parabenos. Ayuda a lograr un efecto inmediato y duradero combatiendo los síntomas de la sequedad vulvovaginal.",
        },
      ],
    };
  },
  methods: {
    toggle(index) {
      this.activeIndex = this.activeIndex === index ? null : index;
    },
  },
};
</script>

<style scoped>
.faq-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px;
  position: relative;
  padding-bottom: 10px;
}

.top-line {
  width: 15%;
  height: 2px;
  background-color: #95D3F8;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
}

.faq-title {
  text-align: center;
  font-size: 36px;
  /* font-family: "Arial", sans-serif; */
  color: #008DB5;
  margin-bottom: 20px;
  font-weight: 400;
}

.faq-title .highlight {
  color: #008DB5; /* Color para "Frecuentes" */
  font-weight: bold; /* Negrita para "Frecuentes" */
}

.faq-content {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
}

.faq-image {
display: flex; 
justify-content: center; 
align-items: center; 
}

.faq-image img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 8px;
}

.faq-accordion-container {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}

.faq-accordion {
  width: 90%;
}

.accordion-item {
  border: 1px solid #DBEBEB;
  border-left-color: #C5E5E4;
  border-left-width: 10px;
  border-radius: 8px;
  margin-bottom: 10px;
  overflow: hidden;
}

.accordion-header {
  background: #DBEBEB;
  color: #707070;
  padding: 15px;
  text-align: left;
  font-size: 18px;
  border: none;
  width: 100%;
  cursor: pointer;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.accordion-body {
  padding: 15px;
  background: #fff;
  font-size: 16px;
  /* font-family: "Arial", sans-serif; */

  line-height: 1.6;
  color: #444;
}

.accordion-icon {
  color: #0092B4;
  font-size: 20px;
  font-weight: bold;
  transition: transform 0.3s;
}

.accordion-icon.rotate {
  transform: rotate(45deg);
}

.bottom-line {
  width: 30%; 
  height: 2px; 
  background-color: #95D3F8; 
  border-radius: 2px;
  position: absolute;
  bottom: -14px; 
  left: 50%;
  transform: translateX(-50%);
}

/* Responsive Design */
@media (max-width: 768px) {
  .faq-content {
      grid-template-columns: 1fr;
  }

  .accordion-header {
      font-size: 15px;
  }

  .accordion-body {
      font-size: 14px;
  }
}
</style>
