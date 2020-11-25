<template>
  <div id="app">
    <p>count: {{ count }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    count() {
      return this.$store.state.count;
    }
  }
}
</script>
