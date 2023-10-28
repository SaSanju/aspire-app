<template>
  <q-btn-group class="q-pa-md q-shadow-top-1" spread>
    <q-btn class="text-center">
      <q-img
        size="24px"
        src="@/assets/Logo.png"
        class="button-image"
      />
      <div class="button-text">Home</div>
    </q-btn>
    <q-btn class="text-center">
      <q-img
        size="24px"
        src="@/assets/pay.png"
        class="button-image"
      />
      <div class="button-text">Cards</div>
    </q-btn>
    <q-btn class="text-center">
      <q-img
        size="24px"
        src="@/assets/Payments.png"
        class="button-image"
      />
      <div class="button-text">Payments</div>
    </q-btn>
    <q-btn class="text-center">
      <q-img
        size="24px"
        src="@/assets/Credit.png"
        class="button-image"
      />
      <div class="button-text">Credit</div>
    </q-btn>
    <q-btn class="text-center">
      <q-img
        size="24px"
        src="@/assets/Account.png"
        class="button-image"
      />
      <div class="button-text">Profile</div>
    </q-btn>
  </q-btn-group>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style scoped>
.text-center {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.button-image {
  width: 24px; /* Adjust image width as needed */
  height: 24px; /* Adjust image height as needed */
}

.button-text {
  color: #0C365A;
    font-size: 9px;
    font-family: sans-serif;
    font-style: normal;
    margin-top: 5px;
}

</style>