<template>
  <div id="listTwo">
    <h2>Product List Two</h2>
    <ul>
      <li v-for="(tick, i) in saleProducts" :key="i">
          <span class="name">{{tick.name}}</span>
        <span class="price">${{tick.price}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
computed:{
    products(){
      return this.$store.state.products
    },
    saleProducts(){
      return this.$store.getters.saleProducts;
    }
  }
  
}
</script>


<style scoped>
#listTwo{
    background:#D1E4FF;
    box-shadow: 1px 2px 3px rgba(0,0,0,0.2);
    margin-bottom: 30px;
    padding: 10px 20px;
}
#listTwo ul{
    padding: 0;
    list-style-type: none;
}
#listTwo li{
    margin-right:10px;
    margin-top:10px;
    padding: 20px;
    background: rgba(255,255,255,0.7);
}
.price{
    font-weight: bold;
    color: #860CE8;
    display: block;
}
</style>
