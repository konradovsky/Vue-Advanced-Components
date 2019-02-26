<template>
 <div class="min-h-screen bg-grey-darker p-8">
    <div class="max-w-sm mx-auto">
      <div class="card">
        <label class="block">
          <span class="form-label mb-2">Select a date</span>
          <date-picker v-model="date" format="DD-MM-YYYY" :option="{firstDay: 1}"/>
        </label>
      </div>
    </div>
  </div>
</template>

<script>
import DatePicker from './components/DatePicker'
export default {
  data(){
    return {
      date: '2019-02-21'
    }
  },
  components: {
    DatePicker
  },

}
</script>

<style/>