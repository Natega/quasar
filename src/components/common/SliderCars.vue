<template>
   <div id="q-app" style="min-height: 100vh;">
  <div class="q-pa-md">

    <q-carousel
      v-model="slide"
      transition-prev="slide-right"
      transition-next="slide-left"
      swipeable
      animated
      control-color="primary"
      navigation
      padding
      arrows
      height="300px"
      class="bg-grey-1 shadow-2 rounded-borders"
    >
      <q-carousel-slide :name="1" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
        <div class='col'>
            <q-img class="rounded-borders  full-width" src="https://www.ggsauto.fr/images/generateur/gammes/6jnvm35k-ds7_crossback.jpeg_1000_800_ratio_.jpg">
            <div class="absolute-bottom text-subtitle1 text-center">
           <div class="row">
                <div class='col text-center'>DS7</div>
                <div class='col text-center'>DS7</div>
            </div>
        </div>

            </q-img>
        </div >
         <div class='col'>
            <q-img class="rounded-borders  full-width" src="https://www.ggsauto.fr/images/generateur/gammes/6jnvm35k-ds7_crossback.jpeg_1000_800_ratio_.jpg">
              <div class="absolute-bottom text-subtitle1 text-center">
              <div class="row">
                <div class='col text-center'>DS7</div>
                <div class='col text-center'>DS7</div>
            </div>
            </div>
            </q-img>
        </div >
        <div class='col'>
            <q-img class="rounded-borders  full-width" src="https://www.ggsauto.fr/images/generateur/gammes/6jnvm35k-ds7_crossback.jpeg_1000_800_ratio_.jpg"></q-img>
        </div >
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/cat.jpg"></q-img>
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/linux-avatar.png"></q-img>
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/parallax2.jpg"></q-img>
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/quasar.jpg"></q-img>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="3" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/cat.jpg"></q-img>
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/linux-avatar.png"></q-img>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="4" class="column no-wrap">
        <div class="row fit justify-start items-center q-gutter-xs q-col-gutter no-wrap">
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/material.png"></q-img>
          <q-img class="rounded-borders col-3 full-height" src="https://cdn.quasar.dev/img/donuts.png"></q-img>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
</div>
</template>

<script>
import { reactive, toRefs } from 'vue'

export default {
  setup () {
    const state = reactive({
      slide: 1
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
