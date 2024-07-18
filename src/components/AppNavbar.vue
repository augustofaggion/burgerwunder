<template>
  <div>
    <!-- Add Logo later May a icon-->
    <nav class="navbar">
      <!-- Use v-for to iterate over navLinks -->
      <a v-for="link in navLinks" :key="link.url" :href="link.url">{{ link.text }}</a>
      <a href="">Bestelle jetzt</a>
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
          url: "/"
        },
        {
          text: "Menu",
          url: "/menu"
        },
        {
          text: "Kontakt",
          url: "/kontakt"
        }
      ]
    };
  },
};
</script>
