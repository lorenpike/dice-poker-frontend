<template>
  <div>
    <h1>Dice Poker</h1>
    <Dice @wasClicked="rollDice()" :number="diceNumber" />
  </div>
</template>

<script>
import Dice from "./components/Dice.vue"

export default {
  name: 'App',
  components: {
    Dice
  },
  data() {
    return {
      diceNumber: 1
    }
  },
  methods: {
    rollDice() {
      this.diceNumber = Math.ceil(Math.random()*6)
      console.log(this.diceNumber)
    }
  }
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
