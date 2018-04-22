<template>
  <div class="main">
    <div class="browse">
      <img src="../assets/img/eye.png" v-on="Read(num)"><span id="span1">{{num.label}}</span>
      <img src=" " :onerror="look"  v-on:click="Click(num2)" id="img2"><span id="span2">{{num2.label}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content',
  data: function(){
    return{
      num: {label: '223'},
      num2: {label: '1123'},
      changeImg: true,
      look: 'this.src="' + require('../assets/img/heart.png') + '"'  ,
    //  bgImg: [require('../assets/img/heart.png'),require('../assets/img/heart1.png')],
    //  imgIndex: 0
    }
  },
 /* computed: {
    imgSrc() {
      return bgImg[this.imgIndex]
    }
  },*/
  methods: {
    Read: function(num){
      
    },
    Click: function(num2){
   //   changeImg=1;
   //   if(changeImg!=changeImg){
   //     num2.label--;
    //    changeImg!=changeImg;
    //  }else{
        num2.label++;
    //    changeImg!=changeImg;
    //  }
     // this.imgIndex = (this.imgIndex+1)%(this.bgImg).length
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
	width: 100%;
  height: 100%;
	position: relative;
  background-color: #fff;
}
.browse {
  width: 100%;
  height: 2.7rem;
}
.browse img,#span1,#span2{
    width: 1.2rem;
    margin: 1rem 22% 0.5rem 20%;
    position: absolute;
    float: left;
}
#img2{
  position: absolute;
  left: 40%;
}
#span1,#span2{
  color: #655858;
}
#span1{
  left: 8%;
}
#span2{
  left: 48%;
}
</style>
