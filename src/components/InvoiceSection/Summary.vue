<template>
  <div class="text-end mt-3">
    <p class="mb-0">Ara Toplam : {{ new Intl.NumberFormat('en-US',{ style: 'currency', currency: 'USD' }).format(subTotal) }}</p>
    <p class="mb-0">KDV Toplam : {{ new Intl.NumberFormat('en-US',{ style: 'currency', currency: 'USD' }).format(taxTotal) }}</p>
    <p class="mb-0">Genel Toplam : {{ new Intl.NumberFormat('en-US',{ style: 'currency', currency: 'USD' }).format(total) }}</p>
  </div>
</template>

<script setup>
  import {computed} from "vue";

  const props = defineProps({items:Array})
  const subTotal = computed(() => props.items.reduce((toplam,item) => toplam + item.totalPrice, 0))
  const taxTotal = computed(()=> subTotal.value * 0.18)
  const total = computed(()=> subTotal.value + taxTotal.value)
</script>

<style scoped>

</style>