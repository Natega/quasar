<template>
  <router-view />
</template>
<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  setup () {
    console.log(this)
    return { expanded: true }
  },
  name: 'App'
})
</script>
<style>

</style>
