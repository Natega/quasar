<template>
  <q-page class="row items-center justify-evenly full">

    <div class="row" >
      <div class="col-5  my-center">
        <div>
        <p class='my-title'>
          A vehicle without commitment
        </p>
        <p class='my-text'>
          Maintenance and insurance included. No additional costs.
          For the duration you wish, 3 months, 1 year. Leave when you want
        </p>
         <div class="row">
           <f-button class='q-mr-md' outline rounded size="lg">Am I eligible?</f-button>
           <f-button  rounded size="lg">Find my vehicule</f-button>
         </div>
  </div>
      </div>
      <div class="col-6 offset-1">
      <iframe class="rounded" width="100%" height="400" src="https://www.youtube.com/embed/MdonjMvtjXI"
      title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

      </div>
    </div>
  </q-page>

 <div class='row'>
   <div class="col offset-1 col-10">
  <f-card class='scroll-up' toto="Coucou">
      <div>
        <div class='my-mark font-25 q-mb-lg'>How does it work?</div>
        </div>
      <div class='row'>
        <div class="col">
          <q-badge rounded outline color="grey" label="1"></q-badge>
          <br/>
          <q-icon name="token" style="color:  #FF0080; font-size: 7em;"></q-icon>
          <div class='my-mark font-18 q-mt-md'>Selet yout favorite vehicule</div>
          <div class='my-mark '>Choose from our many new and recent models</div>
        </div>
        <div class="col">
          <q-badge rounded outline color="grey" label="2"></q-badge>
           <br/>
          <q-icon name="format_size" style="color:  #FF0080; font-size: 7em;"></q-icon>
          <div class='my-mark font-18 q-mt-md'>Selet yout favorite vehicule</div>
          <div class='my-mark '>Choose from our many new and recent models</div>

        </div>
        <div class="col">
           <q-badge rounded outline color="grey" label="3"></q-badge>
          <br/>
          <q-icon name="list" style="color:  #FF0080; font-size: 7em;"></q-icon>
            <div class='my-mark font-18 q-mt-md'>Selet yout favorite vehicule</div>
          <div class='my-mark  q-mb-md'>Choose from our many new and recent models</div>
        </div>
      </div>

  </f-card>
    </div>
   </div >
    <div class='row'>
   <div class="col offset-1 col-10">
     <div class="my-mark font-25">A wide range of vehicles</div>
     </div>
      </div>
     <f-slider-cars />
</template>

<script lang="ts">
import { Todo, Meta } from 'components/models'
import FCard from 'components/common/Card.vue'
import FSliderCars from 'components/common/SliderCars.vue'
import FButton from 'components/common/Button.vue'
import { useMeta } from 'quasar'
import { defineComponent, ref } from 'vue'
export default defineComponent({
  name: 'PageIndex',
  components: { FCard, FSliderCars, FButton },
  setup () {
    useMeta({
      meta: {
        myKey: { name: 'description', content: 'My Website' }
      }
    })

    const todos = ref<Todo[]>([
      {
        id: 1,
        content: 'ct1'
      },
      {
        id: 2,
        content: 'ct2'
      },
      {
        id: 3,
        content: 'ct3'
      },
      {
        id: 4,
        content: 'ct4'
      },
      {
        id: 5,
        content: 'ct5'
      }
    ])
    const meta = ref<Meta>({
      totalCount: 1200
    })
    return { todos, meta }
  }
})
</script>
<style lang="scss" scoped>
.scroll-up{
  position:relative;
  top:-100px;
}
  .full{
        background:linear-gradient(#6D53B2,#009DE0);
        height:100vh
    }
.my-mark{
   color: #573781;
}
.font-25{
   font-size: 25px;
}
.font-18{
   font-size: 18px;
}
.my-title{
    font-weight: bold;
    font-size: 42px;
    color: white;
    line-height: 41px;
    font-family: 'Roboto';
}
.my-center {
  display: flex;
  justify-content: center;
  align-items: center;

}
.my-text{

    font-size: 18px;
    color: white;
    font-family: 'Roboto';
}
.rounded{
  border-radius: 5%;
}
</style>
