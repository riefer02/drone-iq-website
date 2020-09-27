<template>
  <v-col
    cols="12"
    lg="3"
    xs="12"
    sm="12"
    class="d-flex justify-center mx-5 mb-5"
  >
    <v-card class="" flat min-width="300px">
      <!--  <v-img
      class="white--text align-end"
      height="200px"
      src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
    >
      <v-card-title>Top 10 Australian beaches</v-card-title>
    </v-img> -->

      <!--   <v-card-subtitle class="pb-0">Number 10</v-card-subtitle> -->
      <div class="custom-icon">
        <v-icon v-if="item.icon" x-large>mdi-{{ item.icon }}</v-icon>
      </div>

      <h2 class="mb-10 font-weight-regular">{{ item.title }}</h2>

      <div>{{ item.description }}</div>

      <!--    <v-card-actions>
      <v-btn color="orange" text>
        Share
      </v-btn>

      <v-btn color="orange" text>
        Explore
      </v-btn>
    </v-card-actions> -->
    </v-card>
  </v-col>
</template>

<script>
export default {
  name: "Card",
  props: {
    item: {
      type: Object,
      required: true,
    },
  },

  data() {
    return {};
  },
};
</script>

<style>
.v-card {
  flex-grow: 1;
}

.custom-icon {
  position: absolute;
  right: 1%;
  top: 1px;
  height: 50px;
  width: 50px;
  opacity: 60%;
}
</style>
