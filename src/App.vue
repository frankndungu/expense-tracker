<template>
  <Header />
  <div class="container">
    <Balance :total="total" />
    <IncomeExpenses />
    <TransactionList :transactions="transactions" />
    <AddTransaction />
  </div>
</template>

<script setup>
import Header from "./components/Header.vue";
import Balance from "./components/Balance.vue";
import IncomeExpenses from "./components/IncomeExpenses.vue";
import TransactionList from "./components/TransactionList.vue";
import AddTransaction from "./components/AddTransaction.vue";

import { computed, ref } from "vue";

const transactions = ref([
  { id: 1, text: "Skin Care", amount: -30.0 },
  { id: 2, text: "Salary", amount: 850.0 },
  { id: 3, text: "Food", amount: -45.0 },
  { id: 4, text: "Business", amount: 4500.0 },
]);

const total = computed(() => {
  return transactions.value.reduce((acc, transaction) => {
    return acc + transaction.amount;
  }, 0);
});
</script>
