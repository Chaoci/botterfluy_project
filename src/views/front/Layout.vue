<template>
  <div>
    <div class="loader-icon">
      <vue-loaders v-if="isLoading" name="ball-scale-multiple" color="#FBB5B5" scale="2.5"></vue-loaders>
    </div>
    <div v-if="iscomplate">
      <div class="topOutline"></div>
      <div class="rightOutline"></div>
      <div class="bottomOutline"></div>
      <div class="leftOutline"></div>
      <div class="leftText d-flex phone-none" data-aos="fade-right" data-aos-duration="1500">
        <div class="line"></div>
        <p>Copyright ©2022 馨援結醫. All rights reserved.</p>
      </div>
      <Header></Header>
      <router-view></router-view>
      <Footer></Footer>
    </div>
  </div>
</template>

<script>
// 載入 Header 跟 Footer 元件
import Header from '../../components/Header.vue'
import Footer from '../../components/Footer.vue'

// 載入 vue-loaders
import 'vue-loaders/dist/vue-loaders.css'

export default {
  data () {
    return {
      isLoading: false,
      iscomplate: true
    }
  },
  components: {
    Header,
    Footer
  },
  created () {
    // const vm = this
    // vm.isLoading = true
    // setTimeout(() => {
    //   vm.isLoading = false
    //   vm.iscomplate = true
    // }, 2000)
  }
}
</script>
