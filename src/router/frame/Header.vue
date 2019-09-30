<template>
  <div>
    <b-navbar toggleable="lg" type="dark" class="bg-dark" variant="info">
      <b-navbar-brand href="#" class="text text-light" id="title">JM APP</b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <b-nav-item @click="redirect('/Login')" class="text text-light" id="login">Login</b-nav-item>
            <b-nav-item @click="redirect('/Register')" class="text text-light" id="signup">Sign Up</b-nav-item>
          </b-navbar-nav>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>
<style scoped lang="scss">
@import "assets/colors.scss";
#title {
  color: $danger !important;
}
</style>
<script>
import ROUTER from "router";
export default {
  methods: {
    redirect(router) {
      ROUTER.push(router);
    }
  }
};
</script>
