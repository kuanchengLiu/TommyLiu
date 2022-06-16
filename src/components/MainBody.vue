<template>
  <div>
    <v-carousel>
      <v-carousel-item
        v-for="n in image"
        :key="n"
        :src="n"
        reverse-transition="fade-transition"
        transition="fade-transition"
      ></v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      image: [require("@/assets/736461.png"), require("@/assets/67855.jpg")],
    };
  },
};
</script>

<style lang="scss" scoped></style>
