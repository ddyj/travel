<template>
  <div>
     <homeheader :city="city"></homeheader>
     <homeswiper :list="swiperlist"></homeswiper>
     <homeicons :list="iconlist"></homeicons>
     <homerecommend :list="recommendlist"></homerecommend>
     <homeweekend :list="weekendlsit"></homeweekend>
  </div>
</template>

<script>
import homeheader from './components/header.vue'
import homeswiper from './components/swiper.vue'
import homeicons from './components/icons.vue'
import homerecommend from './components/recommend.vue'
import homeweekend from './components/weekend.vue'
import axios from 'axios'
export default {
  name: 'home',
  components: {
    homeheader: homeheader,
    homeswiper: homeswiper,
    homeicons: homeicons,
    homerecommend: homerecommend,
    homeweekend: homeweekend
  },
  data: function () {
    return {
      city: '',
      swiperlist: [],
      iconlist: [],
      recommendlist: [],
      weekendlsit: []
    }
  },
  methods: {
    gethomeinfo: function () {
      axios.get('/api/index.json')
        .then(this.gethomeinfosucc)// .then(funcation)==>.then((data)=>{ })==>.then(函数名)里的data是指接口成功返回的数据,包含请求头,请求体,等信息
    },
    gethomeinfosucc: function (res) {
      res = res.data
      if (res.ret && res.data) {
        this.city = res.data.city// res.ret是后端输入数据，即判断为后端输入数据 A&&B前面A条件成立，B条件成立
        this.swiperlist = res.data.swiperlist
        this.iconlist = res.data.iconlist
        this.recommendlist = res.data.recommendlist
        this.weekendlsit = res.data.weekendlist
      }
    }
  },
  mounted: function () {
    this.gethomeinfo()
  }

}
</script>

<style></style>
