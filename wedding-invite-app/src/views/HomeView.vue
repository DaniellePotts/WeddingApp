<script >
import { RouterLink, RouterView } from "vue-router";
import Navigation from '../components/Navigation.vue'

export default
  {
    data() {
      return {
        name: 'Vue.js'
      }
    },
    components:{
      Navigation
    }
  }


</script>

<template>
 <Navigation/>
  <div class="flex-container">

    <div class="flex-item-left">

      <div class="content-image-hover">

        <img class="img"
          src="https://media-cldnry.s-nbcnews.com/image/upload/newscms/2019_45/2619891/181026_penguin_couple.jpg" />
        <!-- <div class="bottom-left">
          <span>Danielle & Elliott's Wedding</span>
        </div> -->

      </div>
    </div>
    <div class="flex-item-right initial-info">
      <div class="content-image-hover">
        <img style="height: 520px; width: 100%;" class="img" src="../assets/flower-g7006753f2_1920.png" />
        <div class="centered">
          <p>Roker Hotel, Sunderland</p>
          <p>Friday, September 8th 2023</p>
          <button class="button button4">
            <RouterLink to="/invites" class="rsvp-button">RSVP</RouterLink>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>


<style scoped>
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}

.topnav {
  overflow: hidden;
  background-color: #333;
}

.topnav a {
  float: left;
  display: block;
  color: #f2f2f2;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
  font-size: 17px;
}

.topnav a:hover {
  background-color: #ddd;
  color: black;
}

.topnav a.active {
  background-color: #04AA6D;
  color: white;
}

.topnav .icon {
  display: none;
}

@media screen and (max-width: 600px) {
  .topnav a:not(:first-child) {
    display: none;
  }

  .topnav a.icon {
    float: right;
    display: block;
  }
}

@media screen and (max-width: 600px) {
  .topnav.responsive {
    position: relative;
  }

  .topnav.responsive .icon {
    position: absolute;
    right: 0;
    top: 0;
  }

  .topnav.responsive a {
    float: none;
    display: block;
    text-align: left;
  }
}

.rsvp-button {
  color: black
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


.initial-info {
  color: black
}



.img {
  height: 100%;
  width: 100%;
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


</style>
