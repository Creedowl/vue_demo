<template>
  <div id="foo">
    <p>{{ result }}</p>
    <button @click="bar()">bar</button>
  </div>
</template>

<script>
export default {
  name: 'Foo',
  data(){
    return {
      result : 'naive'
    }
  },
  methods: {
    bar(){
      /* eslint-disable */
      this.result = 'loading...'
      this.$axios.post('http://httpbin.org/post')
        .then(res => {this.result = res})
        .catch(res => {console.error(res)})
    }
  }
}
</script>

<style>

</style>
