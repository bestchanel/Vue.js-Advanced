<template>
  <main>
    <button @click="counter++">Counter Up</button>
    <h3>{{ counter }}</h3>
    <button @click="counter--">Counter Down</button>
    <h3>{{ person.name }} {{ person.age }}</h3>
    <button @click="updateperson">Update Person</button>
    <h3>{{ brand }}</h3>
  </main>
</template>

<script setup lang="ts">

import { onMounted, reactive, ref } from "vue";
const counter = ref(0)

const person = reactive({ name: 'Woraprat', age: 22 })

const updateperson = () => {
  person.name = 'Best',
    person.age = 22
}

onMounted(()=>{
  setTimeout(() => {
    person.name = 'Best'
  }, 2000);
})


</script>

<script lang="ts">
export default {
  data() {
    return {
      brand: "Pook"
    }
  },
}

</script>

<style scoped></style>