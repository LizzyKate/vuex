<template>
  <div id="app">
    <listOne ></listOne>
    <listTwo ></listTwo>
  </div>
</template>

<script>
import listOne from './components/listOne'
import listTwo from './components/listTwo'

export default {
  components: {
    listOne:listOne,
    listTwo:listTwo
  },
  data(){
    return {
      
    }
  }
}
</script>

<style>
body{
  font-family: Ubuntu;
  color: #555;
}
</style>
