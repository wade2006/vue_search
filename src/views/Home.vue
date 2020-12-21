<template>
  <div class="home">
    <div class="search_box">
      <div class="search_x" @mousemove="moveevent">
      <input type="text" v-on:keyup.enter="openlink(value)" v-model="value" class="search_input" placeholder="Type something to search" :style="{width:inputwidth+'px'}"/>
      <span class="iconfont iconbtn" @click="openlink(value)" >&#xe6dc;</span>
      </div>
     <div class="item">
       <ul class="search_list">
      <li v-for="(item,index) in data" :key="index"  class="search_tags" @click="openlink(item.q)">
        {{item.q}}
      </li>
    </ul>
     </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      value: "",
      inputwidth:0,
      data:[]
    };
  },
  methods:{
    moveevent(){
      this.inputwidth=400
    },
    openlink(val){
     if(val){
        window.open(`https://www.baidu.com/s?wd=${val}`)
     }
    }
  },
  watch: {
    async value(val) {
      if(val!=""){
        const data = await this.$jsonp(
        `https://www.baidu.com/sugrec?prod=pc&cb=getData&wd=${val}`,
        {
          callbackQuery: "cb",
          callbackName: "jsonp_func",
        }
      );
      this.data=data.g;
      this.inputwidth=400
      }else{
        this.data=[]
      }
    },
  },
};
</script>
<style >
   .home{
     width: 100%;
     height: 100vh;
     /* background: #2c3e50; */
     background: #16a085;
   }
   .search_box{
     position: absolute;
     left: 50%;
     top:30%;
     transform: translate(-50%,-50%);

   }
   .search_x{
     height: 30px;
     background: white;
     padding: 10px;
     display: flex;
     justify-content: space-between;
     align-items: center;
     border-radius: 30px;
   }
   .search_input{
     border: none;
     outline: none;
     transition: 0.5s;
     
   }
   .iconbtn{
     height: 26px;
     width: 26px;
     display: flex;
     justify-content: center;
     align-items: center;
     font-size: 20px;
     color: #16a085;
   }
   /* .search_x:hover .search_input{
     width: 400px;
   } */
   .item{
     position:absolute;
     width: 410px;
     margin-top: 10px;
     transition: 0.5s;
   }
   .search_list{
     width: 100%;
     border-radius: 20px;
     background: rgba(255, 255, 255, 0.4);
     overflow: hidden;
     font-size: small;
   }
   .search_tags{
     list-style: none;
     width: 100%;
     height: 35px;
     line-height: 35px;
     color: rgba(255, 255, 255, 0.8);
     /* text-indent: 15px; */
     cursor: pointer;
   }
   .search_tags:hover{
     text-indent: 10px;
     color: rgba(255, 255, 255, 1);

   }
</style>
