<template>
  <input :value="value" class="form-input" type="text" ref="input" placeholder="YYYY-MM-DD">
</template>

<script>
import Pikaday from 'pikaday';
import 'pikaday/css/pikaday.css';

export default {
  props: {
    value: { required: true },
    format: { default: 'YYYY-MM-DD' },
    options: { default: {} }
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      format: this.format,
      onSelect: () => {
        this.$emit('input', picker.toString());
      },
      ...this.options
    });
  }
};
</script>

<style src="../assets/app.css"/>