<template>
  <div>
    <div>
      <div class="menu-burger">
        <div class="menu-card" v-for="burger in menuItems" :key="burger">
          <h1>{{ burger.title }}</h1>
          <p>{{ burger.description }}</p>
          <ul>
            <li v-for="menuItem in burger.menu" :key="menuItem">
              {{ menuItem }}
            </li>
          </ul>
          <a href="">Bestelle jetzt</a>
        </div>
        <h2>Nur 9,99 €</h2>
      </div>
    </div>
  </div>
  <!-- Check figma gallery section as an example of menu -->
</template>

<!-- Need to export-->
<script>
export default {
  name: "AppMenu",
  data() {
    return {
      // Menu
      menuItems: [
        {
          title: "Beff Wunder Burger",
          image: "burger1.jpg",
          description: "200g Beef Patty, Tomato, Lettuce, Onion, Mayo, Mustard",
          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],
        },
        {
          title: "Chicken Wunder Burger",
          image: "burger2.jpg",
          description: "200g Chicken Patty, Tomato, Lettuce, Onion, Mayo, Mustard",

          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],
        },
        {
          title: "Veggie Wunder Burger",
          image: "burger3.jpg",
          description: "200g Veggie Patty, Tomato, Lettuce, Onion, Mayo, Mustard",

          menu: ["Burger", "Pommes", "Getränk", "Saucen", "Apfeltasche"],
        },
      ],
    };
  },
};
</script>
