<template>
  <div class="mainMenu">
    <span v-for="(menu, idx) in menuElement" :key="menu"
      >{{ menu }} {{ idx }}</span
    >
  </div>

  <div>
    원룸샵
    <h4 v-for="roomNames in products" v-bind:key="roomNames">
      {{ roomNames }} 원룸
      <p>50 만원</p>
    </h4>
  </div>
  <!-- <div>
    <div v-for="nameAndPrice in productsAndPrice" v-bind:key="nameAndPrice">
      {{ nameAndPrice[0]["roomLocation"] }}
    </div>
  </div> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      products: ["역삼동원룸", "천호동원룸", "마포구원룸"],
      price: [50, 60, 70],
      productsAndPrice: [
        { roomLocation: "역삼동원룸", roomPrice: "50" },
        { roomLocation: "천호동원룸", roomPrice: "60" },
        { roomLocation: "마포구원룸", roomPrice: "70" },
      ],
      menuElement: ["home", "shop", "about", "docs"],
    };
  },
  components: {},
};
</script>

<style>
.mainMenu {
  text-transform: uppercase;
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.mainMenu span {
  color: white;
  padding: 10px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
