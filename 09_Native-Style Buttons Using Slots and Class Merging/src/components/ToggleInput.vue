<template>
  <span class="toggle" role="checkbox" tabindex="0"
    @click="toggle"
    @keydown.space.prevent="toggle"
    :aria-checked="toggled.toString()"
  ></span>
</template>

<script>
export default {
  model: {
    prop: 'toggled'
  },
  props: ["toggled"],
  methods: {
    toggle() {
      this.$emit("input", !this.toggled)
    }
  }
}
</script>
