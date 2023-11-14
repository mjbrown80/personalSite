<template>
  <div id="app">
    <Header/> 
    <div id="nav">
      <button @click="navigateTo( 'WelcomePage' )">Home</button>&nbsp;
      <button @click="navigateTo('Paintings')">Paintings</button>&nbsp;
      <button @click="navigateTo('Blog')">Blog</button>&nbsp;
      <button @click="navigateTo('About')">About</button>&nbsp;
      <button @click="navigateTo('login')">Login</button>
      <button @click="navigateTo('logout')" v-if="$store.state.token != ''">Logout</button>
    </div>
    <router-view />
  </div>
</template>

<script>
import Header from './components/Header.vue';


export default {
  components: {
    Header,
  
   },
  methods: {
    navigateTo(routeName){
      this.$router.push({name: routeName});
    }
  }
}
</script>

<style>

#nav{
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
}
#nav button {
  background-color: brown;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s;
}
#nav button:hover{
  background-color: orange;
}
</style>
