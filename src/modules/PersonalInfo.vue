<template>
  <div id="container">
    <div class="jumbotron">
      <h1>Personal Information</h1>
    </div>
    <div id="card">
      <b-card no-body class="overflow-hidden" style="max-width: 540px;">
        <b-row no-gutters>
          <b-col md="6">
            <b-card-img :src="require('assets/user.png')" class="rounded-0"></b-card-img>
          </b-col>
          <b-col md="6">
            <b-card-body title="Personal Info">
                <hr>
              <b-card-text>
                <h6>Username: {{firstname}}</h6>
                <h6>Email: {{email}}</h6>
                <h6 type="password">Password: {{password}}</h6>
              </b-card-text>
              <button @click = "update()">Update</button>

            </b-card-body>
          </b-col>
        </b-row>
      </b-card>
    </div>
  </div>
</template>

<style>
.jumbotron{
    padding: 20px;
    text-align: center;
}
#card {
  margin-top: 50px;
  margin-left: 380px;
}
</style>
<script>

import AUTH from 'services/auth'

export default {
  name: "container",
  data() {
    return {
      firstname: sessionStorage.getItem("Firstname"),
      email: sessionStorage.getItem("Email"),
      password: sessionStorage.getItem("Password")
    };
  },
  methods:{
    update: function(){
      // e.preventDefault();
      AUTH.update(this.firstname,this.email, this.password)
      // AUTH.update()

    }
  }
};
</script>
