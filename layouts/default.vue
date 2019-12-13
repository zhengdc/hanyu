<template>
  <div>
    <!-- 头部 -->
    <header :class="{'headers':changed}">
      <div class="head_logo"><img src="/img/logo.png" alt="">翰禹</div>
      <nav>
        <ul>
          <li v-for="(cate,index) in categorys" :key="index">
            <nuxt-link :to="cate.path" :class="{'active':category==index}">{{cate.name}}</nuxt-link>
          </li>
        </ul>
      </nav>
    </header>
    <!-- 内容 -->
    <nuxt />
    <footer>
      <span>杭州翰禹信息技术有限公司</span>
    </footer>
    <!-- 返回顶部 -->
    <el-backtop></el-backtop>
  </div>
</template>
<script>
  export default {
    head() {
      return {
        title: '杭州翰禹信息技术有限公司',
        link: [{
          rel: 'stylesheet',
          href: '/css/main.css'
        }]
      }
    },
    data() {
      return {
        scroll: 0,
        change: false,
        categorys:[
          {name:'首页',path:'/'},{name:'小禹APP',path:'/product'},{name:'公司介绍',path:'/introduce'},{name:'加入我们',path:'/join'}
        ]
      }
    },
    methods: {
      menu() {
        this.scroll = document.documentElement.scrollTop || document.body.scrollTop;
      }
    },
    computed: {
      changed() {
        if (this.scroll > 80) {
          return true
        }
      },
      category() {
        if (this.$route.path == '/product') {

        }
        switch (this.$route.path) {
          case '/':
            return 0;
            break;
          case '/product':
            return 1;
            break;
          case '/introduce':
            return 2;
            break;
          case '/join':
            return 3;
            break;

        }
      }
    },
    mounted() {
      console.log(this.category)
      window.addEventListener('scroll', this.menu)
    }
  }
</script>
