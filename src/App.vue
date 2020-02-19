<template>
  <div id="app">
    <!--router view display the content of current router address  -->
    <keep-alive exclude="Detail">
    <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
