<template>
    <HeaderComponent />
    <TabPanelComponent />
</template>

<script>
import TabPanelComponent from '../components/TabPanel.vue';
import HeaderComponent from '../components/HeaderComponent.vue';

export default {
  name: 'HomePage',

  components: {
    TabPanelComponent,
    HeaderComponent
  }
}
</script>