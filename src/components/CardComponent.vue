<template>
    <q-card class="green-card">
        <q-card-section>
            <div class="row">
                <div class="col">
                </div>
                <div class="col-auto">
                    <img src="@/assets/CardLogo.png" alt="Image" />
                </div>
            </div>
        </q-card-section>
        <q-card-section class="custom-card-section">
            <q-card-title class="text-white">Mark Henry</q-card-title>
            <p class="text-white q-mt-md">1234  3456  1234  1234</p>
            <div class="row">
                <div class="col-6">
                    <p class="text-white">Thru: 05/24</p>
                </div>
                <div class="col-6">
                    <p class="text-white">CVV: ***</p>
                </div>
            </div>
        </q-card-section>
        <q-card-section class="custom-card-section">
            <div class="row">
                <div class="col">
                </div>
                <div class="col-auto">
                    <img src="@/assets/VisaLogo.png" alt="Image" />
                </div>
            </div>
        </q-card-section>
    </q-card>
</template>
  
<script>
export default {
    // Component options
};
</script>
  
<style scoped>
.green-card {
    background-color: #4caf50;
    height: 220px;
    width: 100%;
    .custom-card-section::v-deep {
      padding-top: 0px; /* Custom padding */
      padding-bottom: 0px;
    }
}

.text-white {
    color: #fff;
    /* White text color */
}
</style>
  