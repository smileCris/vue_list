<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  overflow: hidden;
  font-size: 0.9em;
}
* {
	margin: 0;
	padding: 0;
}
ul,li{
	list-style: none;
}
a{
	text-decoration: none;
}
</style>
