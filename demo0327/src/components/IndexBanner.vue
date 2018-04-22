<template>
  <div class="banner">
			<div class="avatar">
				<img src="../assets/img/tx.jpg"/>
        <span class="intro1">Audrey Hepburn</span>
        <span class="intro2">Actor</span>
			</div>
  </div>
</template>

<script>
export default {
  name: 'IndexBanner'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.banner{
    width: 100%;
    height: 15rem;
    background-image: url("../assets/img/fm.jpg");
    background-size: 100% 100%;  
    -moz-background-size: 100% 100%;  
    -webkit-background-size: 100% 100%;  
    position: relative;
}
.avatar img {
  width: 5rem;
  height: 5rem;
  top: 60%;
  left: 5%;
	border-radius: 50%;
  margin-bottom: .4rem;
  position: absolute;
}
.intro1,.intro2{
  color: #fff;
  font-family: '幼圆';
  font-weight: 600;
}
.intro1{
  position: absolute;
  font-size: 1.2em;
  top: 69%;
  left: 32%;
}
.intro2{
  font-size: 1em;
  position: absolute;
  top: 79%;
  left: 33%;
}
</style>
