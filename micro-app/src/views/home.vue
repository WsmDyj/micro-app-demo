<template>
  <div class="micro-main">
    <img alt="Vue logo" :src="logoPath" />
    <HelloWorld msg="子应用 -- Vite+Vue@3.x" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from '../components/HelloWorld.vue'
const logoPath = new URL('../assets/logo.png', import.meta.url).href

export default defineComponent({
  name: 'Home',
  setup () {
    return { logoPath }
  },
  components: {
    HelloWorld
  }
})
</script>

<style>
.micro-main {
  background: red;
}
</style>
