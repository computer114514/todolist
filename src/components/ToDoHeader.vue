<template>
  <div>
    <div class="header">
      <h1 class="header-head">TODO</h1>
      <input type="text" class="header-input" placeholder="做点什么" v-model.trim="name" @keyup.enter="enterName">
    </div>
  </div>
</template>

<script setup lang="js">
  import {ref} from "vue"
  const name=ref("")
  function enterName(){
    emit('add-to-do',name.value)
    name.value=""
  }
  const emit=defineEmits(['add-to-do'])
</script>

<style>

</style>
