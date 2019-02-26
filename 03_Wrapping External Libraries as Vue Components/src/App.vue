<template>
 <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <div class="card">
        <label class="block">
          <span class="form-label mb-2">Select a date</span>
          <input class="form-input" type="text" id="datepicker" placeholder="YYYY-MM-DD">
        </label>
      </div>
    </div>
  </div>
</template>

<script>
import Pikaday from 'pikaday';
import 'pikaday/css/pikaday.css'
export default {
  mounted(){
    const picker = new Pikaday({
      field: document.getElementById('datepicker'),
      format: "YYYY-MM-DD"
    })
  }

}
</script>

<style src="./assets/app.css"/>