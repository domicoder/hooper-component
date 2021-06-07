<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/home_logo.jpeg')"
          class="my-3"
          contain
          height="200"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3 title-enjoy">PLAYA CALETON VIP</h1>
      </v-col>

      <v-col class="mb-5" cols="12"> </v-col>
    </v-row>

    <h1>{{ beach1 }}</h1>

    <hooper
      group="group1"
      infiniteScroll="true"
      :centerMode="true"
      style="height: 400px"
    >
      <slide v-for="(item, i) in items" :key="i">
        <v-img :src="item.src" class="my-3" contain height="400" />
      </slide>
      <hooper-navigation slot="hooper-addons"></hooper-navigation>
      <hooper-navigation slot="hooper-addons"></hooper-navigation>
    </hooper>
    <hooper group="group1" infiniteScroll="true" :itemsToShow="4">
      <slide v-for="(item, i) in items" :key="i">
        <v-img :src="item.src" class="my-3" contain />
      </slide>
    </hooper>

    <h1 class="mt-5">{{ beach2 }}</h1>

    <hooper
      group="group2"
      infiniteScroll="true"
      :centerMode="true"
      style="height: 400px"
    >
      <slide v-for="(item, i) in items2" :key="i">
        <v-img :src="item.src" class="my-3" contain height="400" />
      </slide>
      <hooper-navigation slot="hooper-addons"></hooper-navigation>
      <hooper-navigation slot="hooper-addons"></hooper-navigation>
    </hooper>
    <hooper group="group2" infiniteScroll="true" :itemsToShow="4">
      <slide v-for="(item, i) in items2" :key="i">
        <v-img :src="item.src" class="my-3" contain />
      </slide>
    </hooper>
  </v-container>
</template>

<script>
import { Hooper, Slide, Navigation as HooperNavigation } from "hooper";
import "hooper/dist/hooper.css";

export default {
  name: "PrincipalPage",
  components: {
    Hooper,
    Slide,
    HooperNavigation,
  },
  data: () => ({
    items: [
      {
        id: "1",
        src: "https://live.staticflickr.com/6079/6136071267_797265d54d.jpg",
      },
      {
        id: "2",
        src: "http://c1.staticflickr.com/4/3652/3286547152_59fd376d3c.jpg",
      },
      {
        id: "3",
        src: "https://c1.staticflickr.com/1/189/442112564_aad204d2de.jpg",
      },
      {
        id: "4",
        src: "https://live.staticflickr.com/8685/17081448532_77263fa0dd.jpg",
      },
      {
        id: "5",
        src: "https://c1.staticflickr.com/5/4451/24162846828_8500a2fec4.jpg",
      },
      {
        id: "6",
        src: "https://farm4.staticflickr.com/3199/2386530366_47bfae6da0_z.jpg",
      },
    ],
    items2: [
      {
        id: "1",
        src: "https://live.staticflickr.com/6079/6136071267_797265d54d.jpg",
      },
      {
        id: "2",
        src: "http://c1.staticflickr.com/4/3652/3286547152_59fd376d3c.jpg",
      },
      {
        id: "3",
        src: "https://c1.staticflickr.com/1/189/442112564_aad204d2de.jpg",
      },
      {
        id: "4",
        src: "https://live.staticflickr.com/8685/17081448532_77263fa0dd.jpg",
      },
      {
        id: "5",
        src: "https://c1.staticflickr.com/5/4451/24162846828_8500a2fec4.jpg",
      },
      {
        id: "6",
        src: "https://farm4.staticflickr.com/3199/2386530366_47bfae6da0_z.jpg",
      },
    ],
    beach1: "Playa Grande",
    beach2: "Playa Chiquita",
  }),
  computed: {
    totalItems() {
      return this.items.length;
    },
  },
};
</script>
<style>
.title-enjoy {
  font-size: 2rem;
  color: #0e2c4c;
  font-family: "Enjoy";
  font-weight: bold;
}
</style>