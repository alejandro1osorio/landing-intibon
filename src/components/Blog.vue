<template>
  <div class="blog-container">
    <h1>Artículos <strong>Recientes</strong></h1>
    <div class="grid-container">
      <div class="article" v-for="article in articles" :key="article.id">
        <img :src="article.image" alt="Imagen del artículo" class="article-image" />
        <h2>{{ article.title }}</h2>
        <p>{{ article.description }}</p>
        <a :href="article.link" target="_blank" class="view-more">Ver más</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Blog",
  data() {
    return {
      articles: [
        { id: 1, title: "Maintaining vulvar", description: "Knowledge of female genital anatomy and physiology is often inadequate or incorrect among women. Precise patient–physician conversations can be inhibited by a reluctance or inability to speak accurately about the vulva and vagina, with the terms often being used interchangeably", image: "https://images.unsplash.com/photo-1740752141538-67e4c4f03217?q=80&w=2146&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/1noiYS7rK8aamzQWjOL9ILh3t_UFt3BQn/view?usp=sharing" },
        { id: 2, title: "Journal of Gynecology Obstetrics.", description: "Intimate hygiene products are widely used by women as part of their daily cleansing routine according to personal preferences, often influenced by their religion, cultural or ethnic norms, as well as medical recommendations However, there is a paucity of scientific literature about the impact of intimate hygiene on the vulvovaginal area The adoption of proper habits is crucial in pre-serving the entire vulvovaginal ecosystem and preventing or reducing a variety of unpleasant symptoms.", image: "https://images.unsplash.com/photo-1740752088885-92b7a1d1d5a0?q=80&w=2032&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", link: "https://drive.google.com/file/d/1PZq97J-4oMrU8V-HxVf-DKUEGmm0WYZi/view?usp=sharing" },
        
      ],
    };
  },
};
</script>

<style scoped>
.blog-container {
  text-align: center;
  padding: 20px;
}

h1 {
  font-size: 2.5em;
  color: #008DB5;
  margin-bottom: 30px;
  font-weight: 300;
}

.grid-container {
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  padding: 0px 10%;
  justify-content: center;
}

.article {
  background-color: #f9f9f9;
  border-radius: 8px;
  padding: 0;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  overflow: hidden;
  padding-bottom: 20px;
}

.article-image {
  width: 100%;
  height: auto;
  border-radius: 8px 8px 8px 8px;
  margin: 0;
}

h2 {
  font-size: 1.5em;
  margin: 10px 0;
  color: #34495e;
}

p {
  font-size: 1em;
  color: #7f8c8d;
  margin: 10px 20px;
  text-align: justify;
}

.view-more {
  text-decoration: none;
  color: #3498db;
  font-weight: bold;
  transition: color 0.3s;
}

.view-more:hover {
  color: #1d6fa5;
}

@media (max-width: 600px) {
  .grid-container {
    grid-template-columns: 1fr;
  }
}
</style>
