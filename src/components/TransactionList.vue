<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li
      v-for="transaction in transactions"
      :key="transaction.id"
      :class="transaction.amount < 0 ? 'minus' : 'plus'"
    >
      {{ transaction.text }} <span>${{ transaction.amount }}</span
      ><button class="delete-btn">X</button>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      transactions: [
        { id: 1, text: "Skin Care", amount: -30.0 },
        { id: 2, text: "Salary", amount: 850.0 },
        { id: 3, text: "Food", amount: -45.0 },
        { id: 4, text: "Business", amount: 4500.0 },
      ],
    };
  },
};
</script>
