<template>
  <!-- <div>
    <div class="jumbotron">
      <h1>Dashboard</h1>
    </div> -->
   
    <div id="card">
      <b-card no-body class="overflow-hidden">
        <center>
          <b-card-img id="image" :src="require('assets/user.png')" class="rounded-0"></b-card-img>
          <b-row no-gutters>
            <b-card-body>
              <h1>HI {{firstname}}!</h1>
              <h3>Welcome</h3>
            </b-card-body>
          </b-row>
        </center>
      </b-card>
    </div>
  <!-- </div> -->
</template>

<style scoped>
.overflow-hidden{
  color:skyblue;
}
#card {
  margin-top: 30px;
  margin-left: 400px;
  height:500px;
  width: 550px;
}
/* .jumbotron{
    padding:20px;
    text-align: center;
    color:blue;
} */
#image {
  width: 250px;
  height: 220px;
}
</style>

<script>
// import ROUTER from "router";
export default {
  name: "card",
  data() {
    return {
      firstname: sessionStorage.getItem("Firstname")
    };
  },
};
</script>

