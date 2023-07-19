<script setup>
  const newName = ref("")

  const emit = defineEmits(["myClick"])

  const changeName = (e) => {
    emit("myClick", newName.value, e)
  }

</script>

<template>
  <div>
    <input type="text" v-model="newName" @input="changeName">
  </div>
</template>