<template>
  <div id="app">
    <div id="nav">
          <router-link v-if="authenticated" to="/login" v-on:click.native="logout()" replace>Logout</router-link>
      </div>
      <router-view @authenticated="setAuthenticated" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data () {
    return {
        authenticated: false,
        mockAccount: {
            username: 'nraboy',
            password: 'password'
        }
    }
  },
  mounted() {
    if(!this.authenticated) {
        this.$router.replace({ name: 'login' })
    }
  },
  methods: {
    setAuthenticated(status) {
        this.authenticated = status
    },
    logout() {
        this.authenticated = false
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
body {
        background-color: #F0F0F0;
    }
    h1 {
        padding: 0;
        margin-top: 0;
    }
    #app {
        width: 1024px;
        margin: auto;
    }
</style>
