<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import { Slide } from 'vue3-burger-menu'
</script>

<template>
  <div class="container">

    <div class="row">
      <div class="column">

        <img src="https://media-cldnry.s-nbcnews.com/image/upload/newscms/2019_45/2619891/181026_penguin_couple.jpg"
          height="290px">
      </div>
      <div class="column">
        <div class="invite-content">
          <span class="text-content">Roker Hotel, Sunderland</span>
          <span>Friday, September 8th 2023</span>
          <button>RSVP</button>
        </div>

      </div>
    </div>
  </div>

</template>

<style scoped>
.container {
  border: 1px solid #DDDDDD;
  width: 200px;
  height: 200px;
  position: relative;
}

.tag {
  float: left;
  position: absolute;
  left: 0px;
  top: 0px;
  background-color: green;
  z-index: 1000;
}

* {
  box-sizing: border-box;
}

.row {
  display: flex;
  width: 50em
}

/* Create two equal columns that sits next to each other */
.column {
  flex: 50%;
  padding: 10px;
  height: 300px;
  background-color: #F8F8F6
}

.invite-content {
  text-align: center;
  padding: 100px;
}

.text-content {
  padding: 5px
}

.center {
  margin: auto;
  width: 60%;
  padding: 10px;
}
</style>
