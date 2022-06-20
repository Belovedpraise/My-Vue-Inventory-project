<template>
    <div>
        <br>
      <hr>
      <!-- {{products}} -->
<h3 class="text-danger">View Your Goods Here</h3>
<!-- <h6>ADD THE NUMBER OF GOODS ADDED HERE :{{num}}</h6> -->
<table class="table">
  <thead>
    <tbody>
      <th>product Name</th>
      <th>product Quantity</th>
      <th>product Price</th>
      <!-- <th>AddGoods</th> -->
 
  <tr v-for="(Goods,index) in products" :key="index">
    <td>{{Goods.productName}}</td>
    <td>{{Goods.productQuantity}}</td>
    <td>{{Goods.productPrice}}</td>
     <!-- <td><button class="btn btn-danger">Add Goods</button></td> -->
  </tr>
  </tbody>
  </thead>
</table>
   </div>
</template>

<script>
export default {
  props:[''],
  //   data(){
  //   return{
  //   productName: "", 
  //   productQuantity: "",
  //   productPrice: "",
  //   products:[]

  //   }
  // },

  methods:{
      
  }
}
</script>

<style>

</style>