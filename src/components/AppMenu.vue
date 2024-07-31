<template>
  <div id="menu">
    <div class="menu-container">
      <div class="menu-burger">
        <div class="menu-card" v-for="burger in menuItems" :key="burger">
          <!-- Add images -->
          <div>
            <img :src="burger.image" alt="" class="image-menu"/>
            <h1>{{ burger.title }}</h1>
            <p>{{ burger.description }}</p>
            <ul>
              <!-- Here add icons for each one using also v for -->
              <li v-for="(menuItem, index) in burger.menu" :key="menuItem">
                {{ burger.icons[index] }}
                {{ menuItem }}
              </li>
            </ul>
            <!-- maybe put together the button with the promotion price -->
            <a href="">Bestelle jetzt</a>
          </div>
        </div>
      </div>
    </div>
    <h2>Nur 9,99 €</h2>
  </div>
  <!-- Check figma gallery section as an example of menu -->
</template>

<!-- Need to export-->
<script>
import beefBurger from '../assets/beef-buger.jpg';
// follow the example above to import the fotos
import chickenBurger from '../assets/beef-buger.jpg';
import veggieBurger from '../assets/beef-buger.jpg';

export default {
  name: "AppMenu",
  data() {
    return {
      // Menu
      menuItems: [
        {
          title: "Beff Wunder Burger",
          image: beefBurger,
          description: "200g Beef Patty, Tomato, Lettuce, Onion, Mayo, Mustard",
          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],

          icons: ["🍔", "🍟", "🥤", "🍅", "🍏"],

        },
        {
          title: "Chicken Wunder Burger",
          image: chickenBurger,
          description:
            "200g Chicken Patty, Tomato, Lettuce, Onion, Mayo, Mustard",

          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],
          icons: ["🍔", "🍟", "🥤", "🍅", "🍏"],
        },
        {
          title: "Veggie Wunder Burger",
          image: veggieBurger,
          description:
            "200g Veggie Patty, Tomato, Lettuce, Onion, Mayo, Mustard",

          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],
          icons: ["🍔", "🍟", "🥤", "🍅", "🍏"],
        },
      ],
    };
  },
};
</script>

<style>
.menu-container {
  display: flex;
  justify-content: center;
  align-items: center; /* Optional: to center items vertically */
}

.menu-burger {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 1rem;
  padding: 1rem;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

.menu-card {
  border: 1px solid #ccc;
  padding: 16px;
  background-color: #fff;
  text-align: center;
}

.image-menu {
  width: 100%;
  height: 300px;
  object-fit: cover;
  border-radius: 8px;
}
</style>
