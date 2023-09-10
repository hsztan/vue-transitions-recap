<template>
  <button type="button" @click="flag = !flag">Toggle</button>

  <transition name="fade">
    <h2 v-if="flag">Hello World!</h2>
  </transition>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      flag: false
    }
  }
}
</script>

<style lang="scss" scoped>
.fade-enter-from {
  opacity: 0;
}

.fade-enter-active {
  transition: all 0.50s linear;
}

.fade-leave-to {
  transition: all 0.50s linear;
  opacity: 0;
}
</style>