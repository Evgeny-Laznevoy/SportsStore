<template>
  <div>
    <v-card
      class="mx-auto mb-2 mt-2"
      outlined
      v-for="(product,i) in products"
      :key="i"
    >
      <v-container fluid>
        <div class="d-flex flex-no-wrap justify-space-between">
          <div>
            <v-card-title>
              {{ product.name }}
            </v-card-title>
            <v-card-subtitle>
              {{ product.description }}
            </v-card-subtitle>
          </div>
          <span>
              {{ product.price }}
          </span>
        </div>
      </v-container>
    </v-card>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "productList",
  computed: {
    ...mapState(["products"]),
  },
};
</script>

<style lang="scss" scoped>
</style>
