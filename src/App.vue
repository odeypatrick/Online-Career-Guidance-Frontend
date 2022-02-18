<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: 'Quicksand', sans-serif;
}

.btn {
  padding: 15px 20px;
  background-color: #0088aa;
  border: none;
  border-radius: 5px;
  font-weight: bold;
  color: #fff;
  cursor: pointer;
  font-size: 16px;
  font-family: inherit;
}
</style>
