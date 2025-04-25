<template>
    <div class="vulvo-container">
      <div class="vulvo-header">
        <h2>En general, las mujeres asociaron la realización de cuidados vulvovaginales con:</h2>
        <p>(Tabla 1)</p>
      </div>
  
      <!-- Tarjeta 1 -->
      <div class="vulvo-card">
        <div class="icon left">
          <img src="../assets/table/iconoTable1.png" alt="Icono salud" />
        </div>
        <p>
          <span class="bullet">•</span> <strong>Resultados positivos</strong> en su salud física y emocional.
        </p>
      </div>
  
      <!-- Tarjeta 2 -->
      <div class="vulvo-card reverse">
        <p>
          <span class="bullet">•</span> Las prácticas de higiene vulvovaginal se vincularon con
          <strong>sentirse seguras y atractivas, con una buena salud</strong> y con tener una vida sexual satisfactoria.
        </p>
        <div class="icon right">
          <img src="../assets/table/iconoTable2.png" alt="Icono seguridad" />
        </div>
      </div>
  
      <!-- Tarjeta 3 -->
      <div class="vulvo-card">
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
    color: #1a1a1a;
  }
  
  .vulvo-header p {
    color: #999;
  }
  
  .vulvo-card {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #fff;
    margin-bottom: 1.5rem;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.04);
    gap: 1rem;
  }
  
  .icon {
    width: 65px;
    height: 65px;
    flex-shrink: 0;
  }
  
  .icon img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
  
  .vulvo-card p {
    font-size: 1rem;
    color: #333;
    line-height: 1.6;
    margin: 0;
    flex: 1;
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
  
  /* Imagen final */
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
  
  /* Ajustes responsive */
  @media (max-width: 600px) {
    .vulvo-container {
      padding: 1rem 1rem;
    }
  
    .vulvo-card {
      padding: 1rem;
    }
  
    .vulvo-card p {
      font-size: 0.95rem;
    }
  
    .icon {
      width: 50px;
      height: 50px;
    }
  }
  </style>
  