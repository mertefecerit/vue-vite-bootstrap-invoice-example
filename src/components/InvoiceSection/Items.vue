<template>
  <h4>Fatura Kalemleri</h4>
  <hr>
  <table class="table table-sm table-striped table-warning">
    <thead class="text-left">
    <tr>
      <th>Ürün Adı</th>
      <th>Adet</th>
      <th>Fiyat</th>
      <th>Toplam</th>
      <th></th>
    </tr>
    </thead>
    <tbody>
      <Item v-for="i in 5" :key="i" />
    </tbody>
  </table>
  <button class="btn btn-block btn-outline-danger w-100 fw-bold"><i class="fas fa-plus"></i> Ekle</button>
</template>

<script setup>
import Item from "./Item.vue";
</script>

<style scoped>

</style>