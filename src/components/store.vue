<template>
  <v-app>
    <div>
      <v-toolbar dark>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>
        <v-toolbar-title>Sports Store</v-toolbar-title>
      </v-toolbar>
    </div>

    <v-main>
      <v-card class="grey lighten-4 mt-6">
        <v-card>
          <v-row no-gutters style="height: 40px">
            <v-col style="width:50%" v-for="row in rows" :key="row" :align-self="row">
              <v-card class="pa-2" outlined title>
                {{ row }}
                <div v-if="row == 'Products'">
                <productList />
              </div>
              </v-card>
            </v-col>
          </v-row>
        </v-card>
      </v-card>
    </v-main>
  </v-app>
</template>

<script>
import productList from "./ProductList";
export default {
  name: "store",
  components: {
    productList,
  },
  data() {
    return {
      rows: ["Categories", "Products"],
    };
  },
};
</script>

<style lang="scss" scoped></style>
