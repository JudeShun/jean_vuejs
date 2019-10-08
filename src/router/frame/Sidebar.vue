<template>
  <sidebar-menu :menu="menu" />
</template>
  <style scoped>
  .v-sidebar-menu{
    height: 95%;
    margin-top:55px;
    background-color:black;
    }
 </style>
<script>
export default {
  data() {
    return {
      menu: [
        {
          header: true,
          title: "Main Navigation",
          hiddenOnCollapse: true
        },
        {
          href: "/Dashboard",
          title: "Dashboard",
          icon: "fa fa-chart-area",
        },
        {
          href: "/Subjects",
          title: "Subjects",
          icon: "fa fa-chart-area",
        },
        {
          href: "/PersonalInfo",
          title: "Personal Info",
          icon: "fa fa-chart-area",
        },
    
        {
          href: "/Logout",
          title: "Logout",
          icon: "fa fa-chart-area",
        }
      ]
    };
  }
};
</script> 