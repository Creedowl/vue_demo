<template>
  <div id="tab">
    <div class="item" @click="router('/')">
      <!-- <font-awesome-icon icon="home" size="2x"/> -->
      <span>Home</span>
    </div>
    <div class="item" @click="router('/about')">
      <!-- <font-awesome-icon icon="info" size="2x"/> -->
      <span>About</span>
    </div>
    <div class="item" @click="router('/foo')">
      <!-- <font-awesome-icon icon="sign-in-alt" size="2x"/> -->
      <span>Foo</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Tab',
  methods: {
    router (url){
      this.$router.push(url)
    }
  }
}
</script>

<style scoped>
#tab {
  display: flex;
  justify-content: space-around;
  align-items: center;
  bottom: 0px;
  position: fixed;
  height: 65px;
  left: 0px;
  width: 100%;
  background-color: aquamarine;
}

.item {
  padding-top: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 50px;
}
</style>

