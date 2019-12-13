<template>
  <div class="">
    <div class="probanner">
      <img src="/img/product.png" alt="product" class="animated zoomInLeft">
    </div>
    <div class="profunction">
      <div class="profunction_title">
          <h1>功能介绍</h1>
          <p>适用中介从业圈子的全方位功能服务</p>
      </div>
      <div>
        <img src="/img/app_content.png" alt="profunction" :class="{'animated':animate, 'heartBeat':animate}">
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        scroll: 0,
        animate: false,
      }
    },
    methods: {
      menu() {
        this.scroll = document.documentElement.scrollTop || document.body.scrollTop;
        if (this.scroll > 140) {
          this.animate = true
        }
      }
    },
    mounted() {
      this.menu()
      window.addEventListener('scroll', this.menu)
    }
  }
</script>
