<template>
  <nav class="navbar" id="boxshadow" role="navigation" aria-label="main navigation">
  <div class="navbar-brand">
    <a class="navbar-item" href="https://bulma.io">
      <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28">
    </a>

    <a role="button" @click="toggleHamburger" class="navbar-burger burger" :class="{'is-active': hamburgerToggled}" aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
      <span aria-hidden="true"></span>
    </a>
  </div>

  <div id="navbarBasicExample" class="navbar-menu" :class="{'is-active': hamburgerToggled}">
    <div class="navbar-start">
      <a class="navbar-item">
        Home
      </a>

      <a class="navbar-item">
        Divisions
      </a>

      <!-- <div class="navbar-item has-dropdown is-hoverable">
        <a class="navbar-link">
          More
        </a>

        <div class="navbar-dropdown">
          <a class="navbar-item">
            About
          </a>
          <a class="navbar-item">
            Jobs
          </a>
          <a class="navbar-item">
            Contact
          </a>
          <hr class="navbar-divider">
          <a class="navbar-item">
            Report an issue
          </a>
        </div>
      </div> -->
    </div>

    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a class="button is-primary">
            <strong>Sign up</strong>
          </a>
          <a class="button is-light">
            Log in
          </a>
        </div>
      </div>
    </div>
  </div>
</nav>
</template>

<script>
export default {
  name: "NavaBar",
  methods: {
    toggleHamburger() {
      this.hamburgerToggled = !this.hamburgerToggled
    }
  },
  data() {
    return {
      hamburgerToggled: false,
      leagueName: "Sunday Futbol League",
      links: ["Home", "Divisions", "Schedules", "Nothing"]
    };
  }
};
</script>

<style lang="scss" scoped>
#boxshadow {
  border: 1px solid;
  padding: 10px;
  box-shadow: 5px 1px;
}
</style>
