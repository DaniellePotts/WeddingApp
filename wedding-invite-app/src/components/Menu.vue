

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Homepage from "./components/Homepage.vue";
import { Slide } from 'vue3-burger-menu'

</script>

<template>
         <div class="tag">
          <Slide>

            <RouterLink to="/venue">Venue</RouterLink>
            <RouterLink to="/contact">Contact</RouterLink>
            <RouterLink to="/invites">Invites</RouterLink>


          </Slide>
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
