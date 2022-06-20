<template>
    <div>
        <br>
      <hr>
      {{product}}
<h3 class="text-danger">User End</h3>
<table class="table">
  <thead>
    <tbody>
      <th>product Name</th>
      <th>product Quantity</th>
      <th>product Price</th>
      <th>AddGoods</th>
 
  <tr v-for="(Goods,index) in products" :key="index">
    <td>{{Goods.productName}}</td>
    <td>{{Goods.productQuantity}}</td>
    <td>{{Goods.productPrice}}</td>
     <td><button class="btn btn-danger" @click="Addgoods()">Add Goods</button></td>
  </tr>
  </tbody>
  </thead>
</table>
   </div>
</template>

<script>
export default {
  props:['products'],
    data(){
    return{
    num:'0'

    }
  },
  methods:{
Addgoods(){
     let {productName, productQuantity ,productPrice} = this
            let newGoods = {productName,productQuantity,productPrice}
            this.productName="",
            this.productQuantity="",
            this.productPrice="",
            this.$emit('addGoods',newGoods)
}
  }
}
</script>

<style>

</style>