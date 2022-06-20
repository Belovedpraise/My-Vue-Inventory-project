<template>

<div class="m-5">
  <hr>
    <h3 class="m-3 bg-danger rounded text-white shadow">INVENTORY SYSTEM</h3> 
    <Admin :products='products' @addGoods ='addGoods'/>

<h3 class="text-danger">Add Goods Here</h3>
<table class="table">
  <thead>
    <tbody>
      <th>product Name</th>
      <th>product Quantity</th>
      <th>product Price</th>
      <th>Delete</th>
 
  <tr v-for="(Goods,index) in products" :key="index">
    <td>{{Goods.productName}}</td>
    <td>{{Goods.productQuantity}}</td>
    <td>{{Goods.productPrice}}</td>
   <td><button class="m-2 btn btn-danger text-white" @click="addDelete(index)">Delete</button></td> 
  </tr>
  </tbody>
  </thead>
     
</table>
 <User :products='products'/>
<View   @Addgoods='Addgoods'/>
</div>   

</template> 

<script>
  import Admin from './components/Admin.vue'
  import User from './components/User.vue'
import View from './components/view.vue'
export default {
  data(){
    return{
    productName: "", 
    productQuantity: "",
    productPrice: "",
    products:[]
    }
  },
 methods:{
addGoods(newGoods){
this.products.push(newGoods)
let {products}=this
this.productName="",
this.productQuantity="",
this.productPrice="",
// this.$emit('addGoods', thenewbutton)
console.log(products);
},
addDelete(index){
  this.products = this.products.filter((_,i)=>i!==index);
}
 },
 components:{
   Admin,
   User,
  View
 }
}


</script>

<style>
.male{
  color:blue;
}
.female{
  color:rgb(228, 25, 150);
}
</style>
