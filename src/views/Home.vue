<template>
  <div class="home">
    <h1>All Locations</h1>
    <div class="destinations">
      <div v-for="destination in destinations" :key="destination.name">
        <router-link
          :to="{
            name: 'DestinationDetails',
            params: { slug: destination.slug }
          }"
        >
          <h2>{{ destination.name }}</h2>
        </router-link>
        <router-link
          :to="{
            name: 'DestinationDetails',
            params: { slug: destination.slug }
          }"
        >
          <figure>
            <img :src="require(`@/assets/${destination.image}`)" />
          </figure>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import store from "@/store.js";

export default {
  name: "Home",
  components: {},
  data() {
    return {
      destinations: store.destinations
    };
  }
};
</script>

<style scoped>
.home {
  max-width: 1400px;
  margin: 0 auto;
}
img {
  max-width: 200px;
}
.destinations {
  display: flex;
  justify-content: space-between;
}
</style>
