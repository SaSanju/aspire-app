<template>
    <q-card class="green-card shadow-0 border-0">
        <q-card-section class="header-section">
            <q-btn-group class="grp-btn-layout" spread>
                <q-btn round>
                    <q-avatar size="32px">
                        <img src="@/assets/FreezeCard.png">
                    </q-avatar>
                    <span class="btn-text">Freez card</span>
                </q-btn>
                <q-btn round>
                    <q-avatar size="32px">
                        <img src="@/assets/SetSpendLimit.png">
                    </q-avatar>
                    <span class="btn-text">Freez card</span>
                </q-btn>
                <q-btn round>
                    <q-avatar size="32px">
                        <img src="@/assets/GPay.png">
                    </q-avatar>
                    <span class="btn-text">Freez card</span>
                </q-btn>
                <q-btn round>
                    <q-avatar size="32px">
                        <img src="@/assets/ReplaceCard.png">
                    </q-avatar>
                    <span class="btn-text">Freez card</span>
                </q-btn>
                <q-btn round>
                    <q-avatar size="32px">
                        <img src="@/assets/DeactivateCard.png">
                    </q-avatar>
                    <span class="btn-text">Freez card</span>
                </q-btn>
            </q-btn-group>
        </q-card-section>
        <q-card-section class="custom-card-section">
            <q-card-title class="text-white">Mark Henry</q-card-title>
            <p class="text-white q-mt-md">1234 3456 1234 1234</p>
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
    <q-separator color="black" inset />
</template>
  
<script>
export default {
    // Component options
};
</script>
  
<style scoped>
.header-section {
    background-color: #EDF3FF;
}
.btn-text {
    color: #0C365A;
    font-size: 12px;
    font-family: sans-serif;
    font-style: normal;
}
.grp-btn-layout {
    box-shadow: none;
    /* Remove the shadow */
}
</style>
  