
<template>
  <div class="container">
    <h1>Shop Swarovski</h1>
    <div>
      Spring Sale
      <strike v-show="oldDiscount">Was {{ oldDiscount }}%</strike>
      <strong> Now {{ discount }}% OFF</strong><br/>
      <a href="#" @click="updateDiscount">discount by 15%</a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      oldDiscount: 0,
      discount: 15,
    }
  },
  watch: {
    discount: {
      handler: function (newVal, oldVal){
        console.log(`actual(${newVal}%) and old(${oldVal}%) discount.`);
        this.oldDiscount = oldVal;
      },
      immediate: false,
      deep: true
    }

  },
  methods: {
    updateDiscount(){
      this.discount = this.discount + 15;
    }
  }
}
</script>
<style lang="scss" scoped>
.container {
  margin: 0 auto;
  padding: 30px;
  max-width: 600px;
  font-family: 'Avenir', Helvetica, sans-serif;
  margin: 0;
}
h1 {
display: block;
margin-top: 70px;
color: #ef5971;
font-family: 'Avenir', Helvetica, Arial, sans-serif;
font-size: 50px;
}
a {
  display: inline-block;
  background: rgb(220, 150, 159);
  border-radius: 10px;
  margin-top: 30px;
  font-size: 14px;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
}
</style>
