<template>
  <v-card class="pa-12" height="100%" flat>
    <v-card
      dark
      class="font rounded-lg"
      elevation="12"
      width="200"
      height="96%"
    >
      <v-navigation-drawer color="grey darken-4" floating permanent>
        <v-list dense rounded>
          <v-list-item-group  mandatory 
          active-class="bg-active">
            <v-list-item v-for="item in items" :key="item.title" link>
              <v-list-item-icon>
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-icon>

              <v-list-item-content>
                <v-list-item-title class="text-caption">{{ item.title }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </v-card>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Products", icon: "mdi-purse" },
        { title: "Order List", icon: "mdi-order-bool-ascending-variant" },
        { title: "Categories", icon: "mdi-shape" },
        { title: "Vendor", icon: "mdi-forum" },
        { title: "Shop", icon: "mdi-shopping" },
        { title: "Customers", icon: "mdi-account-group" },
      ],
    };
  },
};
</script>
<style scoped>
.font {
  font-family: Arial, Helvetica, sans-serif;
}
.bg-active {
  background-color: #ff8c00;
 /* opacity: 100%; */

}
</style>
