<template>
    <div class="m-5">
<h3 class="text-danger">Add New Goods</h3>
<input type="text" class="form-control  w-50 m-2" placeholder="productName" v-model="productName"><br>
<input type="text"  class="form-control w-50 m-2" placeholder="productQuantity" v-model="productQuantity"><br>
<input type="text"  class="form-control  w-50 m-2" placeholder="productPrice" v-model="productPrice"><br>
<input type="submit" class="m-2 btn btn-danger text-white" @click="addGoods()">
   </div>
</template>

<script>
export default {
    data(){
        return{
            productName : '',
            productQuantity: '',
            productPrice : ''
        }
    },
    methods:{
        addGoods(){
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