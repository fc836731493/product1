<template>
  <div class="index-wrap">
     <div class="index-left">
         <div class="index-left-block">
            <h2>全部产品</h2>
            <div :="(product,index) in productList">
               <h3>{{ product.category }}</h3>
               <ul>
                   <li :="item in product.list">
                       <a :href="item.url">{{ item.name }}</a>
                   </li>
               </ul>
             <div v-if="index%2 == 0" class="hr"></div>
            </div>           
         </div>
     </div>
     <div class="index-right">

     </div>
  </div>
</template>

<script>
export default {
   name:"layout",
   data(){
       return{
          productList:[
              {
                  category:"手机应用类",
                  list:[
                      {
                          name:"91助手",
                          url:"http://zs.91.com/"
                      },
                      {
                          name:"豌豆荚",
                          url:"https://www.wandoujia.com/"
                      },
                      {
                          name:"金山毒霸",
                          url:"http://www.ijinshan.com/"
                      }
                  ]
              },
              {
                  category:"开发工具",
                  list:[
                      {
                          name:"webstorm",
                          url:"http://zs.91.com/"
                      },
                      {
                          name:"sublime",
                          url:"https://www.wandoujia.com/"
                      },
                      {
                          name:"hbuild",
                          url:"http://www.ijinshan.com/"
                      },
                      {
                          name:"atom",
                          url:"http://www.ijinshan.com/"
                      }
                  ]
              }
          ]
       }
   }
}
</script>

<style scoped>
.index-wrap {
    width: 1200px;
    margin: 0 auto;
    overflow: hidden;
}
.index-left {
    float: left;
    width: 300px;
    text-align: left;
}
.index-right {
    float: left;
    width: 900px;
}
.index-left-block {
    margin: 15px;
    background: #fff;
    box-shadow:0 0 1px #ddd;
    height: 350px;
}
.index-left-block .hr {
    margin-bottom: 20px;
    height: 1px;
    width: 100%;
    background: #ddd;
}
.index-left-block h2 {
    background: #4fc08d;
    color:#fff;
    padding: 10px 15px;
    margin-bottom: 20px;
}
.index-left-block h3 {
    padding: 0 15px 5px 15px;
    font-weight: bold;
    color: #222;
}
.index-left-block ul {
    padding: 10px 15px;
}
.index-left-block li {
    padding: 5px;
}
.index-board-list {
    overflow: hidden;
}
.index-board-item {
    float: left;
    width: 400px;
    background: #fff;
    box-shadow: 0 0 1px #ddd;
    padding: 20px;
    margin-right: 20px;
    margin-bottom: 20px;
}
.index-board-item-inner {
    min-height: 125px;
    padding-left: 120px;
}
.index-board-car .index-board-item-inner {
    background: url(../assets/images/1.png) no-repeat;
}
.index-board-loud .index-board-item-inner {
    background: url(../assets/images/2.png) no-repeat;
}
.index-board-earth .index-board-item-inner {
    background: url(../assets/images/3.png) no-repeat;    
}
.index-board-hill .index-board-item-inner {
    background: url(../assets/images/4.png) no-repeat;    
}
.index-board-item h2 {
    font-size: 18px;
    font-weight: bold;
    color: #000;
    margin-bottom: 15px;
}
.line-last {
    margin-right: 0;
}
.index-board-button {
    margin-top: 20px;
}
.lastest-news {
    min-height: 350px;
}
.hot-tag {
    background: red;
    color: #fff;
}
.new-item {
    display: inline-block;
    width: 230px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
</style>