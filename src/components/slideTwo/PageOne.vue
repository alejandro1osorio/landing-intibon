<template>
  <div class="page-grid">
    <div class="top-line"></div>
    <h1 class="page-title"><strong>Hidratante</strong> <strong style="border-bottom: 5px solid #008EB4; font-weight: 300;">íntimo</strong></h1>

    <div class="title-image-container">
      <img src="../../assets/logos-sellos/grupo-sellos.png" alt="Imagen descriptiva" class="title-image"/>
    </div>

    <!-- <p class="additional-text">La disminución de los niveles de estrógenos en la menopausia provoca que los tejidos vaginales se vuelvan más <br> secos. Esta afección, que se conoce como atrofia o sequedad vaginal, puede causar dispareunia.<sup>2,3</sup></p> -->

    <div class="image-structure">
      <!-- Contenedor superior izquierdo -->
      <!-- Imagen en el centro -->
      <div class="image-container">
        <div class="container-item">
          <div class="box top-left" style="flex-direction: row; width: 302px;">
            <p>Ayuda a brindar un efecto de hidratación y sensación de bienestar en tu zona íntima externa.</p>
            <img src="../../assets/beneficios-productos/icon9.png" alt="Hidrosense" />
            <span class="line right"></span>
          </div>

          <div class="box top-left" style="flex-direction: row;">
            <p><strong>No altera el pH fisiológico </strong>de la zona vaginal y no mancha la ropa interior. No es agresivo al látex.</p>
            <img src="../../assets/beneficios-productos/icon6.png" alt="Hidrosense" />
            <span class="line right"></span>
          </div>

          <!-- Contenedor inferior izquierdo -->
          <div class="box bottom-left" style="flex-direction: row;">
            <p style="font-size: 0.7rem;"><strong>Rehidratan el tejido mucoso seco,</strong> se absorben en la piel y se adhieren al revestimiento vaginal, <strong>mimetizando las secreciones vaginales.</strong></p>
            <img src="../../assets/beneficios-productos/icon8.png" alt="Algodón" />
            <span class="line right"></span>
          </div>
        </div>
        
        <img src="../../assets/productos/producto2.png" alt="Shampoo y Baño Líquido Recién Nacido" style="max-width: 88%; padding: 0 80px;"/>
        
        <div>
          <div class="box top-right">
            <img src="../../assets/beneficios-productos/icon25.png" alt="Sin Parabenos" />
            <p>Hipoalergénico, ginecológica y <strong>dermatológicamente comprobado.</strong></p>
            <span class="line left"></span>
          </div>

          <div class="box top-right">
            <img src="../../assets/beneficios-productos/icon7.png" alt="Sin Parabenos" />
            <p>Libre de <strong>estrógenos, fragancias y parabenos.</strong></p>
            <span class="line left"></span>
          </div>

          <!-- Contenedor inferior derecho -->
          <!-- <div class="box bottom-right">
            <img src="../../assets/beneficios-productos/icon9.png" alt="No irrita ojos" />
            <p>Incluye 10 cánulas reutilizables: <strong>proceso suave y cómodo.</strong></p>
            <span class="line left"></span>
          </div> -->
        </div>
      </div>
      <!-- Contenedor superior derecho -->
      
    </div>

    <div class="button-group">
      <button @click="setActiveTab('benefits')">Beneficios</button>
      <button @click="setActiveTab('usage')">Modo de uso</button>
      <button @click="setActiveTab('composition')">Composición</button>
    </div>
    <div v-if="activeTab" class="content-tab">
      <div class="tab-header">
        <button class="close-btn" @click="closeTab">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M6 18L18 6M6 6L18 18" stroke="#5d75b8" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </button>
      </div>

      <p v-if="activeTab === 'benefits'" class="text-tab">
        INTIBON® 45+ Gel Hidratante íntimo contiene ácido hialurónico, Vitamina E y un complejo hidratante que ayudan a brindar un efecto de hidratación y sensación de bienestar en tu zona íntima externa. No altera el pH fisiológico de la zona y no mancha la ropa interior.
      </p>
      <p v-if="activeTab === 'usage'">
        SOLO PARA USO EXTERNO. Retire la tapa del tubo y el sello de seguridad. Aprieta el tubo colapsible y aplica la cantidad deseada de gel hidratante íntimo en tus dedos. Extiende el producto sobre la zona vulvar. Vuelve a tapar el tubo.
      </p>
      <p v-if="activeTab === 'composition'">
        Water, Glycerin,Hydroxyethylcellulose, Water/Glycerin, Glyceryl Polyacrylate/Trehalose/Urea/Serine/Pentylene Glycol/Algin/Caprylyl Glycol/Sodium Hyaluronate/Pollulan/Disodium Phospate/Potassium Phospate, Sodium Hyaluronate, Sodium Benzoate, Potassium Sorbate, Tocopheryl Acetate, Lactic Acid.
      </p>
    </div>

    <footer>
      <p class="text-footer">Desarrollado con <strong>Ginecólogo Experto.</strong></p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'PageOne',
  data() {
    return {
      activeTab: '',
    };
  },
  methods: {
    setActiveTab(tab) {
      this.activeTab = tab;
    },
    closeTab() {
      this.activeTab = '';
    }
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

.top-line {
  width: 15%;
  height: 2px;
  background-color: #0077b6;
  position: absolute;
  top: 0;
  left: 50%;
  transform: translateX(-50%);
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

/* .additional-text {
  text-align: center;
  font-size: 1rem;
  color: #214F79;
  margin: 20px 20px;
  max-width: 80%;
  line-height: 1.2;
} */

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

.tab-header {
  display: flex;
  justify-content: flex-end;
  padding: 5px;
}
.close-btn {
  background: transparent;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #E4016A;
}

footer {
  background: #8D7199; 
  font-size: 1.5rem;
  width: 100%; 
  margin-top: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.text-footer {
  color: #fff;
}

@media (max-width: 768px) {
  .title-image {
    max-width: 80%;
  }
  .box {
    visibility: hidden;
  }
/*   .additional-text {
    font-size: 0.9rem;
    max-width: 90%;
  } */

  .content-tab, p {
    font-size: 0.9rem;
  }
}
</style>