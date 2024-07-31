<template>
  <section class="home-section" id="home">

    <div :class="grid-container">
      <div class="text-container header-primary">
        <h1 class="" v-for="(header, index) in headers" :key="index">{{ header }}</h1>
        <button class="btn">Bestelle jetzt</button>
      </div>


    </div>
  </section>
</template>

<script>



export default {
  name: "AppHome",
  data() {
    return {
      headers: ["Ein", "Geschmackserlebnis, das du", "nur bei uns findes!"],

    };
  },
};
</script>

<style>


.home-section {
  display: grid;
  justify-content: center;
  align-items: center;
  padding: 10rem;
  background-color: var(--color-secondary);
  color: var(--color-quaternary);
}

.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  width: 100%;
  padding: 0 2rem;
}

.text-container {
  padding: 50rem;
  background-image: url("../assets/hamburger.jpg");
  /*  Foto von Armando Ascorve Morales von Unsplash */
  /* Remove alcohol bootles in the background */
  background-size: cover;
  object-fit: cover;
  border-radius: 1.5rem;
  /* Add shadow */
}

.header-primary {
  font-size: 2rem;
  font-weight: bold;
  padding: 5rem 15rem 15rem 15rem;
  /* Add shador or borders */
}

.btn {
  font-size: 2.4rem;
  margin: 2rem 0;
  padding: 1rem 2rem;
  color: var(--color-secondary);
  background-color: var(--color-primary);
  border-radius: 15px;
}


</style>
