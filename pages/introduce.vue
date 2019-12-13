<template>
  <div>
    <div class="introduce">
      <div><img src="/img/logo_big.png" alt="">翰禹</div>
    </div>
    <div class="companya">
      <div class="item_title">
        <img src="/img/company.png" alt=""><br>
        <span>公司介绍</span>
      </div>
      <div class="companya_cont">
        <div>
          <img src="/img/companybg.png" alt="" :class="{'animated':animate, 'fadeInLeftBig':animate,'show':animate}">
        </div>
        <div class="companya_cont_des" :class="{'animated':animate, 'fadeInRightBig':animate,'show':animate}">
          <p>翰禹作为一家现代化创新型企业，公司建立了全面、系统的咨 询与服务平台。</p>
          <p>公司通过高效，高素质的个性化专业服务，提供了集信息交流 和服务客户一体的一站式服务平台。</p>
          <p>公司立足于解决中小企业销售人员的社交问题，更大化地共享 信息，增进自身价值，增长收入，实现共赢发展的目标。
          </p>
        </div>
      </div>
    </div>
    <div class="companyb">
      <div class="item_title">
        <img src="/img/vision.png" alt=""><br>
        <span>公司背景</span>
      </div>
      <div class="companyb_cont">
        <div style="text-align: right;">
          <img src="/img/visionbg.png" alt="" :class="{'animated':animate1, 'fadeInRightBig':animate1,'show':animate1}">
        </div>
        <div class="companyb_cont_des" :class="{'animated':animate1, 'fadeInLeftBig':animate1,'show':animate1}">
          <p>翰禹以推动行业发展为己任，积极进行业务探索与实践。公司 坚持以人为本，求实诚信，创新发展，高效务实的经营理念。</p>
          <p>实行可持续发展战略，努力引领同行业的潮流，成为竞争者追 逐的标杆。</p>
          <p>公司以建立科学、高效的现代企业为目标，依靠高素质人才的 聚集，研究和创新，打造属于自己的品牌。“授人以鱼不如授人以渔“，携手翰禹，成就梦想。
          </p>
        </div>
      </div>
    </div>
    <div class="companyc">
      <div class="item_title">
        <img src="/img/address.png" alt=""><br>
        <span>公司地址</span>
      </div>
      <div>
        <baidu-map class="bm-view map" ak="HdGvGREtX30hhmhxWGGZ1wnbhplnM7er" :center="{lng: 120.262778, lat: 30.236726}" :zoom="17">
          </baidu-map>
      </div>
    </div>
  </div>
</template>
<script>
import BaiduMap from 'vue-baidu-map/components/map/Map.vue'
export default {
  data() {
      return {
        scroll: 0,
        animate: false,
        animate1:false
      }
    },
    components: {
      BaiduMap
    },
    methods: {
      menu() {
        this.scroll = document.documentElement.scrollTop || document.body.scrollTop;
        if (this.scroll > 100 && this.scroll<720) {
          this.animate = true
        }
        if(this.scroll > 720){
          this.animate1 = true;

        }
      }
    },
    mounted() {
      this.menu()
      window.addEventListener('scroll', this.menu)
    }
  }
</script>
