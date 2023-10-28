<template>
    <HeaderComponent />
    <TabPanelComponent />
    <CardTransactionPanel />
</template>

<script>
import TabPanelComponent from '../components/TabPanel.vue';
import HeaderComponent from '../components/HeaderComponent.vue';
import CardTransactionPanel from '../components/CardTransactionPanel.vue';

export default {
  name: 'HomePage',

  components: {
    TabPanelComponent,
    HeaderComponent,
    CardTransactionPanel
  }
}
</script>