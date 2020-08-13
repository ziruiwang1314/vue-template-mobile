<template>
  <ul class="ul">
    <li
      class="liTest"
      v-for="list in lists"
      @click="clickTest(list.name)"
      :key="list.name"
    >
      name:{{list.name}}
      sex:{{list.sex}}
      点击一下试试？
    </li>
  </ul>
</template>
<script>
export default {
  data () {
    return {
      lists: []
    }
  },
  mounted () {
    this.init()
  },
  methods: {
    init () {
      this.$api.getTest({'a': 'a'}).then(res => {
        this.lists = res.list
      })
    },
    clickTest (name) {
      alert('你点击了' + name)
    }
  }
}
</script>

<style scoped lang="scss">
  .ul{
    width: 375px;
    background-color: red;
    .liTest {
      font-size: 10px;
    }
  }
</style>
