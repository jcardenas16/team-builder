<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <p class="navbar-brand">{{ leagueName }}</p>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarNav"
      aria-controls="navbarNav"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <router-link class="nav-link" to="/">{{ links[0] }}</router-link>
          <!-- <a class="nav-link" href="#">
            Home
            <span class="sr-only">(current)</span>
          </a>-->
        </li>
        <li class="nav-item">
          <!-- the code below makes it refresh the page when clicked -->
          <!-- <a class="nav-link" href="/about">Divisions</a> -->

          <!-- the code below doesnt make it refresh the page once clicked  -->
          <router-link class="nav-link" to="/divisions">
            {{ links[1] }}
          </router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/schedules">
            {{ links[2] }}
          </router-link>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/#">{{ links[3] }}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavaBar",
  data() {
    return {
      leagueName: "Sunday Futbol League",
      links: ["Home", "Divisions", "Schedules", "Nothing"]
    };
  }
};
</script>

<style scoped></style>
