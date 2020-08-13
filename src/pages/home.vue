<template>
  <div class="fillContent">
    <div class="flex ">
      <div class="main">
        <router-view></router-view>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  name: 'home',
  data () {
    return {}
  }
}
</script>

<style scoped>
  .main {
    height: 100%;
    overflow: hidden;
    flex: 1;
  }
</style>
