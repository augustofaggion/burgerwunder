<template>
  <div id="">
    <div class="about-container">
      <div class="text-about-container">
        <h2 class="header-secondary">Über uns</h2>
        <p class="text" v-for="(paragraph, index) in paragraphs" :key="index">
          {{ paragraph }}
        </p>
      </div>
      <div class="img-about"></div>
    </div>
  </div>
</template>

<!-- Need to export-->
<script>
import imgAbout from "../assets/about-restaurant.jpg";

export default {
  name: "AppAbout",
  data() {
    return {
      paragraphs: [
        "Wir sind eine Familie von drei Brüdern,",
        "die beschlossen haben, ein Restaurant zu eröffnen, das sich auf drei Burger-Menüs spezialisiert.",
        "Unsere Gäste können aus einer Vielfalt an Saucen für unsere berühmten belgischen Pommes wählen.",
        "Kommen Sie vorbei und erleben Sie die Leidenschaft und Hingabe, die wir in jedes Gericht stecken!",
      ],
      image: imgAbout,
    };
  },
};
</script>

<style>
.about-container {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10rem;
  border-radius: 1.5rem;
  box-shadow: 0 0 1rem rgba(0, 0, 0, 0.1);

}
.img-about {
  background-image: url("../assets/about-restaurant.jpg");
  padding: 15rem 30rem;
  margin: 1rem;
  background-size: cover;
}

.text-about-container{
  padding: 5rem;


}

.header-secondary {
  font-size: 5rem;
  font-weight: bold;
}
.text {
  font-size: 1.5rem;
  padding: 1.5rem 0;
}
</style>
