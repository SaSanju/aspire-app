<template>
  <q-dialog v-model="dialogVisible" full-height>
    <q-layout>
      <q-header class="bg-primary">
        <q-toolbar>
          <q-toolbar-title>Add New Card</q-toolbar-title>
        </q-toolbar>
      </q-header>
      <q-page-container>
        <q-card class="column full-height">
          <q-card-section>
            <q-input v-model="cardHolderName" label="Card Holder Name" />
          </q-card-section>
          <q-card-section>
            <q-input v-model="cardNumber" label="Card Number" type="number" />
          </q-card-section>
          <q-card-section>
            <q-input filled v-model="proxyDate" mask="MM/YYYY">
              <template v-slot:append>
                <q-btn icon="event" round color="primary" mask="MM/YYYY">
                  <q-popup-proxy @before-show="updateProxy" cover transition-show="scale" transition-hide="scale">
                    <q-date v-model="cardexpireDate">
                      <div class="row items-center justify-end q-gutter-sm">
                        <q-btn label="Cancel" color="primary" flat v-close-popup />
                        <q-btn label="OK" color="primary" flat @click="save" v-close-popup />
                      </div>
                    </q-date>
                  </q-popup-proxy>
                </q-btn>
              </template>
            </q-input>
          </q-card-section>
          <q-card-section>
            <q-input v-model="cvvNumber" label="CVV Number" type="number" />
          </q-card-section>
          <q-card-actions align="right">
            <q-btn label="Cancel" color="secondary" @click="closeDialog" />
            <q-btn label="Save" color="primary" @click="saveToLocalStorage" />
          </q-card-actions>
        </q-card>
      </q-page-container>
    </q-layout>
  </q-dialog>
</template>
  
<script>
import LocalStorageService from '../services/LocalStorageService';
import { ref } from 'vue';
export default {
  data() {
    return {
      dialogVisible: false,
      cardHolderName: '',
      cardNumber: null,
      cvvNumber: null,
    };
  },
  setup() {
    const cardexpireDate = ref('2019/03/01')
    const proxyDate = ref('2019/03/01')

    return {
      cardexpireDate,
      proxyDate,

      updateProxy() {
        proxyDate.value = cardexpireDate.value
      },

      save() {
        cardexpireDate.value = proxyDate.value
      }
    }
  },
  methods: {
    openDialog() {
      this.dialogVisible = true; // Open the dialog
    },
    closeDialog() {
      this.dialogVisible = false; // Close the dialog
    },
    saveToLocalStorage() {
      if (this.cardHolderName && this.cardNumber !== null) {
        this.cardNumber = parseFloat(this.cardNumber);
        LocalStorageService.saveData(this.cardHolderName, this.cardNumber);
        this.dialogVisible = false;
      }
    },
  },
};
</script>
  