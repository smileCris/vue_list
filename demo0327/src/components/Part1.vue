<template>  
  <div class="page-navbar">  
    <!-- navbar -->  
    <mt-navbar class="page-part" v-model="selected">  
      <mt-tab-item id="1">作品</mt-tab-item>  
      <mt-tab-item id="2">视频</mt-tab-item>  
      <mt-tab-item id="3">资料</mt-tab-item>  
    </mt-navbar>   
    <div class="block"></div>
  
    <!-- tabcontainer -->  
    <mt-tab-container v-model="selected">  
      <mt-tab-container-item id="1" class="listmain">  
        <mt-cell v-for="n in 10" :title="'内容 ' + n" :key="n" class="list" />  
      </mt-tab-container-item>  
      <mt-tab-container-item id="2" class="listmain">  
        <mt-cell v-for="n in 4" :title="'测试 ' + n" :key="n" class="list" />  
      </mt-tab-container-item>  
      <mt-tab-container-item id="3">
        <div class="listmain">
          <mt-cell v-for="data in list_1" :title="data.title" :key="data.id" class="list">
            <span slot="">{{data.desc}}</span>  
          </mt-cell>
        </div>
        <div class="block"></div>
        <div class="listmain">
          <mt-cell v-for="data in list_2" :title="data.title" :key="data.id" class="list">
            <span slot="">{{data.desc}}</span>  
          </mt-cell>
        </div>
        <div class="block"></div>
        <div class="listmain">
          <mt-cell v-for="data in list_3" :title="data.title" :key="data.id" class="list">
            <span slot="">{{data.desc}}</span>  
          </mt-cell>
        </div>
        <div class="block1">模卡</div>
        <div class="listmain">
          <img src="../assets/img/pic1.jpg" />
          <img src="../assets/img/pic2.jpg" />
          <img src="../assets/img/pic3.jpg" />
          <img src="../assets/img/pic4.jpg" />
          <img src="../assets/img/pic5.jpg" />

        </div>
      </mt-tab-container-item>  
    </mt-tab-container>  
  </div>  
</template>  

<script>
export default {
  name: 'Part1',  
  
  data() {  
    return {
			list_1: [], 
			list_2: [], 
			list_3: [],  
      selected: '3'  
    }
  },
	mounted () {
    this.axios.get('https://easy-mock.com/mock/5abcbc5d2b204e1f235690b4/TypeList/list_1',
    {
      headers:{'Access-Control-Allow-Origin': '*'}        //坑五  axios跨域问题 未解决  https://jingyan.baidu.com/article/6525d4b17a6548ac7d2e94f7.html
    })
			        .then((response) => {
			         	this.list_1 = response.data.list_1
			         	this.list_2 = response.data.list_2
			         	this.list_3 = response.data.list_3
			      })
			      .catch(function (error) {
			        console.log(error) 
			      })
	}  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.page-navbar{
  background-color: #fff;
}
.page-part{
	color: #655c5c;
}
.block{
  height: 0.6rem;
  background-color: #eee;
}
.block1{
  padding-left: 1.2rem;
  padding-right: 1.2rem;
  height: 1.2rem;
  background-color: #eee;
  font-size: 0.8em;
  color: #555;
}
.listmain{
  padding-left: 1.2rem;
  padding-right: 1.2rem;
}
span{    
  position: absolute;
  left: 30%;
  right: 14%;
}
.list{
  border-bottom: 1px solid #eee;
}
.listmain img{
  padding: 1rem 0 0 0;
  width: 32%;
  height: 100%;
}
</style>