<template>
    <h1>{{ name }}</h1>
    <table border="1">
        <tr>
<!--            展示表格的行头-->
            <th>学号</th>
            <th>姓名</th>
            <th>年龄</th>
            <th>性别</th>
            <th>成绩</th>
        </tr>
<!--        展示表格的行数据 通过循环遍历这些数据依次展示-->
        <tr v-for="(st,index) in stu" :key="index">
            <td>{{ st.id }}</td>
            <td>{{ st.name }}</td>
            <td>{{ st.age }}</td>
            <td>{{ st.sex }}</td>
<!--            判断成绩是否及格来展示不同颜色的字体-->
            <td v-if="st.score=='不及格'" style="color: red">{{ st.score }}</td>
            <td v-else-if="st.score=='及格'" style="color: #00ff33">{{ st.score }}</td>
            <td v-else style="color: #6a00ff">{{ st.score }}</td>
            
        </tr>

    </table>
 </template>
   
 <script>
   export default {
     data(){
        return{
            
        }
     },
     // 用来引入父类数据 ‘stu’ 为变量名引用时通过组件标签中的属性名来应用
     props:['stu','name']
   }
 </script>
   
   
 <style scoped>
   
 </style>