<template>
  <!-- Needs a child element -->
  <div class="home-section">
    <div :class="grid-box">
      <div class="item header-primary">
        <h1>Ein Geschmackserlebnis, das du nur bei uns findes !</h1>
      </div>
      <div class="item "><button class="btn">Bestelle jetzt</button></div>
    </div>

  </div>
</template>

<!-- Need to export-->
<script>
import hamburger from "../assets/hamburger.jpg";

export default {
  name: "AppHome",
  data() {
    return {
      hamburger: hamburger,
    };
  },
};
</script>

<style>
.home-section {

  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
  padding: 2rem;
  background-color: var(--color-secondary);
  color: var(--color-quaternary);
}

.grid-box {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

}

.item {
  margin: 3rem;
}

.header-primary {
  font-size: 2rem;
  font-weight: bold;
  padding: 0 45rem 0 0;
}

.btn {
  font-size: 2.4rem;
  padding: 1rem 2rem;
  
}





</style>
