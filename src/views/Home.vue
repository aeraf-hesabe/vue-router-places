<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
  </div>
</template>

<script>

import store from '@/store.js'

export default { 
  name: "Home",
  components: {
    
  },
  data() {
    return {
      destinations: store.destinations
    };
  }
};
</script>
