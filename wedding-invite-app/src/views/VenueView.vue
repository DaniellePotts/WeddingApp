<script>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <div class="venue">
    <ul>

      <li>
        <RouterLink to="/home">Home</RouterLink>
      </li>
      <li>
        <RouterLink to="/venue">Venue</RouterLink>
      </li>

      <li>
        <RouterLink to="/contact">Contact</RouterLink>
      </li>
      <li>
        <RouterLink to="/invites">Invites</RouterLink>
      </li>


    </ul>

    <div class="row">

      <div class="column" style="background-color:#f8f8f6;">
        <iframe width="600" height="450" style="border:0" loading="lazy" allowfullscreen
          referrerpolicy="no-referrer-when-downgrade"
          src="https://www.google.com/maps/embed/v1/place?key=AIzaSyD9YauwtDfU_cPN1bWMnf0Jl0y1x9c1MSs&q=Space+Needle,Roker+Hotel+Sunderland">
        </iframe>
      </div>
      <div class="column" style="background-color:#f8f8f6;">
        <div class=" venue-info">
          <div class="address">
            <h1>Roker Hotel, BW Premier Collection</h1>
            <p>Roker Terrace</p>
            <p>Roker</p>
            <p>Sunderland</p>
            <p>SR6 9ND</p>
            <p>Phone: 0191 567 1786</p>
            <p>Website: <a href="https://rokerhotel.co.uk/" target="_blank">https://rokerhotel.co.uk/</a></p>
            <p>Rooms can be booked at a discounted price if you say it's for our wedding</p>

          </div>
          <div class="parking-traveling">
            <h1>Parking & Traveling</h1>
            <p>There is parking located at the front and back of the hotel.</p>
            <p>To travel via public transport, St Peters Metro is the closest station. Alternatively, buses to Roker can
              be found <a target="_blank" href="https://bustimes.org/localities/roker">here</a></p>

          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .venue {}
}


ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover:not(.active) {
  background-color: #111;
}

.active {
  background-color: #04AA6D;
}

.venue-info {
  margin-top: 10%;
  text-align: right;
  color: #4c5747
}

* {
  box-sizing: border-box;
}

.row {
  display: flex;
}

/* Create two equal columns that sits next to each other */
.column {
  flex: 50%;
  padding: 10px;
  height: 100%;
  /* Should be removed. Only for demonstration */
}
</style>
