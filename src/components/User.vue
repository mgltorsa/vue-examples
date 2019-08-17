<template>
  <b-container fluid id="user-view">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-navbar-nav class="ml-auto">
        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template slot="button-content">
            <img src="https://placekitten.com/g/30/30" alt="Kitten" />

            <em>User name</em>
          </template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-navbar>
    <br />
    <br />
    <b-row>
      <b-col sm="6">
        <Side id="side"></Side>
      </b-col>
      <b-col>
        <Main id="main"></Main>
      </b-col>
    </b-row>
      <footer>Footer</footer>
  </b-container>
</template>

<script>
import Main from "./Main.vue";
import Side from "./Side.vue";
export default {
  name: "User",
  props: {
    username: String
  },
  components: {
    Main,
    Side
  }
};
</script>

<style scoped>
footer{
    background:blue;
}
</style>