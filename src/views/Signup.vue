<template>
  <div class="home">
<h2>Welcome to home page</h2>
<button @click="transferMoney()">Transfer</button>
  </div>
</template>

<script>


export default {
  name: 'Home',
  methods:{
    transferMoney(){
      alert(`Transfer Successful`)
      // this.$router.go(1)
      this.$router.push('/about')
    }
  }
}
</script>
