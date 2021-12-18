<script setup>
import TransactionsForm from './components/TransactionsForm.vue'
import TransactionsList from './components/TransactionsList.vue'
</script>

<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-12 col-md-4">
        <TransactionsForm />
      </div>
      <div class="col-12 col-md-7 offset-md-1">
        <TransactionsList />
      </div>
    </div>
  </div>
</template>

<style>
#app {

}
</style>
