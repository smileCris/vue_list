<template>
  <div class="wrapper">
    <div class="top"></div>
    <IndexBanner></IndexBanner>
    <Content></Content>
    <div class="block"></div>
    <Part1></Part1>
  </div>
</template>

<script>
import IndexBanner from '../components/IndexBanner'
import Content from '../components/Content'
import Part1 from '../components/Part1'

export default {
  name: 'Index',
  components: {
      IndexBanner,
      Content,
      Part1
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper{
	width: 100%;
	height: 100%;
	position: relative;
    font-weight: normal;
    background-color: #eee;
}
.top {
  width: 100%;
  height: 3.5rem;
  background-color: #282b2f;
}
.middle {
  display: inline-block;
  margin: 0 10px;
}
.block{
    clear: both;
}
.block1{
    height: 0.6rem;
}
</style>
