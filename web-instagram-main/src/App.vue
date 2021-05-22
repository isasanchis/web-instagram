<template>
  <div id="app">

      <Header />
      <Feed />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Feed from './components/Feed.vue'

export default {
  components: { Header, Feed }
}
</script>

<style lang="scss">

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    text-decoration: none;
    font-family: 'Segoe UI';
    font-size: 14px;
}
body {
  background-color: #fafafa;
  width: 100%;
  margin: 0;
  padding: 0;
}

</style>
