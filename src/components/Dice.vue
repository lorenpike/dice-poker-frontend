<template>
  <h1>{{ number }}</h1>
  <div class="dice" @click="$emit('wasClicked')">
    <div v-if="number === 1">
      <img src="../assets/dice1.png" />
    </div>
    <div v-else-if="number === 2">
      <img src="../assets/dice2.png" />
    </div>
    <div v-else-if="number === 3">
      <img src="../assets/dice3.png" />
    </div>
    <div v-else-if="number === 4">
      <img src="../assets/dice4.png" />
    </div>
    <div v-else-if="number === 5">
      <img src="../assets/dice5.png" />
    </div>
    <div v-else>
      <img src="../assets/dice6.png" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Dice",
  props: {
    number: Number,
  },
  emits: ["onWasClicked"]
};
</script>

<style>
</style>