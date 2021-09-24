<template>
  <h4 class="mt-3">Fatura Listesi</h4>
  <ul class="list-group" v-if="invoiceList.length > 0">
    <li class="list-group-item d-flex justify-content-between align-items-center" v-for="invoice in invoiceList" :key="invoice.id">
      <div>{{invoice.id}}</div>
      <div>{{invoice.contact.name}}</div>
      <div class="d-flex">
        <button class="btn btn-danger btn-sm fw-bold me-2"><i class="far fa-trash-alt"></i></button>
        <button @click="editInvoice(invoice)" class="btn btn-info btn-sm fw-bold"><i class="far fa-eye"></i></button>
      </div>
    </li>
  </ul>
  <div class="alert alert-warning">
    <h6>Henüz bir fatura oluşmadı</h6>
  </div>
</template>

<script setup>
import {provide} from "vue";

defineProps({invoiceList:Array,editInvoice:Function})

</script>

<style scoped>

</style>