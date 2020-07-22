<template>
  <div>
    <div id="app">

      <div id="catalog">
        <div class="text"><img src="../../assets/logo.png" alt="">
          <transition name="bounce">
            <div v-if="show" class="tag">首页</div>
          </transition>
        </div>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">产品类型</div>
        </div>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">产品简介</div>
        </div>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">产品功能</div>
        </div>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">产品销售</div>
        </div>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">联系电话</div>
        </div>
        <div class="text" @click="screen"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">登录></div>
        </div>
        <transition name="slide-fade">
          <div v-if="display">
            <div class="textNew">
              <div>电话</div>
            </div>
            <div class="textNew">
              <div>姓名</div>
            </div>
            <div class="textNew">
              <div>地址</div>
            </div>
          </div>
        </transition>
        <div class="text"><img src="../../assets/logo.png" alt="">
          <div v-if="show" class="tag">你好</div>
        </div>
      </div>

      <div id="body">
        <button @click="exhibit">123</button>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        display: false,
        show: true
      }
    },
    methods: {
      screen () {
        this.display = !this.display
      },
      exhibit () {
        this.show = !this.show
      }
    }
  }
</script>
<style>
  @import url(catalog.css);
</style>
