<script setup>
  import {ref} from "vue";
  const list=ref([
    {id:1,name:"书法",done:false},{id:2,name:"画画",done:true}
  ])
  import ToDoFooter from "@/components/ToDoFooter.vue"
  import ToDoHeader from "@/components/ToDoHeader.vue"
  import ToDoMain from "@/components/ToDoMain.vue"
  const addToDo=(name)=>{
    list.value.push({id:Math.random()*1000,name,done:false})
  }
</script>

<template>
<ToDoHeader @add-to-do="addToDo"></ToDoHeader>
<ToDoMain :list="list" ></ToDoMain>
<ToDoFooter></ToDoFooter>
</template>

<style scoped></style>
