<template>
  <tr>
    <td class="p-2 myw-40"><input type="text" class="form-control" v-model="item.name"></td>
    <td class="p-2 myw-12"><input type="number" class="form-control" v-model="item.qty"></td>
    <td class="p-2 myw-18"><input type="number" class="form-control" v-model="item.unitPrice"></td>
    <td class="align-middle p-2">{{ new Intl.NumberFormat('en-US',{ style: 'currency', currency: 'USD' }).format(totalPrice) }}</td>
    <td class="p-2 text-end "><button @click="deleteItem(item)" class="btn btn-sm fw-bold btn-danger"><i class="fas fa-times"></i></button></td>
  </tr>
</template>

<script setup>
 import {computed, watch, inject} from "vue";
 const props = defineProps({item:Object})
 const totalPrice = computed(() => props.item.qty * props.item.unitPrice)
 const deleteItem = inject("deleteItem");
 watch(totalPrice, (value) => {
   props.item.totalPrice = value
 })
</script>

<style scoped>

</style>