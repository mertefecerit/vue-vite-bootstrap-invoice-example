<template>
  <div class="row justify-content-center">
    <div class="col-lg-8">
      <div class="p-2 rounded mt-3 bg-warning shadow">
        <Contact />
        <Items />
        <Summary />
        <hr>
        <div class="d-flex justify-content-end">
          <button class="btn btn-sm btn-danger fw-bold"><i class="fas fa-save"></i> Kaydet</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Items from './Items.vue'
import Summary from './Summary.vue'
import Contact from "./Contact.vue";

</script>

<style scoped>

</style>