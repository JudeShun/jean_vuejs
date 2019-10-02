<template>
<div>
 <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand href="#">Student's Panel</b-navbar-brand>

    <b-navbar-toggle target="nav-collapse" is-nav v-if="auth.user === null"></b-navbar-toggle>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-form>
          <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
          <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
        </b-nav-form>

        <b-nav-item-dropdown right>
          <!-- Using 'button-content' slot -->
          <template v-slot:button-content>
            <em>User</em>
          </template>
          <b-dropdown-item href="#">Profile</b-dropdown-item>
          <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          <b-dropdown-item href="#" v-on:click="redirect('/login')">Login</b-dropdown-item>
          <b-dropdown-item href="#" v-on:click="redirect('/register')">Register</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
  </b-navbar>
</div>
</template>

<script>
 import ROUTER from 'router'
 import AUTH from "services/auth"
 export default {
   data(){
     return {
       auth: AUTH
     }
   },
     methods : {
         redirect (route) {
             ROUTER.push(route)
         }
     }
 }
</script>