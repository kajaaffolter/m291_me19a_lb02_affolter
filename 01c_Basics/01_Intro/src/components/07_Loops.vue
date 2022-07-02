<template>

  <div>
    <h1>Swarovski</h1>


    <h3>our offers:</h3>
    <ul>
      <li v-for="n in schmuck" :key="n">
        {{n. title}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      schmuck: [
          {
            title: 'Necklaces',
          },{
            title: 'Earrings',
          },{
            title: 'Rings',
          },{
            title: 'Bracelets',
        },

      ]
    }
  },
}
</script>

<style lang="scss" scoped>
li {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  color: #2c3e50;
  margin-top: 10px;
}

h1 {
  margin-top: 60px;
  display: block;
  color: #ef5971;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 50px;
}

h3 {

  color: #dc969f;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 30px;
}
</style>
