<template>
  <navbar></navbar>
  <div>
    <div class="wrapper">
      <div class="hero-image">
      <the-form></the-form>
      </div>
      <div class="text-box bg-white">
      <the-text-box></the-text-box>
      </div>   
    </div>
  </div>
</template>

<script>

import Navbar from './components/Navbar'
import TheForm from './components/TheForm.vue'
import TheTextBox from './components/TheTextBox.vue'

export default {

  components: {
    Navbar,
    TheForm,
    TheTextBox
  }



}
</script>

<style>

.wrapper{
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100vh;
  justify-content: space-evenly;
}

.company-name{
  font-weight: bolder;
}


.hero-image{
  background-image: url('https://images-na.ssl-images-amazon.com/images/I/81utRoav18L._AC_SL1500_.jpg');
  height: 100vh;
  width: 50vw;
  background-size: contain;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

}

.text-box{
  display: flex;
  align-items: center;
  justify-content: center;
  width: 50vw;
  height: 100vh;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  
}
</style>
