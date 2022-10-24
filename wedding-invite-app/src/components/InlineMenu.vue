<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";

</script>

<template>
<div class="inline-menu">
    <ul>
  
  <li><RouterLink to="/home">Home</RouterLink></li>
  <li><RouterLink to="/venue">Venue</RouterLink></li>

  <li><RouterLink to="/contact">Contact</RouterLink></li>
  <li> <RouterLink to="/invites">Invites</RouterLink></li>
 

</ul>
</div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
