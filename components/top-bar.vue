<template>
  <div class="top-bar bg-light">
    <div>
      <img class="d-none d-lg-block cursor-pointer m-2"
           src="~/assets/uploads/align-left.png" alt=""
           @click="isNotSidebar=!isNotSidebar"
           width="30px"
      >
      <img class="cursor-pointer m-2 d-lg-none"
           src="~/assets/uploads/align-left.png" alt=""
           v-b-toggle.sideBar
           width="30px"
      >
    </div>

    <div class="d-flex align-items-center mr-3">
      <h6 class="m-2">Jane S.</h6>
      <img class="m-2" id="top-user-icon" src="~assets/uploads/Profile_icon.svg" alt="">
      <img class="m-2" src="~assets/uploads/settings.svg" alt="">
    </div>
  </div>
</template>

<script>
    export default {
        name: "top-bar",
        head() {
            return {
                bodyAttrs: {
                    class: this.isNotSidebar ? 'isNotSidebar' : ''
                }
            }
        },
        data() {
            return {
                isNotSidebar: false
            }
        }
    }
</script>

<style scoped>
  .burger {
    margin: 10px;
    font-size: 25px;
  }

  .top-bar {
    position: sticky;
    top: 0;
    z-index: 1020;
    width: 100%;
    height: 59px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 9px -1px 13px -5px grey;
  }
</style>
