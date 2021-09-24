<template>
  <h4>Fatura Bilgileri</h4>
  <hr>
  <div class="mb-3">
    <label for="name">Müşteri Adı</label>
    <input id="name" type="text" class="form-control" v-model="contact.name">
  </div>
  <div class="mb-3">
    <label for="customerMail">E-Posta</label>
    <input id="customerMail" type="email" class="form-control" v-model="contact.email">
  </div>

  <div class="d-flex justify-content-between mb-3">
    <div>
      <label for="town">Şehir</label>
      <input id="town" type="text" class="form-control" v-model="contact.town">
    </div>
    <div>
      <label for="zipCode">Posta Kodu</label>
      <input id="zipCode" type="text" class="form-control" v-model="contact.zipcode">
    </div>
    <div>
      <label for="country">Ülke</label>
      <input id="country" type="text" class="form-control" v-model="contact.country">
    </div>
  </div>
</template>

<script setup>
defineProps({contact:Object})
</script>

<style scoped>

</style>