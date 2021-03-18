<template>
  <div>
    <ul>
        <li v-for="item in itemsList" v-bind:key="item.name">

            <h2>{{item.name}}</h2>
            <img v-bind:src="item.image"/>
            <p>{{item.price}}</p>   
            <qtyCounter></qtyCounter>        
        </li>
    </ul>
  </div>
</template>


<script>
import QuantityCounter from './components/QuantityCounter.vue'

export default {
  props:{
      itemsList:{
          type:Array
      }
  },
  components: {
    'qtyCounter': QuantityCounter,
  }
}
</script>

<style scoped>
#itemsList {
  width: 100%;
  max-width: 70%;
  margin: 0px;
  padding: 0 5px;
  box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 10px;
  border: 1px solid #222;
  margin: 10px;
}
img {
  width: 135px;
  height: 135px;
}

#price {
  font-size: 30px;
}

#itemName {
  font-size: 30px;
}

#shoppingBasket {
  position: absolute;
  top: 23%;
  left: 78%;
}
</style>