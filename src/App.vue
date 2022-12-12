<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#workUpdates{
  display: flex;
  flex-flow: row;
  justify-content: space-around;
}

#view{
  width: 50%;

  color: white;
  background: black;

  border-radius: 2px;

  margin-top: 30px;
}

#e-mailArea{
  margin-top: 30px;
  width: 70%;

}

#e-mail{
  width: 70%;

  border: lightgray solid 2px;
  border-radius: 2px;

  height: 30px;

  padding-left: 20px;
}

#sign{
  background: black;
  color: white;

  height: 34px;

  margin-left: 10px;

  border-radius: 2px;
}

footer{
  display: flex;

  justify-content: space-between;
  align-items: center;

  padding: 0 150px;

  margin-top: 150px;
}

footer div{
  display: flex;
  gap: 30px;

  align-items: center;
}

#not-just-text{
  color: rgba(0 0 0 / 0.6);
}

section{
  padding: 0 100px;
}
</style>
