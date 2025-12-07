<template>
  <div class="main">
    <ul class="todolist">
      <li v-for="item in list" :key="item.id" :class="{completed:item.done}">
        <div class="view">
          <input type="checkbox" class="toggle" v-model="item.done">
          <label>{{item.name}}</label>
          <button class="destory">删除</button>
        </div>
      </li>
    </ul>
  </div>
</template>
<script setup lang="js">
    defineProps(['list'])
</script>
<style>

</style>
