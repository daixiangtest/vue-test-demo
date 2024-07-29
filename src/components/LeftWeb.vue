<template>
   <span>左侧</span>
   <button>左侧按钮</button>
   <h3>5555</h3>
   <!-- 通过props的声明的stu 变量名来接收数据 -->
   <MyTable :stu="stu" name="学生表"></MyTable>
</template>
  
<script>
import MyTable from './MyTable.vue';
  export default {
    components:{
      MyTable
    },
    data(){
      return{
        stu: [{id: "01", name: "张三", "age": 18, "sex": "男", "score": "及格"},
                    {id: "02", name: "李四", "age": 19, "sex": "女", "score": "不及格"},
                    {id: "03", name: "王五", "age": 19, "sex": "男", "score": "及格"},
                    {id: "04", name: "刘二", "age": 20, "sex": "女", "score": "不及格"},
                    {id: "05", name: "马六", "age": 21, "sex": "男", "score": "及格"}]
      }
    }
  }
</script>
  
  
<style scoped>
  
</style>