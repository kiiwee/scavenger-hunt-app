<template>
    <div v-if="!check_show" class="w-full max-w-xs">
  <form @submit.prevent class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
    
    <div class="mb-3">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
        Password
      </label>
      <input v-model="pass" class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-white-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
      <p class="text-red-500 text-xs italic">Please enter the password.</p>
    </div>
    <div class="flex items-center justify-between">
      <button 
 @click="checkpass" class="bg-blue-500 hover:bg-blue-700 text-white font-bold  py-2 px-20 rounded focus:outline-none focus:shadow-outline" type="button">
        Reveal Clue
      </button>
    </div>
  </form>
  <p class="text-center text-gray-500 text-xs">
    &copy;2022 Scavenger Hunt
  </p>
</div>
<Clue v-if="check_show"></Clue>
</template>

<script setup lang="ts">
import Clue from './Clue.vue'
import { Console } from 'console';
import { ref, onMounted } from 'vue'
const pass=ref('')
const check_show=ref(0)
function checkpass() {
  if (pass.value=="putka") {
    console.log('Stana')
    check_show.value=1
  } else {
    
  }
}
</script>
