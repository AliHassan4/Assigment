<template>
  <div class="container">
    <div class="row">
      <div class="col-md-8 offset-md-2">
        <div class="light-green text-white text-center">
          <div class="row">
            <div class="col-md-2">
              <span>15:52</span>
            </div>
            <div class="col-md-6 offset-md-3 text-end">
              <i class="fas fa-wifi px-2"></i>
              <i class="fas fa-mobile-alt px-2"></i>
              <i class="fas fa-battery-half px-2"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="col-md-8 offset-md-2">
        <div class="bg-success text-white text-center">
          <div class="row px-5 py-5">
            <div class="col-md-6 text-start">
              <h4><i class="fas fa-bars"></i> Search</h4>
            </div>
            <div class="col-md-2 offset-md-4 text-center">
              <span><i class="fas fa-search"></i></span>
            </div>
          </div>
          <div class="row">
            <ul class="list-group list-group-horizontal">
              <li class="list-group-item underline fs-3">Yesterday</li>
              <li class="list-group-item fs-3">Today</li>
              <li class="list-group-item fs-3">Tomorrow</li>
              <li class="list-group-item">
                <i class="far fa-calendar-alt fa-2x"></i>
              </li>
            </ul>
          </div>
        </div>
        <tabs />
      </div>
    </div>
  </div>
</template>
<script>
import Tabs from "./Tabs.vue";
export default {
  components: { Tabs },
  name: "Home",
};
</script>

<style scoped>
.underline {
  border-bottom: 4px solid white !important;
}
.bg-success {
  background-color: #00b232 !important;
}
.list-group-item {
  width: 25%;
  background-color: transparent;
  border: none;
  color: #fff;
}
.light-green {
  background-color: #00a431;
}
</style>
