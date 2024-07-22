<template>
  <div class="">
    <!-- Add Logo later May a icon-->
    <nav class="navbar">
      <div class="navbar-item"><a href="">Burger Wunder</a></div>
      <!-- Use v-for to iterate over navLinks -->
      <div class="navbar-item">
        <a v-for="link in navLinks" :class="container" :key="link.url" :href="link.url">{{
          link.text
        }}</a>
      </div>
      <div class="navbar-item"><a href="">Bestelle jetzt</a></div>
    </nav>
  </div>
</template>

<script>

export default {
  name: "AppNavbar",
  data() {
    return {
      // Navbar
      navLinks: [
        {
          text: "Home",
          url: "/",
        },
        {
          text: "Menu",
          url: "/menu",
        },
        {
          text: "Kontakt",
          url: "/kontakt",
        },
      ],
    };
  },
};
</script>

<style scoped>
  /* src/navbar.css */
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 1rem;
  background-color: var(--color-primary);
}

.navbar-item a {
  color: white;
  text-decoration: none;
  margin-right: 1rem;
}

.navbar-item a:hover {
  color: var(--color-secondary);
}
</style>
