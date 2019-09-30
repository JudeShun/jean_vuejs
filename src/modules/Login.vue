<template>

  <div class="row loginPage">
      <div class="col-md-4"></div>
      <div class="col-md-4">
        <div class="container">
          <div class="card">
            <div class="card-header">LOGIN</div>
            <div class="card-body">
              <div class="form-group">
                <label for="email" class="bmd-label-floating">Email</label>
                <input
                  type="text"
                  class="form-control"
                  id="email"
                  v-model="email"
                  placeholder="Enter email..."
                />
              </div>
              <div class="form-group">
                <label for="pwd" class="bmd-label-floating">Password</label>
                <input
                  type="password"
                  class="form-control"
                  id="passw"
                  v-model="password"
                  placeholder="Enter password..."
                />
              </div>
              <center>
                <button type="button" class="btn btn-outline-success login-btn" id="btnLogin" @click='submit'>Login</button>
                
              </center>
            </div>
          </div>
        </div>
      </div>
    </div>

  </template>
<style scoped lang="scss">
@import "assets/colors.scss";

#username {
  color: $primary !important;
}
#pass {
  color: $primary !important;
}
</style>
<script>
import AUTH from 'services/auth'
export default {
  data() {
    AUTH
    return {
      email: "",
      password: ""
    };
  },
  methods: {
    submit: function(e) {
      e.preventDefault();
      AUTH.login(this.email, this.password)
    },

  }
};
</script>

<style scoped>
  .card {
  background-color: pink;
  margin-top: 50px;
  padding: 30px;
}
  

.h3 {
  margin-left: 500px;
  margin-top: 300px;
  font-size: 40px;
  font-family: Times new;
}
.nav {
  margin-block: auto;
}

.card-header {
  text-align: center;
  font-weight:bold;
  font-size: 30px;
  letter-spacing: 5px;
  background-color: black;
  color:pink;
  
}

label {
  font-weight:bold;
}

input {
  border: 2px solid black;
}

#btnLogin {
  color: black;
  border: 2px solid black;
  margin-top: 5px;
  padding: 12px 30px;
}

</style>
