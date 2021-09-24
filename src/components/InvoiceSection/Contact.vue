<template>
  <h4>Fatura Bilgileri</h4>
  <hr>
  <div class="mb-3">
    <label for="name">Müşteri Adı</label>
    <input id="name" type="text" class="form-control">
  </div>
  <div class="mb-3">
    <label for="customerMail">E-Posta</label>
    <input id="customerMail" type="email" class="form-control">
  </div>

  <div class="d-flex justify-content-between mb-3">
    <div>
      <label for="town">Şehir</label>
      <input id="town" type="text" class="form-control">
    </div>
    <div>
      <label for="postalCode">Posta Kodu</label>
      <input id="postalCode" type="text" class="form-control">
    </div>
    <div>
      <label for="country">Ülke</label>
      <input id="country" type="text" class="form-control">
    </div>
  </div>
</template>

<script>
export default {
  name: "Contact"
}
</script>

<style scoped>

</style>