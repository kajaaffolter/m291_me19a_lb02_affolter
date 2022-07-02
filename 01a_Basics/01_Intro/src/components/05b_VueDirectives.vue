<template>
  <!--
    Vue Directives: Basic Directives (v-text, v-once, v-html, v-bind, v-if, v-show)
    -->
  <div>
    <h1 v-if="false" v-text="text">Loading...</h1>
    <h2 v-else-if="false" v-html="html" />
    <a
      v-else
      :href="link.url"
      :target="link.target"
      :tabindex="link.tabindex"
      v-text="link.title"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      // v-text
      text: 'demo-5b.vue (text)',
      // v-html
      html: 'demo-5b </br>HTML in<br/><b>your data</b>',
      // v-bind
      link: {
        url: 'https://www.swarovski.com/en-CH/',
        target: '_blank',
        tabindex: '0',
        title: 'Shop of Swarovski',
      },
    }
  },
}
</script>

<style lang="scss" scoped>
h2 {
  margin: 40px 0 0;
  font-weight: normal;
  color: pink;
}
a {
  display: block;
  margin-top: 70px;
  text-align: center;
  color: #ef5971;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-size: 50px;
}
</style>
