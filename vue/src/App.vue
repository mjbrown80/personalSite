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

<style scoped>

#nav{
  display: flex;
  /* justify-content: space-between;
  align-items: center; */
  flex-direction: column; 
  align-items: flex-start;
  margin-right: 20px;
  /* gap: 10px; */
}
#nav button {
  width: 150px;
  background-color: brown;
  color: white;
  padding: 10px 0px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  text-align: center;
  margin-bottom: 10px;
  transition: background-color 0.2s;
}
#nav button:hover{
  background-color: orange;
}
</style>
