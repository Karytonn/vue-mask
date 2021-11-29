<template>
  <div class="contant">
      <div class="form">
          
          <h1 class="title">Vue The Mask</h1>

          <label for="tel" class="label" >Sem mascará</label>
          <input id="tel" class="input" type="tel" placeholder="(62) 98888-7777">

          <label for="tel" class="label" >Com mascará</label>
          <input id="tel" class="input" type="tel" placeholder="(62) 98888-7777" v-mask="['(##) ####-####', '(##) #####-####']">

      </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="postcss" scoped>
.contant {
    @apply grid h-screen w-screen place-content-center m-0 p-0 bg-gray-900;
}
.form {
    @apply bg-gray-700 rounded-lg p-14 ;
}
.title {
    @apply text-5xl text-center text-gray-200 font-bold mb-14;
}
.label {
    @apply block text-gray-400 text-xl font-normal tracking-wide ml-1 mt-4;
}
.input {
    @apply block w-full form-input px-4 py-3 rounded-md;
}
</style>