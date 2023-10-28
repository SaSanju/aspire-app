<template>
  <q-page-container class="q-pa-sm q-ml-md">
    <div class="row q-mb-md">
      <div class="col-xs">
        <label class="text">Account Balance</label>
      </div>
    </div>
    <div class="row">
      <div class="col-xs-7">
        <div class="row">
          <span class="q-mr-xs currency">
            $$
          </span>
          <b class="text">3,000</b>
        </div>
      </div>
      <div class="col-xs-5">
        <q-btn flat @click="openDialog" text-color="blue" unelevated>
          <img src="@/assets/add.png" alt="Image" class="btn-icon-image" />
          New Card
        </q-btn>
      </div>
    </div>
  </q-page-container>
</template>

<script>
export default {
  name: "HeaderComponent",
  methods: {
    openDialog() {
      // Add logic to open the dialog here
    },
  },
}
</script>

<style>
.currency {
  width: 40px;
  height: 22px;
  background-color: #01D167;
  border-radius: 4px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: sans-serif;
  color: #FFFFFF; /* Text color */
  font-size: 12px; /* Text font size */
}
.text {
  font-family: sans-serif;
  font-size: 16px; /* Text font size */
  color: #FFFFFF;
}
.btn-icon-image {
  width: 16px; /* Adjust the width as needed */
  height: 16px; /* Adjust the height as needed */
  margin-right: 1rem;
}

</style>
