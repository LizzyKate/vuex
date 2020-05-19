<template>
  <div id="listOne" >
    <h2>Product List One</h2>
    <ul>
      <li v-for="(tick, i) in saleProducts" :key="i">
        <span class="name">{{tick.name}}</span>
        <span class="price">${{tick.price}}</span>
      </li>
    </ul>
    <button v-on:click="reduce(4)">Reduce Price</button>
  </div>
</template>

<script>

import {mapActions} from 'vuex'
import {mapGetters} from 'vuex'

export default {
data(){
return{

}
},
  computed:{
    products(){
      return this.$store.state.products
    },
   ...mapGetters([
     'saleProducts'
   ])
  },
  methods:{
    ...mapActions([
      'reduce'
    ])
  }
}
</script>


<style scoped>
#listOne{
  background: #FFF8B1;
  box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}
#listOne ul{
  padding: 0;
}
#listOne li{
  display: inline-block;
  margin-right: 10px;
  padding: 20px;
  background: rgba(255,255,255,0.7);
}
.price{
  font-weight: bold;
  color: #E8800C;
}
</style>
