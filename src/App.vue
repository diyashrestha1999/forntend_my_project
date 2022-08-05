<template>
  <v-app >
    <v-card class="d-flex justify-space-around mb-6" height="100%" flat tile >
      <div>
        <sidenav />
      </div>
      <div>
        <ProductList />
      </div>
    </v-card>
  </v-app>
</template>

<script>
import sidenav from "./components/SideNav";
import ProductList from "./components/ProductList";

export default {
  name: "App",

  components: {
    sidenav,
    ProductList,
  },

  data: () => ({
    //
  }),
};
</script>
