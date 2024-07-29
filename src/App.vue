<template>
  <div class="main">
    <div class="top_box">
      <!-- 通过标签名引用组件 -->
      <top-web></top-web>
    </div>
    
    <div class="left">
      <left></left>
    </div>
    <div class="right">
      <right></right>
    </div>
  </div>
  <div>
    <Demo>
      <!-- 默认插槽直接就可以使用 -->
      <button>插槽按钮</button>
      <!-- 具名插槽使用通过template 标签和 v-slot 属性 指定插槽的name 名称 -->
      <template v-slot:box2>
          <button>具名插槽2</button>
      </template>
      <!-- v-slot: 属性可以通过 # 来缩写 -->
      <template #box3>
          <button>具名插槽3</button>
      </template>
      <!-- 指定 变量名scope 接受插槽的值 -->
      <template #box4='scope1'>
          <span>插槽传进来的值：{{ scope1 }}</span>
      </template>

    </Demo>
  </div>
  
</template>

<script>
// 引入组件的文件通过变量名接受
import left from './components/LeftWeb.vue';
import right from './components/RightWeb.vue';
import top from './components/TopWeb.vue';
import Demo from './components/DemoTest.vue'
export default {
  name:'App',
  // 定义组件的标签名称（默认组件标签名与变量名相同）
  components:{
    left,
    right,
    // 前面是标签名后面是变量名
    'top-web':top,
    'Demo':Demo

  }
}


</script>

<style>
  .top_box{
      height: 70px;
      background: red;
  }
  .left{
    height: 500px;
    width: 70%;
    background: #555555;
    display: inline-block;
  }
  .right{
    height: 500px;
    width: 30%;
    background: #356;
    display: inline-block;
  }

</style>
