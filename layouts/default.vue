<template>
  <div>
    <div class="sidenav">
      <sidebar/>
    </div>
    <b-sidebar class="d-lg-none" id="sideBar" backdrop no-header>
      <template #default="{ hide }">
        <sidebar/>
        <font-awesome-icon :icon="['fas','times']" class="close-icon" @click="hide"></font-awesome-icon>
      </template>
    </b-sidebar>
    <!-- Page content -->
    <div class="main">
      <top-bar/>
      <nuxt/>
    </div>
  </div>
</template>

<script>
    import Sidebar from "../components/app-sidebar";
    import TopBar from "../components/top-bar";

    export default {
        components: {TopBar, Sidebar},
    }
</script>
<style scoped>
  .close-icon {
    position: absolute;
    right: 10px;
    top: 10px;
    font-size: 20px;
    color: black;
  }
</style>
<style>
  html {
    font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
    font-size: 16px;
    word-spacing: 1px;
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    box-sizing: border-box;
  }

  *,
  *::before,
  *::after {
    box-sizing: border-box;
    margin: 0;
  }


  .sidenav {
    height: 100%; /* Full-height: remove this if you want "auto" height */
    width: 320px; /* Set the width of the sidebar */
    position: fixed; /* Fixed Sidebar (stay in place on scroll) */
    z-index: 1; /* Stay on top */
    top: 0; /* Stay at the top */
    left: 0;
    overflow-x: hidden; /* Disable horizontal scroll */
    transition: all 0.5s ease 0s;
  }

  /* Style page content */
  .main {
    margin-left: 320px; /* Same as the width of the sidebar */
    min-height: 100vh;
    transition: all 0.5s ease 0s;
  }

  @media (max-width: 992px) {
    .main {
      margin-left: 0
    }

    .sidenav {
      display: none
    }
  }

  .isNotSidebar .main {
    margin-left: 0;
    transition: all 0.5s ease 0s;
  }

  .isNotSidebar .sidenav {
    margin-left: -320px;
    transition: all 0.5s ease 0s;
  }

</style>


