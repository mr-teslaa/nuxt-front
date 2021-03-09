<template>
  <div>
    <nav class="side-navbar">
      <!-- <img :src="navSVG" alt=""> -->
      <div class="d-flex flex-row justify-content-start ml-4">
        <h4 class="nav_logo"> SugoiFit <span>Dashboard</span></h4>
      </div>
      <div class="d-flex flex-row">
        <div class="profile mt-3 mb-4 ">
          <h6 id="profile_name"> Jane S.</h6>
          <h6 id="profile_ID"> ID 1234567</h6>
          <h6 id="role"> Role: Business Owner</h6>
        </div>
        <img class="" id="profile-icon" src="~/assets/uploads/Profile_icon.png" alt="">

      </div>
      <!-- <span class="heading">Main</span> -->
      <ul class="list-unstyled">
        <li>
          <nuxt-link :to="{name:'index'}">Dashboard</nuxt-link>
        </li>
        <li class="d-flex flex-row align-items-center"><a href="">Manage Products </a></li>
        <li class="d-flex flex-row align-items-center"><a href="">Manage Sales </a>
          <font-awesome-icon :icon="['fas','angle-down']" class="mx-2"></font-awesome-icon>
        </li>
        <li class="d-flex flex-row align-items-center"><a href="">Manage Financial Statements </a>
           <font-awesome-icon :icon="['fas','angle-down']" class="mx-2"></font-awesome-icon>
        </li>
        <li class="d-flex flex-row align-items-center"><a href="">View Reports </a>
          <font-awesome-icon :icon="['fas','angle-down']" class="mx-2"></font-awesome-icon>
        </li>
        <li class="d-flex flex-row align-items-center"><a href="">Manage Roles </a>
           <font-awesome-icon :icon="['fas','angle-down']" class="mx-2"></font-awesome-icon>
        </li>

      </ul>

    </nav>
  </div>
</template>

<script>
    export default {
        name: 'sideBar',
        data() {
            return {}
        }
    }
</script>


<style scoped>

</style>
