<template>
  <div id="listOne" >
    <h2>Product List One</h2>
    <ul>
      <li v-for="(tick, i) in producing" :key="i">
        <span class="name">{{tick.name}}</span>
        <span class="price">${{tick.price}}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
props:['producing']
  
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
