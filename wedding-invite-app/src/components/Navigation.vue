<script>
import { RouterLink, RouterView } from "vue-router";



export default
    {
        data() {
            return {
                name: 'Vue.js'
            }
        },
        methods: {
            greet() {
                var x = document.getElementById("myTopnav");
                if (x.className === "topnav") {
                    x.className += " responsive";
                } else {
                    x.className = "topnav";
                }
            }
        },
        
    components: {
      Navigation
  }
    }
</script>

<template>
    <div class="navigation">
        <div class="topnav" id="myTopnav">
            <img style="height:72%; width:10%" src="../assets/floral-design.png"/>
           
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/venue">Venue</RouterLink>
            <RouterLink to="/invites">Invites</RouterLink>
           
            <a href="javascript:void(0);" class="icon" @click="greet">
                <i class="fa fa-bars"></i>
            </a>
        </div>
    </div>
</template>

<style>
.topnav{
overflow: hidden;
    background-color: #333;
    /* align-items: center; */
    background-color: white;
    /* position: fixed; */
    /* text-align: center; */
    /* color: black; */
    top: 0;
    left: 0;
    right: 0;
    height: 80px;
    display: flex;
    align-items: center;
    box-shadow: 0 0 25px 0 black;
}
.topnav a {
    float: left;
    display: block;
    color: black;
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
</style>
