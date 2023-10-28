<template>
  <div class="q-pa-md">
    <div class="q-gutter-y-md" style="max-width: 600px">
      <q-card>
        <q-tabs v-model="tab" dense class="text-white shadow-1" :breakpoint="0" align="left" indicator-color="blue"
          narrow-indicator>
          <q-tab name="My Debit Cards" label="My Debit Cards" />
          <q-tab name="All Company Cards" label="All Company Cards" />
        </q-tabs>

        <q-tab-panels v-model="tab" animated>
          <q-tab-panel name="My Debit Cards" class="q-pa-0">
            <CarouselComponent />
          </q-tab-panel>

          <q-tab-panel name="All Company Cards">
            <div class="text-h6">All Company Cards</div>
            Lorem ipsum dolor sit amet consectetur adipisicing elit.
          </q-tab-panel>
        </q-tab-panels>
      </q-card>
    </div>
  </div>
</template>
  
<script>
import { ref } from 'vue'
import CarouselComponent from './CarouselComponent.vue';

export default {
  components: {
    CarouselComponent
  },
  setup() {
    return {
      tab: ref('My Debit Cards')
    }
  }
}
</script>

<style>
.q-tabs {
  background-color: #0C365A;
  opacity: 100%;

  .q-tab__label {
    color: #FFFFFF;
    font-family: sans-serif;
    font-size: 11px;
    opacity: 100%;
  }
}

.q-panel {
  background-color: #0C365A;
  opacity: 100%;
}
</style>