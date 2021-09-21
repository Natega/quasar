<template>

      <q-card class="my-card" flat bordered>

      <q-card-section>
          <slot>

          </slot>
      </q-card-section>

    </q-card>

</template>

<script>
import { reactive, toRefs } from 'vue'

export default {
  props: {
    toto: {
      type: String,
      default: 'hello'
    }
  },
  setup (props) {
    const state = reactive({
      expanded: true
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
