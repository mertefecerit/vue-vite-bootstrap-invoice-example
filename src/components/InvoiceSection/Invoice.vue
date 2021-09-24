<template>
  <div class="row justify-content-center">
    <div class="col-lg-8">
      <div class="p-2 rounded mt-3 bg-warning shadow">
        <Contact :contact="state.contact"/>
        <Items :items="state.items" :addNewItem="addNewItem"/>
        <Summary :items="state.items"/>
        <hr>
        <div class="d-flex justify-content-end">
          <button @click="onSave" class="btn btn-sm btn-danger fw-bold"><i class="fas fa-save"></i> Kaydet</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Items from './Items.vue'
import Summary from './Summary.vue'
import Contact from "./Contact.vue";
import {provide, reactive} from "vue";
const props = defineProps({saveInvoice:Function})
const state = reactive({
  contact:{
    name: null,
    email: null,
    town: null,
    country: null,
    zipcode:null,
  },
  items:[]
});
    const addNewItem = () => {
      state.items.push({
        id: new Date().getTime(),
        name: null,
        qty: 0,
        unitPrice: 0,
        totalPrice: 0
      })
    }

    const deleteItem = (item) => {
      console.log(item)
      state.items.splice((state.items).indexOf(item),1)
    }

    provide("deleteItem",deleteItem)
    const onSave = () => {
      props.saveInvoice({ ...state, created_at: new Date(), id: new Date().getTime()})
    }
</script>

<style scoped>

</style>