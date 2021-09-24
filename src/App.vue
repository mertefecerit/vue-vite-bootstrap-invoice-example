<script setup>
import Sidebar from "./components/Sidebar.vue";
import InvoiceContent from "./components/InvoiceSection/Invoice.vue";

</script>

<template>
  <div class="container-fluid">
    <div class="row min-vh-100">
      <div class="col-lg-3 bg-light">
        <Sidebar />
      </div>
      <div class="col-lg-9 bg-secondary">
        <InvoiceContent />
      </div>
    </div>
  </div>
</template>