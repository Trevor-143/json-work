<template>
  <div>
    <h1>Human Actions</h1>
    <div v-for="(item, index) in data" :key="index" class="action">
      <img :src="item.image" :alt="item.name">
      <h3> by: {{item.by}} </h3>
      <h3> {{item.name}} </h3>
      <p> {{item.content}} </p>
    </div>
  </div>
</template>


<script>
import { ref } from "vue";
import Data from "./data/info.json"

export default {
  setup() {
    
    const data = ref([])

    data.value = Data

    return {
      data
    }
  }
}
</script>
<style>

.action {
  padding: 2rem;
  background: #eee;
  margin: 2rem 10%;
  border-radius: 3rem;
}
.action img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 50%;
}

</style>