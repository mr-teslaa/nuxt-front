<template>
  <div class="d-flex flex-row py-2 text-center flex-wrap">
    <button class="btnStyle" id="assetBtn" tabindex="0">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span>Add Asset</span>
    </button>
    <b-popover target="assetBtn" triggers="hover" placement="bottom" custom-class="custom-popover">
      <div class="d-flex flex-column">
        <b-link class="pop-link" :to="{name:'transaction-non-current-asset-create'}">Non Current Asset</b-link>
        <hr class="my-0"/>
        <b-link class="pop-link" :to="{name:'transaction-current-asset-create'}">Current Asset</b-link>
      </div>
    </b-popover>
    <button class="btnStyle" id="liabilityBtn" tabindex="0">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span> Add Liabillity</span>
    </button>
    <b-popover target="liabilityBtn" triggers="hover" placement="bottom" custom-class="custom-popover">
      <div class="d-flex flex-column">
        <b-link class="pop-link" :to="{name:'transaction-long-term-liability-create'}">Long Term Liability</b-link>
        <hr class="my-0"/>
        <b-link class="pop-link" :to="{name:'transaction-current-liability-create'}">Liability</b-link>
      </div>
    </b-popover>
    <b-link class="btnStyle pop-link" :to="{name:'transaction-expenses-create'}">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span> Add Expense</span>
    </b-link>
    <b-link class="btnStyle pop-link" :to="{name:'transaction-purchases-create'}">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span>Add Purchases</span>
    </b-link>
    <b-link class="btnStyle pop-link" :to="{name:'transaction-sales-create'}">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span> Add Sales</span>
    </b-link>
    <b-link class="btnStyle pop-link" :to="{name:'transaction-non-current-asset-create'}">
      <font-awesome-icon :icon="['fas','plus']"></font-awesome-icon>
      <span> Add Equity</span>
    </b-link>
  </div>
</template>

<script>
    export default {
        name: "transaction-top"
    }
</script>

<style scoped>
  .btnStyle {
    margin: 5px;
    background-color: #DFFBFF;
    width: 10rem;
    padding: 10px;
    display: flex;
    flex-direction: column;
    text-decoration: none !important;
    color: #222222;
    align-items: center;
    justify-content: center;
    border-radius: 10px;
    border: none;
  }
</style>
