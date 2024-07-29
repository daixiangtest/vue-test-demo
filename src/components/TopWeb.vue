<template>
   <span>顶部{{ count }}</span>
   <button @click.self="add">顶部按钮</button>
</template>
  
<script>
  export default {
    //数据
    data(){
      return{
        count:0

      }

    },
    // 定义的函数方法
    methods:{
      add(){
        this.count++
      }

    },
    // 计算属性
    computed:{

    },
    // 侦听数据
    watch:{

    },
    // 组件注册
    components:{

    }

    
  }
</script>
  
  <!-- scopef 属性声明该样式只对当前组件生效不会影响其他样式 -->
<style scoped>
button{
  background: red;
}
  
</style>
  