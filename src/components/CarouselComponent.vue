<template>
    <q-carousel v-model="slide" navigation swipeable transition-prev="slide-right" transition-next="slide-left" height="300px" animated control-color="primary"
        class="rounded-borders">
        <q-carousel-slide name="style" class="q-pa-0">
            <CardComponent />
        </q-carousel-slide>
        <q-carousel-slide name="tv" class="q-pa-0">
            <CardComponent />
        </q-carousel-slide>
        <q-carousel-slide name="layers" class="q-pa-0">
            <CardComponent />
        </q-carousel-slide>
    </q-carousel>
</template>
  
<script>
import { ref } from 'vue'
import CardComponent from "./CardComponent.vue";

export default {
    components: {
        CardComponent
    },
    setup() {
        return {
            slide: ref('style'),
            lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo provident incidunt ducimus iusto perferendis porro earum. Totam, numquam?'
        }
    }
}
</script>