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
                <button type="button" class="btn btn-outline-success login-btn" id="btnLogin" @click='log'>Login</button>
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
import AUTH from "services/auth";
// import jquery from "jquery";
// import ROUTER from "router";
export default {
  data() {
    AUTH
    return {
      email: "",
      password: ""
    };
  },
  methods: {
    log: function(e) {
      e.preventDefault();
      // let user = AUTH.login(this.email, this.password);
      AUTH.login(this.email, this.password);
      // if (this.email == "" || this.password == "") {
      //   alert("Please Enter your email and password!!! Inputs are Required..");
      //   ROUTER.push("/Login");
      // }
      // AUTH.setUser(user);
      // if (user != null) {
      //   alert("Successfully Login!!!");
      //   ROUTER.push("/Dashboard");
      // } else {
      //   alert("Please Register First!!!");
      //   ROUTER.push("/Login");
      // }

      // let link = `http://localhost:3000/db/create/${this.content.email}/${
      //   this.content.password
      // }`;
      // jquery
      //   .ajax({
      //     url: link,
      //     method: "GET",
      //     headers: {
      //       "Access-control-Allow-Origin": "*"
      //     }
      //   })
      //   .then(response => {
      //     alert(response.username);
      //   });
    }
  }
};
</script>

<style scoped>
  .card {
   background-color:skyblue;
  margin-top: 60px;
  padding: 50px;
  height:500px;
  width:400px;
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
  font-size: 20px;
  letter-spacing: 5px;
  background-color: black; 
  color:skyblue;
  
  
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
