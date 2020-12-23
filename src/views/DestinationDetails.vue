<template>
  <div class="destination">
    <h2>{{ destination.name }} Details</h2>
    <figure>
      <img :src="require(`@/assets/${destination.image}`)" />
    </figure>
    <p>{{ destination.description }}</p>
  </div>
</template>

<script>
import store from "@/store.js";
export default {
  data() {
    return {
      destinationId: this.$route.params.id
    };
  },
  computed: {
    destination() {
      return store.destinations.find(
      destination => destination.id === this.destinationId
      );
    }
  }
};
</script>
