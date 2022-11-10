<template>
  <button
    @click="btnMenu"
    class="c-humbergerButton"
  >
    <span class="c-humbergerButton-bar"></span>
    <span class="c-humbergerButton-bar"></span>
    <span class="c-humbergerButton-bar"></span>
  </button>
</template>

<script>
export default {
  methods: {
    btnMenu () {
      this.$emit('btnMenu')
    }
  }
}
</script>