<template>
  <div class="compose">
    <ul class="example-list">
      <li
        @click="goPage('/compose/pullup-pulldown')"
        class="example-item"
      >
        <span>pullup-pulldown</span>
      </li>
      <li
        @click="goPage('/compose/pullup-pulldown-slide')"
        class="example-item"
      >
        <span>pullup-pulldown-slide</span>
      </li>
      <li
        @click="goPage('/compose/pullup-pulldown-outnested')"
        class="example-item"
      >
        <span>pullup-pulldown-outnested</span>
      </li>
      <li
        @click="goPage('/compose/slide-nested')"
        class="example-item"
      >
        <span>slide-nested</span>
      </li>
      
    </ul>
    <transition name="move">
      <router-view class="view"></router-view>
    </transition>
  </div>
</template>
<script>
export default {
  methods: {
    goPage(path) {
      this.$router.push(path)
    }
  }
}
</script>
<style lang="stylus">
.free-scroll-container
  &.view
    position fixed !important
</style>
