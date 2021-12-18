<template>
  <div>
    <h2 class="text-start mb-3">Transaction history</h2>
    <div v-for="(transaction, index) in transactions"
         class="border border-primary text-start mb-3 p-3"
         :key="transaction.id"
         data-type="transaction"
         :data-account-id="transaction.id"
         :data-amount="transaction.amount"
         :data-balance="accountBalance">
      <div class="">Transferred <span class="fw-bold">{{ transaction.amount }}$</span> from account <span class="fw-bold">{{ transaction.id }}</span> </div>
      <div class="" v-if="index == 0">The current account balance is <span class="fw-bold">{{ accountBalance }}$</span></div>
    </div>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';

export default {
  computed: {
    ...mapGetters([
      'transactions',
      'accountBalance'
    ])
  }
}
</script>