<template>
<button v-on:click="counter += 1">{{ counter }}</button>
</template>
<script>
var data = { counter: 0 }
export default {
  data () {
    return {
      data
    }
  }
}
</script>
<style></style>