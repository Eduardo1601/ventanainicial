<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
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
</style>
<style scoped>
  #login {
      width: 500px;
      border: 1px solid #CCCCCC;
      background-color: #FFFFFF;
      margin: auto;
      margin-top: 200px;
      padding: 20px;
  }
</style>
  <script>
      export default {
          name: 'Login',
          data() {
              return {
                  input: {
                      Usuario: "",
                      password: ""
                  }
              }
          },
          methods: {
              login() {
                  if(this.input.Usuario != "" && this.input.password != "") {
                      if(this.input.Usuario == this.$parent.mockAccount.Usuario && this.input.password == this.$parent.mockAccount.password) {
                          this.$emit("authenticated", true);
                          this.$router.replace({name: "server2" });
                      } else {
                          console.log("El Usuario y / o la contraseña son incorrectas");
                      }
                  } else {
                      console.log("no ha ingresado datos");
                  }
              }
          }
      }
  </script>