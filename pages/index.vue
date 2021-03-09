<template>
  <div>
    <!-- Overview -->
    <div>
      <div class="d-flex justify-content-between my-2">
        <div class="m-3">
          <h5 class="mb-0"> Welcome Back, <span> Jane</span></h5>
          <p class="mb-0">Lorem ipsum dolor sit amet consectetur adi</p>
        </div>

        <div class="m-3 d-flex">
          <div class="mx-2 text-center">
            <p class="mb-0">7:00 PM</p>
            <div class="font-weight-light text-secondary">EST</div>
          </div>
          <div class="mx-2 text-center">
            <p class="mb-0">12:00 AM</p>
            <div class="font-weight-light text-secondary">LONDON</div>
          </div>
        </div>
      </div>
      <!-- Quick Actions -->
      <div class="quick_actions_div d-flex flex-wrap p-2 text-center">
        <nuxt-link :to="{name:'add-transaction'}"
                   class="d-flex flex-column quick_actions">
          <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
          <span>Add Transaction</span>
        </nuxt-link>
        <div class="d-flex flex-column quick_actions">
          <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
          <span> Place Order</span></div>
        <div class="d-flex flex-column quick_actions">
          <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
          <span> Create Invoice</span>
        </div>
        <div class="d-flex flex-column quick_actions">
          <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
          <span> Create Invoice</span>
        </div>

      </div>
    </div>


    <!-- <div id="chartDiv" class ="" ></div> -->

  </div>

</template>

<script>
    import SideBar from '/components/app-sidebar'

    export default {
        components: {SideBar},
        name: 'Dashboard',
        head() {
            return {
                title: "Dashboard",
                meta: [
                    {
                        hid: "description",
                        name: "description",
                        content: "SugoiFit Business Management System Dashboard"
                    }
                ]
            };
        }

    };


</script>

<style scoped>
  #chartDiv {
    width: 50%;
    height: 30%;
    position: absolute;
    top: 300px;
    right: 80px;
  }
</style>
