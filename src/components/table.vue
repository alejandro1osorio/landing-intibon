<template>
    <div class="vulvo-container">
      <div class="vulvo-header">
        <h2>En general, las mujeres asociaron la <br> realización de cuidados vulvovaginales con:</h2>
        <p style="color: #005086;">(Tabla 1)</p>
      </div>
  
      <!-- Tarjeta 1 -->
      <div class="vulvo-card" style="">
        <div class="icon left">
          <img src="../assets/table/iconoTable1.png" alt="Icono salud" />
        </div>
        <p>
          <span class="bullet">•</span> <strong>Resultados positivos</strong> en su salud física y emocional.
        </p>
      </div>
  
      <!-- Tarjeta 2 -->
      <div class="vulvo-card reverse" style="border-radius: 15px 60px 60px 61px;">
        <p>
          <span class="bullet">•</span> Las prácticas de higiene vulvovaginal se vincularon con
          <strong>sentirse seguras y atractivas, con una buena salud</strong> y con tener una vida sexual satisfactoria.
        </p>
        <div class="icon right">
          <img src="../assets/table/iconoTable2.png" alt="Icono seguridad" />
        </div>
      </div>
  
      <!-- Tarjeta 3 -->
      <div class="vulvo-card" style="border-radius: 55px 60px 20px 55px;">
        <div class="icon left">
          <img src="../assets/table/iconoTable3.png" alt="Icono etapas" />
        </div>
        <p>
          <span class="bullet">•</span> <strong>Las prácticas de cuidado íntimo cambiaron</strong>, según las etapas de la vida o eventos que llevaron a alterar los regímenes normales de las encuestadas, desde la menarquia hasta la menopausia, la maternidad, los cambios estacionales y la actividad sexual.
        </p>
      </div>
  
      <!-- Tabla como imagen -->
      <div class="vulvo-image-container">
        <img src="../assets/table/tabla.png" alt="Tabla impacto del cuidado íntimo" />

        <div class="vulvo-caption">
          <p style="color: #005086;"><strong>UK:</strong> United Kingdom. <br><span class="footnote" style="color: #005086;">* Women were asked to identify what elements are positively impacted by performing intimate self-care routines.</span></p>
          <p style="color: #005086;" class="footnote">
            Portugal, Russia and Thailand. Intimate self-care was associated with many benefits for women’s physical and mental health, including the perception of being in good health (25% to 78%) and feeling attractive (19% to 47%).
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .vulvo-container {
    padding: 2rem 1rem;
    max-width: 1100px;
    margin: auto;
    background-color: #f2f2f2;
  }
  
  .vulvo-header {
    text-align: center;
    margin-bottom: 2rem;
  }
  
  .vulvo-header h2 {
    font-size: 1.6rem;
    margin-bottom: 0.3rem;
    color: #005086;
    line-height: 1.09;
    font-weight: 500;
  }
  
  .vulvo-header p {
    color: #999;
  }
  
  /* Tarjetas */
  .vulvo-card {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #fff;
    /* padding: 2rem 1.5rem; */
    margin-bottom: 1.5rem;
    border-radius: 20px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.04);
    gap: 1.5rem;
    border-radius: 55px 60px 20px 55px;
  }
  
  .icon {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .icon img {
    max-width: 100px;
    height: auto;
    object-fit: contain;
  }
  
  .vulvo-card p {
    font-size: 1rem;
    color: #005086;
    line-height: 1.6;
    margin: 0;
    flex: 1;
    text-align: left;
    padding-left: 30px;
  }
  
  .vulvo-card strong {
    color: #005086;
    font-weight: 600;
  }
  
  .bullet {
    color: #005086;
    font-size: 1.3rem;
    margin-right: 0.3rem;
  }
  
  .vulvo-image-container {
    margin-top: 2rem;
    text-align: center;
  }
  
  .vulvo-image-container img {
    max-width: 100%;
    height: auto;
    border-radius: 12px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  }

  .vulvo-caption {
  margin-top: 1rem;
  padding: 0 1rem;
  font-size: 0.75rem;
  color: #4d4d4d;
  text-align: left;
  max-width: 900px;
  margin-left: auto;
  margin-right: auto;
}

.vulvo-caption .footnote {
  font-size: 0.72rem;
  color: #666;
  line-height: 1.4;
}
  
  @media (max-width: 600px) {
    .vulvo-container {
      padding: 1rem;
    }
  
    .vulvo-card,
    .vulvo-card.reverse {
      flex-direction: row !important;
      align-items: flex-start;
    }
  
    .vulvo-card p {
      font-size: 0.50rem;
      padding-left: 8px;
      transform: scale(0.95);
    }
  
    .icon img {
      max-width: 80px;
    }

    .vulvo-caption {
    font-size: 0.65rem;
    padding: 0 0.5rem;
  }

  .vulvo-caption .footnote {
    font-size: 0.6rem;
  }
  }
  </style>
  