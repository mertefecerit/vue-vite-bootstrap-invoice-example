<script setup>
import Sidebar from "./components/Sidebar.vue";
import Invoice from "./components/InvoiceSection/Invoice.vue";
import {ref} from "vue";
const invoiceList = ref([])
const saveInvoice = (invoice) => {
  invoiceList.value.push(invoice)
}
const editInvoice = (invoice) => {

}
</script>

<template>
  <div class="container-fluid">
    <div class="row min-vh-100">
      <div class="col-lg-3 bg-light">
        <Sidebar :invoiceList="invoiceList" :editInvoice="editInvoice"/>
      </div>
      <div class="col-lg-9 bg-secondary">
        <Invoice :saveInvoice="saveInvoice" />
      </div>
    </div>
  </div>
</template>