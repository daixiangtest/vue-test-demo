<template>
    <h3>插槽的使用</h3>
    <!-- slot 实现插槽功能 可以用来接受父组件传入标签对中内容 -->
    <slot></slot>
    <!-- 默认插槽没有指定名称默认使用 -->
    <div class="box">box1
        <slot></slot>
    </div>
    <!-- 具名插槽 通过名称指定插槽 -->
    <div class="box">box2
        <slot name="box2"></slot>
    </div>
    <div class="box">box3
        <slot name="box3"></slot>
    </div>
    <div class="box">box4
        <slot name="box4" text="测试数据"></slot>
    </div>

 </template>
   
 <script>
 
 </script>
   
   
 <style scoped>
 .box{
    width: 200px;
    height: 200px;
    box-shadow: 0 0 5px #000;
    float: left;
 }
   
 </style>