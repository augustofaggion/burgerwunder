<template>
  <!-- Todo icon in hamburger in menu is not centrylized please ajust in the corner -->
   <!-- Link all the links -->
  <div class="">
    <nav class="navbar">
      <div class="navbar-item"><a href="" class="">Burger Wunder</a></div>
      <svg-icon
        :class="isMenuOpen ? 'hideIcon' : 'showIcon'"
        type="mdi"
        :path="openPath"
        @click="toggleMenu"
      >
      </svg-icon>

      <svg-icon
        :class="isMenuOpen ? 'showIcon' : 'hideIcon'"
        type="mdi"
        :path="closePath"
        @click="toggleMenu"
      >
      </svg-icon>
      <div class="navbar-item">
      <div class="menu-container" :class="{ open: isMenuOpen }">
          <!-- Use v-for to iterate over navLinks -->

          <a
            v-for="link in navLinks"
            :class="container"
            :key="link.url"
            :href="link.url"
            >{{ link.text }}</a
          >

          <button href="" class="btn-cta">Bestelle jetzt</button>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiMenu, mdiClose } from "@mdi/js";

export default {
  name: "AppNavbar",
  components: {
    SvgIcon,
  },
  data() {
    return {
      isMenuOpen: false,
      openPath: mdiMenu,
      closePath: mdiClose,
      // Navbar
      navLinks: [
        {
          text: "Home",
          url: "#home",
        },
        {
          text: "Menu",
          url: "#menu",
        },
        {
          text: "Kontakt",
          url: "#kontakt",
        },
      ],
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
  },
};
</script>

<style scoped>

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem;
  background-color: var(--color-primary);
  font-size: 1.6rem;
  height: 6rem;
}

.navbar-item a {
  color: white;
  text-decoration: none;
  margin-right: 1rem;
  padding: 1rem;
  font-weight: bold;
  transition: ease-in-out 0.5s;
}

.navbar-item a:hover {
  border-radius: 1.5rem;
  color: var(--color-secondary);
  border: 1px solid var(--color-secondary);
}

.btn-cta {
  background-color: var(--color-secondary);
  color: var(--color-primary);
  padding: 1rem 2rem;
  border-radius: 1.5rem;
  font-weight: bold;
  text-decoration: none;
  transition: ease-in-out 0.5s;
  font-size: 1.6rem;
}

.btn-cta:hover {
  background-color: var(--color-primary);
  color: var(--color-secondary);
  border: 1px solid var(--color-secondary);
  box-shadow: 1px 1px 1px 1px var(--color-secondary);
}

/* Default state for the menu container (hidden on larger screens) */
.menu-container {
  display: none;
}

/* Show menu container and icons when menu is open */
.menu-container.open {
  display: flex;
  flex-direction: column;
  background-color: var(--color-primary);
  position: absolute;
  top: 6rem;
  left: 0;
  right: 0;
}

/* Icons visibility */
.showIcon {
  display: inline-block;
}

.hideIcon {
  display: none;
}

/* Media query for screen sizes 768px and above */
@media (min-width: 768px) {
  .menu-container {
    display: flex !important;
    flex-direction: row;
    align-items: center;
    position: static;
    background-color: transparent;
  }
  .showIcon, .hideIcon {
    display: none;

  }

}
</style>
