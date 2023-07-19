<script setup>
  import { provide } from 'vue'
  import Example from "../components/Example.vue"
  import Input from "../components/Input.vue"

  const name = ref("Ken")

  const handleEvent = (newName, e) => {
    name.value = newName
  }
  
  provide('num', 2)

</script>

<template>
  <button disabled="">Button</button>
  <p>Hello {{ name }}</p>
  <Input v-model="name" />
  <!-- <input type="text" v-model="name"> -->
  <!-- <Example v-on:myClick="handleEvent" :name="name" /> -->
  <NuxtLink to="/secoundpage">to Secoundpage</NuxtLink>
</template>