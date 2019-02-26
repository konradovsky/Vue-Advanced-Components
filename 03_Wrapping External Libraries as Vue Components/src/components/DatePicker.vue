<template>
  <input :value="date" class="form-input" type="text" ref="input" placeholder="YYYY-MM-DD">
</template>

<script>
import Pikaday from 'pikaday';
import 'pikaday/css/pikaday.css';

export default {
  props: ['date'],
  modal: {
      prop: 'date'
  },
  mounted() {
    const picker = new Pikaday({
      field: this.$refs.input,
      format: 'YYYY MM DD',
      onSelect: () => {
        this.$emit('input', picker.toString())
      }
    });
  }
};
</script>

<style src="../assets/app.css"/>