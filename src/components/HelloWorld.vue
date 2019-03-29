<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Vuejs Enviromental variables</h3>
    <ul>
      <li> The default env variable for deployment type: <b>{{ nodeEnv }}</b> </li>
      <li> The variable will always show in any mode. It in the .env file: <b>{{ defaultEnv }}</b> </li>
      <li> The variable will only show in development mode. It in the .env.development file:<b> {{ devEnv }}</b> </li>
      <li> The variable will only show in production mode. It in the .env.production file:<b> {{ prodEnv }}</b> </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  computed: {
    nodeEnv: function () {
      return process.env.NODE_ENV
    },
    defaultEnv: function () {
      return process.env.VUE_APP_TITLE
    },
    devEnv: function () {
      return process.env.VUE_APP_DEV_TITLE
    },
    prodEnv: function () {
      return process.env.VUE_APP_PROD_TITLE
    }
  },
  mounted: function () {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  padding: 0;
}
li {
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
