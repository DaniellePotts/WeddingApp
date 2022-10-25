<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import { Slide } from 'vue3-burger-menu'

</script>

<template>
  <div class="flex-container">
    <div class="flex-item-left">
      <div class="invite-banner">

        <img class="img"
          src="https://media-cldnry.s-nbcnews.com/image/upload/newscms/2019_45/2619891/181026_penguin_couple.jpg" />
        <div class="top-left">
          <Slide>
           
              <span>
                <RouterLink to="/venue">Venue</RouterLink>
              </span>
              <span>
                <RouterLink to="/invites">Invites</RouterLink>
              </span>
           
          </Slide>
        </div>
      </div>
    </div>
    <div class="flex-item-right initial-info">
      <div class="invite-banner">
        <img class="img" src="./assets/flower-g7006753f2_1920.png" />

        <div class="centered">
          <p>Roker Hotel, Sunderland</p>
          <p>Friday, September 8th 2023</p>
          <button class="button button4">                <RouterLink to="/invites" class="rsvp-button">RSVP</RouterLink>
</button>
        </div>

      </div>
    </div>
  </div>
</template>


<style scoped>
.top-left {
  position: absolute;
  top: 8px;
  left: 16px;
}
.rsvp-button{
  color:black
}
.button {
  background-color: #4CAF50;
  /* Green */
  border: none;
  color: white;
  padding: 16px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  transition-duration: 0.4s;
  cursor: pointer;
}

.button4 {
  background-color: white;
  color: black;
  border: 2px solid #e7e7e7;
}

.button4:hover {
  background-color: #e7e7e7;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.invite-banner {
  position: relative;
  text-align: center;
  color: black;
}

.initial-info {
  color: black
}

.flex-container {
  display: flex;
  flex-wrap: wrap;

  /* this centers vertically */
  align-items: center;

  /* this centers horizontally */
  text-align: center;

  /* background colour for whole container */
  background-color: #f8f8f6;
}

.img {
  height: 100%;
  width: 100%;
}

.flex-item-left {
  flex: 65%;
}

.flex-item-right {
  flex: 35%;
}

.tag {
  float: left;
  position: absolute;
  left: 0px;
  top: 0px;
  background-color: green;
  z-index: 1000;
}

.button {
  color: black;
  border: 2px solid #555555;
  padding: 10px 22px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  margin: 20px 2px;
  cursor: pointer;
}

* {
  box-sizing: border-box;
}

@media (max-width: 800px) {

  .flex-item-right,
  .flex-item-left {
    flex: 100%;
  }
}
</style>
