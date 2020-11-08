<template>
  <div id="app">
    <p>{{ count }}</p>
    <p>{{ doubleCounter }}</p>
    <button @click="increment(1)">+1</button>
    <button @click="decrement(2)">-1</button>
  </div>
</template>

<script>
import {mapGetters, mapMutations, mapActions} from "vuex";

export default {
  computed: {
    count() {
      return this.$store.state.count
    },
    ...mapGetters(["doubleCounter"])
  },
  methods: {
    ...mapActions(["increment"]),
    ...mapMutations(["decrement"])
  }
}
</script>
