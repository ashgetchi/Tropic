<template>
  <form @submit.prevent="submitForm" class="bg-white bg-opacity-90 shadow-md rounded px-8 pt-6 pb-8 mb-4 max-w-md">
    <div class="mb-4">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="username">
        Username
      </label>
      <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" v-model.trim="formdata.username" id="username" type="text" placeholder="Username">
    </div>
    <div class="mb-6">
      <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
        Password
      </label>
      <input class="shadow appearance-none border border-red-500 rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" v-model="formdata.password" id="password" type="password" placeholder="******************">
      <p v-if="!formdata.password" class="text-red-500 text-xs italic">Please choose a password.</p>
    </div>
    <div class="mb-6">
      <select v-model="formdata.referrer">
        <option value="wom"> Word of Mouth </option>
        <option value="google"> Online Advertisement </option>
        <option value="tv"> TV Advertisement </option>
      </select>
    </div>
    <div class="flex items-center justify-between">
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="submit">
        Login
      </button>
      <a class="inline-block align-baseline font-bold text-sm text-blue-500 hover:text-blue-800" href="#">
        Forgot Password?
      </a>
    </div>
  </form>
  <p class="text-center text-gray-500 text-xs">
  </p>

</template>

<script>
import { reactive } from 'vue'
export default {
  setup(){
    
    const formdata = reactive({
      username: '',
      password: '',
      referrer: 'wom'
    })

    const submitForm = () => {
      console.log(formdata.username + '' + formdata.password +'' +formdata.referrer);
      formdata.username = ''
      formdata.password = ''
      formdata.referrer = 'wom'
    }

    return{
      formdata,
      submitForm
    }
  }

}
</script>

<style>

.form-wrapper{
  flex-grow: 1;
  display: flex;
}

</style>