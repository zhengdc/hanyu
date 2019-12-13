<template>
  <div>
   <!-- banner -->
    <div class="banner">
      <div class="banner_title animated rubberBand">
        <h1>信贷生活&nbsp;&nbsp;&nbsp;&nbsp;触手可及</h1>
        <p>解决信息不对称，打造互联网业务拓展新模式</p>
      </div>
    </div>
    <!-- 小禹app -->
    <div class="xyapp">
      <div class="xyapp_title">
        <h1>小禹APP</h1>
        <p>为金融中介从业者量身打造的移动获客平台</p>
      </div>
      <div class="xyapp_content">
        <div class="xyapp_left" :class="{'animated':animate, 'fadeInLeftBig':animate,'show':animate}">
          <div>
            <h3>订单真实可靠</h3>
            <p>优质客源实时更新 抢单过程公开透明</p>
          </div>
          <div>
            <h3>从业者的一致选择</h3>
            <p>平台入驻流程简单 随时随地轻松获客</p>
          </div>
          <div class="xyapp_btn">
            <el-button type="warning">查看详情</el-button>
            <el-button type="warning" plain>立即下载</el-button>
          </div>
        </div>
        <div class="xyapp_right" :class="{'animated':animate, 'fadeInRightBig':animate,'show':animate}">
          <img src="/img/xyapp.png" alt="小禹app">
        </div>
      </div>
    </div>
    <!-- 最新动态 -->
    <div class="newAction">
      <div class="newAction_title">
        <h1>最新动态</h1>
        <p>行业状态、公司近况、活动纪实一览</p>
      </div>
      <div class="swiper">
        <el-carousel :interval="4000" type="card" height="400px">
          <el-carousel-item v-for="(item,index) in datas" :key="index">
            <div class="swiper_item">
              <div class="swiper_img"><img :src="item.src" alt=""></div>
              <h3 class="swiper_title">{{item.title}}</h3>
              <div v-html="item.content" class="swiper_content">

              </div>
            </div>
          </el-carousel-item>
        </el-carousel>
      </div>
    </div>
    <!-- 合作伙伴 -->
    <div class="partnership">
      <h1>合作伙伴</h1>
      <div class="partnership_list">
          <a href="javascript:;"> <img src="/img/hz01.png" alt="aliyun"></a>
         <a href="javascript:;"><img src="/img/hz02.png" alt="aliyun"></a>
         <a href="javascript:;"><img src="/img/hz03.png" alt="aliyun"></a>
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
        datas: [{
            src: '/img/action01.png',
            title: '1征信不好，影响的可不仅仅只是贷款！',
            content: ' 上周，小禹闲着无事就去“中国人民银行征信中心”查了一下自己的征信，这周终于出结果了，满怀期待一看，却是空白的。'
          },
          {
            src: '/img/action02.png',
            title: '2征信不好，影响的可不仅仅只是贷款！',
            content: ' 上周，小禹闲着无事就去“中国人民银行征信中心”查了一下自己的征信，这周终于出结果了，满怀期待一看，却是空白的。'
          },
          {
            src: '/img/action03.png',
            title: '3征信不好，影响的可不仅仅只是贷款！',
            content: ' 上周，小禹闲着无事就去“中国人民银行征信中心”查了一下自己的征信，这周终于出结果了，满怀期待一看，却是空白的。'
          },
          {
            src: '/img/action04.png',
            title: '4征信不好，影响的可不仅仅只是贷款！',
            content: ' 上周，小禹闲着无事就去“中国人民银行征信中心”查了一下自己的征信，这周终于出结果了，满怀期待一看，却是空白的。'
          }
        ]
      }
    },
    methods: {
      menu() {
        this.scroll = document.documentElement.scrollTop || document.body.scrollTop;
        if (this.scroll > 120) {
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
