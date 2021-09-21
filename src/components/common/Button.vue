<template>

    <q-btn :class="isPink ? 'pink2' : 'white2'" style="background: #FF0080; color: white" ><slot></slot></q-btn>
</template>

<script>
import { reactive, toRefs } from 'vue'

export default {
  props: {
    isPink: {
      type: Boolean,
      default: false
    }
  },
  setup (props) {
    const state = reactive({
      count: 0
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>
