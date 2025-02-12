<template>
  <div class="page-grid">
    <!-- <InfoOne /> -->
    <h1 class="page-title">Textura ligera <strong>con <strong style="border-bottom: 5px solid orange;">Color</strong></strong></h1>

    <div class="title-image-container">
      <img src="../assets/logos-sellos/logoIntibon.png" alt="Imagen descriptiva" class="title-image"/>
    </div>

    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row;">
            <p><strong>Physavie 250</strong> Calmante, regula la temperatura y para pieles sensibles.</p>
            <img src="../assets/beneficios-productos/icon6.png" alt="Hidrosense" />
            <span class="line right"></span>
          </div>

          <div class="box top-left" style="flex-direction: row;">
            <p><strong>Coenzima Q10</strong> Protección del daño por radiación UV, Antienvejecimiento e hidratante.</p>
            <img src="../assets/beneficios-productos/icon7.png" alt="Hidrosense" />
            <span class="line right"></span>
          </div>

          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p><strong>Provitamina B5</strong> Hidratante, alivia diversas molestias en la piel y mejora su apariencia.</p>
            <img src="../assets/beneficios-productos/icon8.png" alt="Algodón" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../assets/productos/producto2.png" alt="Shampoo y Baño Líquido Recién Nacido" style="padding: 0 26px;"/>
        
        <div>
          <div class="box top-right">
            <img src="../assets/beneficios-productos/icon9.png" alt="Sin Parabenos" />
            <p style="font-size: 0.7rem;"><strong>Niacinamida</strong>Reduce el enrojecimiento, manchas, mejora la función barrera de la piel y previene la aparición de arrugas.</p>
            <span class="line left"></span>
          </div>

          <!-- Contenedor inferior derecho -->
          <div class="box bottom-right">
            <img src="../assets/beneficios-productos/icon10.png" alt="No irrita ojos" /> <!-- style="transform: translate(3%, 5%) scale(1.30);" -->
            <p><strong>Vitamina E</strong> Retardo del envejecimiento de las células de la piel y antioxidante.</p>
            <span class="line left"></span>
          </div>
        </div>
      </div>
      <!-- Contenedor superior derecho -->
      
    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div class="content-tab">
      <p v-if="activeTab === 'benefits'" class="text-tab">
        INTIBON® 45+ Gel Hidratante íntimo que contiene ácido hialurónico, Vitamina E y un complejo hidratante, ayudan a brindar un efecto de hidratación y sensación de bienestar en tu zona íntima externa. <strong>No altera el pH fisiológico de la zona y no mancha la ropa interior.</strong>
      </p>
      <p v-if="activeTab === 'usage'">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Veritatis, dignissimos.</p>
      <p v-if="activeTab === 'composition'">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, obcaecati?</p>
    </div>

    <footer>
      <p class="text-footer">Desarrollado con <strong>Ginecólogos Expertos.</strong></p>
    </footer>
  </div>
</template>

<script>
/* import InfoOne from './InfoOne.vue'; */

export default {
  name: 'PageOne',
  /* components: { InfoOne }, */
  data() {
    return {
      activeTab: 'benefits',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style scoped>
/* .info-container {
  text-align: center;
  padding: 10px;
  border-radius: 10px;
  margin-bottom: 10px;
} */

.page-grid {
  display: grid;
  grid-template-rows: auto 1fr;
  justify-items: center;
  align-items: center;
  width: 100%;
  height: 100%;
  /* padding: 0 20px; */
  box-sizing: border-box;
  /* gap: 20px; */
}

.page-title {
  font-size: 1.8rem;
  font-weight: 300;
  text-align: center;
  color: #214F79;
}

.title-image-container {
  display: flex;
  justify-content: center;
  margin: 10px 0;
}

.title-image {
  max-width: 55%;
  height: auto;
}

.image-structure {
  display: grid;
  grid-template-areas:
    "top-left image top-right"
    "bottom-left image bottom-right";
  /* grid-template-columns: auto 1fr auto; */
  grid-template-columns: 1fr 0.4fr 1fr;
  grid-template-rows: auto auto;
  gap: 20px;
  align-items: center;
  justify-items: center;
  width: 100%;
}

.image-container {
  grid-area: image;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 130%;
  max-width: 300px;
}

.image-container img {
  max-width: 100%;
  height: auto;
  border-radius: 10px;
  /* box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); */
}

.box {
  display: flex;
  align-items: center;
  width: 280px; /* Aumentado el ancho de los contenedores */
  height: auto;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  gap: 8px; /* Ajustado el espaciado */
  /* padding: 8px; */
  position: relative; /* Necesario para las líneas */
}

.box img {
  max-width: 100px; /* Disminuido el tamaño de las imágenes */
  height: auto;
}

.box p {
  font-weight: 500;
  color: #214F79;
  font-size: 0.8rem; /* Reducido el tamaño del texto */
}

/* Líneas decorativas */
.line {
  position: absolute;
  width: 94px;
  height: 2px;
  background-color: #8D7199;
  top: 50%;
  transform: translateY(-50%);
}

.line.right {
  right: -94px;
}

.line.left {
  left: -94px;
}

.line::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: #8D7199;
  border: 2px solid #c5a6d3;
  border-radius: 50%;
  top: 50%;
  transform: translateY(-50%);
}

.line.right::after {
  right: -10px;
}

.line.left::after {
  left: -10px;
}

.top-left {
  grid-area: top-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
  margin-bottom: 15%;
}

.bottom-left {
  grid-area: bottom-left;
  flex-direction: row-reverse; /* Imagen a la derecha */
  padding-left: 20px;
  border-radius: 57px 59px 59px 17px;
}

.top-right {
  grid-area: top-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
  margin-bottom: 15%;
}

.bottom-right {
  grid-area: bottom-right;
  flex-direction: row; /* Imagen a la izquierda */
  padding-right: 20px;
  border-radius: 100px 100px 35px 100px;
}

.content-tab {
  border: 2px solid #8D7199;
  border-radius: 0px 12px 12px 12px;
  width: 60%;
  padding: 20px;
  background: #F3F3F3;
}

.content-tab, p {
  font-weight: 400;
  color: #214F79;
}

.button-group {
  display: flex;
  gap: 10px;
}

button {
  padding: 5px 10px;
  font-size: 0.9rem;
  border: none;
  border-radius: 5px;
  background-color: #DEE5E7;
  color: #214F79;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  color: white;
  background-color: #8D7199;
}

button:active,
button:focus {
  background-color: #8D7199;
  color: #fff;
}


footer {
  background: #EFCBB5; 
  font-size: 1.5rem;
  width: 100%; 
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #214F79;
}

@media (max-width: 768px) {
  .title-image {
    max-width: 80%;
  }
  .box {
    visibility: hidden;
  }

  .content-tab, p {
    font-size: 0.9rem;
  }
}
</style>