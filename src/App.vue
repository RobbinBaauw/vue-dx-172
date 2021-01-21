<template>
  <input type="number" v-model="myNumber" />
  <input type="checkbox" v-model="myCheckbox" />
</template>

<script lang="ts">
import { ref, watchEffect, defineComponent } from 'vue'

export default defineComponent({
  name: 'App',
  setup: () => {
    const myNumber = ref(0);
    watchEffect(() => console.log(myNumber.value));

    const myCheckbox = ref(false);
    watchEffect(() => console.log(myCheckbox.value));

    return { myNumber, myCheckbox }
  }
})
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
